<!--
Licensed to the Apache Software Foundation (ASF) under one
or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.  The ASF licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

  http://www.apache.org/licenses/LICENSE-2.0
-->

# phinops — System Architecture

**phinops** is a FinOps platform built on Apache Superset. It ingests
multi-cloud billing data (GCP, AWS ×2 orgs, Azure), stores derived snapshots in
PostgreSQL, visualizes them in Superset dashboards, and exposes two Claude-powered
assistants (a Slack bot and an in-app web chat) plus daily cost-anomaly / budget /
marketplace alerts to Slack.

> Deployment today is a **single GCP VM** (`<VM_IP>`). Migration to GKE in the
> `<AGENTS_PROJECT>` project is tracked in issue #2.

---

## 1. High-level architecture

```mermaid
flowchart LR
  %% ─────────── External billing data sources ───────────
  subgraph EXT["External data sources"]
    BQ["GCP BigQuery billing export<br/>{PROD_PROJECT}.{BILLING_DATASET}<br/>gcp_billing_export_v1_*"]
    CEF["AWS Cost Explorer — primary<br/>acct {AWS_ACCOUNT_ID_PRIMARY}"]
    CEM["AWS Cost Explorer — secondary<br/>acct {AWS_ACCOUNT_ID_SECONDARY}"]
    ACM["Azure Cost Management API<br/>tenant {AZURE_TENANT_ID} mgmt-group scope"]
    ACAT["Azure Marketplace Catalog API<br/>catalogapi.azure.com — isMacc flag"]
    CSV["GCP pricing export<br/>Pricing-export.csv"]
  end

  %% ─────────── Identity / access ───────────
  subgraph IDP["Identity & access"]
    GSA["GCP SA {SERVICE_ACCOUNT}@{DEV_PROJECT}<br/>VM Workload Identity Federation"]
    AWSROLE["AWS role phinops-billing-reader<br/>(WIF, primary org)"]
    AZAPP["Azure app reg phinops-billing-reader<br/>ClientAssertion via WIF"]
    MOLO["Secondary-org AWS IAM keys (.env)"]
  end

  GSA -->|"federates"| AWSROLE
  GSA -->|"federates"| AZAPP
  AWSROLE --> CEF
  AZAPP --> ACM
  MOLO --> CEM

  %% ─────────── The VM host ───────────
  subgraph VM["GCP VM — single host (systemd)"]
    direction TB

    subgraph JOBS["Scheduled ingest / alert jobs (systemd timers)"]
      JAZ["azure_spend.py — 08:35"]
      JFC["gcp_smooth_forecast.py — 08:40"]
      JMK["marketplace_alert.py — 09:00"]
      JAL["billing_alerts.py — 09:30"]
      JMA["azure_macc_snapshot.py + _catalog_refresh.py"]
      JCM["gcp_commit / gcp-commit-v2"]
    end

    PG[("PostgreSQL :5432<br/>Superset metadata + FinOps tables/views")]
    RED[("Redis :6379<br/>cache + Celery broker")]

    subgraph SUP["Apache Superset"]
      NGINX["nginx :80 (reverse proxy, HTTP)"]
      WEBSRV["gunicorn — Superset web :8088<br/>Flask / Flask-AppBuilder 5.2"]
      CEL["Celery worker + beat"]
      WEBBOT["Web chat — /finops-chat/ask<br/>+ React FinOpsChat widget (conversation memory)"]
    end

    SLACKBOT["Slack bot — Socket Mode<br/>@mentions, thread memory"]
  end

  %% ─────────── LLM ───────────
  LLM["Claude via Vertex AI<br/>AnthropicVertex ({DEV_PROJECT}, us-east5)<br/>Anthropic API fallback"]

  %% ─────────── Consumers ───────────
  subgraph OUT["Consumers"]
    USERS["FinOps users (browser)"]
    SLACKCH["Slack #<finops-channel>"]
  end

  %% Ingest pulls
  BQ --> JFC & JAL & JMK & JCM
  CEF --> JFC & JAL & JMK
  CEM --> JMK & JAL
  ACM --> JAZ & JMK & JAL & JMA
  ACAT --> JMA
  CSV -->|"gcp_estimate / loader"| PG

  %% Jobs write snapshots
  JAZ --> PG
  JFC --> PG
  JMK --> PG
  JMA --> PG
  JCM --> PG

  %% Alert jobs post to Slack
  JMK -->|"marketplace alert"| SLACKCH
  JAL -->|"burn-rate + anomaly alerts"| SLACKCH

  %% Superset internals
  NGINX --> WEBSRV
  WEBSRV --- PG
  WEBSRV --- RED
  CEL --- RED
  CEL --- PG
  WEBSRV --> WEBBOT

  %% Bots: read data + call tools + LLM
  WEBBOT -->|"agentic tool loop"| LLM
  SLACKBOT -->|"agentic tool loop"| LLM
  WEBBOT -->|"SQL / live cost APIs"| PG
  SLACKBOT -->|"SQL / live cost APIs"| PG
  SLACKBOT -.-> CEF
  SLACKBOT -.-> CEM
  SLACKBOT -.-> ACM
  WEBBOT -.-> CEF
  WEBBOT -.-> ACM

  %% Serving
  USERS --> NGINX
  WEBSRV -->|"dashboards + chat"| USERS
  SLACKBOT --> SLACKCH
```

---

## 2. Data-flow / lineage (source → table → chart)

```mermaid
flowchart TD
  subgraph SRC["Sources"]
    BQ2["BigQuery billing export"]
    CE2["AWS Cost Explorer (primary + secondary)"]
    ACM2["Azure Cost Management"]
    CAT2["Azure Marketplace Catalog (isMacc)"]
    CSV2["GCP pricing CSV"]
  end

  subgraph SNAP["PostgreSQL snapshot tables"]
    T_BUD["cloud_budget / cloud_actuals"]
    T_MKT["cloud_marketplace (+ view cloud_marketplace_summary)"]
    T_AZD["azure_daily_service_spend"]
    T_AZS["azure_service_spend_current_month / _ytd"]
    T_AZM["azure_marketplace_current_month"]
    T_MACC["azure_macc_offer_eligibility / _partnumber_map<br/>_commitment / _progress_v2"]
    T_COMMIT["gcp_commit_progress / _v2"]
    T_PRICE["gcp_sku_pricing"]
    T_MOLO["secondary_daily_service_spend"]
    V_BVA["view cloud_budget_vs_actual"]
    V_YTD["view cloud_ytd_savings"]
  end

  subgraph VIZ["Superset dashboards"]
    D_OV["Cost Overview"]
    D_TR["Trends"]
    D_MACC["(MACC charts on Cost Overview)"]
    D_DB["Databases / Storage / Network / Serverless / Compute"]
    D_MOLO["Secondary-org charts (Cost Overview)"]
  end

  BQ2 --> T_BUD & T_COMMIT & T_MKT
  CE2 --> T_BUD & T_MKT & T_MOLO
  ACM2 --> T_AZD & T_AZS & T_AZM & T_MACC & T_MKT
  CAT2 --> T_MACC
  CSV2 --> T_PRICE

  T_BUD --> V_BVA & V_YTD
  V_BVA --> D_OV
  V_YTD --> D_OV
  T_MKT --> D_OV
  T_AZM --> D_OV
  T_MACC --> D_MACC
  T_COMMIT --> D_OV
  T_AZD & T_AZS --> D_DB
  T_MOLO --> D_MOLO
  T_PRICE -->|"bot estimator tool"| D_OV
```

---

## 3. Scheduled jobs (systemd timers)

| Job (script) | Schedule | Writes / does |
|---|---|---|
| `azure_spend.py` | daily 08:35 | `azure_*` snapshot tables (subscription/service MTD, daily, service-YTD, marketplace YTD incl. GitHub rows) |
| `gcp_smooth_forecast.py` | daily 08:40 | `cloud_actuals.forecast_override` (smooth forecast) + **finalizes prior month** on rollover |
| `marketplace_alert.py` | daily 09:00 | Refreshes `cloud_marketplace` (GCP + AWS primary/secondary + Azure); posts marketplace alert to Slack; re-fires on late charges |
| `billing_alerts.py` | daily 09:30 | Burn-rate (GCP, AWS primary/secondary, Azure) + 7 GCP anomaly analysts + AWS/Azure anomaly checks → Slack |
| `azure_macc_catalog_refresh.py` | weekly | `azure_macc_offer_eligibility` (Catalog `isMacc`) |
| `azure_macc_snapshot.py` | daily | `azure_macc_progress_v2` (eligibility-proxy drawdown) |
| `gcp-commit-v2` | daily | `gcp_commit_progress_v2` (commit drawdown) |
| `marketplace_backfill.py` | one-shot | Idempotent historical backfill of `cloud_marketplace`, all providers |

---

## 4. Identity & access

| Path | Mechanism |
|---|---|
| VM → GCP | Attached service account `<SERVICE_ACCOUNT>@<DEV_PROJECT>.iam.gserviceaccount.com` |
| → AWS (primary, `<AWS_ACCOUNT_ID_PRIMARY>`) | GCP **Workload Identity Federation** → assume role `phinops-billing-reader` (auto-refreshing) |
| → AWS (secondary, `<AWS_ACCOUNT_ID_SECONDARY>`) | Long-lived IAM user keys in `.env` (`SECONDARY_AWS_*`) |
| → Azure (tenant `<AZURE_TENANT_ID>`) | App reg `phinops-billing-reader` (`<AZURE_APP_ID>`), `ClientAssertionCredential` federated from the GCP SA; **Cost Management Reader** at mgmt-group scope |
| → Azure Marketplace Catalog | Anonymous (`catalogapi.azure.com`) |
| Superset login | `AUTH_DB` (admin) — SSO (OAuth/IAP) not yet enabled |
| Bots → Superset | Authenticate as `admin` over `localhost` (`SUPERSET_ADMIN_PASSWORD`) |
| Bots → LLM | Vertex AI (`AnthropicVertex`, project `<DEV_PROJECT>`) or Anthropic API key |

---

## 5. Assistant tool surface (both bots)

`scripts/slack_bot.py` (Socket Mode, thread-scoped memory) and
`superset/views/finops_chat.py` (`/finops-chat/ask`, conversation memory) share an
agentic Claude tool loop:

- **GCP** — `get_gcp_monthly_spend`, `_spend_by_service`, `_spend_by_project`, `_cost_trend`, `run_superset_sql` (BigQuery)
- **AWS** — `get_aws_monthly_spend`, `_spend_by_service`, `_spend_by_account`, `_cost_trend` (primary + secondary)
- **Azure** — `get_azure_monthly_spend`, `_spend_by_service`, `_spend_by_subscription`, `_cost_trend`, **`query_azure_cost`** (flexible deep-query: any dimension/filter, multi-year auto-chunked — the Azure analog of `run_superset_sql`)
- **Pricing** — `lookup_gcp_sku_pricing`, `estimate_gcp_project_cost` (contract pricing from `gcp_sku_pricing`)
- **Charts** — `create_superset_chart`, `read_superset_chart` (web bot)

---

## 6. Key dashboards

`Cost Overview` (flagship: budget-vs-actual, YTD savings, MACC drawdown, marketplace by
product, GitHub, secondary org), `Trends`, `Databases`, `Memorystore`, `Data Analytics`,
`Compute Engine` / `Compute Engine - flexCUD` / `Compute Services`, `Kubernetes`,
`Storage Cost`, `Network Cost`, `Serverless Computing Cost`, `Marketplace Services`,
`Cost Reporting: Credits/Labels/Regions`.

---

## 7. Known gaps / roadmap

- **#1** Citations — bots should cite the source/params behind each answer.
- **#2** Production deployment — migrate to GKE (`<AGENTS_PROJECT>` / `ai-agents`): containers, Cloud SQL, Memorystore, Workload Identity, Secret Manager, ingress + TLS + SSO.
- **#3** Datadog integration — tag-enriched cloud-cost / unit-cost data.
- **#4** Recommended improvements — pipeline failure alerting, chart-config hygiene/lint, tests/CI, secrets out of `.env`, shared bot tool layer.

> **Single-VM caveats:** SPOF, plain-HTTP bare-IP ingress, `admin/admin` auth, secrets in
> `.env`, and silent job failures — all addressed by #2 / #4.
