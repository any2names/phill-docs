# TPL-008 — Access Review Template

## 1. Document control

| Field | Value |
|---|---|
| Document ID | TPL-008 |
| Title | Access Review Template |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | T — Template |
| Classification | Internal (blank template); each completed review is Confidential under SEC-002 |
| Owner | Head of Security Engineering |
| Approver | Chief Information Security Officer (CISO) |
| Effective date | [DECISION REQUIRED: Date of CISO approval] |
| Next review date | Effective date + 12 months |
| Parent document | SEC-003 Identity & Access Management Policy |
| Related documents | SEC-003, SEC-005, CMP-004, CMP-009, GOV-001 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Head of Security Engineering | Initial release |

## 3. Purpose

This Template records an Access Review performed under SEC-003 section 5.12 (all accounts) and
SEC-005 section 5.11 (Privileged Accounts). It captures the evidence an auditor needs to
confirm that the review covered a complete and accurate population, that a qualified reviewer
made a documented decision for every account and entitlement, and that every decision to
revoke or modify access was carried out and verified.

## 4. Instructions

| Item | Instruction |
|---|---|
| Who completes it | The reviewer designated for the system in the Access Review schedule maintained by the Head of GRC (SEC-003.5.12.8): the System Owner, Data Owner or Line Manager. Privileged access sections are reviewed by the System Owner, and Tier 0 roles by the Head of Security Engineering (SEC-005.5.11.2). The Data Custodian prepares Parts A and B. |
| When | At the frequency in SEC-003.7.1 for user access and SEC-005.7.1 for privileged access, and within the completion and remediation times in SEC-003.7.8. A system holding Restricted data or in `[SOX]` Financially Significant System scope uses the higher frequency. |
| One form per | System (or application), per review cycle. Large populations MAY attach the account listing as a spreadsheet export carrying the same columns as Part C; the attachment becomes part of this record. |
| Reviewer independence | A reviewer SHALL NOT review their own accounts (SEC-003.5.12.4). Record the alternate reviewer for those accounts in Part C. |
| Decisions | Every row in Parts C, D and E SHALL carry a decision: **R** Retain · **M** Modify (state the change) · **X** Revoke · **I** Investigate (unmatched or orphaned; disable within 1 business day per SEC-003.5.12.7). A blank decision is not permitted. |
| Remediation | Record each M and X decision in Part G with the ticket reference and completion date, then verify against the target system (SEC-003.5.12.6). |
| Where stored | The completed form, population extract and remediation evidence are stored in the Organization's GRC evidence repository under the system's record, named `TPL-008_<system>_<YYYY-Qn>`. |
| How long | Retained for the period for access reviews in CMP-004. |
| Classification | A completed form lists accounts and entitlements and is Confidential under SEC-002. |

## 5. Form

### Part A — Review details

| Field | Value |
|---|---|
| System / application name | |
| Asset Inventory identifier (SEC-001) | |
| System Owner | |
| Data Owner(s) | |
| Highest Classification Level of data (SEC-002) | ☐ Public ☐ Internal ☐ Confidential ☐ Restricted |
| Regulatory scope | ☐ `[SOX]` Financially Significant System ☐ `[PCI]` CDE ☐ `[HIPAA]` ePHI ☐ `[GDPR]`/`[CPRA]` Personal Data ☐ None |
| Review type | ☐ User access (SEC-003) ☐ Privileged access (SEC-005) ☐ Combined |
| Required frequency | ☐ Quarterly ☐ Every 6 months |
| Review period covered (from – to) | |
| Review launched (date) | |
| Review due (launch + completion time in SEC-003.7.8) | |
| Primary reviewer (name, role) | |
| Alternate reviewer for reviewer's own accounts (name, role) | |
| Prepared by (Data Custodian) | |
| Prior review reference and date | |
| Open items carried forward from prior review | ☐ None ☐ Yes (list in Part G) |

### Part B — Population completeness and accuracy

| Field | Value |
|---|---|
| Source of account listing (system, directory, or Identity Provider) | |
| Extraction method (report name, query, script, API) | |
| Query or report parameters (attach if script) | |
| Extracted by (name) | |
| Extraction date and time | |
| Total accounts extracted | |
| Total entitlements / role assignments extracted | |
| Account types included | ☐ Workforce Member ☐ Third-Party ☐ Service Account ☐ Privileged ☐ Break-glass ☐ Built-in / default |
| Completeness check performed (e.g. record count matched to system console, screenshot with timestamp) | |
| Accuracy check performed (e.g. sample of 5 accounts traced to system) | |
| HR / Third-Party roster used for matching (source and date) | |
| `[SOX]` IPE evidence attached per CMP-009 | ☐ Yes ☐ N/A |
| Evidence file references | |

### Part C — User account review

| # | Account ID | Display name | Account type | Owner / sponsor | Department / job title | HR or contract status | Role(s) / entitlement(s) | Data Classification accessible | Last login | SoD conflict (GOV-001) | Decision (R / M / X / I) | Justification (required for Restricted access, M, X, I) | Reviewer initials |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | | | | | | | | | | ☐ Yes ☐ No | | | |
| 2 | | | | | | | | | | ☐ Yes ☐ No | | | |
| 3 | | | | | | | | | | ☐ Yes ☐ No | | | |
| 4 | | | | | | | | | | ☐ Yes ☐ No | | | |
| 5 | | | | | | | | | | ☐ Yes ☐ No | | | |
| 6 | | | | | | | | | | ☐ Yes ☐ No | | | |
| 7 | | | | | | | | | | ☐ Yes ☐ No | | | |
| 8 | | | | | | | | | | ☐ Yes ☐ No | | | |
| 9 | | | | | | | | | | ☐ Yes ☐ No | | | |
| 10 | | | | | | | | | | ☐ Yes ☐ No | | | |

Flags the preparer SHALL mark before review (tick all that apply per row, or in the attached listing):

| Flag | Meaning | Required action |
|---|---|---|
| ☐ Terminated | HR or contract status shows Separation | X — and report as a late leaver revocation (SEC-003.7.3) |
| ☐ Inactive | No login in the inactivity period in SEC-003.7.6 | X, unless documented exemption |
| ☐ Unmatched | No matching Workforce Member, sponsor or Service Account owner | I — disable within 1 business day |
| ☐ Mover | Department or job title changed since last review | Confirm access fits new role |
| ☐ Expired | Third-Party or temporary account past expiry date | X |
| ☐ SoD | Conflicting role combination | X or approved Exception (CMP-003) reference |

### Part D — Privileged access review (SEC-005)

| # | Account ID | Owner | Account class (personal admin / built-in / Break-glass / cloud root or owner / privileged Service Account) | Tier (0 / 1 / 2) | Assignment (JIT-eligible / standing) | Standing-Privilege Register reference (if standing) | Vaulted in PAM? | Phishing-resistant MFA? | Role-based training current (PPL-002)? | Last use | Decision (R / M / X / I) | Justification | Reviewer initials |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | | | | | | | ☐ Y ☐ N | ☐ Y ☐ N | ☐ Y ☐ N | | | | |
| 2 | | | | | | | ☐ Y ☐ N | ☐ Y ☐ N | ☐ Y ☐ N | | | | |
| 3 | | | | | | | ☐ Y ☐ N | ☐ Y ☐ N | ☐ Y ☐ N | | | | |
| 4 | | | | | | | ☐ Y ☐ N | ☐ Y ☐ N | ☐ Y ☐ N | | | | |
| 5 | | | | | | | ☐ Y ☐ N | ☐ Y ☐ N | ☐ Y ☐ N | | | | |

| Privileged-specific checks | Result |
|---|---|
| Break-glass Account(s) tested this quarter (SEC-005.7.3); test date and reference | |
| All Break-glass and cloud root uses in period reviewed within the time in SEC-005.7.3 and SEC-005.7.14 | ☐ Yes ☐ No — list exceptions |
| Standing assignments not on Standing-Privilege Register | ☐ None ☐ Found — list in Part G |
| `[SOX]` Privileged activity log review completed per CMP-009 | ☐ Yes ☐ N/A — reference |

### Part E — Service Account review

| # | Service Account ID | Asset Owner | Documented purpose | Target systems | Entitlements | Credential type (workload identity / certificate / key / password) | Last credential rotation | Interactive login detected in period? | Last authentication | Decision (R / M / X / I) | Justification | Reviewer initials |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | | | | | | | | ☐ Y ☐ N | | | | |
| 2 | | | | | | | | ☐ Y ☐ N | | | | |
| 3 | | | | | | | | ☐ Y ☐ N | | | | |
| 4 | | | | | | | | ☐ Y ☐ N | | | | |

### Part F — Summary

| Measure | Count |
|---|---|
| Accounts reviewed (Parts C + D + E) | |
| Accounts reviewed as a percentage of population extracted in Part B | % (must be 100%) |
| Retain (R) | |
| Modify (M) | |
| Revoke (X) | |
| Investigate (I) | |
| Of which: terminated Workforce Members or Third Parties still active | |
| Of which: inactive beyond SEC-003.7.6 | |
| Of which: SoD conflicts | |
| Of which: unmatched / orphaned | |
| Date review decisions completed | |
| Completed within the time in SEC-003.7.8? | ☐ Yes ☐ No — escalated to CISO on (date) |

Reviewer conclusion (tick one):

- ☐ All access is required for current job function and authorized; no changes required.
- ☐ All access is required and authorized once the changes listed in Part G are completed.
- ☐ Significant issues found (terminated users active, unapproved privileged access, or SoD conflicts); escalated to the CISO and Head of GRC on (date): ________

### Part G — Remediation tracking

| # | Account ID | Part / row | Decision (M / X / I) | Change required | Ticket reference | Assigned to | Due date (decision + time in SEC-003.7.8) | Completed date | Verified against target system by (name) | Verification date and evidence reference | Root Cause (for terminated, unapproved or orphaned access) |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | | | | | | | | | | | |
| 2 | | | | | | | | | | | |
| 3 | | | | | | | | | | | |
| 4 | | | | | | | | | | | |
| 5 | | | | | | | | | | | |

| Remediation status | Value |
|---|---|
| All M and X items completed within the time in SEC-003.7.8 | ☐ Yes ☐ No |
| Late items escalated to CISO (date) | |
| Security Event raised to SOC Manager for any access used after it should have been removed (reference) | ☐ N/A ☐ Reference: |

### Part H — Quality check (Head of GRC or delegate)

| Check | Result |
|---|---|
| Population evidence in Part B supports completeness and accuracy | ☐ Pass ☐ Fail |
| Every row has a decision and, where required, a justification | ☐ Pass ☐ Fail |
| Reviewer did not review own access | ☐ Pass ☐ Fail |
| Remediation verified against the target system | ☐ Pass ☐ Fail |
| Review and remediation completed on time | ☐ Pass ☐ Fail |
| Checked by (name) and date | |

## 6. Approval signatures

| Role | Name | Signature | Date |
|---|---|---|---|
| Prepared by: Data Custodian | | | |
| Reviewer: System Owner / Data Owner / Line Manager | | | |
| Alternate reviewer (reviewer's own accounts) | | | |
| Privileged access reviewer (Tier 0): Head of Security Engineering | | | |
| Remediation verified by: Data Custodian | | | |
| Quality check: Head of GRC | | | |

Template approval:

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Head of Security Engineering | | | |
| Approver: CISO | | | |
