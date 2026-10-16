# CMP-006 — Whistleblower & Security Concern Reporting Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | CMP-006 |
| Title | Whistleblower & Security Concern Reporting Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | General Counsel (GC) |
| Approver | Audit Committee † (SOX §301) |
| Effective date | [DECISION REQUIRED: Date of Audit Committee approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-001, GOV-004, CMP-001, CMP-002, CMP-004, CMP-005, CMP-007, RES-001, RES-002, RES-003, SEC-011, PPL-001, PPL-002 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | GC | Initial release |

## 3. Purpose

This document establishes how Workforce Members, Third Parties and other persons raise
concerns about information security, privacy, data protection, accounting, internal
accounting controls, auditing matters, and violations of law or of suite documents, and how
the Organization receives, triages, investigates and resolves those concerns. It sets the
confidentiality and anonymity protections that apply to reporters, and prohibits
retaliation against anyone who reports in good faith or assists an investigation.

It implements the Audit Committee's obligation under `[SOX]` §301 (Securities Exchange Act
§10A(m)(4)) to establish procedures for the receipt, retention and treatment of complaints
about accounting, internal accounting controls and auditing matters, including the
confidential, anonymous submission of concerns by employees.

## 4. Scope

- **People:** all Workforce Members, including former Workforce Members and job applicants
  where the concern arose in the course of the work relationship or recruitment;
  Third Parties and their personnel; shareholders; members of administrative, management
  or supervisory bodies; volunteers and trainees; and facilitators, colleagues or relatives
  who assist or are connected with a reporter.
- **Subject matter:**
  - suspected or actual Security Incidents, Personal Data Breaches and Control failures
    that the reporter is unwilling or unable to report through the routine channel in RES-001;
  - circumvention, override or falsification of Controls or Evidence;
  - violations of suite documents, laws or regulations relating to information security,
    privacy, data protection, consumer protection, financial services or public health;
  - `[SOX]` questionable accounting, internal accounting controls or auditing matters,
    including fraud and misstatement of financial records;
  - `[HIPAA]` conduct believed to be unlawful or to violate professional or clinical
    standards involving PHI (45 CFR §164.502(j));
  - retaliation for a prior report.
- **Systems and data:** every channel, case-management system and record used to receive,
  investigate and retain reports, and all Personal Data within them.
- **Locations:** all locations and jurisdictions in which the Organization operates.
  Where local law grants greater protection, local law prevails.
- **Exclusions:** personal workplace grievances that do not involve the subject matter above
  are handled by the CHRO under PPL-001. External vulnerability reports are received through
  the Vulnerability Disclosure Program under SEC-011. Routine reporting of Security Events is
  governed by RES-001 and GOV-004; this document supplements, and does not replace, those duties.

## 5. Policy statements

### 5.1 Duty and right to report

- **CMP-006.5.1.1** Workforce Members SHALL report any suspected matter within the subject-matter scope of section 4 through a channel in section 5.2. Reporting a Security Event through the RES-001 channel satisfies this duty for Security Events.
- **CMP-006.5.1.2** A reporter SHALL NOT be required to have proof. A report made in good faith, on information the reporter honestly believes to be true at the time of the report, is protected under section 5.6 even if the concern is not substantiated.
- **CMP-006.5.1.3** No Workforce Member SHALL be required to report first through an internal channel before reporting to a regulator, law enforcement agency or other competent authority where the law permits external reporting.
- **CMP-006.5.1.4** No agreement, policy, confidentiality clause or separation agreement used by the Organization SHALL prohibit or impede a person from communicating directly with, or receiving an award from, a regulator or law enforcement agency concerning a possible violation of law (including SEC Rule 21F-17 under the Securities Exchange Act). The GC SHALL review template agreements for this requirement every 12 months.
- **CMP-006.5.1.5** Managers who receive a concern within scope SHALL forward it to the case-management system (section 5.2) within 1 business day of receipt and SHALL NOT investigate it themselves.

### 5.2 Reporting channels

- **CMP-006.5.2.1** The Organization SHALL maintain all of the following reporting channels:
  1. **Direct report** to a manager, the CISO, the CPO, the DPO, the Head of GRC, the Internal Audit Director, the GC or the CHRO;
  2. **Security channel** for Security Events under RES-001 (security operations mailbox, ticket queue and hotline);
  3. **Ethics Hotline**: a telephone line and web intake form operated by an independent Third Party, available 24 hours a day, 7 days a week, in every language in which the Organization employs at least 50 Workforce Members [DECISION REQUIRED: Language threshold for hotline coverage. Recommended default: every language spoken by 50 or more Workforce Members, plus English];
  4. **Anonymous channel**: the Ethics Hotline configured to accept reports without collecting the reporter's identity, telephone number, IP address or device identifiers, with a two-way anonymous messaging function using a case key;
  5. **Audit Committee channel** `[SOX]`: a dedicated mailbox and postal address, accessible only to the Audit Committee Chair and the person the Audit Committee designates, for accounting, internal accounting control and auditing complaints and for any concern involving the CEO, CFO, GC, CISO or a member of the Board of Directors;
  6. **In-person meeting** with the GC or a designee, held within 7 days of a reporter's request, where required by EU Whistleblower Directive 2019/1937 Art. 9(2).
- **CMP-006.5.2.2** The Third Party operating the Ethics Hotline SHALL be assessed and contracted under RSK-003 as a Tier 1 Critical Vendor (RSK-003.5.2.1), and its contract SHALL prohibit disclosure of reporter identity or metadata to the Organization without the reporter's consent.
- **CMP-006.5.2.3** All channels in CMP-006.5.2.1 items 3–5 SHALL route reports into a single case-management system with access restricted under section 5.5.
- **CMP-006.5.2.4** Channel details SHALL be published on the Organization's intranet, in GOV-004 acknowledgement materials, in the training required by PPL-002, at each physical work location, and on the Organization's public website for external reporters.
- **CMP-006.5.2.5** `[GDPR]` For each EU/EEA legal entity with 50 or more workers, the GC SHALL designate a local or shared internal reporting channel meeting EU Whistleblower Directive 2019/1937 Art. 8, and the published channel information SHALL include the external reporting procedures of the competent national authorities (Art. 9(1)(g)).
- **CMP-006.5.2.6** The GC SHALL test each channel in CMP-006.5.2.1 items 3–5 every 6 months by submitting a test report and confirming receipt, routing and acknowledgement within the times in section 7.

### 5.3 Receipt, acknowledgement and triage

- **CMP-006.5.3.1** Every report SHALL be logged in the case-management system with a unique case number, date and time of receipt, channel, category and (where known) reporter contact method, within 1 business day of receipt.
- **CMP-006.5.3.2** Workforce Members designated by the GC SHALL acknowledge receipt to the reporter, through the channel used, within 7 days of receipt, unless the reporter has declined acknowledgement or acknowledgement would reveal the reporter's identity.
- **CMP-006.5.3.3** The GC or designee SHALL triage each report within 2 business days of receipt and assign one of the categories and routings in section 5.3.6.
- **CMP-006.5.3.4** A report indicating an active or imminent Security Incident or Personal Data Breach SHALL be routed to the SOC Manager within 4 hours of receipt, for handling under RES-002. The reporter's identity SHALL be withheld from the SOC Manager unless it is necessary for containment and the reporter consents.
- **CMP-006.5.3.5** A report indicating imminent risk to the health or safety of any person SHALL be escalated to the GC and the relevant emergency service immediately on receipt.
- **CMP-006.5.3.6** Triage categories and routing:

| Category | Examples | Investigation lead | Oversight / notification |
|---|---|---|---|
| A — Accounting & audit `[SOX]` | Accounting fraud, ITGC override in a Financially Significant System, misleading statements to auditors | Internal Audit Director or external investigator appointed by the Audit Committee | Audit Committee Chair notified within 5 business days of receipt |
| B — Senior leadership | Any concern implicating the CEO, CFO, GC, CISO, CPO, an ISSC member or a director | Investigator appointed by the Audit Committee Chair | Audit Committee Chair notified within 2 business days of receipt |
| C — Information security | Control circumvention, unauthorized access, data exfiltration, falsified Evidence | CISO (or Internal Audit Director if the CISO's function is implicated) | ISSC informed in the quarterly report (section 5.8) |
| D — Privacy & data protection | Unlawful processing, ignored DSRs, transfers without safeguards | CPO, with the DPO | ISSC informed in the quarterly report |
| E — `[HIPAA]` PHI | Misuse or unlawful disclosure of PHI | HIPAA Privacy Officer, with the HIPAA Security Officer for ePHI | ISSC informed in the quarterly report |
| F — Retaliation | Adverse action following a report or participation in an investigation | GC (or Audit Committee appointee if the GC is implicated) | Audit Committee Chair notified within 5 business days of receipt |
| G — Other legal or policy | Other violations of law or suite documents | GC or designee | ISSC informed in the quarterly report |

- **CMP-006.5.3.7** A person implicated by a report, or who reports to an implicated person, SHALL NOT receive, triage, investigate or decide on that report. The GC SHALL record each recusal in the case file.
- **CMP-006.5.3.8** A report that is out of scope SHALL be referred to the responsible function (for example, the CHRO under PPL-001) within 5 business days of triage, with the reporter informed of the referral where the reporter can be contacted.

### 5.4 Investigation

- **CMP-006.5.4.1** The investigation lead SHALL document an investigation plan within 10 business days of triage, stating scope, allegations, evidence sources, interviewees and target completion date.
- **CMP-006.5.4.2** Investigations SHOULD be completed within 90 days of receipt. Where an investigation will exceed 90 days, the investigation lead SHALL record the reason and a revised target date, and the GC SHALL approve the extension.
- **CMP-006.5.4.3** The investigation lead SHALL provide feedback to the reporter on actions taken or planned within 3 months of the acknowledgement of receipt (or, where no acknowledgement was sent, within 3 months and 7 days of receipt), to the extent feedback does not prejudice the investigation or the rights of others (EU Whistleblower Directive 2019/1937 Art. 9(1)(f)).
- **CMP-006.5.4.4** Investigators SHALL be independent of the subject matter and SHALL have completed investigation training in the preceding 24 months. The GC MAY engage external counsel or forensic investigators; where engaged by the Audit Committee under `[SOX]` §301, they report to the Audit Committee.
- **CMP-006.5.4.5** Collection of electronic Evidence SHALL follow the integrity and chain-of-custody requirements of CMP-004. Monitoring or collection of Workforce Member communications SHALL be authorized in writing by the GC and SHALL comply with GOV-004 and, for Personal Data, CMP-005.
- **CMP-006.5.4.6** The GC SHALL issue a Legal Hold under CMP-004 within 1 business day of determining that an investigation may lead to litigation, regulatory proceedings or termination of employment.
- **CMP-006.5.4.7** Persons who are the subject of a report SHALL be informed of the allegations and given an opportunity to respond before any finding is made against them, unless the GC determines in writing that notice would jeopardize the investigation, the preservation of Evidence or the reporter's protection. Notice deferred on that basis SHALL be given before the investigation closes.
- **CMP-006.5.4.8** Each investigation SHALL conclude with a written report stating the allegations, Evidence reviewed, findings (substantiated, partially substantiated, unsubstantiated, or inconclusive), Root Cause where determinable, and recommended actions.
- **CMP-006.5.4.9** Substantiated findings involving a person's conduct SHALL be referred to the CHRO for action under CMP-007 within 5 business days of the investigation report. Findings involving a Third Party SHALL also be referred to the Head of Procurement for contractual action under CMP-007 and RSK-003.
- **CMP-006.5.4.10** Findings that reveal a Control Deficiency SHALL be logged as an issue under CMP-002.5.8.1, and findings that reveal a Risk SHALL be entered in the Risk Register under RSK-001.
- **CMP-006.5.4.11** Where an investigation identifies a possible Personal Data Breach, the notification assessment SHALL be performed under RES-003; where it identifies a possible Material Cybersecurity Incident `[SOX]`, the materiality determination SHALL be performed under RES-003.

### 5.5 Confidentiality and anonymity

- **CMP-006.5.5.1** The identity of a reporter, and any information from which the identity can be directly or indirectly deduced, SHALL NOT be disclosed to anyone beyond the staff authorized to receive or follow up on the report without the reporter's explicit written consent, except where disclosure is required by law or by a court or regulator. Where disclosure is legally required, the reporter SHALL be informed in advance unless that would jeopardize the related investigation or proceedings.
- **CMP-006.5.5.2** Access to the case-management system SHALL be limited to named individuals approved by the GC, and for Category A and B cases to individuals approved by the Audit Committee Chair. Access SHALL use MFA per SEC-004 and SHALL be reviewed quarterly.
- **CMP-006.5.5.3** The case-management system SHALL log all access to case files, and the GC SHALL review the access log for each Category A, B and F case at closure and for all cases quarterly.
- **CMP-006.5.5.4** Case files and reports SHALL be classified Restricted under SEC-002.
- **CMP-006.5.5.5** No person SHALL attempt to identify an anonymous reporter. An attempt to identify an anonymous reporter is a Category 4 violation under CMP-007.
- **CMP-006.5.5.6** The identity of persons concerned by a report SHALL be protected to the same standard as the reporter's while the investigation is open.
- **CMP-006.5.5.7** `[GDPR]` Processing of Personal Data in reports SHALL be recorded in the ROPA (TPL-010), SHALL have a DPIA (TPL-005) before the channel is introduced or materially changed, and SHALL follow CMP-005. Personal Data that is manifestly not relevant to a report SHALL NOT be collected or, if accidentally collected, SHALL be deleted within 30 days of identification.
- **CMP-006.5.5.8** Data subject access and other DSRs concerning case files SHALL be handled under CMP-010; the DPO SHALL consult the GC before disclosing any information that could identify a reporter.

### 5.6 Non-retaliation

- **CMP-006.5.6.1** No Workforce Member or Third Party acting for the Organization SHALL take, threaten or attempt any retaliatory action against a person because that person, in good faith: made a report under this document or to a regulator, law enforcement agency or member of the legislature; participated or assisted in an investigation or proceeding; refused to take part in conduct the person believed to be unlawful; or is a facilitator, colleague or relative of such a person.
- **CMP-006.5.6.2** Retaliatory action includes dismissal, suspension, demotion, withholding of promotion or training, negative performance evaluation or reference, change of duties or location, reduction in pay or hours, disciplinary action, coercion, intimidation, harassment, ostracism, discrimination, early termination of a Third-Party contract, blacklisting, and referral for psychiatric or medical assessment.
- **CMP-006.5.6.3** `[SOX]` The Organization SHALL comply with SOX §806 (18 U.S.C. §1514A) and SHALL NOT discharge, demote, suspend, threaten, harass or discriminate against an employee for providing information or assisting an investigation regarding conduct the employee believes constitutes mail, wire, bank or securities fraud, a violation of an SEC rule or regulation, or a violation of federal law relating to fraud against shareholders.
- **CMP-006.5.6.4** `[GDPR]` For reporters in the EU/EEA, the Organization SHALL apply the protections of EU Whistleblower Directive 2019/1937 as transposed in the applicable Member State, including the reversal of the burden of proof (Art. 21(5)): in any proceeding in which the reporter claims detriment, the Organization SHALL be able to demonstrate that the measure was based on duly justified grounds unrelated to the report.
- **CMP-006.5.6.5** `[HIPAA]` The Organization SHALL NOT intimidate, threaten, coerce, discriminate against, or take other retaliatory action against any individual for filing a complaint with the Secretary of HHS, for testifying, assisting or participating in a compliance review or proceeding, or for a disclosure protected by 45 CFR §164.502(j) (45 CFR §164.530(g)(2) and §160.316).
- **CMP-006.5.6.6** Before any adverse employment or contractual action is taken against a person who made a report within the preceding 24 months, the CHRO (or, for Third Parties, the Head of Procurement) SHALL obtain the GC's written confirmation that the action is unrelated to the report.
- **CMP-006.5.6.7** The GC SHALL contact each identified reporter in Categories A, B and F at 3 and 12 months after case closure to ask whether any retaliation has occurred, and SHALL log a Category F case for each allegation received.
- **CMP-006.5.6.8** Substantiated retaliation SHALL be sanctioned under CMP-007 as a Category 4 violation, and the Organization SHALL take action to remedy the detriment to the reporter.
- **CMP-006.5.6.9** Protection under this section does not extend to a person who knowingly makes a false report. A knowingly false report is a violation under CMP-007. A report that is mistaken but made in good faith SHALL NOT be treated as false.
- **CMP-006.5.6.10** A reporter's own involvement in the reported conduct is not excused by the report, but the CHRO SHALL treat self-reporting as a mitigating factor under CMP-007.

### 5.7 `[SOX]` Audit Committee procedures for accounting and auditing complaints

- **CMP-006.5.7.1** `[SOX]` The Audit Committee SHALL own the procedures in this section and SHALL approve this document and every material change to it.
- **CMP-006.5.7.2** `[SOX]` Every complaint concerning accounting, internal accounting controls or auditing matters, from any source and through any channel, SHALL be classified Category A and SHALL be reported to the Audit Committee Chair within 5 business days of receipt, regardless of preliminary assessment of merit.
- **CMP-006.5.7.3** `[SOX]` The Audit Committee Chair SHALL decide within 10 business days of notification whether the complaint is investigated by the Internal Audit Director, by the GC, or by external counsel or forensic accountants reporting directly to the Audit Committee. A complaint implicating management involved in financial reporting SHALL be investigated by a party reporting directly to the Audit Committee.
- **CMP-006.5.7.4** `[SOX]` The Audit Committee SHALL have authority to engage independent advisors at the Organization's expense under Securities Exchange Act §10A(m)(5)-(6), and management SHALL NOT restrict access to records, systems or personnel needed for the investigation.
- **CMP-006.5.7.5** `[SOX]` The Internal Audit Director SHALL present a log of all Category A and B complaints, their status and their resolution to the Audit Committee at every scheduled meeting and at least quarterly.
- **CMP-006.5.7.6** `[SOX]` The CFO and the Internal Audit Director SHALL assess each substantiated Category A finding for its effect on internal control over financial reporting and for deficiency classification under CMP-002, and the CFO SHALL consider the finding in the §302 certification and §404 assessment (CMP-009).
- **CMP-006.5.7.7** `[SOX]` The GC SHALL inform the External Auditor of Category A complaints, and of their resolution, where the complaint could affect the financial statements or internal control over financial reporting, in coordination with the Audit Committee Chair.
- **CMP-006.5.7.8** `[SOX]` Records of complaints and their treatment SHALL be retained under CMP-004.

### 5.8 Reporting, oversight and records

- **CMP-006.5.8.1** The GC SHALL report quarterly to the ISSC, with anonymized aggregate data: reports received by channel and category, time to acknowledge, time to triage, cases open and closed, substantiation rate, retaliation allegations, and actions taken.
- **CMP-006.5.8.2** The GC SHALL report quarterly to the Audit Committee on all categories, including the data in CMP-006.5.8.1 and the status of each Category A, B and F case.
- **CMP-006.5.8.3** Trends in Category C, D and E reports SHALL be considered in the enterprise risk assessment under RSK-002 and in the obligations register review under CMP-001.
- **CMP-006.5.8.4** Case files, investigation reports and decisions SHALL be retained, protected and deleted under CMP-004. Case files under Legal Hold SHALL NOT be deleted.
- **CMP-006.5.8.5** Internal Audit SHALL audit the operation of this document at least every 24 months under CMP-002.5.2.8.

### 5.9 Awareness

- **CMP-006.5.9.1** The training required by PPL-002 SHALL include the reporting channels, the anonymous option, confidentiality protections and non-retaliation.
- **CMP-006.5.9.2** Managers SHALL complete training on receiving reports and on non-retaliation within 30 days of appointment to a people-management role, and every 24 months thereafter.
- **CMP-006.5.9.3** The Head of GRC SHALL include channel information in each Third-Party onboarding pack issued under RSK-003.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| Audit Committee | Approves this document; owns `[SOX]` §301 procedures; receives Category A, B and F notifications; appoints independent investigators; receives quarterly reports. |
| Audit Committee Chair | Receives Audit Committee channel reports; decides investigation routing for Category A (CMP-006.5.7.3) and B cases; approves case-system access for those cases. |
| GC | Owns this document; designates the Workforce Members who handle reports; operates channels; triages reports; enforces confidentiality; approves extensions, monitoring and Legal Holds; protects reporters from retaliation; reports to the ISSC and Audit Committee. |
| Internal Audit Director | Investigates Category A cases when assigned; maintains the Category A/B log for the Audit Committee; audits this document under CMP-002. |
| CFO | `[SOX]` Assesses substantiated Category A findings for financial reporting impact; supports investigations without directing them. |
| CISO | Leads Category C investigations unless conflicted; supplies forensic support under CMP-004. |
| CPO / DPO | Lead Category D investigations; maintain ROPA and DPIA coverage of the channels (CMP-006.5.5.7); handle DSRs concerning case files. |
| HIPAA Privacy Officer / HIPAA Security Officer | `[HIPAA]` Lead Category E investigations. |
| SOC Manager | Handles reports routed under CMP-006.5.3.4 as Security Incidents under RES-002. |
| CHRO | Applies sanctions under CMP-007; confirms with the GC before adverse action against reporters (CMP-006.5.6.6); handles out-of-scope grievances under PPL-001. |
| Head of Procurement | Contracts and manages the hotline Third Party under RSK-003; applies Third-Party remedies under CMP-007. |
| Head of GRC | Includes reporting information in Third-Party onboarding; links findings to CMP-002 issues and the Risk Register. |
| Managers | Forward concerns within 1 business day; do not investigate; do not retaliate. |
| Workforce Members | Report concerns within scope; cooperate with investigations; maintain confidentiality of investigations they take part in. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| CMP-006.7.1 | Ethics Hotline availability | 24 hours a day, 7 days a week; anonymous option on telephone and web |
| CMP-006.7.2 | Manager forwarding of a received concern | Within 1 business day |
| CMP-006.7.3 | Case logged in case-management system | Within 1 business day of receipt |
| CMP-006.7.4 | Acknowledgement to reporter | Within 7 days of receipt |
| CMP-006.7.5 | Triage and categorization | Within 2 business days of receipt |
| CMP-006.7.6 | Routing of active or imminent Security Incident to SOC Manager | Within 4 hours of receipt |
| CMP-006.7.7 | `[SOX]` Audit Committee Chair notification — Category A and F | Within 5 business days of receipt |
| CMP-006.7.8 | Audit Committee Chair notification — Category B | Within 2 business days of receipt |
| CMP-006.7.9 | `[SOX]` Audit Committee routing decision on Category A | Within 10 business days of notification |
| CMP-006.7.10 | Investigation plan | Within 10 business days of triage |
| CMP-006.7.11 | Investigation completion target | 90 days from receipt; extension approved by GC |
| CMP-006.7.12 | Feedback to reporter | Within 3 months of acknowledgement |
| CMP-006.7.13 | Referral of substantiated conduct findings to CHRO | Within 5 business days of investigation report |
| CMP-006.7.14 | Legal Hold issued after litigation risk identified | Within 1 business day |
| CMP-006.7.15 | In-person meeting on request | Within 7 days of request |
| CMP-006.7.16 | Channel test | Every 6 months |
| CMP-006.7.17 | Case-management system access review | Quarterly |
| CMP-006.7.18 | Retaliation follow-up with reporter (Categories A, B, F) | 3 and 12 months after closure |
| CMP-006.7.19 | GC review before adverse action against a reporter | Required for reports in the preceding 24 months |
| CMP-006.7.20 | Manager training on receiving reports | Within 30 days of appointment, then every 24 months |
| CMP-006.7.21 | Retention of reports and case files | Per CMP-004 (whistleblower reports) |
| CMP-006.7.22 | Reporting to ISSC and Audit Committee | Quarterly |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Reports acknowledged within 7 days | 100% | Quarterly | GC |
| Reports triaged within 2 business days | ≥ 95% | Quarterly | GC |
| `[SOX]` Category A complaints notified to Audit Committee Chair within 5 business days | 100% | Quarterly | GC |
| Reporters receiving feedback within 3 months | 100% (excluding uncontactable anonymous reporters) | Quarterly | GC |
| Investigations closed within 90 days | ≥ 80% | Quarterly | GC |
| Semi-annual channel tests passed | 100% | Every 6 months | GC |
| Substantiated retaliation cases | 0 | Quarterly | GC |
| Proportion of reports made anonymously | Tracked; trend reported (no target) | Quarterly | GC |
| Workforce Members aware of the anonymous channel (annual training assessment item) | ≥ 90% correct | Every 12 months | CISO (via PPL-002) |
| Manager reporting-training completion | 100% | Quarterly | CHRO |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following requirements SHALL NOT receive an Exception: the anonymous channel
(CMP-006.5.2.1 item 4); the Audit Committee channel and procedures (CMP-006.5.2.1 item 5 and
section 5.7); confidentiality of reporter identity (CMP-006.5.5.1); the prohibition on
identifying anonymous reporters (CMP-006.5.5.5); non-retaliation (section 5.6); and the
prohibition on impeding communication with regulators (CMP-006.5.1.4).

## 10. Enforcement

Non-compliance is handled under CMP-007.

Retaliation, attempts to identify an anonymous reporter, breach of investigation
confidentiality, destruction of Evidence relevant to a report, and obstruction of an
investigation are Category 4 violations under CMP-007. A knowingly false report is
handled under CMP-007, with the category determined by the harm caused.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| CMP-006.5.1 – 5.2 | 7.4; A.6.8, A.5.31 | GV.RR-04, GV.OC-03 | IR-6, PL-4 | 14.6 | CC1.1, CC2.2, CC2.3 | APO01, MEA03 | SOX §301; EU Directive 2019/1937 Arts. 7–9; SEC Rule 21F-17; 45 CFR §164.530(d) |
| CMP-006.5.3 – 5.4 | A.5.24, A.5.26, A.5.28, A.6.8 | RS.MA-01, RS.AN-03 | IR-4, IR-6, AU-9 | 17.3 | CC2.2, CC7.3, CC7.4 | DSS02, MEA03 | EU Directive 2019/1937 Art. 9; GDPR Art. 5 |
| CMP-006.5.5 | A.5.12, A.5.15, A.5.34 | PR.AA-05, PR.DS-01 | AC-3, AC-6, AU-2 | 3.3, 6.5 | CC6.1, C1.1, P-series (if in scope) | DSS05 | EU Directive 2019/1937 Art. 16; GDPR Arts. 5, 30, 35 |
| CMP-006.5.6 | A.6.4, A.5.31 | GV.RR-04 | PS-8 | — | CC1.1, CC1.5 | APO07 | SOX §806 (18 U.S.C. §1514A); EU Directive 2019/1937 Arts. 19–21; 45 CFR §§160.316, 164.530(g)(2) |
| CMP-006.5.7 | 5.1, 9.3 | GV.OV-01, GV.RR-01 | PM-1 | — | CC1.2, CC2.3 | EDM01, MEA02 | SOX §301 (Exchange Act §10A(m)(4)–(6)); SOX §§302, 404 |
| CMP-006.5.8 – 5.9 | 7.3, 9.1, 9.3 | GV.OV-01, PR.AT-01 | AT-2, PM-1 | 14.1, 14.6 | CC1.4, CC2.2, CC4.1 | APO07, MEA01 | EU Directive 2019/1937 Art. 18 |

## 12. Related documents

ISP-000, GOV-001, GOV-004, GOV-006, CMP-001, CMP-002, CMP-003, CMP-004, CMP-005, CMP-007,
CMP-009, CMP-010, RSK-001, RSK-002, RSK-003, SEC-002, SEC-004, SEC-011, RES-001, RES-002,
RES-003, PPL-001, PPL-002, TPL-005, TPL-010, REF-002

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: General Counsel (GC) | | | |
| Approver: Audit Committee Chair, on behalf of the Audit Committee | | | |
