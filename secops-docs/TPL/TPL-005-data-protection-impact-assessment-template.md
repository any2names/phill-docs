# TPL-005 — Data Protection Impact Assessment Template

## 1. Document control

| Field | Value |
|---|---|
| Document ID | TPL-005 |
| Title | Data Protection Impact Assessment Template |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | T — Template |
| Classification | Internal (blank template); a completed DPIA is Confidential |
| Owner | Data Protection Officer (DPO) |
| Approver | Chief Privacy Officer (CPO) |
| Effective date | [DECISION REQUIRED: Date of CPO approval] |
| Next review date | Effective date + 12 months, and on the event-triggered reviews in GOV-002.7.4 |
| Parent document | CMP-005 Data Privacy & Protection Policy |
| Related documents | CMP-004, CMP-005, CMP-010, RSK-001, RSK-002, RSK-003, RSK-006, SEC-002, TPL-001, TPL-002, TPL-010 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | DPO | Initial release |

## 3. Purpose

This Template records a Data Protection Impact Assessment (DPIA) containing every element
required by GDPR Article 35(7), the advice of the DPO required by Article 35(2), the views of
Data Subjects sought under Article 35(9), and the prior consultation decision required by
Article 36. It also records the screening decision for processing that does not need a full
DPIA, so the Organization can show why no DPIA was performed.

**Conditional module.** This Template applies only where the Organization processes Personal
Data of EU/EEA residents `[GDPR]` or California consumers `[CPRA]` (README "Conditional
modules").

## 4. Instructions

| Item | Instruction |
|---|---|
| Who completes it | The Data Owner (or the project owner, where the processing is new) completes Parts A to F, with input from the System Owner and the CISO's delegate for security measures. The DPO completes Part G. The CPO records the decision in Part H. |
| When | Part A (screening) at project initiation for every new processing activity, and for every change to an existing one that the ROPA (TPL-010) records as a change of purpose, data category, recipient, transfer or technology. Parts B to H before the processing starts, where Part A concludes a DPIA is required. Re-assessment on the triggers set in CMP-005. |
| Prerequisite | A draft ROPA entry (TPL-010) for the processing activity. The DPIA reference is recorded in that ROPA entry. |
| Risk scoring | Use the likelihood × impact method and levels in RSK-002.7.1 and RSK-002.7.2. In Part E, "impact" is assessed as the severity of the consequences **for Data Subjects**, not for the Organization. |
| High residual risk | A residual risk at High or Critical level under RSK-002 is treated as "high risk" for Article 36. Processing SHALL NOT start until Part H is completed and, where required, prior consultation has concluded. |
| Risks for the Organization | Each risk with a residual level of Medium or higher is also entered in the Risk Register (TPL-001). Any residual risk accepted is accepted under RSK-001 using TPL-002. |
| AI systems | Where the processing involves an AI System, also complete the AI Impact Assessment required by RSK-006.5.3.3 and cross-reference it in Part B. |
| Where it is stored | The privacy compliance repository controlled by the DPO, with access restricted under SEC-003. A completed DPIA is Confidential (SEC-002). |
| Retention | For the period set in CMP-004 row R-18 (privacy accountability records). |
| Instructions for completion | Answer every field. Write "N/A" with a reason where a field does not apply. Tick ☐ boxes by replacing them with ☒. Attach diagrams and supporting documents and list them in Part I. |

## 5. Form

### Part A — Screening

**A.1 Identification**

| Field | Value |
|---|---|
| DPIA reference |  |
| Processing activity name |  |
| ROPA entry reference (TPL-010) |  |
| Business unit |  |
| Data Owner |  |
| Project owner (if different) |  |
| Date screening completed |  |

**A.2 Mandatory DPIA cases (GDPR Art. 35(3)). If any box is ticked, a DPIA is required.**

| # | Case | Yes |
|---|---|---|
| A.2.1 | Systematic and extensive evaluation of personal aspects based on automated processing, including profiling, on which decisions with legal or similarly significant effects are based | ☐ |
| A.2.2 | Processing on a large scale of special categories of data (Art. 9(1)) or of data relating to criminal convictions and offences (Art. 10) | ☐ |
| A.2.3 | Systematic monitoring of a publicly accessible area on a large scale | ☐ |
| A.2.4 | Processing type appears on the published DPIA list of a competent Supervisory Authority (Art. 35(4)). List and item: ____ | ☐ |

**A.3 High-risk criteria (EDPB-endorsed WP29 Guidelines WP248 rev.01). If two or more boxes are ticked, a DPIA is required unless the DPO records in A.4 why high risk is unlikely.**

| # | Criterion | Yes |
|---|---|---|
| A.3.1 | Evaluation or scoring, including profiling and predicting | ☐ |
| A.3.2 | Automated decision-making with legal or similarly significant effect | ☐ |
| A.3.3 | Systematic monitoring | ☐ |
| A.3.4 | Sensitive data or data of a highly personal nature (including Sensitive Personal Information, financial data, location data) | ☐ |
| A.3.5 | Data processed on a large scale | ☐ |
| A.3.6 | Matching or combining datasets | ☐ |
| A.3.7 | Data concerning vulnerable Data Subjects (e.g. children, employees, patients) | ☐ |
| A.3.8 | Innovative use or application of new technological or organizational solutions (including AI Systems) | ☐ |
| A.3.9 | Processing that prevents Data Subjects from exercising a right or using a service or contract | ☐ |

**A.4 Screening outcome**

| Field | Value |
|---|---|
| Number of A.2 boxes ticked |  |
| Number of A.3 boxes ticked |  |
| Outcome | ☐ Full DPIA required (complete Parts B–I) ☐ DPIA not required (complete A.4 rationale and Part H sign-off only) ☐ DPIA performed voluntarily |
| Rationale (mandatory where a DPIA is not required despite one A.3 criterion, or two or more A.3 criteria) |  |
| `[CPRA]` Processing presents "significant risk" to consumers' privacy under Cal. Code Regs. tit. 11, §7150 (e.g. selling or sharing Personal Information, processing Sensitive Personal Information, using automated decision-making technology for a significant decision) | ☐ Yes (complete Part J) ☐ No |
| DPO screening review: name and date |  |

### Part B — Systematic description of the processing (Art. 35(7)(a))

**B.1 Parties**

| Field | Value |
|---|---|
| Controller (legal entity) and contact |  |
| Joint Controllers and arrangement reference (Art. 26) |  |
| Processors and Subprocessors (name, service, location, DPA reference under RSK-003) |  |
| DPO contact |  |
| EU representative (Art. 27), if applicable |  |

**B.2 Purposes**

| Field | Value |
|---|---|
| Purpose(s) of the processing |  |
| Legitimate interest pursued, where Art. 6(1)(f) is the lawful basis |  |
| Expected benefits for the Organization, Data Subjects and society |  |

**B.3 Nature of the processing**

| Field | Value |
|---|---|
| How data is collected (directly, observed, derived, from third parties) and sources |  |
| Operations performed (collection, recording, storage, use, combination, disclosure, deletion) |  |
| Automated decision-making or profiling involved, and its logic |  |
| Information Systems and Cloud Services used (with Asset Inventory IDs) |  |
| New technologies or AI Systems used (RSK-006 assessment reference) |  |
| Data flow diagram attached (reference in Part I) | ☐ Yes |

**B.4 Scope of the processing**

| Field | Value |
|---|---|
| Categories of Data Subjects |  |
| Categories of Personal Data |  |
| Special categories (Art. 9) or criminal offence data (Art. 10) |  |
| Number of Data Subjects (estimate) |  |
| Volume of records (estimate) |  |
| Frequency and duration of processing |  |
| Geographic scope of Data Subjects and processing locations |  |
| Retention period (from TPL-010 and CMP-004) and deletion method |  |
| Recipients and categories of recipients |  |
| Transfers to third countries and transfer mechanism (CMP-005) |  |

**B.5 Context of the processing**

| Field | Value |
|---|---|
| Relationship with Data Subjects (customer, employee, patient, child, other) |  |
| Degree of control Data Subjects have over their data |  |
| Whether Data Subjects would expect this processing |  |
| Vulnerable groups involved |  |
| Prior concerns, complaints, incidents or public concern about this type of processing |  |
| Approved codes of conduct or certifications relied on (Art. 35(8)) |  |

### Part C — Consultation

| Stakeholder | Consulted? | Date | Summary of views | How views were addressed |
|---|---|---|---|---|
| Data Subjects or their representatives (Art. 35(9)), or reason why not consulted | ☐ |  |  |  |
| CISO or delegate (security measures) | ☐ |  |  |  |
| System Owner(s) | ☐ |  |  |  |
| Processors (Art. 28(3)(f)) | ☐ |  |  |  |
| GC (lawful basis, transfers) | ☐ |  |  |  |
| Works council or employee representatives (where required by local law) | ☐ |  |  |  |
| Other: | ☐ |  |  |  |

### Part D — Necessity and proportionality (Art. 35(7)(b))

| # | Question | Answer and evidence |
|---|---|---|
| D.1 | Lawful basis under Art. 6(1), for each purpose |  |
| D.2 | Condition under Art. 9(2) for special categories, or authority under Art. 10 |  |
| D.3 | Where consent is relied on: how it is obtained, recorded and withdrawn (Art. 7) |  |
| D.4 | Why the processing is necessary to achieve each purpose |  |
| D.5 | Less intrusive alternatives considered and why they were rejected |  |
| D.6 | Data minimisation: why each data category is needed; categories removed |  |
| D.7 | Purpose limitation: controls preventing use for incompatible purposes |  |
| D.8 | Accuracy: how data is kept accurate and up to date |  |
| D.9 | Storage limitation: retention period justification and deletion mechanism |  |
| D.10 | Transparency: Privacy Notice reference and how information under Arts. 13–14 is provided |  |
| D.11 | Data Subject rights: how each right is supported under CMP-010, including any limitations |  |
| D.12 | Processors: Art. 28 contract terms in place (RSK-003) |  |
| D.13 | Transfers: Chapter V mechanism and Transfer Impact Assessment reference (CMP-005) |  |
| D.14 | Conclusion: is the processing necessary and proportionate? | ☐ Yes ☐ Yes, with changes listed in Part F ☐ No (processing SHALL NOT proceed) |

### Part E — Risks to the rights and freedoms of Data Subjects (Art. 35(7)(c))

Assess inherent risk before the new measures in Part F, considering illegitimate access,
unwanted modification and loss of Personal Data, and harms such as discrimination, identity theft
or fraud, financial loss, reputational damage, loss of confidentiality of data protected by
professional secrecy, physical harm, loss of control over Personal Data, and inability to exercise
rights.

| Risk ID | Risk description (source, event, harm to Data Subjects) | Rights and freedoms affected | Likelihood (1–5, RSK-002) | Impact on Data Subjects (1–5, RSK-002) | Inherent score | Inherent level (RSK-002) |
|---|---|---|---|---|---|---|
| R1 |  |  |  |  |  |  |
| R2 |  |  |  |  |  |  |
| R3 |  |  |  |  |  |  |
| R4 |  |  |  |  |  |  |
| R5 |  |  |  |  |  |  |

### Part F — Measures to address the risks (Art. 35(7)(d))

Record safeguards, security measures and mechanisms to protect Personal Data and demonstrate
compliance. Cite the suite document that sets each control rather than restating it.

| Measure ID | Measure | Risk ID(s) addressed | Home document / control | Owner | Due date | Status (☐ Planned ☐ Implemented ☐ Verified) | Residual likelihood | Residual impact | Residual score | Residual level |
|---|---|---|---|---|---|---|---|---|---|---|
| M1 |  |  |  |  |  | ☐ ☐ ☐ |  |  |  |  |
| M2 |  |  |  |  |  | ☐ ☐ ☐ |  |  |  |  |
| M3 |  |  |  |  |  | ☐ ☐ ☐ |  |  |  |  |
| M4 |  |  |  |  |  | ☐ ☐ ☐ |  |  |  |  |
| M5 |  |  |  |  |  | ☐ ☐ ☐ |  |  |  |  |

| Field | Value |
|---|---|
| Highest residual risk level after measures |  |
| Risk Register (TPL-001) references for residual risks at Medium or above |  |
| Risk Acceptance (TPL-002) references, where any residual risk is accepted |  |

### Part G — DPO advice (Art. 35(2))

| Field | Value |
|---|---|
| DPO advice on: whether to carry out the processing; the measures; whether prior consultation is required |  |
| Is the DPIA complete and compliant with Art. 35(7)? | ☐ Yes ☐ No (list gaps): |
| DPO recommendation | ☐ Proceed ☐ Proceed after measures in Part F are verified ☐ Prior consultation required (Art. 36) ☐ Do not proceed |
| Was the DPO advice followed? (completed by the CPO) | ☐ Yes ☐ No |
| If not followed, reasons (mandatory) |  |
| DPO name, signature and date |  |

### Part H — Outcome and prior consultation (Art. 36)

**H.1 Decision**

| Field | Value |
|---|---|
| Residual high risk remains (residual level High or Critical under RSK-002)? | ☐ Yes ☐ No |
| Decision | ☐ Approved to proceed ☐ Approved subject to conditions ☐ Prior consultation required before processing ☐ Rejected |
| Conditions |  |
| Decision maker (CPO; risk acceptance authority under RSK-001 where any residual risk is accepted) |  |
| Date |  |

**H.2 Prior consultation with the Supervisory Authority (complete only where residual high risk remains)**

| Field | Value |
|---|---|
| Lead or competent Supervisory Authority |  |
| Date submitted |  |
| Information provided (Art. 36(3)) | ☐ (a) responsibilities of the Controller, Joint Controllers and Processors ☐ (b) purposes and means of the processing ☐ (c) measures and safeguards ☐ (d) DPO contact details ☐ (e) this DPIA ☐ (f) other information requested |
| Authority acknowledgement date |  |
| Written advice due date (8 weeks from receipt, or 14 weeks where extended under Art. 36(2)) |  |
| Extension notified by the authority? | ☐ Yes ☐ No |
| Advice received date and summary |  |
| Actions taken in response |  |
| Processing start authorized by CPO (date) |  |

**H.3 Review**

| Field | Value |
|---|---|
| Next review trigger or date (per CMP-005.5.9.6) |  |
| ROPA (TPL-010) entry updated with DPIA reference | ☐ Yes |

### Part I — Attachments

| # | Document | Reference / location |
|---|---|---|
| I.1 | Data flow diagram |  |
| I.2 | ROPA entry (TPL-010) |  |
| I.3 | Privacy Notice text |  |
| I.4 | Transfer Impact Assessment |  |
| I.5 | Processor due diligence (RSK-003) |  |
| I.6 | AI System assessment (RSK-006) |  |
| I.7 | Other |  |

### Part J — `[CPRA]` California risk assessment supplement

[ASSUMPTION: The California Privacy Protection Agency's risk assessment regulations (Cal. Code
Regs. tit. 11, §7150 et seq.) are in force for the Organization. The GC SHALL confirm the
applicable content requirements and submission deadlines and record them in the Obligations
Register (CMP-001). Remove this Part if they do not apply.]

| Field | Value |
|---|---|
| Specific purpose of the processing (not described in generic terms) |  |
| Categories of Personal Information, including Sensitive Personal Information, and the Minimum Necessary for the purpose |  |
| Operational elements: method of collection, retention, number of consumers, disclosures, technology used |  |
| Benefits to the Organization, consumers, other stakeholders and the public |  |
| Negative impacts to consumers' privacy |  |
| Safeguards planned to address the negative impacts (cross-reference Part F) |  |
| Whether the Organization will initiate the processing (decision) |  |
| Individuals who provided information for the assessment (by role) |  |
| Individuals who reviewed and approved the assessment (by role), and date |  |

## 6. Approval signatures

### 6.1 Completed assessment

| Role | Name | Signature | Date |
|---|---|---|---|
| Assessor (Data Owner or project owner) | | | |
| System Owner | | | |
| CISO or delegate (security measures) | | | |
| DPO (advice, Part G) | | | |
| CPO (decision, Part H) | | | |

### 6.2 Template approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Data Protection Officer (DPO) | | | |
| Approver: Chief Privacy Officer (CPO) | | | |
