# TPL-001 — Risk Register Template

## 1. Document control

| Field | Value |
|---|---|
| Document ID | TPL-001 |
| Title | Risk Register Template |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | T — Template |
| Classification | Internal (template); completed Risk Register: Confidential |
| Owner | Head of GRC |
| Approver | Chief Information Security Officer (CISO) |
| Effective date | [DECISION REQUIRED: Date of CISO approval] |
| Next review date | Effective date + 12 months |
| Parent document | RSK-001 Risk Management Policy |
| Related documents | RSK-002, RSK-003, RSK-004, RSK-006, CMP-003, CMP-004, TPL-002 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Head of GRC | Initial release |

## 3. Purpose

This Template defines the mandatory structure of the Risk Register required by RSK-001, so
that every Risk is recorded with the same fields, scored using the RSK-002 method, linked to
its treatment, acceptance and Evidence, and reportable to the ISSC and the Audit Committee.

## 4. Instructions

| Item | Instruction |
|---|---|
| Who maintains it | The Head of GRC maintains the Risk Register. Risk Owners update status, treatment progress and review dates for their own Risks. Assessors record scores and rationale. |
| When an entry is created | When a Risk is identified from any source in RSK-001.5.2.2, and within 10 business days of rating for Risks transferred from a local risk log (RSK-001.5.1.4). |
| When it is updated | On every score change, treatment milestone, Risk Acceptance, Exception link, Risk Owner review at the frequency in RSK-001, and closure. The ISSC reviews the register at the frequency set in RSK-001. |
| Format | Implement as a GRC tool, database or controlled spreadsheet with one row per Risk using the fields in section 5. Field names and allowed values SHALL NOT be changed without approval of this Template. Each change SHALL be logged with user and timestamp. |
| Scoring | Use the likelihood and impact criteria, level bands and Control effectiveness rules in RSK-002. Do not average impact dimensions. |
| Classification and access | The completed register is Confidential under SEC-002. Access is restricted as set in RSK-001. |
| Storage and retention | Store in the GRC repository designated by the Head of GRC. Closed entries are retained for the period set in CMP-004 and SHALL NOT be deleted from the register before that period ends. |
| Linked forms | Risk Acceptances: TPL-002. Exceptions: TPL-003. Third-party Risks: TPL-004 results. |

## 5. Form

### 5.1 Risk identification

| Field | Description / allowed values | Value |
|---|---|---|
| Risk ID | `RSK-YYYY-NNNN`, assigned by the Head of GRC, never reused | |
| Date identified | YYYY-MM-DD | |
| Identified by (role) | Role of the person or the process that identified the Risk | |
| Source | ☐ Enterprise assessment ☐ Triggered assessment ☐ Vulnerability (SEC-011) ☐ Security Incident (RES-002) ☐ Audit finding (CMP-002) ☐ Third-party assessment (RSK-003) ☐ Threat Model / intelligence (RSK-005) ☐ BIA (RSK-004) ☐ AI assessment (RSK-006) ☐ Exception (CMP-003) ☐ Workforce report ☐ `[PCI]` TRA ☐ Other: ____ | |
| Risk title | Short statement, ≤ 15 words | |
| Risk statement | "Because of <cause / Vulnerability>, <Threat source> may <Threat event>, resulting in <impact on objective>." | |
| Primary Risk category (RSK-001) | ☐ C1 Information security ☐ C2 Privacy ☐ C3 Regulatory ☐ C4 Financial reporting `[SOX]` ☐ C5 Operational resilience ☐ C6 Third-party ☐ C7 Technology & AI ☐ C8 Strategic & reputational ☐ C9 People & safety | |
| Secondary categories | Any of C1–C9 | |
| Affected Information Assets / systems | Asset Inventory IDs (SEC-001) | |
| Highest Classification Level involved (SEC-002) | ☐ Public ☐ Internal ☐ Confidential ☐ Restricted | |
| Recovery Tier of affected services (RSK-004) | ☐ Tier 0 ☐ Tier 1 ☐ Tier 2 ☐ Tier 3 ☐ N/A | |
| Regulation tags | ☐ `[PCI]` ☐ `[HIPAA]` ☐ `[SOX]` ☐ `[GDPR]` ☐ `[CPRA]` ☐ None | |
| Related Third Party and vendor tier (RSK-003) | Name and Tier 1–4, if applicable | |
| MITRE ATT&CK technique(s) (RSK-005) | Technique IDs, if applicable | |
| Risk Owner (name and role) | Assigned within the period set in RSK-001 | |
| Date Risk Owner assigned | YYYY-MM-DD | |

### 5.2 Inherent Risk (RSK-002)

| Field | Description / allowed values | Value |
|---|---|---|
| Likelihood (1–5) | Rare 1 · Unlikely 2 · Possible 3 · Likely 4 · Almost certain 5 | |
| Likelihood rationale | Criterion met in RSK-002 section 5.2 and data relied on | |
| Impact — Financial (1–5) | | |
| Impact — Regulatory & legal (1–5) | | |
| Impact — Operational (1–5) | | |
| Impact — Reputational (1–5) | | |
| Impact — Safety & privacy (1–5) | | |
| Impact score | Highest of the five dimensions | |
| Impact rationale | Criterion met in RSK-002 section 5.3 | |
| Inherent Risk score (L × I) | Per RSK-002.7.1 | |
| Inherent Risk level | ☐ Low ☐ Medium ☐ High ☐ Critical (bands per RSK-002.7.2) | |

### 5.3 Existing Controls

| # | Control description | Control ID (REF-001) | Control Owner | Type (preventive / detective / corrective) | Axis reduced (likelihood / impact) | Effectiveness (Effective / Partially effective / Ineffective) | Evidence reference and date |
|---|---|---|---|---|---|---|---|
| 1 | | | | | | | |
| 2 | | | | | | | |
| 3 | | | | | | | |

### 5.4 Residual Risk (RSK-002)

| Field | Description / allowed values | Value |
|---|---|---|
| Residual likelihood (1–5) | After Control reductions allowed by RSK-002 section 5.5 | |
| Residual impact (1–5) | Highest dimension after Control reductions | |
| Residual Risk score (L × I) | Per RSK-002.7.1 | |
| Residual Risk level | ☐ Low ☐ Medium ☐ High ☐ Critical | |
| Category tolerance (RSK-001 section 5.3) | Maximum Residual Risk without acceptance for the category | |
| Within tolerance? | ☐ Yes ☐ No | |
| Assessor (role) and date | | |
| Independent reviewer (role) and date | Head of GRC or CISO for High and Critical | |
| Date score finalized | Starts the treatment deadline | |

### 5.5 Treatment

| Field | Description / allowed values | Value |
|---|---|---|
| Treatment option(s) | ☐ Mitigate ☐ Transfer ☐ Avoid ☐ Accept | |
| Treatment plan deadline | Date score finalized + deadline for the level in RSK-002 | |
| Interim measures (Critical only) | Measures and date implemented (deadline in RSK-002) | |
| Target Residual Risk score and level | | |
| Change / ticket references | SEC-013 change IDs; SEC-011 Vulnerability IDs | |

| Milestone # | Action | Control Owner | Due date | Status (Not started / In progress / Complete / Overdue) | Completion Evidence |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

### 5.6 Acceptance, Exceptions and escalation

| Field | Description / allowed values | Value |
|---|---|---|
| Risk Acceptance reference (TPL-002) | Form ID | |
| Acceptance approver (role) | Per authority in RSK-001 | |
| Acceptance approval date | | |
| Acceptance expiry date | Within the validity in RSK-001 | |
| Consecutive acceptance count | 1, 2 … | |
| Linked Exception (CMP-003 / TPL-003) | Exception ID | |
| Escalations | Date and recipient of each escalation under RSK-001 section 5.6 | |
| Audit Committee notified (Critical acceptances) | Date | |

### 5.7 Monitoring and closure

| Field | Description / allowed values | Value |
|---|---|---|
| Required Risk Owner review frequency | Per RSK-001 for the current level | |
| Last Risk Owner review date | | |
| Next review due | | |
| Linked KRI (GOV-003) | KRI ID | |
| Status | ☐ Open — assessing ☐ Open — treatment in progress ☐ Open — accepted ☐ Closed | |
| Closure date | | |
| Closure reason | ☐ Risk source removed ☐ Residual Risk within tolerance and Evidence obtained ☐ Merged into Risk ID ____ ☐ Avoided | |
| Retention end date | Closure date + period in CMP-004 | |

### 5.8 Change log

| Date | Changed by (role) | Field(s) changed | Previous value | New value | Reason |
|---|---|---|---|---|---|
| | | | | | |

### 5.9 Register summary view (for ISSC reporting)

| Risk ID | Title | Category | Risk Owner | Inherent score / level | Residual score / level | Within tolerance | Treatment status | Acceptance expiry | Next review |
|---|---|---|---|---|---|---|---|---|---|
| | | | | | | | | | |

## 6. Approval signatures

This Template is approved as follows. Individual Risk Register entries do not require
signature; approvals of treatment and acceptance are recorded in sections 5.4–5.6 and on TPL-002.

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Head of GRC | | | |
| Approver: CISO | | | |
