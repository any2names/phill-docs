# CMP-005 — Data Privacy & Protection Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | CMP-005 |
| Title | Data Privacy & Protection Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Privacy Officer (CPO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months, and on the event triggers in GOV-002 |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-001, GOV-002, GOV-006, CMP-001, CMP-003, CMP-004, CMP-007, CMP-008, CMP-010, RSK-001, RSK-002, RSK-003, RSK-006, SEC-002, SEC-003, SEC-006, SEC-010, SEC-017, RES-003, PPL-002, TPL-005, TPL-010 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CPO | Initial release |

## 3. Purpose

This Policy establishes the Organization's mandatory requirements for the lawful, fair,
transparent and secure processing of Personal Data across its lifecycle. It sets the
principles, lawful-basis rules, notice and consent requirements, privacy risk assessment
triggers, record-keeping, Processor and international transfer controls, and
regulation-specific privacy rights obligations that every business process, Information
System and Third Party processing Personal Data on the Organization's behalf SHALL meet.

This Policy is the single home for privacy requirements in the suite, including `[GDPR]`
Chapter V international transfer requirements. It does not restate retention periods
(CMP-004), Data Subject Request handling steps and deadlines (CMP-010), breach notification
(RES-003), or Third-Party tiering and reassessment (RSK-003).

## 4. Scope

| Dimension | In scope |
|---|---|
| People | All Workforce Members; members of the Board of Directors acting for the Organization |
| Personal Data | All Personal Data processed by or for the Organization, in any form (electronic, paper, audio, video), about customers, end users, prospects, Workforce Members, applicants, Third-Party contacts and any other natural person, including Sensitive Personal Information, `[HIPAA]` PHI, and `[PCI]` CHD where it relates to an identifiable person |
| Processing roles | Processing where the Organization acts as Controller, Joint Controller, Processor, `[CPRA]` business, service provider or contractor, or `[HIPAA]` Covered Entity or Business Associate |
| Systems | All Information Systems, Cloud Services, AI Systems, Endpoints and Media that store, process or transmit Personal Data, including development, test and analytics environments |
| Locations | All Organization locations and remote work locations; all jurisdictions recorded in the Obligations Register (CMP-001) [DECISION REQUIRED: Regions in scope. Recommended default: United States and EU/EEA] |
| Third Parties | All Processors, Subprocessors, `[HIPAA]` Business Associates, Joint Controllers and recipients of Personal Data |

Personal Data that has been irreversibly anonymized so that no natural person is
identifiable by any means likely to be used is out of scope. Pseudonymized Personal Data
remains in scope.

## 5. Policy statements

### 5.1 Privacy governance

- **CMP-005.5.1.1** The CPO SHALL be accountable for the Organization's privacy program, for this Policy, and for reporting privacy program status to the ISSC at least quarterly through the metrics in section 8.
- **CMP-005.5.1.2** `[GDPR]` The Organization SHALL appoint a DPO where GDPR Art. 37(1) applies and SHALL record the Art. 37(1) applicability assessment in the Obligations Register (CMP-001). [DECISION REQUIRED: DPO appointment. Recommended default: Appoint a DPO where Art. 37(1) applies, e.g. large-scale processing of Sensitive Personal Information]
- **CMP-005.5.1.3** `[GDPR]` Where a DPO is appointed, the Organization SHALL publish the DPO's contact details, notify them to each competent Supervisory Authority, involve the DPO in all privacy matters listed in GDPR Art. 38–39, and SHALL NOT instruct, dismiss or penalize the DPO for performing those tasks.
- **CMP-005.5.1.4** `[GDPR]` Where the Organization is established outside the EU/EEA and is subject to GDPR under Art. 3(2), it SHALL designate an EU representative in writing under Art. 27, unless an Art. 27(2) exemption is documented by the GC.
- **CMP-005.5.1.5** `[HIPAA]` Where the Organization is a Covered Entity, it SHALL designate a HIPAA Privacy Officer. Where it is a Business Associate, the CPO SHALL designate the role accountable for meeting BAA privacy obligations. [DECISION REQUIRED: HIPAA status. Recommended default: Business Associate]
- **CMP-005.5.1.6** Each Data Owner SHALL be accountable for the compliance of processing activities within their data set with this Policy, and SHALL record each such activity in the ROPA under section 5.8.
- **CMP-005.5.1.7** `[GDPR]` Where processing is cross-border, the DPO SHALL identify the lead Supervisory Authority under GDPR Art. 56, based on the Organization's main establishment, and SHALL record it in the ROPA (TPL-010 field A.5). [DECISION REQUIRED: Lead Supervisory Authority. Recommended default: the authority of the Member State of the Organization's EU main establishment.]

### 5.2 Privacy principles

The Organization SHALL apply the following principles to all processing of Personal Data, whatever the jurisdiction (GDPR Art. 5; Cal. Civ. Code §1798.100).

- **CMP-005.5.2.1** Lawfulness, fairness and transparency: Personal Data SHALL be processed only on a lawful basis recorded under section 5.3 and in accordance with a Privacy Notice issued under section 5.4.
- **CMP-005.5.2.2** Purpose limitation: Personal Data SHALL be collected only for specified, explicit and legitimate purposes recorded in the ROPA, and SHALL NOT be further processed in a manner incompatible with those purposes (section 5.6).
- **CMP-005.5.2.3** Data minimization: Personal Data SHALL be limited to the fields necessary for the recorded purpose (section 5.7).
- **CMP-005.5.2.4** Accuracy: Data Owners SHALL provide a means for correcting inaccurate Personal Data and SHALL act on correction requests under CMP-010.
- **CMP-005.5.2.5** Storage limitation: Personal Data SHALL be retained only for the period set for its purpose in the ROPA and deleted or anonymized under the retention schedule in CMP-004, using methods in SEC-017.
- **CMP-005.5.2.6** Integrity and confidentiality: Personal Data SHALL be classified and handled under SEC-002 and protected by the controls in the SEC series. Sensitive Personal Information SHALL be classified Restricted.
- **CMP-005.5.2.7** Accountability: The Organization SHALL be able to demonstrate compliance with each principle through Evidence managed under CMP-004.

### 5.3 Lawful basis for processing

- **CMP-005.5.3.1** Before any new processing activity begins, the Data Owner SHALL identify and record in the ROPA one lawful basis for each purpose. `[GDPR]` The lawful basis SHALL be one of those in GDPR Art. 6(1).
- **CMP-005.5.3.2** `[GDPR]` Where the lawful basis is legitimate interests (Art. 6(1)(f)), the Data Owner SHALL complete and the DPO (or CPO where no DPO is appointed) SHALL approve a written Legitimate Interests Assessment covering purpose, necessity and balancing before processing begins.
- **CMP-005.5.3.3** `[GDPR]` Processing of Sensitive Personal Information under GDPR Art. 9 SHALL additionally have a recorded Art. 9(2) condition. Processing of Personal Data relating to criminal convictions and offences SHALL have a recorded Art. 10 authorization confirmed by the GC.
- **CMP-005.5.3.4** The lawful basis for a purpose SHALL NOT be changed after collection without CPO approval and an updated Privacy Notice. Consent SHALL NOT be substituted by another basis after consent has been withdrawn.
- **CMP-005.5.3.5** `[HIPAA]` PHI SHALL be used or disclosed only as permitted or required by 45 CFR §164.502 and, where the Organization is a Business Associate, only as permitted by the applicable BAA.

### 5.4 Privacy Notices

- **CMP-005.5.4.1** The Organization SHALL provide a Privacy Notice to individuals at or before the point of collection of their Personal Data. `[GDPR]` Notices SHALL contain the information required by GDPR Art. 13 (direct collection) or Art. 14 (indirect collection).
- **CMP-005.5.4.2** `[GDPR]` Where Personal Data is obtained from a source other than the Data Subject, the Privacy Notice SHALL be provided within one month of obtaining it, or at first communication or first disclosure to another recipient if earlier (Art. 14(3)).
- **CMP-005.5.4.3** `[CPRA]` The Organization SHALL provide a notice at collection listing the categories of personal information and Sensitive Personal Information collected, purposes, whether each is sold or shared, and the retention period or criteria for each category, and SHALL maintain an online privacy policy meeting Cal. Civ. Code §1798.130(a)(5).
- **CMP-005.5.4.4** `[HIPAA]` Where the Organization is a Covered Entity, it SHALL issue and maintain a Notice of Privacy Practices meeting 45 CFR §164.520.
- **CMP-005.5.4.5** Each external Privacy Notice SHALL be approved by the CPO and the GC before publication, reviewed at least every 12 months, and updated before any new purpose, new category of Personal Data, or new category of recipient takes effect.
- **CMP-005.5.4.6** The Organization SHALL provide a Workforce Privacy Notice covering Workforce Member and applicant Personal Data, including monitoring under GOV-004 section 5.13 and phishing-simulation results under PPL-002, maintained by the CHRO and approved by the CPO.
- **CMP-005.5.4.7** All superseded Privacy Notice versions SHALL be retained with their effective dates as Evidence under CMP-004.

### 5.5 Consent

- **CMP-005.5.5.1** Where consent is the lawful basis, it SHALL be freely given, specific, informed and unambiguous, given by a clear affirmative act, and SHALL NOT be bundled with acceptance of terms of service or made a condition of a service where not necessary for that service (GDPR Art. 4(11), Art. 7).
- **CMP-005.5.5.2** `[GDPR]` Consent for processing of Sensitive Personal Information under Art. 9(2)(a), for automated individual decision-making under Art. 22(2)(c), and for transfers under Art. 49(1)(a) SHALL be explicit.
- **CMP-005.5.5.3** The Organization SHALL record, for each consent: the identity of the individual, date and time, the version of the consent text and Privacy Notice presented, the method of capture, and the purposes covered. Consent records SHALL be retained as Evidence under CMP-004.
- **CMP-005.5.5.4** Withdrawal of consent SHALL be as easy as giving it, available through at least the same channel by which consent was given, and effective for all systems within 15 business days of receipt.
- **CMP-005.5.5.5** `[GDPR]` Consent for information society services offered directly to a child under 16, or the lower age set by the applicable Member State law, SHALL be given or authorized by the holder of parental responsibility (Art. 8).
- **CMP-005.5.5.6** `[CPRA]` The Organization SHALL NOT sell or share the personal information of consumers it knows to be under 16 without affirmative opt-in authorization from the consumer (ages 13–15) or a parent or guardian (under 13) (Cal. Civ. Code §1798.120(c)).
- **CMP-005.5.5.7** Electronic direct marketing SHALL be sent only with consent or under a statutory exemption confirmed by the GC, and every message SHALL include an opt-out mechanism.
- **CMP-005.5.5.8** Non-essential cookies and similar tracking technologies SHALL NOT be set on devices of EU/EEA users before consent is obtained, and consent tools SHALL present "reject" with equal prominence to "accept".

### 5.6 Purpose limitation

- **CMP-005.5.6.1** Each purpose for which Personal Data is processed SHALL be recorded in the ROPA before processing for that purpose begins.
- **CMP-005.5.6.2** Before Personal Data is used for a purpose not recorded in the ROPA, the Data Owner SHALL submit a compatibility assessment considering the factors in GDPR Art. 6(4) to the CPO. Processing for the new purpose SHALL NOT begin until the CPO approves it in writing and the ROPA and Privacy Notice are updated.
- **CMP-005.5.6.3** Personal Data SHALL NOT be used to train, fine-tune or evaluate AI Systems unless that purpose is recorded in the ROPA and approved under section 5.6.2 and RSK-006.
- **CMP-005.5.6.4** `[CPRA]` Personal information SHALL NOT be used for purposes incompatible with the disclosed purposes or retained beyond what is necessary and proportionate for them (Cal. Civ. Code §1798.100(c)).

### 5.7 Data minimization and de-identification

- **CMP-005.5.7.1** Each data collection point (form, API, import, integration) SHALL collect only the fields recorded as necessary in the ROPA for the purpose. Optional fields SHALL be marked as optional to the individual.
- **CMP-005.5.7.2** Production Personal Data SHALL NOT be used in development or test environments. Where test data derived from production is required, it SHALL be anonymized or pseudonymized before transfer, under SEC-010.
- **CMP-005.5.7.3** Government identifiers, Sensitive Personal Information and financial account numbers SHALL be masked in user interfaces and reports except where the full value is required for the recorded purpose.
- **CMP-005.5.7.4** Pseudonymization keys and re-identification tables SHALL be stored separately from the pseudonymized data set, classified Restricted, and protected under SEC-006.
- **CMP-005.5.7.5** A data set SHALL be treated as anonymized only after the DPO (or CPO where no DPO is appointed) has approved a written re-identification risk assessment for it.
- **CMP-005.5.7.6** `[HIPAA]` Where PHI is de-identified, it SHALL be de-identified using the Safe Harbor or Expert Determination method in 45 CFR §164.514(b), and the method used SHALL be documented.

### 5.8 Record of Processing Activities

- **CMP-005.5.8.1** `[GDPR]` The Organization SHALL maintain a ROPA using TPL-010 covering every processing activity for which it acts as Controller (Art. 30(1)) and as Processor (Art. 30(2)).
- **CMP-005.5.8.2** Each ROPA entry SHALL identify the Data Owner, purposes, lawful basis, categories of Data Subjects and Personal Data, Information Systems used, recipients, Processors, international transfers and transfer mechanism, retention period by reference to CMP-004, and the security measures applied.
- **CMP-005.5.8.3** The Data Owner SHALL update the ROPA before a new processing activity begins and within 30 days of a change to an existing activity.
- **CMP-005.5.8.4** The DPO (or CPO where no DPO is appointed) SHALL review the complete ROPA for accuracy and completeness at least every 12 months, and SHALL reconcile it against the Asset Inventory (SEC-001) and the Third-Party inventory (RSK-003) during that review.
- **CMP-005.5.8.5** `[GDPR]` The ROPA SHALL be producible to a Supervisory Authority within 5 business days of request.
- **CMP-005.5.8.6** `[CPRA]` The ROPA SHALL record, for each category of personal information, whether it is sold or shared and whether it is Sensitive Personal Information used for purposes beyond those permitted by Cal. Code Regs. tit. 11, §7027(m).

### 5.9 Data Protection Impact Assessments

- **CMP-005.5.9.1** The Data Owner SHALL complete a privacy screening, using section 1 of TPL-005, for every new processing activity and every change to an existing activity that adds a purpose, a category of Personal Data, a recipient, an international transfer or a new technology.
- **CMP-005.5.9.2** A full DPIA using TPL-005 SHALL be completed, and approved under section 5.9.4, before processing begins where any of the following triggers apply:
  - (a) systematic and extensive evaluation of individuals, including profiling, that produces legal or similarly significant effects (GDPR Art. 35(3)(a));
  - (b) large-scale processing of Sensitive Personal Information or of Personal Data relating to criminal convictions (Art. 35(3)(b));
  - (c) systematic monitoring of a publicly accessible area on a large scale (Art. 35(3)(c));
  - (d) any processing type on the published DPIA list of a competent Supervisory Authority (Art. 35(4));
  - (e) any two or more of: evaluation or scoring; automated decision-making; systematic monitoring; Sensitive Personal Information; large scale; matching or combining data sets; vulnerable Data Subjects (including children and employees); innovative technology, including AI Systems; processing that prevents individuals exercising a right or using a service;
  - (f) a new international transfer of Restricted Personal Data to a country without an Adequacy Decision;
  - (g) `[CPRA]` processing that presents significant risk to consumers' privacy as defined by California regulations, including selling or sharing personal information or processing Sensitive Personal Information;
  - (h) `[HIPAA]` a new use or disclosure of PHI, or a new system that creates, receives, maintains or transmits ePHI.
- **CMP-005.5.9.3** Each DPIA SHALL describe the processing and its necessity and proportionality, assess risks to individuals using the likelihood and impact scales in RSK-002, and record the measures that reduce each risk.
- **CMP-005.5.9.4** DPIAs SHALL be reviewed by the DPO (or CPO where no DPO is appointed), with the CISO or delegate assessing security measures, and approved by the CPO. Residual Risk scored High or Critical under RSK-002 SHALL be accepted only under RSK-001.
- **CMP-005.5.9.5** `[GDPR]` Where a DPIA shows high residual risk that the Organization cannot mitigate, the DPO SHALL consult the competent Supervisory Authority under Art. 36 before processing begins, with GC concurrence.
- **CMP-005.5.9.6** Each approved DPIA SHALL be reviewed by the Data Owner at least every 24 months and before any change that meets a trigger in CMP-005.5.9.1.
- **CMP-005.5.9.7** Change requests under SEC-013 and design reviews under SEC-010 for systems processing Personal Data SHALL reference the completed TPL-005 screening or DPIA, and SHALL NOT be approved without it.

### 5.10 Privacy by design and by default

- **CMP-005.5.10.1** `[GDPR]` Privacy requirements derived from this Policy SHALL be included in the requirements and design review stage of every project and system change subject to SEC-010 that processes Personal Data (Art. 25(1)).
- **CMP-005.5.10.2** `[GDPR]` Systems SHALL be configured by default so that only Personal Data necessary for each purpose is processed and, by default, Personal Data is not made accessible to an indefinite number of persons without the individual's intervention (Art. 25(2)).
- **CMP-005.5.10.3** Access to Personal Data SHALL be granted under SEC-003 on Least Privilege and Need to Know. Bulk export of Restricted Personal Data SHALL require Data Owner approval.
- **CMP-005.5.10.4** New Information Systems that store Personal Data SHALL support, before production release: deletion or anonymization of an individual's records, export of an individual's records in a structured, commonly used, machine-readable format, correction of records, and suppression of processing for an individual.
- **CMP-005.5.10.5** Automated retention enforcement SHALL be implemented for each system holding Personal Data, so that records past the retention period set under CMP-004 are deleted or anonymized without manual intervention, unless subject to a Legal Hold.
- **CMP-005.5.10.6** `[GDPR]` Decisions based solely on automated processing, including profiling, that produce legal or similarly significant effects SHALL NOT be made unless an Art. 22(2) exception applies and is recorded in the ROPA, and the individual is offered human intervention, the opportunity to express their view, and the opportunity to contest the decision.

### 5.11 Processor and recipient management

- **CMP-005.5.11.1** Processors and Subprocessors SHALL be onboarded, tiered, assessed and reassessed under RSK-003. Any Third Party that will process Restricted Personal Data SHALL complete the privacy sections of TPL-004 (sections 5.9 and 5.14) before contract signature.
- **CMP-005.5.11.2** `[GDPR]` Processing by a Processor SHALL be governed by a written Data Processing Agreement containing every term in GDPR Art. 28(3), signed before any Personal Data is disclosed.
- **CMP-005.5.11.3** `[GDPR]` Processors SHALL NOT engage a Subprocessor without the Organization's prior written specific or general authorization; under general authorization the Processor SHALL give notice of each intended change and the Organization SHALL have the right to object (Art. 28(2)). The GC SHALL set the objection window in each agreement. [DECISION REQUIRED: Minimum Subprocessor change notice period required in Data Processing Agreements. Recommended default: 30 days]
- **CMP-005.5.11.4** `[CPRA]` Contracts with service providers, contractors and third parties to which personal information is sold or shared SHALL contain the terms required by Cal. Civ. Code §1798.100(d) and §1798.140(ag) and (j).
- **CMP-005.5.11.5** `[HIPAA]` PHI SHALL be disclosed to a Business Associate, or by the Organization as a Business Associate to a subcontractor, only under a BAA meeting 45 CFR §164.504(e).
- **CMP-005.5.11.6** Where the Organization acts as Processor, it SHALL process Personal Data only on documented instructions of the Controller, SHALL record those instructions in the ROPA, and SHALL inform the Controller without undue delay if an instruction infringes applicable law (GDPR Art. 28(3)(a), (h)).
- **CMP-005.5.11.7** Joint Controller arrangements SHALL be documented in a written agreement under GDPR Art. 26 approved by the GC.
- **CMP-005.5.11.8** At contract end, the Data Owner SHALL obtain the Processor's written certification of return or deletion of Personal Data within 30 days of termination.

### 5.12 International transfers `[GDPR]` (Chapter V)

- **CMP-005.5.12.1** `[GDPR]` Personal Data subject to GDPR SHALL NOT be transferred, or made remotely accessible, to a recipient in a country outside the EU/EEA unless the transfer is recorded in the ROPA and rests on one of the following, in order of preference:
  - (a) an Adequacy Decision under Art. 45, including certification of the US recipient under the EU-U.S. Data Privacy Framework where applicable;
  - (b) Art. 46 safeguards: the European Commission Standard Contractual Clauses (Commission Implementing Decision (EU) 2021/914) using the correct module, or Binding Corporate Rules approved under Art. 47;
  - (c) a derogation under Art. 49, only for occasional and non-repetitive transfers, approved by the DPO and the GC in writing.
- **CMP-005.5.12.2** `[GDPR]` For every transfer relying on Art. 46 safeguards, the Data Owner SHALL complete a Transfer Impact Assessment before the transfer begins, assessing the law and practice of the destination country, the recipient's exposure to public-authority access, and the supplementary measures (technical, contractual and organizational) applied. The DPO (or CPO) SHALL approve each Transfer Impact Assessment.
- **CMP-005.5.12.3** `[GDPR]` Where a Transfer Impact Assessment concludes that the destination law impinges on the effectiveness of the safeguards and supplementary measures cannot close the gap, the transfer SHALL NOT proceed, or SHALL be suspended within 30 days of that conclusion.
- **CMP-005.5.12.4** `[GDPR]` Transfer Impact Assessments SHALL be reviewed at least every 24 months, and within 30 days of a change in destination law, an Adequacy Decision being adopted or invalidated, or a change in the recipient's processing.
- **CMP-005.5.12.5** `[GDPR]` Onward transfers by Processors and Subprocessors SHALL be bound by the same transfer mechanism and assessed under CMP-005.5.12.2.
- **CMP-005.5.12.6** `[GDPR]` Executed SCCs, BCR approvals, Data Privacy Framework certification checks and Transfer Impact Assessments SHALL be retained as Evidence under CMP-004.
- **CMP-005.5.12.7** Transfers of Personal Data out of other jurisdictions with transfer restrictions recorded in the Obligations Register (CMP-001) SHALL follow the mechanism specified there, approved by the GC.

### 5.13 `[CPRA]` Sale, sharing and Sensitive Personal Information

- **CMP-005.5.13.1** `[CPRA]` The CPO SHALL determine, and record in the ROPA, whether each disclosure of personal information constitutes a "sale" or "sharing" (cross-context behavioral advertising) under Cal. Civ. Code §1798.140(ad) and (ah).
- **CMP-005.5.13.2** `[CPRA]` Where the Organization sells or shares personal information, it SHALL provide a clear and conspicuous "Do Not Sell or Share My Personal Information" link, or an alternative opt-out link meeting §1798.135, on its websites and in its applications.
- **CMP-005.5.13.3** `[CPRA]` The Organization SHALL treat an Opt-out Preference Signal, including Global Privacy Control, as a valid request to opt out of sale and sharing for that browser or device and any associated consumer profile (Cal. Code Regs. tit. 11, §7025).
- **CMP-005.5.13.4** `[CPRA]` Opt-out requests SHALL be honored and the opt-out communicated to all third parties to which personal information was sold or shared after the request, within the deadline in CMP-010.7.4 (Cal. Code Regs. tit. 11, §7026(f)). Request handling SHALL follow CMP-010.
- **CMP-005.5.13.5** `[CPRA]` After an opt-out, the Organization SHALL wait at least 12 months before requesting that the consumer authorize sale or sharing again (§1798.135(c)(4)).
- **CMP-005.5.13.6** `[CPRA]` Sensitive Personal Information SHALL be used only for the purposes permitted by Cal. Code Regs. tit. 11, §7027(m). Where it is used for any other purpose, the Organization SHALL provide a "Limit the Use of My Sensitive Personal Information" link and SHALL honor such requests within the deadline in CMP-010.7.4 (§7027(g)).
- **CMP-005.5.13.7** `[CPRA]` The Organization SHALL NOT discriminate against a consumer for exercising a privacy right, and any financial incentive tied to personal information SHALL be offered only with a notice of financial incentive under §1798.125.

### 5.14 `[HIPAA]` Minimum Necessary

- **CMP-005.5.14.1** `[HIPAA]` Uses and disclosures of, and requests for, PHI SHALL be limited to the Minimum Necessary to accomplish the intended purpose (45 CFR §164.502(b)), except for the exclusions in §164.502(b)(2).
- **CMP-005.5.14.2** `[HIPAA]` The HIPAA Privacy Officer (or, for a Business Associate, the role designated under CMP-005.5.1.5) SHALL maintain a documented list of Workforce Member roles requiring access to PHI, the categories of PHI each role needs, and any conditions on access (45 CFR §164.514(d)(2)). Access SHALL be provisioned under SEC-003 only in line with this list.
- **CMP-005.5.14.3** `[HIPAA]` Routine and recurring disclosures and requests for PHI SHALL follow standard protocols approved by the HIPAA Privacy Officer; non-routine disclosures and requests SHALL be reviewed individually against documented criteria before release (§164.514(d)(3)–(4)).
- **CMP-005.5.14.4** `[HIPAA]` A Limited Data Set or de-identified data SHALL be used in place of PHI wherever it satisfies the purpose.
- **CMP-005.5.14.5** `[HIPAA]` HIPAA Security Rule safeguards for ePHI are set in CMP-008 and are not restated here.

### 5.15 Data Subject rights

- **CMP-005.5.15.1** The Organization SHALL honor the rights of individuals under applicable law, including `[GDPR]` access, rectification, erasure, restriction, portability, objection and rights relating to automated decision-making (Art. 15–22), and `[CPRA]` the rights to know, delete, correct, opt out of sale and sharing, and limit use of Sensitive Personal Information.
- **CMP-005.5.15.2** Data Subject Requests SHALL be received, verified, fulfilled, recorded and closed under CMP-010, within the deadlines set in CMP-010.
- **CMP-005.5.15.3** The Organization SHALL provide at least two methods for submitting Data Subject Requests, including a web form or email address, and `[CPRA]` a toll-free telephone number unless the §1798.130(a)(1)(A) online-only exemption applies.
- **CMP-005.5.15.4** Any Workforce Member who receives a Data Subject Request SHALL forward it to the privacy request channel defined in CMP-010 within 1 business day of receipt.
- **CMP-005.5.15.5** Where the Organization is a Processor, it SHALL forward Data Subject Requests to the relevant Controller and assist the Controller under the Data Processing Agreement, and SHALL NOT respond to the individual on the substance unless instructed by the Controller.

### 5.16 Security of Personal Data and Personal Data Breaches

- **CMP-005.5.16.1** Personal Data SHALL be protected by the controls set in SEC-002 (classification and handling), SEC-003 (access), SEC-006 (Encryption) and SEC-012 (logging), according to its Classification Level.
- **CMP-005.5.16.2** Any Workforce Member who suspects a Personal Data Breach SHALL report it within the time limit in RES-001.5.2.1 through the security reporting channel in RES-001.5.2.2. Internal escalation, assessment and notification of authorities, individuals and Controllers SHALL follow RES-003.
- **CMP-005.5.16.3** The DPO (or CPO) SHALL maintain the `[GDPR]` Art. 33(5) record of all Personal Data Breaches, whether or not notified, using the incident records produced under RES-002.

### 5.17 Training and awareness

- **CMP-005.5.17.1** Privacy content SHALL be included in security awareness training under PPL-002. Workforce Members in roles that process Restricted Personal Data, handle Data Subject Requests, or design systems processing Personal Data SHALL complete role-based privacy training at the frequency set in PPL-002.

### 5.18 Monitoring and assurance

- **CMP-005.5.18.1** The CPO SHALL perform a privacy compliance review of at least 25% of ROPA entries every 12 months, selected by risk, so that every entry is reviewed at least every 48 months, testing lawful basis, notice, minimization, retention enforcement and Processor contracts against this Policy.
- **CMP-005.5.18.2** Findings from privacy compliance reviews SHALL be tracked to closure within the issue remediation timelines set in CMP-002.
- **CMP-005.5.18.3** Privacy obligations, and changes to them, SHALL be recorded and assessed in the Obligations Register under CMP-001.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CPO | Owns this Policy and the privacy program; approves Privacy Notices (with GC), DPIAs, purpose compatibility assessments and sale/sharing determinations; reports privacy metrics to the ISSC quarterly. |
| DPO `[GDPR]` | Advises on and monitors GDPR compliance; reviews DPIAs and Transfer Impact Assessments; approves Legitimate Interests Assessments and anonymization assessments; reviews the ROPA every 12 months; acts as contact point for supervisory authorities and Data Subjects; maintains the Art. 33(5) breach record. Where no DPO is appointed, the CPO performs these tasks. |
| GC | Approves Privacy Notices, Art. 49 derogations, Joint Controller agreements, Art. 10 authorizations and Art. 27 exemptions; sets contractual terms for Processors; concurs on Art. 36 prior consultation. |
| HIPAA Privacy Officer `[HIPAA]` | Maintains minimum-necessary role lists and disclosure protocols; maintains the Notice of Privacy Practices where the Organization is a Covered Entity. |
| CISO | Assesses security measures in DPIAs and Transfer Impact Assessments; ensures SEC-series controls protect Personal Data. |
| Head of GRC | Records privacy obligations in the Obligations Register (CMP-001); manages privacy Evidence under CMP-004. |
| Head of Procurement | Ensures no Processor contract is signed without the agreement terms in sections 5.11–5.12. |
| CTO | Ensures privacy-by-design requirements (section 5.10) are built into SEC-010 lifecycle gates. |
| CHRO | Maintains the Workforce Privacy Notice. |
| Data Owner | Records processing in the ROPA; completes screenings, DPIAs, Legitimate Interests Assessments, compatibility assessments and Transfer Impact Assessments; ensures collection is minimized and retention is enforced. |
| System Owner | Implements deletion, export, correction, suppression and automated retention capabilities (CMP-005.5.10.4–5.10.5). |
| Workforce Member | Processes Personal Data only as authorized; forwards Data Subject Requests within 1 business day; reports suspected Personal Data Breaches immediately. |
| Third Party (Processor) | Processes Personal Data only under documented instructions and the Data Processing Agreement; supports DSRs, DPIAs and audits. |

Role names and accountabilities are established in GOV-001 and consolidated in REF-002.

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| CMP-005.7.1 | Lawful basis recorded in ROPA | Before processing begins, per purpose |
| CMP-005.7.2 | `[GDPR]` Notice for indirectly collected data | Within one month of obtaining, or earlier at first communication or disclosure |
| CMP-005.7.3 | Privacy Notice review | Every 12 months and before any new purpose, data category or recipient category |
| CMP-005.7.4 | Consent withdrawal effective across systems | Within 15 business days of receipt |
| CMP-005.7.5 | ROPA update on change | Before new activity; within 30 days of change to existing activity |
| CMP-005.7.6 | Full ROPA review | Every 12 months |
| CMP-005.7.7 | `[GDPR]` ROPA production to Supervisory Authority | Within 5 business days of request |
| CMP-005.7.8 | DPIA timing | Completed and approved before processing begins |
| CMP-005.7.9 | DPIA review | Every 24 months and before triggering change |
| CMP-005.7.10 | `[GDPR]` Transfer Impact Assessment | Before transfer; reviewed every 24 months and within 30 days of a relevant legal or processing change |
| CMP-005.7.11 | `[GDPR]` Suspension of transfer that fails TIA | Within 30 days of conclusion |
| CMP-005.7.12 | `[CPRA]` Opt-out of sale/sharing honored | Per CMP-010.7.4 |
| CMP-005.7.13 | `[CPRA]` Limit-use-of-SPI request honored | Per CMP-010.7.4 |
| CMP-005.7.14 | `[CPRA]` Wait before re-requesting opt-in after opt-out | At least 12 months |
| CMP-005.7.15 | Processor return/deletion certification at contract end | Within 30 days of termination |
| CMP-005.7.16 | Forwarding of a DSR received by a Workforce Member | Within 1 business day |
| CMP-005.7.17 | DSR response deadlines | Per CMP-010 |
| CMP-005.7.18 | Personal Data retention and deletion after purpose ends | Per CMP-004 |
| CMP-005.7.19 | Breach escalation and notification | Per RES-003 |
| CMP-005.7.20 | Processor reassessment frequency | Per RSK-003, by vendor tier |
| CMP-005.7.21 | Privacy compliance review coverage | ≥ 25% of ROPA entries every 12 months; every entry at least every 48 months |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| ROPA entries with lawful basis, retention reference and Data Owner recorded | 100% | Quarterly | DPO |
| ROPA entries reviewed within the last 12 months | 100% | Quarterly | DPO |
| New processing activities launched with a completed TPL-005 screening (and DPIA where triggered) before go-live | 100% | Quarterly | CPO |
| DPIAs past their 24-month review date | 0 | Quarterly | DPO |
| `[GDPR]` Restricted transfers with executed SCCs (or other Chapter V mechanism) and a current Transfer Impact Assessment | 100% | Quarterly | DPO |
| Processors processing Personal Data with an executed Data Processing Agreement (and BAA where PHI is involved) | 100% | Quarterly | Head of Procurement |
| `[CPRA]` Opt-out and limit-use requests honored within the CMP-010.7.4 deadline | 100% | Monthly | CPO |
| Consent withdrawals effective within 15 business days | 100% | Monthly | CPO |
| External Privacy Notices reviewed within 12 months | 100% | Quarterly | CPO |
| Privacy compliance review findings closed within CMP-002 timelines | ≥ 95% | Quarterly | CPO |
| Systems holding Personal Data with automated retention enforcement | 100% of systems placed in production after the effective date; ≥ 90% of all systems | Quarterly | CPO |

Metrics are reported to the ISSC under the cadence in GOV-003.

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following requirements SHALL NOT receive an Exception, because they implement legal
obligations: the requirement for a lawful basis (5.3.1, 5.3.3, 5.3.5); Art. 28 and BAA
contract terms (5.11.2, 5.11.5); the Chapter V transfer mechanism requirement (5.12.1); the
`[CPRA]` opt-out, Opt-out Preference Signal and limit-use requirements (5.13.2–5.13.4,
5.13.6); and the `[HIPAA]` Minimum Necessary standard (5.14.1). Every Exception request
under this Policy SHALL be reviewed by the CPO and the GC before approval.

## 10. Enforcement

Non-compliance is handled under CMP-007.

Unauthorized disclosure, sale or use of Personal Data for a purpose not recorded in the ROPA
SHALL also be handled as a Security Incident under RES-001. Breaches of privacy terms by a
Processor SHALL be handled under the contractual remedies in RSK-003 and CMP-007.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| CMP-005.5.1 Governance | 5.3; A.5.2, A.5.34 | GV.RR-02, GV.OC-03 | PM-19, PT-1 | — | CC1.3, P1.1 | APO01, APO14 | GDPR Art. 24, 27, 37–39; 45 CFR §164.530(a) |
| CMP-005.5.2 Principles | A.5.34 | GV.PO-01 | PT-2, PT-3 | 3.1 | P1.1 | APO14 | GDPR Art. 5; Cal. Civ. Code §1798.100 |
| CMP-005.5.3 Lawful basis | A.5.31, A.5.34 | GV.OC-03 | PT-2 | — | P3.1 | MEA03 | GDPR Art. 6, 9, 10; 45 CFR §164.502(a) |
| CMP-005.5.4 Notices | A.5.34 | GV.OC-03 | PT-5 | — | P1.1 | MEA03 | GDPR Art. 12–14; Cal. Civ. Code §1798.100(a), §1798.130; 45 CFR §164.520 |
| CMP-005.5.5 Consent | A.5.34 | GV.OC-03 | PT-4 | — | P2.1 | MEA03 | GDPR Art. 7, 8; Cal. Civ. Code §1798.120(c) |
| CMP-005.5.6 Purpose limitation | A.5.34 | GV.PO-01 | PT-3 | 3.1 | P4.1 | APO14 | GDPR Art. 5(1)(b), 6(4); Cal. Civ. Code §1798.100(c) |
| CMP-005.5.7 Minimization & de-identification | A.5.34, A.8.11, A.8.33 | PR.DS-01 | PT-3, SI-12, SA-3 | 3.1, 16.8 | P3.1, C1.1 | APO14 | GDPR Art. 5(1)(c), 25, 32; 45 CFR §164.514(b) |
| CMP-005.5.8 ROPA | A.5.9, A.5.34 | ID.AM-07 | PM-5, PT-3 | 3.2 | P3.1 | APO14 | GDPR Art. 30 |
| CMP-005.5.9 DPIA | 6.1.2; A.5.34 | ID.RA-01, GV.RM-01 | RA-3, RA-8 | — | CC3.2, P3.1 | APO12 | GDPR Art. 35, 36 |
| CMP-005.5.10 Privacy by design | A.5.8, A.8.25, A.8.10 | PR.PS-01 | SA-8, SA-3, AC-6 | 3.1 | CC8.1, P4.2 | BAI02, BAI03 | GDPR Art. 22, 25 |
| CMP-005.5.11 Processors | A.5.19, A.5.20, A.5.34 | GV.SC-01, GV.SC-05 | SA-9, SR-6 | 15.1, 15.4 | CC9.2, P6.1 | APO10 | GDPR Art. 26, 28; Cal. Civ. Code §1798.100(d); 45 CFR §164.504(e) |
| CMP-005.5.12 International transfers | A.5.14, A.5.34 | GV.OC-03 | SA-9 | — | P6.1 | MEA03 | GDPR Art. 44–49 |
| CMP-005.5.13 CPRA sale/sharing & SPI | A.5.34 | GV.OC-03 | PT-2, PT-4 | — | P2.1, P6.1 | MEA03 | Cal. Civ. Code §1798.120, §1798.121, §1798.125, §1798.135; Cal. Code Regs. tit. 11, §7025–7027 |
| CMP-005.5.14 Minimum Necessary | A.5.15, A.5.34 | PR.AA-05 | AC-6, PT-2 | 6.8 | CC6.3 | DSS05 | 45 CFR §164.502(b), §164.514(d) |
| CMP-005.5.15 Data Subject rights | A.5.34 | GV.OC-03 | PM-22, PT-2 | — | P5.1, P5.2 | MEA03 | GDPR Art. 12, 15–22; Cal. Civ. Code §1798.105–.130 |
| CMP-005.5.16 Security & breaches | A.5.24, A.5.34 | RS.CO-02 | IR-4, IR-6 | 17.1 | CC7.3, P6.3 | DSS02 | GDPR Art. 32–34 (see RES-003) |
| CMP-005.5.17 – 5.18 Training & assurance | 7.2, 9.2; A.6.3 | PR.AT-01, ID.IM-01 | AT-2, AT-3, CA-2 | 14.1 | CC1.4, CC4.1 | MEA03 | GDPR Art. 39(1)(b); 45 CFR §164.530(b) |

## 12. Related documents

ISP-000, GOV-001, GOV-002, GOV-003, GOV-006, CMP-001, CMP-002, CMP-003, CMP-004, CMP-007,
CMP-008, CMP-010, RSK-001, RSK-002, RSK-003, RSK-006, SEC-001, SEC-002, SEC-003, SEC-006,
SEC-010, SEC-012, SEC-013, SEC-017, RES-001, RES-002, RES-003, PPL-002, TPL-004, TPL-005,
TPL-010, REF-001, REF-002

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CPO | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
