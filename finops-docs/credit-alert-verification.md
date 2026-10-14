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

# Credit-burn alert — fix & verification notes

## Background

`check_credit_acceleration()` in `scripts/billing_alerts.py` fired a bogus alert:

> TOP ISSUE — GCP Credit Burn Rate Spiking
> Projected credit consumption this month: **$X** vs $Y last month (**+1,511%**)

### Root cause
The check linearly extrapolated partial-month credits:
`projected = curr_credits / days_elapsed × days_in_month`.
GCP credits post in **lumps** (CUD / commitment credits, monthly true-ups), not
smoothly, so early in the month this explodes — a day-1/2 credit posting scaled
by ~30 produced the inflated figure.

### Fix
Replaced the projection with an **apples-to-apples same-period comparison**:
credits used *through day N this month* vs *through day N of the previous month*
— no extrapolation. Added two guards:
- **Day-5 minimum** — no comparison in the first few days of a month.
- **$100k absolute-delta floor** — must be both a ≥20% jump *and* a ≥$100k MTD
  dollar move, so percentage-only or tiny swings don't fire.

## Verification

### 1. Underlying SQL (real BigQuery data)
Same-period MTD query through day 15, validated directly:

| Month | Credits through day 15 |
|---|---:|
| 2026-05 | $X |
| 2026-06 | $Y |

Real, bounded numbers (June actually *lower* than May same-period) — no blow-up.

### 2. Decision logic (real function, simulated date + controlled data)
Drove the actual `check_credit_acceleration()` with a faked `date.today()` and
controlled credit rows across five scenarios:

| Scenario (simulated) | Result | Why correct |
|---|---|---|
| Day 15 — genuine spike (+60% / +$300k) | **FIRES** | real, material acceleration |
| Day 15 — small move (+4%) | silent | below 20% gate |
| Day 15 — big % but tiny $ (+100%, +$500) | silent | below $100k floor *(old bug class)* |
| Day 15 — current < prior (June<May) | silent | no false "spiking" |
| Day 4 — massive spike present | silent | day-5 guard holds |

Firing message is accurate and defensible:
> Credits used through day 15: $800,000 this month vs $500,000 same period last month (+60%)

### Re-running the verification
On the VM (BigQuery creds via `bq`; Superset admin auth is unrelated):
```bash
# SQL sanity (any two adjacent months, choose a cutoff day):
bq --project_id=<PROD_PROJECT> query --use_legacy_sql=false \
 "SELECT invoice.month AS m,
    ROUND(ABS(SUM(IFNULL((SELECT SUM(c.amount) FROM UNNEST(credits) c),0))),0) AS credits_mtd
  FROM \`<PROD_PROJECT>.<BILLING_DATASET>.gcp_billing_export_v1_<BILLING_ACCOUNT_ID>\`
  WHERE invoice.month IN ('202605','202606')
    AND EXTRACT(DAY FROM DATE(usage_start_time)) <= 15
  GROUP BY m ORDER BY m"
```
Logic is unit-testable by monkeypatching `billing_alerts.date` (fake `today()`)
and `billing_alerts._run` (controlled rows), then asserting on
`check_credit_acceleration(None)`.

## Status
Fixed, committed, verified. No further action; the daily
`billing-alerts` timer picks up the corrected logic.
