# RSK-006 — AI & Emerging Technology Risk Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | RSK-006 |
| Title | AI & Emerging Technology Risk Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Information Security Officer (CISO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | RSK-001 Risk Management Policy |
| Related documents | RSK-002, RSK-003, RSK-005, SEC-001, SEC-002, SEC-010, CMP-001, CMP-005, GOV-004, PPL-002, RES-002, TPL-005 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CISO | Initial release |

## 3. Purpose

This Policy sets the Organization's requirements for governing the Risk of developing,
procuring, deploying and using AI Systems, including Generative AI, and other emerging
technologies. It is aligned to ISO/IEC 42001:2023 (AI management system) and the NIST AI
Risk Management Framework 1.0 functions — Govern, Map, Measure and Manage — and to the EU AI
Act where it applies. It ensures that each AI System is inventoried, classified by Risk,
assessed before use, subject to human oversight proportionate to its Risk, evaluated for
bias, robustness and security, and used only with data its approval permits.

## 4. Scope

- **AI Systems:** every AI System developed, fine-tuned, procured, deployed or used by or for the Organization, including Generative AI tools, AI features embedded in Cloud Services and other software, AI agents that can take actions, and models accessed through APIs.
- **Emerging Technology:** other technologies designated by the ISSC as Emerging Technology under section 5.10.
- **People:** all Workforce Members who use, build, buy or oversee AI Systems.
- **Data:** all data used to train, fine-tune, ground, prompt or evaluate an AI System, and all AI outputs, at every Classification Level.
- **Locations:** all locations, including remote work.
- **Third parties:** Third Parties that provide AI Systems or AI-enabled services, and Third Parties that use AI Systems to process Organization data.
- **Out of scope:** conventional statistical analysis and deterministic rules-based automation that do not infer outputs from inputs.

## 5. Policy statements

### 5.1 Govern: accountability and AI management system

- **RSK-006.5.1.1** The ISSC SHALL act as the Organization's AI governance body. It SHALL approve this Policy, the approved AI tools list (section 5.4), every AI System classified High (section 5.3), and any AI use case proposed as an exception to section 5.3.2.
- **RSK-006.5.1.2** The CISO SHALL be accountable for the Organization's AI management system and SHALL maintain the processes in this Policy. The CPO SHALL be consulted on every AI System that processes Personal Data, and the GC on every AI System classified High or subject to the EU AI Act.
- **RSK-006.5.1.3** Each AI System SHALL have a named System Owner accountable for its use, performance and compliance with this Policy, and a Data Owner for each data set used to train, fine-tune or ground it.
- **RSK-006.5.1.4** The CISO SHALL establish and communicate AI objectives and the Organization's position on responsible AI (covering fairness, transparency, accountability, privacy, safety and security), approved by the ISSC, at least every 12 months.
- **RSK-006.5.1.5** AI Risk SHALL be managed within the risk process in RSK-001 under category C7, scored using RSK-002, and recorded in the Risk Register.
- **RSK-006.5.1.6** Workforce Members who use AI Systems SHALL complete AI literacy training, and Workforce Members who build, procure or oversee AI Systems SHALL complete role-based AI training, delivered under PPL-002 (PPL-002.5.2.2 and PPL-002.5.4.4) before first use or role assignment and every 12 months thereafter.
- **RSK-006.5.1.7** Acceptable and prohibited behaviors for individual use of AI tools are set in GOV-004; this Policy sets the approval, data and Control requirements those behaviors rely on.

### 5.2 Map: AI System inventory

- **RSK-006.5.2.1** The CISO SHALL maintain an AI System inventory as part of, or linked to, the Asset Inventory (SEC-001). No AI System SHALL be used for Organization business until it is recorded in the inventory.
- **RSK-006.5.2.2** The inventory SHALL record for each AI System: name and version; System Owner; provider (internal or Third Party, with vendor tier under RSK-003); model type and foundation model where known; intended purpose and use case(s); users and affected persons; AI Risk Class (section 5.3); highest Classification Level of data permitted (section 5.5); whether Personal Data is used for training, grounding or prompts; Human Oversight Mode (section 5.6); deployment location and data residency; whether the system can take autonomous actions; evaluation dates (section 5.8); `[GDPR]` lawful basis and DPIA reference; and EU AI Act role and category where applicable (section 5.9).
- **RSK-006.5.2.3** System Owners SHALL update the inventory within 10 business days of a change in purpose, model, provider, data, user population or autonomy.
- **RSK-006.5.2.4** The CISO SHALL reconcile the inventory against network, Cloud Service, expense and software-discovery data at least quarterly to identify unapproved AI use. Unapproved AI Systems found SHALL be blocked or submitted for approval within 10 business days and reported as Shadow IT.
- **RSK-006.5.2.5** AI features newly enabled by a supplier in an already-approved Cloud Service or application SHALL be treated as a new AI System and SHALL remain disabled until approved under this Policy, where the service allows them to be disabled.

### 5.3 Map: risk classification of AI use cases

- **RSK-006.5.3.1** Each AI use case SHALL be classified by the System Owner, and confirmed by the CISO, into one of the following AI risk classes before approval:

| AI Risk Class | Criteria (any one) | Approval |
|---|---|---|
| Prohibited | Practices listed in section 5.3.2 | Not permitted |
| High | Makes or materially influences decisions with legal or similarly significant effects on individuals (for example employment, credit, insurance, access to healthcare or essential services); processes Restricted data; is a safety component; operates autonomously with the ability to change production systems, execute financial transactions or communicate externally without human review; falls within an EU AI Act high-risk category (Annex III) or is a safety component under Annex I | ISSC |
| Limited | Interacts directly with customers or the public; generates content published externally; processes Confidential data or Personal Data not classified Restricted; produces code deployed to production | CISO, with CPO where Personal Data is processed |
| Minimal | Internal productivity use on Public or Internal data, with all outputs reviewed by the user before use | System Owner, using an approved AI tool from section 5.4 |

- **RSK-006.5.3.2** The following uses SHALL NOT be developed, procured or deployed: social scoring of individuals; manipulation of individuals through subliminal or deceptive techniques causing harm; exploitation of vulnerabilities of individuals due to age, disability or social or economic situation; emotion recognition of Workforce Members in the workplace, except for medical or safety reasons; biometric categorization to infer race, political opinions, trade union membership, religious or philosophical beliefs, sex life or sexual orientation; untargeted scraping of facial images to build facial recognition databases; predicting an individual's likelihood of committing a criminal offence based solely on profiling; and real-time remote biometric identification in publicly accessible spaces.
- **RSK-006.5.3.3** Each AI System SHALL be assessed using an AI Impact Assessment covering intended purpose, affected persons and groups, potential harms (to individuals, groups, the Organization and society), likelihood and severity under RSK-002, and mitigating Controls. The impact assessment SHALL be completed before approval for High and Limited classes and SHALL be reviewed at least every 12 months for High class.
- **RSK-006.5.3.4** `[GDPR]` `[CPRA]` Where an AI System processes Personal Data in a manner likely to result in high risk, including any High-class AI System that processes Personal Data, a DPIA SHALL be completed using TPL-005 under CMP-005 before processing begins. The AI Impact Assessment and DPIA MAY be combined in one record.
- **RSK-006.5.3.5** An AI System's risk class SHALL be re-confirmed by the CISO whenever its purpose, autonomy, data or user population changes.

### 5.4 Approved Generative AI tools

- **RSK-006.5.4.1** The CISO SHALL maintain and publish to all Workforce Members an approved AI tools list stating, for each tool: the approved version or service tier; the maximum Classification Level of data that may be input; permitted use cases; and any conditions (for example "Enterprise tenant only, signed in with Organization SSO").
- **RSK-006.5.4.2** A Generative AI tool SHALL be added to the approved list only after: assessment of the provider under RSK-003 and section 5.7; contractual commitments that Organization inputs and outputs are not used to train or improve the provider's models, are retained for no longer than 30 days unless the Organization configures otherwise, and are processed only in approved locations; enforcement of Organization SSO and MFA per SEC-004; availability of audit logs of use to the Organization; and ISSC approval.
- **RSK-006.5.4.3** Individual use of tools on the approved list, including the prohibition on personal accounts and consumer versions, is governed by GOV-004.5.8.1 to GOV-004.5.8.3.
- **RSK-006.5.4.4** The approved list SHALL be reviewed by the CISO at least every 6 months and within 10 business days of a material change to a listed provider's terms, ownership or security posture.
- **RSK-006.5.4.5** The Head of Security Engineering SHALL implement technical Controls to block access to known Generative AI services that are not on the approved list from Organization-managed Endpoints and networks, and SHALL apply Data Loss Prevention Controls to approved services where technically supported.

### 5.5 Data input restrictions by Classification Level

- **RSK-006.5.5.1** Data SHALL be input to, or used to train, fine-tune or ground, an AI System only within the limits below. Classification Levels and their handling rules are set in SEC-002.

| Classification Level (SEC-002) | Minimal-class approved tool | AI System approved at Limited class | AI System approved at High class |
|---|---|---|---|
| Public | Permitted | Permitted | Permitted |
| Internal | Permitted | Permitted | Permitted |
| Confidential | Not permitted | Permitted where the AI System's inventory entry states Confidential as its maximum level | Permitted where stated in the inventory entry |
| Restricted | Not permitted | Not permitted | Permitted only where the inventory entry states Restricted, the ISSC has approved the specific data types, and the conditions in 5.5.2 are met |

- **RSK-006.5.5.2** Restricted data SHALL be used with an AI System only where: the AI System is hosted within the Organization's environment or a vendor Tier 1 Third Party assessed under RSK-003; the data is encrypted per SEC-006; `[HIPAA]` a BAA covering the AI service is in place before any PHI is input; `[PCI]` no CHD or SAD is input unless the AI System is within the CDE scope defined in SEC-019; `[GDPR]` a completed DPIA supports the processing; and Secrets are never input.
- **RSK-006.5.5.3** Personal Data SHALL be used to train, fine-tune or evaluate a model only as permitted by CMP-005.5.6.3.
- **RSK-006.5.5.4** Outputs of an AI System SHALL be classified at the highest Classification Level of the data input to produce them, unless the Data Owner reclassifies them under SEC-002.
- **RSK-006.5.5.5** AI Systems that retrieve data on a user's behalf (for example retrieval-augmented generation or agents) SHALL enforce the requesting User's access rights at retrieval time, so that no User obtains through the AI System data they are not authorized to access under SEC-003.

### 5.6 Human oversight

- **RSK-006.5.6.1** Each AI System SHALL be assigned one of the following oversight modes, recorded in the inventory:

| Oversight mode | Description | Required for |
|---|---|---|
| Human-in-the-loop | A trained human reviews and approves each output before it takes effect | All High-class decisions with legal or similarly significant effects on individuals; autonomous actions that change production systems, move funds or communicate externally |
| Human-on-the-loop | A human monitors operation in real time or near real time and can intervene or stop the system | Other High-class AI Systems; Limited-class AI Systems that interact with customers |
| Human-in-command | A human sets the use and reviews outputs before reliance | Limited and Minimal class |

- **RSK-006.5.6.2** Each human reviewer for a High-class AI System SHALL be trained on the system's capabilities, limitations and known failure modes, and SHALL have the authority to override or reject outputs. Reviewers' decisions SHALL be logged.
- **RSK-006.5.6.3** Each High-class AI System and each AI System able to take autonomous actions SHALL have a documented means to halt it, tested at least every 12 months.
- **RSK-006.5.6.4** `[GDPR]` Decisions based solely on automated processing that produce legal or similarly significant effects on a Data Subject SHALL NOT be made except as permitted by GDPR Art. 22(2), with the safeguards of Art. 22(3), including the right to obtain human intervention, as confirmed by the CPO.
- **RSK-006.5.6.5** `[CPRA]` The CPO SHALL determine, and record in the inventory, whether each AI System constitutes automated decision-making technology subject to regulations under Cal. Civ. Code §1798.185, and SHALL implement the required notices and opt-out or access rights.
- **RSK-006.5.6.6** Users of an AI System SHALL be informed that they are interacting with an AI System, and content generated by AI and published externally SHALL be labelled as AI-generated, unless it is obvious from context or the content has been substantially edited by a human who takes responsibility for it.
- **RSK-006.5.6.7** Workforce Members SHALL review AI outputs for accuracy before relying on them and remain accountable for work products that incorporate AI outputs. AI-generated code SHALL be subject to the same review and testing as human-written code under SEC-010.

### 5.7 Model and vendor assessment

- **RSK-006.5.7.1** Third Parties providing AI Systems SHALL be tiered and assessed under RSK-003, and SHALL also complete the AI module of TPL-004.
- **RSK-006.5.7.2** The AI-specific assessment SHALL cover at minimum: training data provenance and licensing; whether customer data is used for training; data retention and deletion; model documentation (for example a model card or system card) describing intended use, limitations and evaluation results; security testing including adversarial and prompt-injection testing; bias and fairness testing; incident notification and model change notification commitments; Subprocessors, including foundation model providers; data location; and, where applicable, the provider's EU AI Act conformity status.
- **RSK-006.5.7.3** Contracts for AI Systems classified High or Limited SHALL include, in addition to the clauses in RSK-003: a prohibition on training on Organization data without written consent; notification at least 30 days before material model changes; notification of AI-related Security Incidents within the timeframe RSK-003 sets for the vendor's tier; cooperation with the Organization's evaluations and regulatory obligations; and intellectual property indemnity for outputs where commercially available.
- **RSK-006.5.7.4** Internally developed or fine-tuned models SHALL be developed under SEC-010, with model artifacts, training data sets and evaluation results version-controlled, and with training data sets recorded with their source, Classification Level and Data Owner.
- **RSK-006.5.7.5** Open-weight and third-party models downloaded for internal use SHALL be obtained from sources approved under SEC-010.5.9.8, verified for integrity, and scanned for embedded malicious code before use.

### 5.8 Measure and Manage: evaluation, monitoring and incidents

- **RSK-006.5.8.1** Before production deployment, and at least every 12 months thereafter, each High-class AI System SHALL be evaluated for: accuracy and performance against documented acceptance criteria; bias and fairness across relevant demographic groups, using documented metrics and thresholds approved by the CPO; robustness to input variation, distribution shift and adversarial inputs; security, including prompt injection, data leakage, model extraction, training data poisoning and insecure output handling; and privacy, including memorization or disclosure of Personal Data.
- **RSK-006.5.8.2** Limited-class AI Systems SHALL be evaluated for accuracy, security (including prompt injection and data leakage) and, where they affect individuals, bias, before production deployment and after each material model change.
- **RSK-006.5.8.3** Security evaluation of High-class and customer-facing Limited-class AI Systems SHALL include adversarial testing (red teaming) by persons independent of the development team, using the AI Threat Model required by RSK-005.
- **RSK-006.5.8.4** Evaluation results SHALL be documented with the methods, data sets, metrics, thresholds, results and pass or fail decision, and approved by the System Owner and the CISO. A High-class AI System that fails an evaluation threshold SHALL NOT be deployed, or SHALL be withdrawn from production within 5 business days, unless the ISSC accepts the Risk under RSK-001.
- **RSK-006.5.8.5** System Owners SHALL monitor High-class AI Systems in production for performance degradation, drift and bias against the evaluation thresholds at least monthly, and Limited-class AI Systems at least quarterly, and SHALL record results.
- **RSK-006.5.8.6** AI System prompts, outputs, tool calls and human-review decisions for High-class AI Systems SHALL be logged under SEC-012 (SEC-012.5.2.1, Log Source 21) and retained per CMP-004.
- **RSK-006.5.8.7** Failures of an AI System that cause or could cause harm to individuals, unauthorized disclosure, or a breach of this Policy SHALL be reported and handled as Security Incidents under RES-002. Serious incidents involving AI Systems subject to the EU AI Act SHALL be reported to the GC within 24 hours of identification for assessment of regulatory reporting duties.
- **RSK-006.5.8.8** Each AI System SHALL be decommissioned by the System Owner when no longer used, including removal from the inventory, revocation of credentials and integrations, and deletion or return of training data and model artifacts per CMP-004 and SEC-017.

### 5.9 EU AI Act

- **RSK-006.5.9.1** [DECISION REQUIRED: Does the Organization place AI Systems on the EU market, put them into service in the EU, or use AI Systems whose outputs are used in the EU, so that Regulation (EU) 2024/1689 (EU AI Act) applies? Recommended default: Yes, applies as a deployer; provider obligations apply only where the Organization develops an AI System and places it on the market under its own name.] Where the EU AI Act applies, the GC SHALL record its obligations in the Obligations Register (CMP-001), including the dates on which each obligation becomes applicable.
- **RSK-006.5.9.2** For each AI System within scope of the EU AI Act, the inventory SHALL record the Organization's role (provider, deployer, importer or distributor) and the system's category (prohibited, high-risk, transparency obligations, general-purpose AI model, or minimal).
- **RSK-006.5.9.3** Where the Organization is a deployer of a high-risk AI System, the System Owner SHALL: use the system in accordance with the provider's instructions; assign human oversight to trained persons with authority under section 5.6; ensure input data under the Organization's control is relevant and representative; monitor operation and inform the provider of risks or serious incidents; retain automatically generated logs for at least 6 months, or longer where required by CMP-004; inform Workforce Members and their representatives before deploying a high-risk AI System in the workplace; and, where the Organization is a deployer covered by Art. 27, complete a fundamental rights impact assessment before first use.
- **RSK-006.5.9.4** Where the Organization is a provider of a high-risk AI System, the CTO SHALL implement a risk management system, data governance, technical documentation, record-keeping, transparency, human oversight, accuracy, robustness and cybersecurity measures, a quality management system, conformity assessment and post-market monitoring meeting EU AI Act Chapter III, Section 2 and Section 3, before the system is placed on the market.
- **RSK-006.5.9.5** The transparency obligations in EU AI Act Art. 50 (disclosure of AI interaction, marking of synthetic content, and disclosure of deep fakes) SHALL be met through RSK-006.5.6.6.

### 5.10 Other Emerging Technology

- **RSK-006.5.10.1** The ISSC SHALL designate a technology as Emerging Technology where it is new to the Organization and its security, privacy or regulatory Risk is not addressed by an existing suite document (for example quantum computing, distributed ledger, extended reality, brain-computer interfaces or autonomous robotics).
- **RSK-006.5.10.2** Before production use of a designated Emerging Technology, the System Owner SHALL complete a risk assessment under RSK-002 and a Threat Model under RSK-005, and SHALL obtain CISO approval. Pilots MAY use only Public and Internal data unless the ISSC approves otherwise.
- **RSK-006.5.10.3** The CISO SHALL assess the Organization's exposure to cryptographically relevant quantum computing at least every 12 months, including an inventory of cryptographic dependencies maintained under SEC-006, and SHALL report the migration readiness to the ISSC.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| ISSC | AI governance body; approves this Policy, the approved AI tools list, High-class AI Systems and emerging-technology designations; accepts AI Risks under RSK-001. |
| CISO | Owns this Policy and the AI management system; maintains the AI System inventory and approved tools list; confirms risk classes; approves Limited-class AI Systems and evaluation results. |
| CPO | Reviews AI Systems processing Personal Data; approves bias metrics and thresholds; confirms Art. 22 and ADMT compliance; approves use of Personal Data for training. |
| DPO | `[GDPR]` Advises on DPIAs for AI Systems. |
| GC | Records EU AI Act and other AI legal obligations; reviews High-class and EU AI Act systems; assesses serious-incident reporting duties. |
| CTO | Ensures internally developed AI follows SEC-010; meets EU AI Act provider obligations where applicable. |
| Head of Security Engineering | Implements blocking and Data Loss Prevention Controls for AI services; supports adversarial testing. |
| SOC Manager | Includes AI threats in threat intelligence and threat modeling under RSK-005; monitors AI logs. |
| Head of GRC | Records AI Risks in the Risk Register; coordinates AI vendor assessments under RSK-003. |
| Head of Procurement | Ensures AI tools are purchased only after approval under this Policy. |
| CHRO | Informs Workforce Members before workplace deployment of High-class AI Systems. |
| System Owner | Classifies and registers AI Systems; maintains inventory entries; implements oversight, evaluation and monitoring; decommissions systems. |
| Data Owner | Approves use of owned data sets for AI training, fine-tuning and grounding. |
| Workforce Members | Use only approved tools within data limits; review outputs; report AI failures. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| RSK-006.7.1 | AI risk classes | Prohibited · High · Limited · Minimal |
| RSK-006.7.2 | Approval authority by class | High: ISSC · Limited: CISO (+ CPO if Personal Data) · Minimal: System Owner using an approved tool |
| RSK-006.7.3 | Inventory update after change | Within 10 business days |
| RSK-006.7.4 | Inventory reconciliation for unapproved AI | Quarterly; unapproved AI blocked or submitted within 10 business days |
| RSK-006.7.5 | Approved AI tools list review | Every 6 months; within 10 business days of material provider change |
| RSK-006.7.6 | Provider retention of inputs and outputs (approved Generative AI tools) | No training on Organization data; retention ≤ 30 days unless configured by the Organization |
| RSK-006.7.7 | Maximum Classification Level for Minimal-class approved tools | Internal |
| RSK-006.7.8 | Restricted data in AI Systems | High-class only, ISSC-approved data types, conditions in 5.5.2 |
| RSK-006.7.9 | AI Impact Assessment review (High) | Every 12 months |
| RSK-006.7.10 | High-class evaluation (accuracy, bias, robustness, security, privacy) | Before deployment and every 12 months |
| RSK-006.7.11 | Production monitoring | High monthly · Limited quarterly |
| RSK-006.7.12 | Withdrawal after failed High-class evaluation | Within 5 business days unless ISSC accepts the Risk |
| RSK-006.7.13 | Halt mechanism test (High and autonomous) | Every 12 months |
| RSK-006.7.14 | Material model change notice (contractual) | At least 30 days |
| RSK-006.7.15 | EU AI Act serious incident to GC | Within 24 hours of identification |
| RSK-006.7.16 | EU AI Act deployer log retention | At least 6 months, or longer per CMP-004 |
| RSK-006.7.17 | AI training | Before first use or role assignment, then every 12 months, under PPL-002 |
| RSK-006.7.18 | Quantum readiness assessment | Every 12 months |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| AI Systems in use that are recorded in the inventory | 100% | Quarterly | CISO |
| Unapproved AI services detected in use | Trend downward; all resolved within 10 business days | Quarterly | CISO |
| High-class AI Systems with current evaluation (≤ 12 months) | 100% | Quarterly | CISO |
| High and Limited-class AI Systems with completed impact assessment | 100% | Quarterly | CISO |
| AI Systems processing Personal Data with DPIA where required | 100% | Quarterly | CPO |
| Data Loss Prevention events on approved AI tools involving Confidential or Restricted data | Trend downward | Monthly | Head of Security Engineering |
| AI training completion | ≥ 95% within 30 days of assignment | Quarterly | CISO |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

No Exception SHALL be granted to the prohibited uses in RSK-006.5.3.2, to RSK-006.5.5.2 (conditions for Restricted data), or to `[GDPR]` RSK-006.5.6.4.

## 10. Enforcement

Non-compliance is handled under CMP-007.

Input of Confidential or Restricted data into an AI System not approved for that Classification Level SHALL be reported as a Security Event under RES-002 and assessed for Personal Data Breach under RES-003.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| RSK-006.5.1 | 5.1, 5.3, 7.2 | GV.RR-02, GV.PO-01, PR.AT-01 | PM-9, AT-3 | 14.1 | CC1.3, CC2.2 | APO01, EDM03 | EU AI Act Art. 4 |
| RSK-006.5.2 | A.5.9 | ID.AM-01, ID.AM-02 | CM-8, PM-5 | 1.1, 2.1 | CC6.1 | BAI09.01 | `[GDPR]` Art. 30 |
| RSK-006.5.3 | 6.1.2 | ID.RA-04, ID.RA-05 | RA-3, RA-8 | — | CC3.2 | APO12.02 | EU AI Act Art. 5, 6, 27; `[GDPR]` Art. 35 |
| RSK-006.5.4 – 5.5 | A.5.10, A.5.12, A.5.14 | PR.DS-01, PR.DS-02, PR.AA-05 | AC-3, AC-4, SC-7 | 3.3, 3.13 | CC6.1, C1.1 | DSS05.02 | `[GDPR]` Art. 5(1)(b), 25; `[HIPAA]` §164.502(e); `[PCI]` 3.2.1 |
| RSK-006.5.6 | A.5.2 | GV.RR-02 | PM-9 | — | CC1.3 | APO01.02 | `[GDPR]` Art. 22; Cal. Civ. Code §1798.185; EU AI Act Art. 14, 26, 50 |
| RSK-006.5.7 | A.5.19, A.5.20, A.8.25 | GV.SC-06, GV.SC-07 | SA-9, SR-6 | 15.4, 16.1 | CC9.2 | APO10.03 | EU AI Act Art. 25 |
| RSK-006.5.8 | A.8.29, A.8.16, A.5.24 | ID.RA-01, DE.CM-09, RS.MA-01 | CA-8, SI-4, IR-4 | 16.13 | CC4.1, CC7.2 | MEA01, BAI07 | EU AI Act Art. 9, 15, 26, 73 |
| RSK-006.5.9 | 4.2 | GV.OC-03 | PM-9 | — | CC2.3 | MEA03 | EU AI Act Chapter III |
| RSK-006.5.10 | 6.1.2, A.8.24 | ID.RA-05 | RA-3, SC-12 | 3.10 | CC3.4 | APO04 | — |

### 11.1 AI framework alignment

| Requirement | ISO/IEC 42001:2023 | NIST AI RMF 1.0 |
|---|---|---|
| RSK-006.5.1 | 4.4, 5.1, 5.2, 5.3, 7.2, 7.3 | GOVERN 1, GOVERN 2, GOVERN 3 |
| RSK-006.5.2 | 6.1.2, 8.1 | MAP 1, MAP 4 |
| RSK-006.5.3 | 6.1.2, 6.1.4, 8.2, 8.4 | MAP 1, MAP 3, MAP 5 |
| RSK-006.5.4 – 5.5 | 6.1.3, 8.3 | MANAGE 1, MANAGE 2 |
| RSK-006.5.6 | 6.1.3, 8.3 | GOVERN 3, MAP 3, MANAGE 2 |
| RSK-006.5.7 | 8.1, 8.3 | GOVERN 6, MAP 4, MANAGE 3 |
| RSK-006.5.8 | 9.1, 10.2 | MEASURE 1, MEASURE 2, MEASURE 3, MANAGE 4 |
| RSK-006.5.9 | 4.1, 4.2 | GOVERN 1 |

## 12. Related documents

RSK-001, RSK-002, RSK-003, RSK-005, GOV-004, SEC-001, SEC-002, SEC-003, SEC-004, SEC-006, SEC-010, SEC-012, SEC-017, SEC-019, CMP-001, CMP-003, CMP-004, CMP-005, CMP-007, RES-002, RES-003, PPL-002, TPL-004, TPL-005, TPL-010, REF-001

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CISO | | | |
| Approver: ISSC Vice-Chair, on behalf of the ISSC (CISO recused as Document Owner under GOV-001.5.3.9) | | | |
