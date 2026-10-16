# CMP-003 — Policy Exception & Waiver Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | CMP-003 |
| Title | Policy Exception & Waiver Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Head of GRC |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-001, GOV-002, GOV-003, GOV-006, RSK-001, RSK-002, CMP-001, CMP-002, CMP-004, CMP-005, CMP-006, CMP-007, CMP-008, CMP-009, SEC-019, TPL-001, TPL-002, TPL-003, REF-001 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Head of GRC | Initial release |

## 3. Purpose

This Policy establishes the single process by which the Organization requests, evaluates,
approves, records, monitors, renews and closes Exceptions to SHALL and SHALL NOT
requirements in the Information Security & GRC Policy Suite. It ensures that every
deviation is known, risk-assessed, approved at the level matching its Residual Risk,
protected by Compensating Controls where possible, time-limited, and tracked to closure,
and that requirements imposed by law or by binding contract are never waived internally.

## 4. Scope

- **People:** All Workforce Members who request, assess, approve or own an Exception, and
  all Risk Owners, Control Owners, System Owners, Asset Owners and Data Owners affected by one.
- **Documents:** Every SHALL and SHALL NOT requirement in every suite document (ISP, GOV, RSK,
  CMP, SEC, RES, PPL, TPL and REF series), and every Configuration Baseline, procedure or
  work instruction that implements them. SHOULD requirements are outside this Policy's
  approval process (GOV-006.5.2.1) but their documented justifications are subject to the
  register sampling in section 5.9.
- **Systems and data:** All Information Systems, Cloud Services and Information Assets,
  at every Classification Level, in every location, including the CDE `[PCI]`, ePHI systems
  `[HIPAA]` and Financially Significant Systems `[SOX]`.
- **Third Parties:** Third Parties that request deviation from a suite requirement flowed down
  to them by contract. Deviations from a Third Party's contractual security obligations are
  requested under this Policy by the Organization's relationship owner; contractual
  amendments themselves are governed by RSK-003.
- **Out of scope:** Acceptance of a Risk that does not involve deviation from a suite
  requirement (RSK-001, TPL-002); case-by-case departures from the sanctions matrix
  (CMP-007); and addressable-specification decisions `[HIPAA]` (CMP-008).

## 5. Policy statements

### 5.1 General principles

- **CMP-003.5.1.1** No Workforce Member SHALL deviate from a SHALL or SHALL NOT requirement of a suite document unless an Exception covering that deviation has been approved under this Policy and is in force, except as permitted by CMP-003.5.7 (emergency Exceptions).
- **CMP-003.5.1.2** An Exception SHALL apply to one requirement (or one stated group of requirements in the same document), for named Information Assets, for a stated period. Blanket Exceptions covering a whole document, a whole Classification Level or "all systems" SHALL NOT be approved.
- **CMP-003.5.1.3** An Exception SHALL NOT be used to defer remediation of a Vulnerability beyond the SLA in SEC-011 without the request identifying the Vulnerability, its severity and the Compensating Controls applied.
- **CMP-003.5.1.4** An Exception SHALL NOT be approved where the requested deviation is listed in section 5.2 (non-exceptionable requirements).
- **CMP-003.5.1.5** An Exception does not change the requirement it deviates from. Where the Document Owner concludes that a requirement is unworkable for a recurring class of cases, the Document Owner SHALL propose a change to the document under GOV-002 instead of approving repeated Exceptions. Three or more approved Exceptions against the same requirement in a rolling 12-month period SHALL trigger a GOV-002 review of that requirement by its Document Owner, started within 30 days.
- **CMP-003.5.1.6** The existence of an approved Exception SHALL NOT be represented to a customer, auditor, QSA, regulator or other external party as compliance with the requirement. Disclosure of Exceptions to external assessors is governed by CMP-001 and CMP-002.
- **CMP-003.5.1.7** Every Exception SHALL be recorded in the Exception Register (section 5.8) before it takes effect.

### 5.2 Requirements that SHALL NOT receive an Exception

- **CMP-003.5.2.1** No Exception SHALL be approved, by any authority, for the following:
  1. Any requirement whose deviation would cause the Organization to breach an applicable law or regulation recorded in the Obligations Register (CMP-001), including statutory notification deadlines (RES-003) and Data Subject Request deadlines (CMP-010).
  2. `[PCI]` Storage of Sensitive Authentication Data after authorization, in any form, including in logs, debug files, Backups or databases.
  3. `[PCI]` Use of a PCI DSS compensating control (Appendix B) or customized approach (Appendix D) without the Compensating Controls Worksheet or Targeted Risk Analysis and the QSA validation required by CMP-003.5.5.6 and RSK-002.5.8.4.
  4. `[HIPAA]` Any Required implementation specification of 45 CFR Part 164 Subpart C, and the sanction policy required by §164.308(a)(1)(ii)(C) (CMP-007, CMP-008).
  5. `[GDPR]` `[CPRA]` The requirement for a lawful basis for processing, Art. 28 Processor contract terms, Chapter V transfer mechanisms, and `[CPRA]` opt-out of sale/sharing, Opt-out Preference Signals and limitation of use of Sensitive Personal Information, as listed in CMP-005 section 9.
  6. `[SOX]` Deviation from a Key Control in a Financially Significant System where the deviation has not been assessed by the CFO for its effect on internal control over financial reporting (CMP-009).
  7. Legal Hold directives, and the prohibition on deleting, altering or concealing records under Legal Hold (CMP-004).
  8. Non-retaliation, reporter confidentiality, the anonymous reporting channel and the `[SOX]` Audit Committee complaint procedures (CMP-006 section 9).
  9. Internal Audit independence and escalation requirements listed in CMP-002 section 9.
  10. Due-process requirements and the prohibition on sanctioning protected reporting (CMP-007 section 9).
  11. Segregation of duties between a document's owner and its approver (GOV-002), and between the requester and approver of an Exception (CMP-003.5.4.5).
  12. A binding contractual obligation to a customer or Third Party, unless that counterparty has given written consent to the deviation, verified by the GC.
  13. Any requirement listed as non-exceptionable in section 9 of the document that contains it.
- **CMP-003.5.2.2** Where a requirement listed in CMP-003.5.2.1 cannot be met, the accountable owner SHALL record the gap as a Risk in the Risk Register (TPL-001), notify the GC within 1 business day, and remediate under the Risk Treatment deadline in RSK-002. The GC SHALL determine whether any disclosure or notification is legally required.
- **CMP-003.5.2.3** The Head of GRC SHALL reject, within 2 business days of receipt, any request for a deviation listed in CMP-003.5.2.1, recording the rejection and the reason in the Exception Register, and SHALL route the requester to CMP-003.5.2.2.

### 5.3 Request content

- **CMP-003.5.3.1** Every Exception request SHALL be submitted using TPL-003 through the Organization's GRC ticketing or workflow system. Requests by email, chat or verbal agreement SHALL NOT be accepted, except as an initial notification under CMP-003.5.7.
- **CMP-003.5.3.2** A request is complete only when it contains all of the following:
  1. Requester name, role and business unit, and the accountable executive sponsor (director level or above).
  2. The suite document ID and requirement ID(s) (e.g. `SEC-004.5.2.1`) deviated from, quoted verbatim.
  3. A precise description of the deviation: what is done instead of the requirement.
  4. The Information Assets, Information Systems, accounts, locations or Third Parties affected, by Asset Inventory identifier (SEC-001), and their Classification Level (SEC-002) and Recovery Tier (RSK-004).
  5. Whether the affected scope includes the CDE `[PCI]`, ePHI `[HIPAA]`, a Financially Significant System `[SOX]`, or Personal Data `[GDPR]` `[CPRA]`.
  6. The business justification, including why the requirement cannot be met and the cost, operational or technical constraint that prevents it.
  7. Alternatives considered and why they were rejected.
  8. Inherent Risk and Residual Risk scored under RSK-002 (likelihood, impact, score and level), with and without Compensating Controls.
  9. Compensating Controls proposed (section 5.5), each with an owner and the Evidence that will demonstrate operation.
  10. The requested start date and end date, which SHALL NOT exceed the maximum duration in CMP-003.7.1.
  11. A remediation plan to achieve compliance by the end date, with milestones, owners and dates, or a statement that a GOV-002 change to the requirement is being proposed.
  12. Whether this is a new request or a renewal, and for a renewal, the prior Exception ID and the renewal count.
- **CMP-003.5.3.3** The Head of GRC SHALL check each request for completeness within 3 business days of submission and SHALL return incomplete requests to the requester stating each missing element. The decision clock in CMP-003.7.3 starts on the date the request is marked complete.

### 5.4 Assessment and approval

- **CMP-003.5.4.1** The Head of GRC SHALL assign each complete request an Exception ID and SHALL obtain a risk review from the CISO's delegate in the security function, who SHALL validate the Residual Risk score under RSK-002.
- **CMP-003.5.4.2** The following specialist reviews SHALL be obtained before approval where the affected scope includes:
  - `[PCI]` the CDE: the Head of Security Engineering, confirming the effect on PCI DSS scope and validation (SEC-019);
  - `[HIPAA]` ePHI systems: the HIPAA Security Officer (CMP-008);
  - `[SOX]` Financially Significant Systems: the CFO or delegate, assessing the effect on internal control over financial reporting (CMP-009);
  - `[GDPR]` `[CPRA]` Personal Data: the CPO and the GC (CMP-005 section 9);
  - a contractual obligation: the GC.
- **CMP-003.5.4.3** Exceptions SHALL be approved by the authority matching the validated Residual Risk level, as set for Risk Acceptance in RSK-001. Where the validated Residual Risk level is Critical, the Audit Committee notification required by RSK-001 SHALL also apply.
- **CMP-003.5.4.4** Where a specialist review under CMP-003.5.4.2 is negative, the request SHALL be escalated to the next authority level above that set in CMP-003.5.4.3, and the negative review SHALL be attached to the decision record.
- **CMP-003.5.4.5** The requester, the executive sponsor and the Control Owner of the affected requirement SHALL NOT approve their own request. Where the approving authority is the requester, approval passes to the next authority level.
- **CMP-003.5.4.6** The approver SHALL record a decision of approved, approved with conditions, or rejected, with the reasons, within the decision time in CMP-003.7.3. Conditions SHALL be specific and verifiable.
- **CMP-003.5.4.7** An approved Exception's end date SHALL NOT exceed the maximum duration in CMP-003.7.1, and SHALL NOT extend beyond the expiry of any Risk Acceptance it relies on.
- **CMP-003.5.4.8** Approved Exceptions with a validated Residual Risk of High or Critical SHALL also be recorded as Risks in the Risk Register (TPL-001), cross-referenced by Exception ID.
- **CMP-003.5.4.9** Exceptions for Vulnerabilities listed in the CISA KEV catalog on internet-facing assets (SEC-011) SHALL be approved by at least the CISO, regardless of the validated Residual Risk level.

### 5.5 Compensating Controls

- **CMP-003.5.5.1** Every Exception with a validated Residual Risk of Medium or above SHALL be supported by at least one Compensating Control. An Exception with Low Residual Risk SHOULD be supported by a Compensating Control.
- **CMP-003.5.5.2** Each Compensating Control SHALL:
  1. meet the intent and rigor of the original requirement;
  2. provide a level of defense comparable to the original requirement against the Threat the requirement addresses;
  3. go beyond other requirements of the suite, so that a Control already required elsewhere is not counted as compensating;
  4. be commensurate with the additional Risk created by not meeting the original requirement.
- **CMP-003.5.5.3** Each Compensating Control SHALL have a named Control Owner, a defined operating frequency, and Evidence of operation stored under CMP-004.
- **CMP-003.5.5.4** The Control Owner SHALL provide Evidence that each Compensating Control is implemented before the Exception takes effect, and SHALL provide Evidence of continued operation at the frequency stated in CMP-003.7.8.
- **CMP-003.5.5.5** Failure of a Compensating Control SHALL be reported by its Control Owner to the Head of GRC within 1 business day of detection. The Head of GRC SHALL suspend the Exception, and the deviation SHALL be remediated or a revised Exception approved within 10 business days. A failure that results in a Security Event SHALL also be handled under RES-001.
- **CMP-003.5.5.6** `[PCI]` Where a PCI DSS requirement is met by a compensating control, the Head of Security Engineering SHALL also document a Compensating Controls Worksheet (PCI DSS Appendix C) and obtain validation by the QSA during each annual assessment (CMP-001). The internal Exception record SHALL reference the worksheet.

### 5.6 Duration, renewal and expiry

- **CMP-003.5.6.1** Exceptions SHALL be time-limited to the maximum durations in CMP-003.7.1. No Exception SHALL be open-ended or tied to an unspecified event.
- **CMP-003.5.6.2** The Head of GRC SHALL notify the requester and the Control Owner 30 days and 10 business days before an Exception's end date.
- **CMP-003.5.6.3** A renewal request SHALL be submitted at least 15 business days before the end date, using TPL-003, and SHALL include the progress achieved against the remediation plan and the reason remediation was not completed. A renewal is assessed and approved as a new request under section 5.4.
- **CMP-003.5.6.4** Renewals are limited as set in CMP-003.7.2. After the final permitted renewal, the deviation SHALL be either remediated by the end date or submitted for Risk Acceptance under RSK-001 using TPL-002.
- **CMP-003.5.6.5** On the end date of an Exception that has not been renewed, the Exception expires. The Control Owner SHALL bring the affected scope into compliance by the end date. Continued deviation after expiry is non-compliance under CMP-007, and the Head of GRC SHALL report it to the ISSC at its next meeting.
- **CMP-003.5.6.6** An Exception SHALL be closed early when the requirement is met, when the affected Information Asset is decommissioned, or when the requirement is changed under GOV-002 so the deviation is no longer a deviation. The Control Owner SHALL provide closure Evidence within 10 business days of the triggering event.
- **CMP-003.5.6.7** The approving authority, the CISO or the ISSC MAY revoke an Exception at any time where Residual Risk increases, conditions are breached or a Compensating Control fails. Revocation takes effect on the date stated in the revocation notice.

### 5.7 Emergency Exceptions

- **CMP-003.5.7.1** Where a deviation is required to restore service, contain a Security Incident or meet an urgent legal obligation, and the normal process cannot complete in time, the CISO (or, for Sev-1 incidents, the Incident Commander under RES-002 with CISO notification) MAY grant a verbal or written emergency Exception.
- **CMP-003.5.7.2** An emergency Exception SHALL NOT be granted for a requirement listed in CMP-003.5.2.1.
- **CMP-003.5.7.3** An emergency Exception SHALL be recorded in the Exception Register within 1 business day of being granted, SHALL be valid for no more than 10 business days, and SHALL be followed by a complete TPL-003 request within 5 business days. If the full request is not approved before the emergency Exception expires, the deviation SHALL cease.

### 5.8 Exception Register

- **CMP-003.5.8.1** The Head of GRC SHALL maintain a single Exception Register for the Organization, in the GRC tool, as the authoritative record of all Exception requests and decisions.
- **CMP-003.5.8.2** The register SHALL record, for each request: Exception ID; status (submitted, incomplete, under review, approved, approved with conditions, rejected, suspended, revoked, expired, closed); requester and sponsor; document and requirement IDs; affected Information Assets and regulated scope flags; Inherent and Residual Risk scores and levels; Compensating Controls and their owners; approving authority and decision date; start and end dates; renewal count; linked Risk Register entry and Risk Acceptance (if any); remediation milestones and status; and the location of supporting Evidence.
- **CMP-003.5.8.3** The register SHALL be classified Confidential under SEC-002. Write access SHALL be limited to the Head of GRC and named GRC personnel, and every change SHALL be logged with user and timestamp.
- **CMP-003.5.8.4** Register entries and supporting records SHALL be retained under the retention schedule in CMP-004.
- **CMP-003.5.8.5** The register SHALL be made available to Internal Audit (CMP-002), and to External Auditors and QSAs on request through the process in CMP-002.

### 5.9 Monitoring and reporting

- **CMP-003.5.9.1** The Head of GRC SHALL review the full register monthly to identify Exceptions approaching expiry, overdue remediation milestones, missing Compensating Control Evidence and expired Exceptions still in effect.
- **CMP-003.5.9.2** The Head of GRC SHALL report to the ISSC quarterly: the number of open Exceptions by Residual Risk level and by document; new, renewed, expired, revoked and closed Exceptions; Exceptions at their final renewal; and requirements that triggered CMP-003.5.1.5.
- **CMP-003.5.9.3** Open Exceptions with Critical Residual Risk SHALL be included in the KRI dashboard to the Audit Committee as KRI-04, at the cadence in GOV-003.5.5.1.
- **CMP-003.5.9.4** Each quarter, the Head of GRC SHALL test a sample of at least 10% of open Exceptions (minimum 5, or all if fewer) to confirm that Compensating Controls operate and the deviation remains within its approved scope, and SHALL sample SHOULD-requirement justifications recorded by Document Owners during the same period.
- **CMP-003.5.9.5** Internal Audit SHALL assess the operation of this Policy within the audit plan cycle set in CMP-002.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| Requester (any Workforce Member) | Completes TPL-003; proposes Compensating Controls and a remediation plan; implements the remediation; requests renewal or closure. |
| Executive sponsor | Confirms the business need and accepts accountability for the deviation and its remediation. |
| Head of GRC | Owns this Policy; checks completeness; assigns IDs; rejects non-exceptionable requests; maintains the Exception Register; issues expiry notices; monitors and reports to the ISSC; tests Compensating Controls. |
| CISO | Approves at the level set in RSK-001; grants emergency Exceptions; may revoke any Exception; ensures security risk review of every request. |
| Head of Security Engineering | `[PCI]` Reviews CDE Exceptions; maintains Compensating Controls Worksheets; supports risk scoring. |
| Risk Owner | Approves Low Residual Risk Exceptions at the level set in RSK-001; records related Risks. |
| Control Owner | Operates Compensating Controls; provides Evidence of implementation and operation; reports Compensating Control failure within 1 business day. |
| CPO and GC | Review every Exception affecting Personal Data; GC verifies counterparty consent for contractual deviations and determines legal disclosure. |
| HIPAA Security Officer | `[HIPAA]` Reviews Exceptions affecting ePHI systems. |
| CFO | `[SOX]` Assesses Exceptions affecting Key Controls in Financially Significant Systems. |
| ISSC | Approves High Residual Risk Exceptions; receives quarterly reporting; may revoke any Exception. |
| CEO | Approves Critical Residual Risk Exceptions as set in RSK-001. |
| Audit Committee | Receives notification of Critical Residual Risk Exceptions as set in RSK-001, and the KRI dashboard. |
| Document Owners | Propose changes to requirements that attract repeated Exceptions (CMP-003.5.1.5). |
| Internal Audit Director | Audits the operation of this Policy and the register under CMP-002. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| CMP-003.7.1 | Exception maximum duration | 12 months; 90 days where residual risk is Critical |
| CMP-003.7.2 | Exception renewals | Max 2 consecutive renewals, then remediate or obtain risk acceptance per RSK-001 |
| CMP-003.7.3 | Exception decision time | Within 10 business days of a complete request |
| CMP-003.7.4 | Exception approval authority | Same as risk acceptance authority in RSK-001, by residual risk level |
| CMP-003.7.5 | Completeness check of a submitted request | Within 3 business days of submission |
| CMP-003.7.6 | Rejection of a non-exceptionable request | Within 2 business days of receipt |
| CMP-003.7.7 | Compensating Controls required | At least one for every Exception with Residual Risk Medium or above |
| CMP-003.7.8 | Evidence of Compensating Control operation | Before the Exception takes effect, then at least quarterly (monthly where Residual Risk is High or Critical) |
| CMP-003.7.9 | Reporting a Compensating Control failure | Within 1 business day of detection; remediation or revised Exception within 10 business days |
| CMP-003.7.10 | Expiry notices | 30 days and 10 business days before end date |
| CMP-003.7.11 | Renewal request submission | At least 15 business days before end date |
| CMP-003.7.12 | Emergency Exception | Recorded within 1 business day; valid max 10 business days; full request within 5 business days |
| CMP-003.7.13 | Repeated Exceptions trigger document review | 3 approved Exceptions against the same requirement in 12 months; review started within 30 days |
| CMP-003.7.14 | Register review by Head of GRC | Monthly |
| CMP-003.7.15 | Reporting to ISSC | Quarterly |
| CMP-003.7.16 | Compensating Control sample testing | Quarterly; at least 10% of open Exceptions, minimum 5 |
| CMP-003.7.17 | Closure Evidence after early-closure trigger | Within 10 business days |
| CMP-003.7.18 | Retention of Exception records | Per CMP-004 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Complete requests decided within 10 business days | 100% | Monthly | Head of GRC |
| Open Exceptions past their end date (expired but still in effect) | 0 | Monthly | Head of GRC |
| Open Exceptions with current Compensating Control Evidence | 100% | Monthly | Head of GRC |
| Exceptions approved at an authority below that required by RSK-001 | 0 | Quarterly | Head of GRC |
| Non-exceptionable requests approved | 0 | Quarterly | Head of GRC |
| Open Exceptions by Residual Risk level (trend) | Decreasing quarter on quarter | Quarterly | Head of GRC |
| Exceptions at their 2nd renewal | Reported 100% to ISSC | Quarterly | Head of GRC |
| Emergency Exceptions followed by a full request within 5 business days | 100% | Quarterly | CISO |
| Remediation milestones met on time | ≥ 90% | Quarterly | Head of GRC |
| Deviations found by audit or testing with no Exception on record | 0 | Each audit | Internal Audit Director |

## 9. Exceptions

This Policy defines the Exception process and cannot itself be the subject of an Exception.
No Exception SHALL be granted to any requirement of this Policy, including the approval
authorities, the maximum durations and renewal limits, and the list in CMP-003.5.2.1.
Changes to this Policy are made only under GOV-002.

## 10. Enforcement

Non-compliance is handled under CMP-007.

The following are treated as violations under CMP-007: deviating from a SHALL requirement
without an approved Exception in force; continuing a deviation after an Exception has
expired, been suspended or been revoked; approving one's own Exception or approving above
one's authority; misrepresenting Risk, scope or Compensating Controls in a request; and
falsifying Compensating Control Evidence. Deviations by a Third Party without an approved
Exception are handled under the contractual remedies in CMP-007 and RSK-003.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| CMP-003.5.1 – 5.2 | 5.1, 6.1.3; A.5.1, A.5.31, A.5.36 | GV.PO-01, GV.PO-02, GV.RM-01 | PM-9, PL-1, RA-7 | — | CC1.3, CC5.3 | APO01, APO12 | PCI DSS 3.3.1, 12.1.1; HIPAA §164.306(b), §164.316(a); GDPR Art. 5(2), 24 |
| CMP-003.5.3 – 5.4 | 6.1.2, 6.1.3; A.5.4 | GV.RM-01, GV.RM-06, ID.RA-05 | PM-9, RA-3, RA-7 | — | CC3.2, CC5.2 | APO12 | PCI DSS 12.3.1; HIPAA §164.308(a)(1)(ii)(B) |
| CMP-003.5.5 | 6.1.3; A.5.36 | GV.RM-01, ID.RA-06 | CA-2, PM-9 | — | CC4.1, CC5.1 | APO12, MEA02 | PCI DSS Appendix B, Appendix C |
| CMP-003.5.6 – 5.7 | 6.1.3, 8.3 | GV.RM-01, ID.RA-06 | PM-9, RA-7 | — | CC3.2, CC5.2 | APO12 | — |
| CMP-003.5.8 – 5.9 | 7.5, 9.1, 9.3; A.5.36 | GV.OV-01, GV.OV-03 | PM-4, PM-9, CA-5 | — | CC2.1, CC4.1, CC4.2 | APO12, MEA01, MEA02 | SOX §404 |

## 12. Related documents

ISP-000, GOV-001, GOV-002, GOV-003, GOV-006, RSK-001, RSK-002, RSK-003, RSK-004, CMP-001,
CMP-002, CMP-004, CMP-005, CMP-006, CMP-007, CMP-008, CMP-009, CMP-010, SEC-001, SEC-002,
SEC-011, SEC-019, RES-001, RES-002, RES-003, TPL-001, TPL-002, TPL-003, REF-001

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Head of GRC | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
