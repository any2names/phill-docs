# TPL-002 — Risk Acceptance Form

## 1. Document control

| Field | Value |
|---|---|
| Document ID | TPL-002 |
| Title | Risk Acceptance Form |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | T — Template |
| Classification | Internal (template); completed form: Confidential |
| Owner | Head of GRC |
| Approver | Chief Information Security Officer (CISO) |
| Effective date | [DECISION REQUIRED: Date of CISO approval] |
| Next review date | Effective date + 12 months |
| Parent document | RSK-001 Risk Management Policy |
| Related documents | RSK-002, CMP-003, CMP-004, TPL-001, TPL-003 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Head of GRC | Initial release |

## 3. Purpose

This form records a Risk Acceptance under RSK-001 section 5.5: an informed, time-limited
decision by the authorized approver to retain a Residual Risk without further treatment. It
captures the information the approver needs to decide, and the conditions, expiry and
signatures an auditor needs to verify that the acceptance was authorized and remains valid.

## 4. Instructions

| Item | Instruction |
|---|---|
| Who completes it | The Risk Owner completes sections 5.1–5.5. The Head of GRC completes section 5.6 (validation). The approver completes section 5.7. |
| When | Before the treatment-plan deadline in RSK-002 for the Risk's level, whenever the Risk Owner selects "Accept"; at renewal of an expiring acceptance; and when RSK-002 or RSK-004 requires a Risk Acceptance (for example a lower Recovery Tier than the criteria produce). |
| Not to be used for | Non-compliance with a law, regulation or binding contract, including PCI DSS: use TPL-003 under CMP-003 instead (RSK-001.5.5.5). Critical Residual Risks in categories C2, C3, C4 or C9, which cannot be accepted (RSK-001.5.3.3). |
| Approval authority and validity | As set in RSK-001 section 5.5, by Residual Risk level. The approver SHALL NOT be the Risk Owner except for Low Residual Risk, and SHALL NOT own the activity giving rise to the Risk. |
| Submission | Submit to the Head of GRC, who validates the form within 5 business days and routes it to the approver. |
| Storage and retention | The Head of GRC stores the signed form in the GRC repository and links it to the Risk Register entry (TPL-001). Retain for the period set in CMP-004. |
| Classification | Completed forms are Confidential under SEC-002. |

## 5. Form

### 5.1 Request details

| Field | Value |
|---|---|
| Acceptance ID (assigned by Head of GRC) | `RA-YYYY-NNNN` |
| Risk ID (TPL-001) | |
| Risk title | |
| Request type | ☐ New ☐ Renewal (previous acceptance ID: ____ ; consecutive count: ____ ) |
| Risk Owner (name, role) | |
| Business unit | |
| Date submitted | |

### 5.2 Risk description

| Field | Value |
|---|---|
| Risk statement (cause, Threat event, impact) | |
| Primary Risk category (RSK-001) | ☐ C1 ☐ C5 ☐ C6 ☐ C7 ☐ C8 ☐ C2 / C3 / C4 / C9 (Critical not acceptable) |
| Affected Information Assets / systems | |
| Highest Classification Level involved | ☐ Public ☐ Internal ☐ Confidential ☐ Restricted |
| Regulation tags | ☐ `[PCI]` ☐ `[HIPAA]` ☐ `[SOX]` ☐ `[GDPR]` ☐ `[CPRA]` ☐ None |

### 5.3 Risk scoring (from RSK-002)

| | Likelihood (1–5) | Impact (1–5) | Score (RSK-002.7.1) | Level (RSK-002.7.2) |
|---|---|---|---|---|
| Inherent Risk | | | | |
| Residual Risk (to be accepted) | | | | |

| Check | Yes | No |
|---|---|---|
| Residual Risk is within the "Maximum acceptable Residual Risk" for the category (RSK-001 section 5.3) | ☐ | ☐ |
| Scores independently reviewed under RSK-002 | ☐ | ☐ |

### 5.4 Justification and alternatives

| Field | Value |
|---|---|
| Business justification for accepting rather than treating | |
| Treatment options considered and why rejected (mitigate / transfer / avoid), with estimated cost of each | |
| Controls relied on to limit the Risk (with Control IDs and effectiveness rating) | |
| Monitoring in place during the acceptance (KRIs, alerts, reviews) | |
| Remediation plan, if any, to be completed before expiry | |

### 5.5 Conditions and duration

| Field | Value |
|---|---|
| Requested start date | |
| Requested expiry date (within RSK-001 validity) | |
| Conditions that void this acceptance (in addition to RSK-001.5.5.7) | |
| Compliance obligations reviewed (Obligations Register, CMP-001) — confirms no legal non-compliance is being accepted | ☐ Confirmed by Risk Owner ☐ Confirmed by GC (required for categories C3 and C4) |
| Privacy review (required for category C2 or any Personal Data) | ☐ Confirmed by CPO / DPO ☐ N/A |

**Risk Owner declaration:** I confirm that the information above is complete and accurate, that I understand the Risk being accepted, and that I will monitor it and notify the Head of GRC within 5 business days of any change that increases its score or triggers a voiding condition.

| Risk Owner name | Signature | Date |
|---|---|---|
| | | |

### 5.6 Validation (Head of GRC)

| Check | Yes | No | Notes |
|---|---|---|---|
| Form complete | ☐ | ☐ | |
| Residual Risk level confirmed | ☐ | ☐ | |
| Not a legal or contractual non-compliance (otherwise route to CMP-003) | ☐ | ☐ | |
| Not a Critical Residual Risk in C2, C3, C4 or C9 | ☐ | ☐ | |
| Required approver identified per RSK-001 section 5.5 | ☐ | ☐ | |
| Approver independent of the Risk and the activity | ☐ | ☐ | |
| Renewal count within RSK-001 limit; next-level approval obtained where required | ☐ | ☐ | |
| Expiry date within RSK-001 validity for the level | ☐ | ☐ | |

| Approver routed to | ☐ Risk Owner (Low) ☐ CISO (Medium) ☐ ISSC (High) ☐ CEO (Critical) |
|---|---|

| Head of GRC name | Signature | Date validated |
|---|---|---|
| | | |

### 5.7 Decision

| Field | Value |
|---|---|
| Decision | ☐ Approved ☐ Approved with conditions ☐ Rejected — treat the Risk |
| Additional conditions set by approver | |
| Approved expiry date | |
| For High: ISSC meeting date and minute reference | |
| For Critical: date Audit Committee notified (deadline in RSK-001) | |

| Approver role | Name | Signature | Date |
|---|---|---|---|
| | | | |

### 5.8 Post-decision tracking (Head of GRC)

| Field | Value |
|---|---|
| Risk Register updated (date) | |
| Expiry reminder sent to Risk Owner (date; notice period in RSK-001) | |
| Voided before expiry? | ☐ No ☐ Yes — date and reason: |
| Outcome at expiry | ☐ Risk treated ☐ Risk closed ☐ New acceptance (ID: ____ ) |

## 6. Approval signatures

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Head of GRC | | | |
| Approver: CISO | | | |
