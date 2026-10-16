# TPL-003 — Policy Exception Request Form

## 1. Document control

| Field | Value |
|---|---|
| Document ID | TPL-003 |
| Title | Policy Exception Request Form |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | T — Template |
| Classification | Internal (Confidential once completed) |
| Owner | Head of GRC |
| Approver | Chief Information Security Officer (CISO) |
| Effective date | [DECISION REQUIRED: Date of CISO approval] |
| Next review date | Effective date + 12 months, and on any change to CMP-003 |
| Parent document | CMP-003 Policy Exception & Waiver Policy |
| Related documents | CMP-003, CMP-004, RSK-001, RSK-002, TPL-001, TPL-002, SEC-001, SEC-002, RSK-004 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Head of GRC | Initial release |

## 3. Purpose

This form records a request for an Exception to a SHALL or SHALL NOT requirement of a suite
document, its risk assessment, specialist reviews, Compensating Controls and decision, so
that every Exception meets the content and approval requirements of CMP-003.

## 4. Instructions

| Item | Instruction |
|---|---|
| Who completes it | Part A–F: the requester, with the executive sponsor. Part G: the Head of GRC (completeness) and the CISO's delegate (risk validation). Part H: each required specialist reviewer. Part I: the approving authority. Part J: the Head of GRC. |
| When | Before any deviation begins; for a renewal, at least 15 business days before the current end date (CMP-003.5.6.3); after an emergency Exception, within 5 business days (CMP-003.5.7.3). |
| Scope of one form | One requirement, or one stated group of requirements in the same document, for named Information Assets (CMP-003.5.1.2). Use a separate form for each document. |
| Do not use for | Requirements listed in CMP-003.5.2.1; these are rejected and routed to the Risk Register. Risk Acceptance without a requirement deviation uses TPL-002. |
| Where submitted | The GRC ticketing or workflow system. Email, chat and verbal requests are not accepted (CMP-003.5.3.1). |
| Completeness | Every field marked * is mandatory. Incomplete forms are returned within 3 business days, and the decision clock starts only when the form is complete (CMP-003.5.3.3). |
| Risk scoring | Use the scoring method and risk levels in RSK-002.7.1 and RSK-002.7.2. |
| Approval authority | Determined by validated Residual Risk level as set in RSK-001 (CMP-003.7.4). |
| Classification | A completed form is Confidential under SEC-002. |
| Storage and retention | The completed form, attachments and decision are stored in the Exception Register and the Evidence repository, and retained per CMP-004 (risk register entries, risk acceptances, exceptions). |

## 5. Form

### Part A — Request type and requester

| Field | Value |
|---|---|
| Exception ID (assigned by GRC) | |
| Request type * | ☐ New ☐ Renewal ☐ Follow-up to emergency Exception ☐ Scope change to approved Exception |
| Prior Exception ID (renewal / follow-up / scope change) | |
| Renewal number (1 or 2) | ☐ 1st renewal ☐ 2nd (final) renewal |
| Requester name * | |
| Requester role and business unit * | |
| Executive sponsor (director level or above) name and role * | |
| Control Owner of the affected requirement * | |
| Date submitted * | |

### Part B — Requirement deviated from

| Field | Value |
|---|---|
| Suite document ID and title * | |
| Requirement ID(s) * (e.g. SEC-004.5.2.1) | |
| Requirement text, quoted verbatim * | |
| Description of the deviation: what will be done instead * | |
| Confirmation that the requirement is not in CMP-003.5.2.1 or in section 9 of its document as non-exceptionable * | ☐ Confirmed |

### Part C — Scope

| Field | Value |
|---|---|
| Information Assets / Information Systems affected (Asset Inventory IDs, SEC-001) * | |
| Accounts, locations or Third Parties affected | |
| Highest Classification Level of data involved (SEC-002) * | ☐ Public ☐ Internal ☐ Confidential ☐ Restricted |
| Recovery Tier of affected systems (RSK-004) * | ☐ Tier 0 ☐ Tier 1 ☐ Tier 2 ☐ Tier 3 ☐ Not assigned |
| Number of Users or records affected (estimate) | |

Regulated scope (tick all that apply) *:

| Flag | Applies | Required specialist review (Part H) |
|---|---|---|
| `[PCI]` CDE or connected-to system component | ☐ Yes ☐ No | Head of Security Engineering |
| `[HIPAA]` ePHI system | ☐ Yes ☐ No | HIPAA Security Officer |
| `[SOX]` Financially Significant System | ☐ Yes ☐ No | CFO or delegate |
| `[GDPR]` `[CPRA]` Personal Data | ☐ Yes ☐ No | CPO and GC |
| Contractual obligation to a customer or Third Party | ☐ Yes ☐ No | GC (counterparty written consent required) |
| None of the above | ☐ | — |

### Part D — Justification

| Field | Value |
|---|---|
| Business justification: why the requirement cannot be met * | |
| Constraint type * | ☐ Technical ☐ Cost ☐ Operational ☐ Third-Party dependency ☐ Legal / contractual ☐ Other: ____ |
| Business impact if the Exception is rejected * | |
| Alternatives considered and reasons rejected * | |
| Linked Vulnerability (if deferring remediation beyond the SEC-011 SLA): ID and severity | |
| Linked Security Incident (emergency follow-up only): incident ID | |

### Part E — Risk assessment (RSK-002)

| Assessment | Likelihood (1–5) | Impact (1–5) | Score (RSK-002.7.1) | Level (Low / Medium / High / Critical, per RSK-002.7.2) |
|---|---|---|---|---|
| Inherent Risk of the deviation (no Compensating Controls) * | | | | |
| Residual Risk with proposed Compensating Controls * | | | | |
| Residual Risk as validated by CISO's delegate (Part G) | | | | |

| Field | Value |
|---|---|
| Threat(s) the original requirement addresses * | |
| Risk scenario description * | |
| Linked Risk Register entry (TPL-001), required where validated Residual Risk is High or Critical | |
| Linked Risk Acceptance (TPL-002), if any | |

### Part F — Compensating Controls, duration and remediation

Compensating Controls (at least one where Residual Risk is Medium or above; CMP-003.5.5.1) *:

| # | Compensating Control description | How it meets the intent of the requirement | Control Owner | Operating frequency | Evidence of operation | Implemented before start? |
|---|---|---|---|---|---|---|
| 1 | | | | | | ☐ Yes ☐ No |
| 2 | | | | | | ☐ Yes ☐ No |
| 3 | | | | | | ☐ Yes ☐ No |

Compensating Control test (CMP-003.5.5.2). Each must be ticked for each control:

| Test | CC 1 | CC 2 | CC 3 |
|---|---|---|---|
| Meets the intent and rigor of the original requirement | ☐ | ☐ | ☐ |
| Provides comparable defense against the same Threat | ☐ | ☐ | ☐ |
| Goes beyond Controls already required elsewhere in the suite | ☐ | ☐ | ☐ |
| Commensurate with the additional Risk created | ☐ | ☐ | ☐ |
| `[PCI]` Compensating Controls Worksheet (PCI DSS Appendix C) attached | ☐ N/A | ☐ N/A | ☐ N/A |

| Field | Value |
|---|---|
| Requested start date * | |
| Requested end date * (max per CMP-003.7.1) | |
| Remediation approach * | ☐ Achieve compliance by end date ☐ Propose change to requirement under GOV-002 ☐ Decommission affected asset |

Remediation plan *:

| # | Milestone | Owner | Target date | Evidence of completion |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

Renewal only: progress since last approval and reason remediation is not complete:

| Field | Value |
|---|---|
| Milestones completed | |
| Milestones missed and reasons | |
| Compensating Control failures during the prior period | ☐ None ☐ Yes (describe): |

Requester and sponsor declaration *:

☐ The information in this request is accurate and complete. I understand that the deviation
may not begin until the Exception is approved and recorded, that it ends on the approved end
date, and that misrepresentation is a violation under CMP-007.

| Role | Name | Signature | Date |
|---|---|---|---|
| Requester | | | |
| Executive sponsor | | | |

### Part G — GRC completeness and risk validation

| Field | Value |
|---|---|
| Completeness check result | ☐ Complete ☐ Returned — missing elements: |
| Date marked complete (decision clock starts) | |
| Non-exceptionable (CMP-003.5.2.1)? | ☐ No ☐ Yes — rejected, routed to Risk Register (date): |
| Validated Residual Risk level | ☐ Low ☐ Medium ☐ High ☐ Critical |
| Required approval authority (RSK-001) | ☐ Risk Owner ☐ CISO ☐ ISSC ☐ CEO (Audit Committee notified) |
| Escalated one level due to negative specialist review (CMP-003.5.4.4) | ☐ No ☐ Yes |
| Maximum end date permitted (CMP-003.7.1) | |
| Head of GRC name, signature, date | |
| CISO's delegate (risk validation) name, signature, date | |

### Part H — Specialist reviews (complete each that applies from Part C)

| Reviewer | Recommendation | Comments / conditions | Name | Signature | Date |
|---|---|---|---|---|---|
| `[PCI]` Head of Security Engineering | ☐ Support ☐ Do not support | | | | |
| `[HIPAA]` HIPAA Security Officer | ☐ Support ☐ Do not support | | | | |
| `[SOX]` CFO or delegate | ☐ Support ☐ Do not support | | | | |
| `[GDPR]` `[CPRA]` CPO | ☐ Support ☐ Do not support | | | | |
| GC (Personal Data or contractual) | ☐ Support ☐ Do not support | | | | |
| GC: counterparty written consent verified | ☐ N/A ☐ Verified (reference): | | | | |

### Part I — Decision

| Field | Value |
|---|---|
| Decision | ☐ Approved ☐ Approved with conditions ☐ Rejected |
| Reasons for decision | |
| Conditions (specific and verifiable) | |
| Approved start date | |
| Approved end date | |
| Compensating Control Evidence frequency (CMP-003.7.8) | ☐ Quarterly ☐ Monthly (High / Critical) |
| Audit Committee notification date (Critical only) | |

Confirmation that the approver is not the requester, sponsor or Control Owner (CMP-003.5.4.5): ☐ Confirmed

| Role | Name | Signature | Date |
|---|---|---|---|
| Approving authority | | | |

## 6. Approval signatures

### Part J — Register and closure (Head of GRC)

| Field | Value |
|---|---|
| Recorded in Exception Register (date, before start) | |
| Compensating Control implementation Evidence received (date) | |
| Expiry notice sent: 30 days before end date | |
| Expiry notice sent: 10 business days before end date | |
| Closure reason | ☐ Requirement met ☐ Asset decommissioned ☐ Requirement changed (GOV-002) ☐ Expired ☐ Revoked ☐ Converted to Risk Acceptance (TPL-002) |
| Closure Evidence location (CMP-004) | |
| Closure date | |

| Role | Name | Signature | Date |
|---|---|---|---|
| Head of GRC (register entry) | | | |
| Head of GRC (closure) | | | |
| Control Owner (closure Evidence) | | | |
