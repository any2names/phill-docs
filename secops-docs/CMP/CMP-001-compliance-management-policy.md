# CMP-001 — Compliance Management Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | CMP-001 |
| Title | Compliance Management Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Head of GRC |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months, and on the event-triggered reviews defined in GOV-002 |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-001, GOV-002, GOV-003, GOV-006, RSK-001, RSK-002, RSK-003, CMP-002, CMP-003, CMP-004, CMP-005, CMP-008, CMP-009, CMP-010, SEC-011, SEC-019, RES-003, REF-001, REF-002, REF-003 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Head of GRC | Initial release |

## 3. Purpose

This Policy establishes how the Organization identifies, records, assesses, monitors and
demonstrates compliance with the legal, regulatory, contractual and voluntary information
security and privacy obligations that apply to it. It sets the requirements for the
Obligations Register, regulatory change management, the Compliance Calendar, and the
management of external certifications, attestations and regulator-mandated assessments,
including the SOC 2 Type II examination, `[PCI]` PCI DSS validation and the `[HIPAA]`
Security Rule risk analysis.

## 4. Scope

- **People:** all Workforce Members who own, implement or evidence an obligation recorded in the Obligations Register, and all roles named in section 6.
- **Systems:** all Information Systems, Cloud Services and Information Assets within the scope of the Information Security Program defined in ISP-000, including the CDE `[PCI]`, systems holding ePHI `[HIPAA]` and Financially Significant Systems `[SOX]`.
- **Data:** all Personal Data, PHI, CHD and financial reporting data subject to a recorded obligation, and all Evidence produced to demonstrate compliance.
- **Locations:** all jurisdictions in which the Organization operates, is established, offers goods or services, or processes Personal Data, as recorded under CMP-001.5.2. [DECISION REQUIRED: Regions in scope (SUITE-REGISTER E#7). Recommended default: United States and EU/EEA]
- **Third Parties:** obligations that flow down to Third Parties by contract, and obligations the Organization accepts in contracts with customers, partners and Third Parties.

Out of scope: tax, employment, competition and other legal obligations that have no information security or privacy content. These are managed by the GC under the Organization's legal compliance program.

## 5. Policy statements

### 5.1 Compliance program governance

- **CMP-001.5.1.1** The Head of GRC SHALL operate the compliance management program defined in this Policy and SHALL be accountable for the completeness and currency of the Obligations Register and the Compliance Calendar.
- **CMP-001.5.1.2** The GC SHALL be accountable for the legal interpretation of each statutory and regulatory obligation and SHALL approve every applicability determination recorded under CMP-001.5.3.
- **CMP-001.5.1.3** The CPO SHALL be accountable for privacy obligations (including those tagged `[GDPR]` and `[CPRA]`); the HIPAA Security Officer and HIPAA Privacy Officer SHALL be accountable for obligations tagged `[HIPAA]`; the CFO SHALL be accountable for obligations tagged `[SOX]`; the CISO SHALL be accountable for obligations tagged `[PCI]` and for the SOC 2 Type II examination.
- **CMP-001.5.1.4** Each obligation SHALL have exactly one named obligation owner at the level of functional lead or above, recorded in the Obligations Register.
- **CMP-001.5.1.5** The Head of GRC SHALL report the compliance status of the Organization to the ISSC at each quarterly ISSC meeting, and to the Audit Committee and Board of Directors at the cadence set in GOV-003.5.5.1, with the content in GOV-003.5.6.2 and GOV-003.5.6.3.
- **CMP-001.5.1.6** Compliance requirements SHALL be implemented through suite documents. Where an obligation is not yet addressed by a suite document requirement, the Head of GRC SHALL record the gap in REF-003 and assign a remediation owner and target date.

### 5.2 Obligations Register

- **CMP-001.5.2.1** The Head of GRC SHALL maintain a single Obligations Register covering all legal, regulatory, contractual and voluntary information security and privacy obligations of the Organization.
- **CMP-001.5.2.2** The Obligations Register SHALL contain, for each obligation, the fields listed in CMP-001.5.2.3. An entry missing any mandatory field SHALL be recorded with status "Not assessed".
- **CMP-001.5.2.3** Mandatory fields of each Obligations Register entry:

  | # | Field | Content |
  |---|---|---|
  | 1 | Obligation ID | Unique identifier, never reused (format `OBL-nnnn`) |
  | 2 | Source type | Statute · Regulation · Regulator guidance or order · Industry standard (e.g. PCI DSS) · Contract · Certification or attestation commitment · Internal commitment |
  | 3 | Source and citation | Instrument name, version and article, section or requirement number |
  | 4 | Jurisdiction | Country, state or region; "Global" for non-territorial sources |
  | 5 | Regulation tag | `[PCI]`, `[HIPAA]`, `[SOX]`, `[GDPR]`, `[CPRA]`, other, or none |
  | 6 | Obligation summary | Plain-language statement of what the Organization must do or not do |
  | 7 | Applicability determination | Applicable · Not applicable · Partially applicable, with rationale and GC approval date |
  | 8 | Effective date | Date the obligation takes or took effect |
  | 9 | Obligation owner | Role and named individual |
  | 10 | Implementing requirements | Suite document requirement IDs (e.g. `SEC-003.5.2.1`) that implement the obligation |
  | 11 | Controls | Control IDs mapped in REF-001 |
  | 12 | Evidence | Evidence types and repository location, managed under CMP-004 |
  | 13 | Compliance status | Compliant · Partially compliant · Non-compliant · Not assessed |
  | 14 | Last assessed date / next assessment date | Dates of the last and next status assessment under CMP-001.5.7 |
  | 15 | Related risks | Risk Register entry IDs (TPL-001) |
  | 16 | Consequence of non-compliance | Penalty range, contractual remedy or certification impact |
  | 17 | Related Exceptions / Risk Acceptances | CMP-003 Exception IDs and RSK-001 Risk Acceptance IDs |
  | 18 | Change history | Date, change description, author for each modification |

- **CMP-001.5.2.4** The Obligations Register SHALL be reviewed in full by the Head of GRC, with each obligation owner, on the cadence in CMP-001.7.1. Each review SHALL be recorded with date, participants, entries changed and open actions.
- **CMP-001.5.2.5** A new or changed obligation SHALL be assessed and entered in the Obligations Register within the time in CMP-001.7.1, measured from the date the obligation is published or, for contractual obligations, the date the contract is executed.
- **CMP-001.5.2.6** The Head of Procurement and the GC SHALL provide the Head of GRC with the information security and privacy commitments of every executed customer and Third-Party contract that departs from the Organization's standard contract terms, within 10 business days of execution.
- **CMP-001.5.2.7** The Obligations Register SHALL be classified Confidential under SEC-002 and SHALL be retained, with prior versions, under CMP-004.
- **CMP-001.5.2.8** The Obligations Register SHALL be the authoritative record for whether a regulation-tagged clause in any suite document applies to the Organization (GOV-006.5.2.2).

### 5.3 Applicability determination

- **CMP-001.5.3.1** For each obligation, the obligation owner SHALL propose an applicability determination with written rationale, and the GC SHALL approve or reject it within 10 business days of submission.
- **CMP-001.5.3.2** The Head of GRC SHALL record the applicability of each conditional module listed in the README "Conditional modules" table (`[PCI]`, `[HIPAA]`, `[SOX]`, `[GDPR]`, `[CPRA]`). Where a module is determined not applicable, the Head of GRC SHALL initiate removal of the tagged documents and clauses through GOV-002.
- **CMP-001.5.3.3** `[HIPAA]` The GC SHALL record whether the Organization acts as a Covered Entity, a Business Associate, or both. [DECISION REQUIRED: HIPAA status (SUITE-REGISTER E#3). Recommended default: Business Associate]
- **CMP-001.5.3.4** `[PCI]` The CISO SHALL record the Organization's PCI DSS entity type (merchant, service provider, or both), merchant or service provider level, and validation method as required by the acquirer or payment brands.
- **CMP-001.5.3.5** `[GDPR]` The CPO SHALL record, for each processing context, whether the Organization acts as Controller, Processor or both, and whether GDPR Art. 3(2) territorial scope or Art. 27 representative requirements apply.
- **CMP-001.5.3.6** `[CPRA]` The CPO SHALL record whether the Organization meets the "business" thresholds of Cal. Civ. Code §1798.140(d), and whether it meets the thresholds that trigger cybersecurity audit and risk assessment obligations under regulations adopted pursuant to Cal. Civ. Code §1798.185.
- **CMP-001.5.3.7** Applicability determinations SHALL be re-confirmed at each annual full review of the Obligations Register and within the time in CMP-001.7.1 after any material organizational change (new market, acquisition, new product handling a new regulated data type).

### 5.4 Regulatory change management

- **CMP-001.5.4.1** The Head of GRC SHALL maintain a list of regulatory change sources for every jurisdiction and regulation recorded as applicable. Sources SHALL include, as applicable: regulator publications (e.g. HHS Office for Civil Rights, the SEC, the California Privacy Protection Agency, EU supervisory authorities and the European Data Protection Board), the PCI Security Standards Council, standards bodies (e.g. ISO, NIST, AICPA), outside counsel alerts, and industry associations.
- **CMP-001.5.4.2** The Head of GRC SHALL scan the sources in CMP-001.5.4.1 at least monthly and SHALL record each item identified in a regulatory change log with date identified, source, summary and initial relevance (Relevant · Not relevant · Monitor).
- **CMP-001.5.4.3** For each item marked Relevant, the Head of GRC SHALL, with the obligation owner and GC, complete a documented impact assessment within the time in CMP-001.7.1 that records: affected obligations, affected suite documents and requirement IDs, affected Controls and systems, implementation actions, owners, cost estimate, and the date by which compliance is required.
- **CMP-001.5.4.4** The implementation plan for a regulatory change SHALL set a completion date no later than the effective date of the change. Where that date cannot be met, the obligation owner SHALL record a Risk in the Risk Register under RSK-001 and, where a suite requirement is affected, request an Exception under CMP-003.
- **CMP-001.5.4.5** Changes to suite documents arising from a regulatory change SHALL be made through the event-triggered review in GOV-002.
- **CMP-001.5.4.6** Items marked Monitor (e.g. proposed rules, consultations, draft standards) SHALL be re-evaluated at each quarterly Obligations Register review until finalized or withdrawn.
- **CMP-001.5.4.7** The Head of GRC SHALL report open regulatory changes, their implementation status and any change whose effective date is within 90 days to the ISSC at each quarterly meeting.

### 5.5 Compliance Calendar

- **CMP-001.5.5.1** The Head of GRC SHALL maintain a Compliance Calendar listing every recurring and one-time compliance activity with a due date arising from the Obligations Register or a suite document.
- **CMP-001.5.5.2** Each Compliance Calendar entry SHALL record: activity, source obligation ID or suite requirement ID, owner, due date, recurrence, reminder dates, evidence required, and completion status with completion date.
- **CMP-001.5.5.3** The Compliance Calendar SHALL include, as a minimum and where the related module applies:
  - SOC 2 Type II examination milestones (readiness, period start and end, fieldwork, report issuance, Bridge Letter issuance);
  - suite document reviews under GOV-002 and policy attestation campaigns;
  - Access Reviews (SEC-003, SEC-005), vulnerability scans and Penetration Tests (SEC-011), restore tests (SEC-018), BC/DR exercises (RES-004) and IR plan tests (RES-002);
  - enterprise risk assessment (RSK-002), BIA refresh (RSK-004) and vendor reassessments (RSK-003);
  - annual and role-based training campaigns (PPL-002);
  - `[PCI]` annual ROC or SAQ and Attestation of Compliance, quarterly ASV scans, CDE scope confirmation (SEC-019) and, for service providers, the quarterly personnel reviews in CMP-001.5.6.16;
  - `[HIPAA]` the annual risk analysis and technical and non-technical evaluation (CMP-001.5.6.18 – 5.6.20);
  - `[SOX]` quarterly ITGC sub-certifications and the annual management assessment under CMP-009;
  - `[GDPR]` `[CPRA]` ROPA review (TPL-010), Privacy Notice review (CMP-005) and DSR metrics publication where required (CMP-010);
  - `[CPRA]` annual cybersecurity audit and risk assessment submissions where applicable under CMP-001.5.3.6;
  - Internal Audit engagements under the annual audit plan (CMP-002).
- **CMP-001.5.5.4** The Compliance Calendar system SHALL send reminders to the owner 90, 30 and 7 days before each due date, and to the owner and the Head of GRC on the due date if the activity is not marked complete.
- **CMP-001.5.5.5** An activity not completed by its due date SHALL be escalated by the Head of GRC to the owner's executive within 5 business days, and SHALL be reported to the ISSC at its next meeting.
- **CMP-001.5.5.6** An activity SHALL be marked complete only when its required Evidence is stored in the Evidence repository under CMP-004.
- **CMP-001.5.5.7** The Head of GRC SHALL publish the Compliance Calendar for the next 12 months to all owners by the start of each fiscal year and SHALL review it monthly for new, changed or overdue entries.

### 5.6 Certification, attestation and assessment management

#### General

- **CMP-001.5.6.1** The Head of GRC SHALL maintain a register of every external certification, attestation report, assessment and validation the Organization holds or has committed to (by contract, regulation or published statement), recording for each: type, scope, issuing firm or assessor, period covered, issue date, expiry or next due date, and owner.
- **CMP-001.5.6.2** No Workforce Member SHALL represent to a customer, prospect, regulator or the public that the Organization holds a certification, attestation or compliance status that is not current in the register in CMP-001.5.6.1. Marketing and sales statements on compliance status SHALL be approved by the Head of GRC and the GC before publication.
- **CMP-001.5.6.3** The scope of each external assessment SHALL be documented and approved by the accountable executive (CMP-001.5.1.3) before fieldwork begins, and SHALL be consistent with REF-001.
- **CMP-001.5.6.4** Auditors, QSAs and assessors SHALL be engaged under a written engagement letter approved by the accountable executive. External Auditors' independence and coordination with Internal Audit are governed by CMP-002.
- **CMP-001.5.6.5** Every exception, finding, deviation or qualified opinion in an external report SHALL be entered as an issue, classified and remediated under CMP-002, with a written management response recorded within 30 days of report issuance.
- **CMP-001.5.6.6** External reports SHALL be classified Confidential under SEC-002 and SHALL be released to external parties only under a non-disclosure agreement or the issuing firm's report-use restrictions, with each release logged by the Head of GRC.

#### SOC 2 Type II examination

- **CMP-001.5.6.7** The Organization SHALL obtain a SOC 2 Type II examination report covering the Trust Services Criteria selected in ISP-000. [DECISION REQUIRED: SOC 2 Trust Services Criteria in scope (SUITE-REGISTER E#2). Recommended default: Security, Availability and Confidentiality]
- **CMP-001.5.6.8** The examination period SHALL be 12 months, and successive periods SHALL be contiguous with no gap. [DECISION REQUIRED: Length of the first examination period. Recommended default: 6 months, followed by contiguous 12-month periods]
- **CMP-001.5.6.9** Before the first examination period begins, the Head of GRC SHALL complete a readiness assessment against the selected criteria. Every gap rated High or Critical under RSK-002 SHALL be remediated, or covered by an approved Exception (CMP-003), before the period start date.
- **CMP-001.5.6.10** The Head of GRC SHALL prepare the system description, and the CISO and CEO SHALL sign management's assertion, before report issuance.
- **CMP-001.5.6.11** The Head of GRC SHALL maintain the list of complementary user entity controls (CUECs) and complementary subservice organization controls (CSOCs) stated in the report. CUECs SHALL be communicated to customers with each report release. CSOCs SHALL be monitored through the Third-Party assurance process in RSK-003.5.5.5.
- **CMP-001.5.6.12** Where a customer requests assurance for the period between the end of the most recent examination period and the date of request, the Head of GRC MAY issue a Bridge Letter signed by the CISO, covering no more than 3 months after the period end.
- **CMP-001.5.6.13** Control testing in preparation for, and between, examination periods SHALL be performed under CMP-002.

#### `[PCI]` PCI DSS validation

- **CMP-001.5.6.14** `[PCI]` The Organization SHALL validate PCI DSS v4.0.1 compliance every 12 months by the method required for its entity type and level. [DECISION REQUIRED: PCI DSS validation level (SUITE-REGISTER E#4). Recommended default: Report on Compliance (ROC) by a QSA; SAQ for lower-volume merchants]
- **CMP-001.5.6.15** `[PCI]` The CISO SHALL be accountable for the protection of CHD and the PCI DSS compliance program (PCI DSS 12.4.1), and SHALL submit the signed Attestation of Compliance (AOC) to the acquirer and, where required, payment brands by the due date recorded in the Compliance Calendar.
- **CMP-001.5.6.16** `[PCI]` Where the Organization is a service provider, the Head of GRC SHALL perform reviews at least every 3 months confirming that personnel are performing the tasks required by PCI DSS 12.4.2 (daily log reviews, firewall and router rule-set reviews, application of configuration standards, response to security alerts, and change management), and SHALL record the results and their sign-off by the CISO (PCI DSS 12.4.2.1).
- **CMP-001.5.6.17** `[PCI]` CDE scope confirmation, ASV scanning and segmentation testing SHALL follow SEC-019 and SEC-011. Targeted risk analyses required by PCI DSS 12.3.1, and any customized-approach controls (12.3.2), SHALL be performed under RSK-002 section 5.8 and recorded in REF-001.

#### `[HIPAA]` Security Rule risk analysis and evaluation

- **CMP-001.5.6.18** `[HIPAA]` The Security Rule risk analysis and risk management (45 CFR §164.308(a)(1)(ii)(A)–(B)) SHALL be performed under CMP-008 section 5.3.
- **CMP-001.5.6.19** `[HIPAA]` The risk analysis frequency and update triggers are set in CMP-008.5.3.5. The Head of GRC SHALL schedule them in the Compliance Calendar.
- **CMP-001.5.6.20** `[HIPAA]` The technical and non-technical evaluation (45 CFR §164.308(a)(8)) SHALL be performed under CMP-008 section 5.11 and scheduled in the Compliance Calendar. Implementation decisions for each addressable specification are documented in CMP-008.

#### Other assessments

- **CMP-001.5.6.21** `[SOX]` The annual management assessment of ITGC supporting SOX §404, and quarterly sub-certifications supporting SOX §302, SHALL follow CMP-009 section 5.10 (sub-certifications under CMP-009.5.10.4) and be scheduled in the Compliance Calendar.
- **CMP-001.5.6.22** `[CPRA]` Where applicable under CMP-001.5.3.6, the CPO and CISO SHALL complete the cybersecurity audit and risk assessment required by regulations adopted under Cal. Civ. Code §1798.185 and SHALL submit any required certification by the regulatory due date recorded in the Compliance Calendar.
- **CMP-001.5.6.23** Any additional certification (e.g. ISO/IEC 27001:2022) SHALL be pursued only on ISSC approval, after which it SHALL be added to the register in CMP-001.5.6.1 and the Compliance Calendar.

### 5.7 Compliance status assessment and monitoring

- **CMP-001.5.7.1** Each obligation owner SHALL assess and record the compliance status of each of their obligations at least every 12 months, supported by Evidence stored under CMP-004. Obligations tagged `[PCI]`, `[HIPAA]`, `[SOX]`, `[GDPR]` or `[CPRA]` SHALL be assessed at least every 6 months.
- **CMP-001.5.7.2** A status of "Compliant" SHALL be supported by current Evidence from control testing under CMP-002, an external report under CMP-001.5.6, or a documented self-assessment reviewed by the Head of GRC.
- **CMP-001.5.7.3** Any obligation assessed as "Partially compliant" or "Non-compliant" SHALL, within 10 business days of the assessment: be recorded as an issue and classified under CMP-002; be entered as a Risk in the Risk Register under RSK-001; and have a remediation owner and target date within the remediation timelines in CMP-002.
- **CMP-001.5.7.4** Where non-compliance may itself require notification to a regulator, customer or individual, the obligation owner SHALL notify the GC within 1 business day of identification. Breach-related notifications follow RES-003.
- **CMP-001.5.7.5** The Head of GRC SHALL report, at each quarterly ISSC meeting: Obligations Register status by regulation tag, non-compliant obligations, overdue Compliance Calendar items, open regulatory changes, and upcoming external assessments.

### 5.8 Regulator and external inquiries

- **CMP-001.5.8.1** Any Workforce Member who receives a regulator inquiry, examination notice, subpoena, or a formal compliance inquiry from a payment brand or acquirer SHALL forward it to the GC within 1 business day of receipt and SHALL NOT respond substantively without GC authorization.
- **CMP-001.5.8.2** The GC SHALL designate a single point of contact for each regulator inquiry and SHALL log each inquiry, response, commitment and deadline. Commitments made to a regulator SHALL be entered in the Obligations Register within 10 business days.
- **CMP-001.5.8.3** Records relating to a regulator inquiry SHALL be placed under Legal Hold by the GC where the inquiry is an investigation or examination, under CMP-004.

### 5.9 Contractual obligations and customer assurance

- **CMP-001.5.9.1** The Head of GRC SHALL maintain standard responses for customer security and privacy questionnaires, reviewed every 12 months and on each new external report under CMP-001.5.6. Responses SHALL be consistent with the current Obligations Register and external reports.
- **CMP-001.5.9.2** Non-standard information security or privacy commitments proposed in a customer or Third-Party contract SHALL be reviewed by the Head of GRC before contract execution. Commitments the Organization cannot evidence SHALL NOT be accepted without written approval of the accountable executive in CMP-001.5.1.3.
- **CMP-001.5.9.3** Obligations that the Organization must flow down to Third Parties SHALL be identified in the Obligations Register and implemented through RSK-003.

### 5.10 Records

- **CMP-001.5.10.1** The Obligations Register, regulatory change log, impact assessments, Compliance Calendar, certification register, external reports, management assertions and regulator correspondence SHALL be retained under the retention schedule in CMP-004.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| ISSC | Approves this Policy; receives the quarterly compliance status report; approves pursuit of new certifications (CMP-001.5.6.23). |
| Audit Committee | Receives compliance reporting at the cadence in GOV-003; oversees external assurance. |
| CEO | Co-signs SOC 2 management's assertion (CMP-001.5.6.10). |
| CISO | Accountable for the SOC 2 Type II examination and `[PCI]` compliance program; signs AOC, Bridge Letters and management's assertion; signs off service-provider quarterly reviews. |
| CFO | Accountable for `[SOX]` obligations and the annual ITGC assessment under CMP-009. |
| GC | Interprets legal obligations; approves applicability determinations; controls regulator inquiries; approves external compliance statements; issues Legal Holds. |
| CPO | Accountable for privacy obligations; records `[GDPR]` role and `[CPRA]` thresholds; leads `[CPRA]` cybersecurity audit and risk assessment with the CISO. |
| DPO | Advises the CPO on `[GDPR]` obligations and applicability; monitors GDPR compliance under GDPR Art. 39. |
| HIPAA Security Officer | Performs the `[HIPAA]` risk analysis and Security Rule evaluation. |
| HIPAA Privacy Officer | Owns `[HIPAA]` Privacy Rule obligations recorded in the Obligations Register. |
| Head of GRC | Owns this Policy; maintains the Obligations Register, regulatory change log, Compliance Calendar and certification register; runs reviews and readiness; reports status. |
| Head of Procurement | Provides contract security and privacy commitments to the Head of GRC (CMP-001.5.2.6). |
| Internal Audit Director | Provides independent assurance over this program under CMP-002. |
| Obligation owners | Assess and evidence compliance status; implement regulatory changes; maintain register fields for their obligations. |
| Control Owners | Operate Controls mapped to obligations and produce Evidence under CMP-004. |

Role names and accountabilities are established in GOV-001 and consolidated in REF-002.

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| CMP-001.7.1 | Obligations Register review | Quarterly; new or changed obligation assessed within 30 days of publication |
| CMP-001.7.2 | Regulatory change source scan | At least monthly |
| CMP-001.7.3 | GC decision on applicability determination | Within 10 business days of submission |
| CMP-001.7.4 | Contract commitments provided to Head of GRC | Within 10 business days of contract execution |
| CMP-001.7.5 | Compliance Calendar reminders | 90, 30 and 7 days before due date, and on due date |
| CMP-001.7.6 | Escalation of overdue calendar activity | To owner's executive within 5 business days; ISSC at next meeting |
| CMP-001.7.7 | Compliance status assessment per obligation | Every 12 months; every 6 months for regulation-tagged obligations |
| CMP-001.7.8 | Issue and Risk recorded after non-compliant assessment | Within 10 business days |
| CMP-001.7.9 | Notification of GC of potentially notifiable non-compliance | Within 1 business day |
| CMP-001.7.10 | Regulator inquiry forwarded to GC | Within 1 business day of receipt |
| CMP-001.7.11 | Management response to external report findings | Within 30 days of report issuance |
| CMP-001.7.12 | SOC 2 Type II examination period | 12 months, contiguous; first period per decision (default 6 months) |
| CMP-001.7.13 | SOC 2 Bridge Letter coverage | Max 3 months after period end |
| CMP-001.7.14 | `[PCI]` PCI DSS validation | Every 12 months (ROC by QSA, or SAQ where permitted) |
| CMP-001.7.15 | `[PCI]` Service-provider personnel reviews (PCI DSS 12.4.2) | At least every 3 months |
| CMP-001.7.16 | `[HIPAA]` Risk analysis | Per CMP-008.7.3 |
| CMP-001.7.17 | `[HIPAA]` Security Rule evaluation | Per CMP-008.7.6 |
| CMP-001.7.18 | Exceptions to obligations-driven requirements | Per CMP-003 |
| CMP-001.7.19 | Retention of compliance records | Per CMP-004 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Obligations Register quarterly reviews completed on schedule | 100% | Quarterly | Head of GRC |
| New or changed obligations assessed within 30 days of publication | 100% | Quarterly | Head of GRC |
| Obligations with all mandatory fields populated | 100% | Quarterly | Head of GRC |
| Obligations with status "Not assessed" or assessment overdue | 0 | Quarterly | Head of GRC |
| Obligations rated Non-compliant | 0 open beyond the CMP-002 remediation timeline | Quarterly | Obligation owners |
| Compliance Calendar activities completed by due date | ≥ 95%; 100% for regulation-tagged activities | Monthly | Head of GRC |
| SOC 2 Type II report issued with unqualified opinion | Yes | Per examination period | CISO |
| SOC 2 exceptions noted by service auditor | 0 for Key Controls | Per examination period | CISO |
| `[PCI]` AOC submitted by due date | 100% | Every 12 months | CISO |
| `[HIPAA]` Risk analysis completed within cycle | 100% | Every 12 months | HIPAA Security Officer |
| Regulator inquiries forwarded to GC within 1 business day | 100% | Quarterly | GC |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

No Exception SHALL be granted that permits the Organization to be out of compliance with a
statutory or regulatory obligation recorded as applicable in the Obligations Register, or
to make a compliance representation prohibited by CMP-001.5.6.2. Where an obligation cannot
be met, the obligation owner SHALL record a Risk under RSK-001 and the GC SHALL determine
any required disclosure.

## 10. Enforcement

Non-compliance is handled under CMP-007.

A false or unapproved representation of the Organization's certification or compliance
status (CMP-001.5.6.2), or a substantive response to a regulator without GC authorization
(CMP-001.5.8.1), SHALL be referred to the GC and CHRO for handling under CMP-007.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| CMP-001.5.1 | 4.2, 5.3; A.5.2, A.5.31 | GV.OC-03, GV.RR-02 | PM-1, PM-2 | — | CC1.3, CC2.2 | APO01, MEA03 | GDPR Art. 5(2), 24; PCI DSS 12.4.1 |
| CMP-001.5.2 – 5.3 | 4.2, 6.1.3; A.5.31, A.5.34 | GV.OC-03 | PM-1, PL-1 | — | CC3.1, CC2.3 | MEA03 | GDPR Art. 3, 24, 27; Cal. Civ. Code §1798.140; 45 CFR §160.103 |
| CMP-001.5.4 | 4.1, 4.2, 6.3; A.5.31 | GV.OC-03, ID.IM-01 | PM-1 | — | CC3.4 | MEA03, APO12 | — |
| CMP-001.5.5 | 9.1; A.5.36 | GV.OV-01 | CA-7 | — | CC4.1 | MEA01, MEA03 | PCI DSS 12.4.2 |
| CMP-001.5.6 | 9.1, 9.2; A.5.35, A.5.36 | GV.OV-01, ID.IM-01 | CA-2, CA-7 | — | CC2.3, CC4.1, CC4.2 | MEA04 | PCI DSS 12.3.1, 12.4.1, 12.4.2; 45 CFR §164.308(a)(1)(ii)(A)–(B), §164.308(a)(8); SOX §§302, 404; Cal. Civ. Code §1798.185 |
| CMP-001.5.7 | 9.1, 10.2; A.5.36 | GV.OV-01, GV.OV-03 | CA-5, CA-7 | — | CC4.1, CC4.2 | MEA01, MEA03 | GDPR Art. 5(2), 24 |
| CMP-001.5.8 – 5.9 | 4.2; A.5.5, A.5.31 | GV.OC-03, GV.SC-01 | PM-1, SA-4 | 15.4 | CC2.3, CC9.2 | APO10, MEA03 | GDPR Art. 31; PCI DSS 12.8.5 |
| CMP-001.5.10 | 7.5.3; A.5.33 | GV.PO-01 | AU-11 | — | CC2.1 | MEA03 | — |

## 12. Related documents

ISP-000, GOV-001, GOV-002, GOV-003, GOV-006, RSK-001, RSK-002, RSK-003, CMP-002, CMP-003,
CMP-004, CMP-005, CMP-007, CMP-008, CMP-009, CMP-010, SEC-002, SEC-011, SEC-019, RES-003,
TPL-001, TPL-010, REF-001, REF-002, REF-003

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Head of GRC | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
