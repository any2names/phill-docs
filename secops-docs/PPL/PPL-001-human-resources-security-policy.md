# PPL-001 — Human Resources Security Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | PPL-001 |
| Title | Human Resources Security Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Human Resources Officer (CHRO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-001, GOV-002, GOV-004, CMP-004, CMP-005, CMP-007, SEC-001, SEC-003, SEC-005, RSK-003, PPL-002, TPL-009 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CHRO | Initial release |

## 3. Purpose

This Policy sets the information security requirements that apply across the Workforce Member
lifecycle: screening before and during employment, terms of employment and engagement,
onboarding, role change, leave and Separation. It ensures that individuals are suitable for the
access they receive, understand and accept their security obligations, have access that
matches their current role, and return Organization assets and lose access when they leave. It
links breaches of security obligations to the disciplinary process in CMP-007.

## 4. Scope

- **People:** every Workforce Member (employees, contractors, temporary workers, interns and volunteers), candidates for those positions, and the managers, HR personnel and sponsors who act on their behalf.
- **Systems:** the human resources information system (HRIS) and every Information System that consumes joiner, mover and leaver events from it.
- **Data:** Personal Data of candidates and Workforce Members processed for screening, onboarding and Separation.
- **Locations:** all Organization sites and regions in the scope of ISP-000; screening is performed in accordance with the law of the location where the individual works.
- **Third parties:** staffing agencies, contractor firms and screening providers. Third Party personnel who are not Workforce Members are covered by RSK-003, which SHALL require the equivalent of sections 5.2 and 5.6.

## 5. Policy statements

### 5.1 Position risk designation

- **PPL-001.5.1.1** The CHRO, with the CISO, SHALL assign every position one of two Screening Levels before it is advertised or filled:
  - **Standard:** every position not designated Enhanced.
  - **Enhanced:** positions that hold or approve Privileged Accounts; `[PCI]` positions with access to the CDE; `[HIPAA]` positions with access to ePHI beyond the Minimum Necessary for scheduling or administration; positions with access to Restricted data in bulk; positions in the security, GRC, IT operations and internal audit functions; `[SOX]` positions with authority to post, approve or change data in Financially Significant Systems or to initiate or approve payments; and every role named in GOV-001 sections 5.4.2–5.4.5.
- **PPL-001.5.1.2** The position's Screening Level SHALL be recorded in the HRIS and SHALL be reviewed whenever the position's access or responsibilities change.

### 5.2 Screening

- **PPL-001.5.2.1** Pre-employment screening SHALL be completed before the individual is given access to Confidential or Restricted data.
- **PPL-001.5.2.2** Identity verification and right-to-work verification SHALL be completed before any account is provisioned for the individual.
- **PPL-001.5.2.3** Screening SHALL include, where permitted by the law of the work location, the following checks:

| Check | Standard | Enhanced |
|---|---|---|
| Identity verification against government-issued photo identification | ✓ | ✓ |
| Right to work | ✓ | ✓ |
| Employment history verification (most recent 5 years) | ✓ | ✓ |
| Verification of claimed professional qualifications and certifications | ✓ (where required for the role) | ✓ |
| Sanctions and watch-list screening | ✓ | ✓ |
| Criminal record check | — | ✓ |
| References (at least 2, including 1 professional) | — | ✓ |
| `[SOX]` Credit or financial-integrity check for positions with authority over funds or Financially Significant Systems | — | ✓ |

- **PPL-001.5.2.4** Screening SHALL be performed in accordance with applicable law, including consumer reporting law (for example the US Fair Credit Reporting Act), local limits on criminal history inquiries, and data protection law. The GC SHALL maintain, and review every 12 months, a jurisdiction matrix recording which checks are permitted in each work location.
- **PPL-001.5.2.5** `[GDPR]` Criminal record checks on individuals in the EU/EEA SHALL be performed only where authorized by Union or Member State law (GDPR Art. 10). The DPO SHALL be consulted on the screening process and a DPIA SHALL be completed under TPL-005 where it involves criminal record data or large-scale processing.
- **PPL-001.5.2.6** Candidates SHALL be informed of the checks to be performed, and their consent or other lawful basis SHALL be recorded before screening begins. Screening Personal Data SHALL be processed in accordance with CMP-005.
- **PPL-001.5.2.7** Adverse or incomplete screening results SHALL be adjudicated by the CHRO, with the GC, against criteria approved by the CHRO and reviewed every 12 months. For Enhanced positions, the CISO SHALL be consulted. The decision and reasons SHALL be recorded, and any applicable pre-adverse-action notice requirements SHALL be met.
- **PPL-001.5.2.8** Where screening cannot be completed before the start date, the individual MAY start only with access limited to Public and Internal information, approved in writing by the CHRO, and the screening SHALL be completed within 30 days of the start date or the individual's access SHALL be suspended.
- **PPL-001.5.2.9** Rescreening SHALL be performed every 3 years for Workforce Members in positions that hold Privileged Accounts and `[PCI]` positions with access to the CDE, where lawful.
- **PPL-001.5.2.10** A Workforce Member who moves into an Enhanced position SHALL complete the Enhanced checks not previously performed before receiving the access that made the position Enhanced.
- **PPL-001.5.2.11** Workforce Members SHALL disclose to the CHRO, within 5 business days, any criminal charge or conviction, or regulatory sanction, arising during employment that is relevant to an Enhanced position, where such disclosure may lawfully be required.
- **PPL-001.5.2.12** Contracts with staffing agencies and contractor firms SHALL require screening equivalent to the Screening Level of the position, completed before access, with Evidence of completion available to the Organization on request (RSK-003).

### 5.3 Terms of employment and engagement

- **PPL-001.5.3.1** Every employment contract, contractor agreement and engagement letter SHALL include, or incorporate by reference:
  1. the confidentiality obligations in GOV-004 section 5.11, including their continuation after Separation;
  2. assignment to the Organization of intellectual property created in the course of the work, as permitted by local law;
  3. the obligation to comply with GOV-004 and every suite document that applies to the role;
  4. the obligation to return all Organization assets at Separation;
  5. notice that breaches of security obligations are handled under CMP-007 and MAY lead to termination and legal action; and
  6. notice of monitoring as set out in GOV-004 section 5.13.
- **PPL-001.5.3.2** The GC SHALL approve the standard clauses implementing PPL-001.5.3.1 and SHALL review them every 12 months.
- **PPL-001.5.3.3** Signed terms SHALL be obtained before any account is provisioned for the individual.
- **PPL-001.5.3.4** Job descriptions for positions with security accountabilities SHALL state them, as required by GOV-001.
- **PPL-001.5.3.5** `[HIPAA]` Workforce Members with access to PHI SHALL be informed in their terms of the sanctions for failing to comply with HIPAA policies, applied under CMP-007.

### 5.4 Onboarding

- **PPL-001.5.4.1** The HRIS SHALL be the authoritative source of Workforce Member identity, status, position, manager, work location and start and end dates. Account provisioning SHALL be triggered only by an HRIS record, as required by SEC-003.
- **PPL-001.5.4.2** HR SHALL create the HRIS record at least 2 business days before the start date, except where the CHRO approves a shorter period in writing.
- **PPL-001.5.4.3** Before any account is enabled, HR SHALL confirm in the HRIS that: identity and right to work are verified (PPL-001.5.2.2); terms are signed (PPL-001.5.3.3); and the Workforce Member has attested under GOV-002 using TPL-009 or its electronic equivalent.
- **PPL-001.5.4.4** Before access to Confidential or Restricted data is enabled, HR SHALL confirm in the HRIS that screening at the position's level is complete (PPL-001.5.2.1).
- **PPL-001.5.4.5** HR SHALL enroll every new Workforce Member in the training required by PPL-002 on the start date.
- **PPL-001.5.4.6** Every Endpoint, token, badge and other asset issued to a Workforce Member SHALL be recorded against that individual in the Asset Inventory (SEC-001) at issue.
- **PPL-001.5.4.7** Every contractor, temporary worker, intern and volunteer SHALL have a named Organization sponsor and an end date recorded in the HRIS. The end date SHALL be no more than 12 months after the start or the last extension.

### 5.5 Role change

- **PPL-001.5.5.1** HR SHALL record every change of position, manager, department or work location in the HRIS no later than its effective date.
- **PPL-001.5.5.2** The HRIS change SHALL generate a notification to the identity and access management function within 1 business day of being recorded, so that access is changed within the timeframe in SEC-003.
- **PPL-001.5.5.3** The new manager SHALL confirm the access required for the new role, and the previous manager SHALL confirm the access no longer required, before the SEC-003 timeframe ends.
- **PPL-001.5.5.4** Where the new position has a higher Screening Level, PPL-001.5.2.10 applies. Where it requires additional role-based training under PPL-002, the CISO SHALL assign it within 5 business days of the change.
- **PPL-001.5.5.5** Where the new position requires a different Attestation Set under GOV-002, the Workforce Member SHALL attest to the additional documents before receiving the access they govern.

### 5.6 Leave of absence

- **PPL-001.5.6.1** HR SHALL record in the HRIS any leave of absence expected to exceed 30 days, at the latest on the first day of leave, and the HRIS SHALL notify the identity and access management function within 1 business day. Access treatment during leave is set in SEC-003.5.8.2.
- **PPL-001.5.6.2** On return, HR SHALL record the return in the HRIS no later than the return date, and the Workforce Member SHALL complete any training or attestation that fell due during the leave within 30 days of return.

### 5.7 Separation

- **PPL-001.5.7.1** HR SHALL record every Separation in the HRIS with its effective date and time. For voluntary Separations, the record SHALL be made within 1 business day of the resignation being received and in any case before the Separation time.
- **PPL-001.5.7.2** For involuntary Separations, HR SHALL notify the CISO, or the CISO's delegate in the identity and access management function, before the individual is told, so that access is revoked at or before notification as required by SEC-003.
- **PPL-001.5.7.3** Access SHALL be revoked within the timeframe in SEC-003. HR and the manager SHALL NOT approve any extension of access beyond the Separation time except as permitted by SEC-003.
- **PPL-001.5.7.4** The separating Workforce Member SHALL return all Organization assets, including Endpoints, Mobile Devices, Media, tokens, badges, keys and paper records, within 5 business days of the Separation date. The manager SHALL confirm return against the Asset Inventory record (SEC-001).
- **PPL-001.5.7.5** Where an asset is not returned within 5 business days, the manager SHALL report it under RES-001 as a lost asset, and the CIO SHALL initiate remote lock or wipe where the asset supports it (SEC-008).
- **PPL-001.5.7.6** Before the Separation date, or at the exit meeting for involuntary Separations, HR SHALL remind the Workforce Member in writing of their continuing confidentiality and intellectual property obligations (GOV-004 section 5.11) and SHALL request a signed acknowledgement using TPL-009. Refusal to sign SHALL be recorded and does not remove the obligations.
- **PPL-001.5.7.7** The manager SHALL arrange the transfer of business information held by the separating Workforce Member to a successor or approved repository before the Separation date. Treatment of the former Workforce Member's mailbox and files after Separation SHALL follow CMP-004.5.2.9.
- **PPL-001.5.7.8** Where the separating Workforce Member held a Privileged Account or knew a shared Secret, the System Owner SHALL rotate every shared Secret known to them within the timeframe set in SEC-005.5.12.3.
- **PPL-001.5.7.9** Where HR or the manager has reason to believe that a separating Workforce Member intends to remove Organization information or harm Information Assets, they SHALL notify the CISO before the Separation is communicated; the CISO MAY direct enhanced monitoring authorized under GOV-004 section 5.13.
- **PPL-001.5.7.10** The HRIS SHALL record the end date of every contractor, temporary worker, intern and volunteer. Where no extension is recorded by the end date, the engagement SHALL be processed as a Separation.

### 5.8 Disciplinary linkage

- **PPL-001.5.8.1** Breaches of suite documents by Workforce Members SHALL be handled under CMP-007. HR SHALL apply CMP-007 consistently regardless of seniority.
- **PPL-001.5.8.2** HR SHALL record every disciplinary action arising from a security or privacy breach in the HRIS with a reference to the related Security Incident or investigation record, and SHALL inform the CISO of the outcome within 5 business days of the decision.
- **PPL-001.5.8.3** `[HIPAA]` Sanctions applied for violations of HIPAA policies SHALL be documented under CMP-007 and retained under CMP-004.
- **PPL-001.5.8.4** Where a Workforce Member is suspended pending investigation, HR SHALL notify the identity and access management function at the start of the suspension, so that access is disabled under SEC-003.5.8.5.

### 5.9 Records

- **PPL-001.5.9.1** Screening results, signed terms, acknowledgements and Separation records SHALL be classified Restricted (screening results) or Confidential (all others) under SEC-002, accessible only to HR and those with a documented need, and retained under CMP-004.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CHRO | Owns this Policy; designates position Screening Levels with the CISO; adjudicates adverse screening results; ensures HRIS events are recorded on time; applies CMP-007 |
| CISO | Co-designates Screening Levels; consulted on Enhanced adjudications; assigns role-based training on role change; receives involuntary Separation notices |
| GC | Maintains the screening jurisdiction matrix; approves standard contract clauses; co-adjudicates adverse results |
| DPO / CPO | Advise on lawful processing of screening data; review screening DPIAs |
| CIO | Initiates remote lock or wipe of unreturned assets; records assets in the Asset Inventory |
| System Owners | Rotate shared Secrets known to separating privileged users |
| Managers and sponsors | Confirm access on role change; confirm asset return; transfer business information; sponsor non-employee Workforce Members |
| Head of Procurement | Ensures staffing agency and contractor firm contracts include screening requirements (RSK-003) |
| Workforce Members | Complete screening, sign terms, attest, return assets and disclose relevant charges or sanctions |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| PPL-001.7.1 | Pre-employment screening | Completed before access to Confidential or Restricted data; rescreening every 3 years for privileged and CDE roles, where lawful |
| PPL-001.7.2 | Asset return on Separation | Within 5 business days |
| PPL-001.7.3 | Identity, right to work and signed terms | Before any account is provisioned |
| PPL-001.7.4 | HRIS record before start date | At least 2 business days |
| PPL-001.7.5 | Screening completion where started late | Within 30 days of start, else access suspended |
| PPL-001.7.6 | Employment history verified | Most recent 5 years |
| PPL-001.7.7 | HRIS role-change notification to identity and access management | Within 1 business day of being recorded |
| PPL-001.7.8 | Voluntary Separation recorded in HRIS | Within 1 business day of resignation, and before the Separation time |
| PPL-001.7.9 | Involuntary Separation notice to CISO or delegate | Before the individual is told |
| PPL-001.7.10 | Maximum non-employee engagement term without extension | 12 months |
| PPL-001.7.11 | Leave of absence notification | Leave > 30 days, recorded by first day; notification within 1 business day |
| PPL-001.7.12 | Disciplinary outcome reported to CISO | Within 5 business days of decision |
| PPL-001.7.13 | Disclosure of relevant charges or sanctions by Enhanced Workforce Members | Within 5 business days, where lawful |
| PPL-001.7.14 | Access revocation and access change timeframes | As set in SEC-003 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| New hires with screening complete before access to Confidential or Restricted data | 100% | Monthly | CHRO |
| Accounts provisioned before signed terms and attestation | 0 | Monthly | CHRO |
| Privileged and CDE Workforce Members with screening within the last 3 years | 100% (where lawful) | Quarterly | CHRO |
| Separations recorded in HRIS before the Separation time | 100% | Monthly | CHRO |
| Assets returned within 5 business days of Separation | ≥ 98% | Monthly | CIO |
| Separations with access revoked within the SEC-003 timeframe (GOV-003 KPI-05) | Per GOV-003 | Monthly | CISO |
| Non-employee Workforce Members past end date without extension or Separation | 0 | Monthly | CHRO |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003. No Exception MAY be
granted to PPL-001.5.2.2 (identity and right to work before access), PPL-001.5.7.2 (prior
notice of involuntary Separation) or to screening required by law or by PCI DSS 12.7.1 `[PCI]`.
Where local law prohibits a check in PPL-001.5.2.3, the omission is recorded in the GC's
jurisdiction matrix and is not an Exception.

## 10. Enforcement

Non-compliance is handled under CMP-007. Misrepresentation by a candidate or Workforce Member
during screening SHALL be handled under CMP-007 and MAY result in withdrawal of an offer or
termination.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| PPL-001.5.1 – 5.2 | A.6.1 | GV.RR-04 | PS-2, PS-3 | — | CC1.4 | APO07.01 | `[PCI]` 12.7.1; `[HIPAA]` §164.308(a)(3)(ii)(B); `[GDPR]` Art. 6, 9, 10, 88 |
| PPL-001.5.3 | A.6.2, A.6.6 | GV.RR-04 | PS-6, PL-4 | — | CC1.1, CC1.4 | APO07.06 | `[HIPAA]` §164.308(a)(1)(ii)(C) |
| PPL-001.5.4 | A.5.16, A.6.2 | PR.AA-01 | PS-3, AC-2 | 5.1, 6.1 | CC6.2 | APO07, DSS05.04 | `[HIPAA]` §164.308(a)(3)(ii)(A) |
| PPL-001.5.5 – 5.6 | A.5.18, A.6.5 | PR.AA-05 | PS-5, AC-2 | 6.1, 6.2 | CC6.2, CC6.3 | APO07 | `[HIPAA]` §164.308(a)(4) |
| PPL-001.5.7 | A.5.11, A.6.5 | PR.AA-05 | PS-4, PS-7 | 6.2 | CC6.2, CC6.5 | APO07.06, DSS05.04 | `[HIPAA]` §164.308(a)(3)(ii)(C); `[PCI]` 8.2.5 |
| PPL-001.5.8 | A.6.4 | GV.RR-04 | PS-8 | — | CC1.5 | APO07 | `[HIPAA]` §164.308(a)(1)(ii)(C) |
| PPL-001.5.9 | A.5.33, A.5.34 | PR.DS-01 | PS-1 | 3.3 | C1.1 | APO07 | `[GDPR]` Art. 5(1)(e), 32 |

## 12. Related documents

GOV-001, GOV-002, GOV-004, RSK-003, CMP-003, CMP-004, CMP-005, CMP-007, SEC-001, SEC-002,
SEC-003, SEC-005, SEC-008, RES-001, PPL-002, TPL-005, TPL-009

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CHRO | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
