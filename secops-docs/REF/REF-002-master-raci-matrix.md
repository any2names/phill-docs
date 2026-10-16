# REF-002 — Master RACI Matrix

## 1. Document control

| Field | Value |
|---|---|
| Document ID | REF-002 |
| Title | Master RACI Matrix |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | Ref — Master reference |
| Classification | Internal |
| Owner | Head of GRC |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months, and on approval of any new or revised suite document |
| Parent document | GOV-001 Security Governance & Organization Policy |
| Related documents | ISP-000, GOV-001, GOV-002, GOV-006, REF-001, REF-003 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Head of GRC | Initial release |

## 3. Purpose

This document brings together, in one matrix, who is Responsible, Accountable, Consulted and
Informed for the major activities across the Information Security & GRC Policy Suite. It also
lists which documents each role owns and approves, and confirms that no Document Owner
approves their own document.

GOV-001 sets role accountabilities (section 5.4) and a summary RACI for program-level activities
(section 6.1). Each topic document sets the responsibilities for its own activities in its
section 6. This matrix consolidates both. It creates no new accountabilities.

## 4. Scope

- **Documents:** all 61 suite documents listed in the README.
- **Roles:** the canonical roles in SUITE-REGISTER section B, as columns in the exact form listed there.
- **Activities:** 117 major recurring or event-driven activities, grouped into six domains: governance and program management; risk management; compliance, audit and privacy; security controls; incident response, business continuity and disaster recovery; and people. Activities that only one role performs with no other party involved are not listed; they stay in the topic document.
- **Users:** every role holder, Document Owners when they consult under GOV-002.5.4.1, the Head of GRC when maintaining the role-assignment register, and auditors.

## 5. RACI matrix

### 5.1 Conventions

- **REF-002.5.1.1** Letters have the following meanings:

| Letter | Meaning |
|---|---|
| R | Responsible: performs the activity. An activity MAY have more than one R. |
| A | Accountable: answerable for the outcome; approves or signs off. **Each activity has exactly one A.** "A/R" means the accountable role also performs the activity. |
| C | Consulted: gives input before a decision (two-way). |
| I | Informed: told of the outcome (one-way). |

- **REF-002.5.1.2** Where a topic document names a role that is not canonical, the matrix shows it in the canonical column below:

| Role named in a topic document | Shown in column | Basis |
|---|---|---|
| Risk Owner, business sponsor, BCP owner, business unit leader | Asset Owner | GOV-001.5.4.6 (the Asset Owner is the default Risk Owner); RSK-003.5.1.4; RES-004 §6 |
| Control Owner, remediation owner | System Owner, unless the topic document names another role | GOV-001.5.4.6 |
| Requester, developer, privileged user, manager | Workforce Member | GOV-001.5.4.6 |
| Incident Commander, other IR roles | SOC Manager (who staffs the roster under RES-002) | RES-002 §6 |
| DR Coordinator | Chief Information Officer (CIO) (who appoints the coordinator under RES-005) | RES-005 §6 |
| Change Advisory Board (CAB) | Chief Information Officer (CIO) (who establishes and chairs the CAB) | SEC-013 §6 |
| Crisis Management Team | Its chair and members, shown individually | RES-004 §6 |
| Penetration tester, ASV, auditor, Processor | Third Party | GOV-006 |

- **REF-002.5.1.3** Regulation-tagged activities (`[PCI]`, `[HIPAA]`, `[SOX]`, `[GDPR]`, `[CPRA]`) apply only where the conditional module applies (README "Conditional modules"). Columns for the HIPAA Security Officer, HIPAA Privacy Officer and Data Protection Officer (DPO) apply only where those designations are made under GOV-001.5.5.
- **REF-002.5.1.4** Where an individual holds more than one role under a combination permitted by GOV-001.5.8, the individual carries every letter of every role held, subject to the recusals in GOV-001.5.3.9 and GOV-001.5.8.2.

### 5.2 Maintenance

- **REF-002.5.2.1** The Head of GRC SHALL update this matrix within 10 business days of the approval of any new or revised suite document, and of any change to GOV-001 section 5.4.
- **REF-002.5.2.2** Before an update is published, the Head of GRC SHALL confirm that every activity has exactly one A, that every letter matches GOV-001 and the topic document, and that every column name matches SUITE-REGISTER section B.
- **REF-002.5.2.3** Where GOV-001 and a topic document assign an activity differently, this matrix SHALL follow the topic document. The Head of GRC SHALL record the discrepancy in appendix A and SHALL submit the GOV-001 correction to the CISO, as GOV-001's owner, within 10 business days. Where the discrepancy is with GOV-001 section 5.4 accountabilities, GOV-001.5.4.1 governs and the topic document SHALL be corrected instead.
- **REF-002.5.2.4** Every Document Owner SHALL consult, as a minimum, the roles marked R or A for their document's activities in this matrix when drafting or revising the document (GOV-002.5.4.1).
- **REF-002.5.2.5** The Head of GRC SHALL use this matrix to confirm, at each update of the role-assignment register (GOV-001.5.1.2), that every role with an A or R in an activity that applies to the Organization has a named holder.

### 5.3 Activity matrix

#### 5.3.1 Governance and program management

| ID | Activity | Source | Board of Directors | Audit Committee | Chief Executive Officer (CEO) | Information Security Steering Committee (ISSC) | Chief Financial Officer (CFO) | Chief Information Officer (CIO) | Chief Technology Officer (CTO) | Chief Information Security Officer (CISO) | Chief Privacy Officer (CPO) | General Counsel (GC) | Chief Human Resources Officer (CHRO) | Data Protection Officer (DPO) | HIPAA Security Officer | HIPAA Privacy Officer | Head of GRC | Head of Security Engineering | SOC Manager | Internal Audit Director | Business Continuity Manager | Head of Facilities | Head of Procurement | Asset Owner | Data Owner | System Owner | Data Custodian | Workforce Member | Third Party |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| RACI-GOV-01 | Approve and review the Information Security Program Charter | ISP-000; GOV-001 §6.1 | A | R | C | C |  | I | I | R | I | C | I | I |  |  | C |  |  | I |  |  |  |  |  |  |  |  |  |
| RACI-GOV-02 | Conduct the annual management review of the program | ISP-000.5.8; GOV-001.5.3.10 |  | I | I | A |  |  |  | R |  |  |  |  |  |  | R |  |  | C |  |  |  |  |  |  |  |  |  |
| RACI-GOV-03 | Produce metrics, KRI dashboard and annual program report | GOV-003; GOV-001 §6.1 | I | I | I | C |  | C | C | A | C |  |  | C |  |  | R |  |  | I |  |  |  |  |  |  |  |  |  |
| RACI-GOV-04 | Appoint and remove the CISO | GOV-001.5.2.4 |  | I | A | I |  |  |  |  |  |  | C |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| RACI-GOV-05 | Establish the ISSC and approve changes to its charter | GOV-001.5.3.1, 5.3.13 |  |  | A | R |  |  |  | R |  | C |  |  |  |  | C |  |  |  |  |  |  |  |  |  |  |  |  |
| RACI-GOV-06 | Convene the ISSC; circulate papers and minutes | GOV-001.5.3.5, 5.3.11 |  |  |  |  | I | I | I | A | I | C | I | I | I |  | R |  |  | I |  |  |  |  |  |  |  |  |  |
| RACI-GOV-07 | Maintain the role-assignment register and named deputies | GOV-001.5.1.2 – 5.1.4 |  |  | I | C |  |  |  |  |  |  | C |  |  |  | A/R |  |  |  |  |  |  |  |  |  |  |  |  |
| RACI-GOV-08 | Designate statutory officers (HIPAA Security Officer, HIPAA Privacy Officer, DPO) `[HIPAA]` `[GDPR]` | GOV-001.5.5 |  | I | A |  |  |  |  | C | C | R |  | I | I | I | R |  |  |  |  |  |  |  |  |  |  |  |  |
| RACI-GOV-09 | Identify and enforce Segregation of Duties conflicts in each Information System | GOV-001.5.7.3 – 5.7.4 |  |  |  |  | C |  |  |  |  |  |  |  |  |  | C |  |  | I |  |  |  |  |  | A/R | R |  |  |
| RACI-GOV-10 | Sign off the security risk assessment for projects at the design gate | GOV-001.5.11 |  |  |  |  |  |  |  | A | C |  |  |  |  |  | C | C |  |  |  |  |  |  |  | R |  |  |  |
| RACI-GOV-11 | Approve Tier 1 Policies | GOV-002.5.5; GOV-001 §6.1 |  | I | I | A |  | C | C | C | C | C | C | C |  |  | R |  |  | I |  |  |  |  |  |  |  |  |  |
| RACI-GOV-12 | Approve Tier 2 Standards (CMP-009 by the CFO; CMP-008 by the ISSC where the CISO is HIPAA Security Officer) | GOV-002.5.5; README; GOV-001 §6.1 |  |  |  | I |  | C | C | A | C | I |  | C |  |  | R |  |  | I |  |  |  |  |  |  |  |  |  |
| RACI-GOV-13 | Maintain the policy suite, repository and review calendar; escalate overdue reviews | GOV-002.5.7 – 5.8; GOV-001 §6.1 |  |  |  | I |  | C | C | A | C | C | C | C |  |  | R |  |  | I |  |  |  |  |  |  |  |  |  |
| RACI-GOV-14 | Obtain Workforce policy attestation at hire and annually | GOV-002.5.9 |  |  |  |  |  |  |  | R |  |  | R |  |  |  | A |  |  |  |  |  |  |  |  |  |  | R | R |
| RACI-GOV-15 | Maintain and enforce the Acceptable Use Policy | GOV-004 |  |  |  | I |  | C | C | A |  | C | C |  |  |  |  |  |  |  |  |  |  |  |  |  |  | R | R |
| RACI-GOV-16 | Maintain the control mapping matrix and Key Control list | REF-001 |  |  |  |  | C |  |  | A |  |  |  |  | C |  | R | C |  | C |  |  |  |  |  |  |  |  |  |
| RACI-GOV-17 | Approve and track the implementation roadmap | REF-003; GOV-001.5.3.10 |  | I | I | A | C |  |  | R |  |  |  |  |  |  | R |  |  |  |  |  |  |  |  |  |  |  |  |

#### 5.3.2 Risk management

| ID | Activity | Source | Board of Directors | Audit Committee | Chief Executive Officer (CEO) | Information Security Steering Committee (ISSC) | Chief Financial Officer (CFO) | Chief Information Officer (CIO) | Chief Technology Officer (CTO) | Chief Information Security Officer (CISO) | Chief Privacy Officer (CPO) | General Counsel (GC) | Chief Human Resources Officer (CHRO) | Data Protection Officer (DPO) | HIPAA Security Officer | HIPAA Privacy Officer | Head of GRC | Head of Security Engineering | SOC Manager | Internal Audit Director | Business Continuity Manager | Head of Facilities | Head of Procurement | Asset Owner | Data Owner | System Owner | Data Custodian | Workforce Member | Third Party |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| RACI-RSK-01 | Ratify Risk Appetite and Risk Tolerance | RSK-001.5.3; GOV-001 §6.1 | I | A | R | R |  | I | I | R | I | C | I | I |  |  | R |  |  | I |  |  |  |  |  |  |  |  |  |
| RACI-RSK-02 | Maintain the Risk Register and assign Risk Owners | RSK-001.5.2 |  |  |  | I |  |  |  | C |  |  |  |  |  |  | A |  |  |  |  |  |  | R |  |  |  |  |  |
| RACI-RSK-03 | Perform the enterprise risk assessment | RSK-002.5.6; GOV-001 §6.1 |  | I | I | C |  | C | C | A | C | C | C | C |  |  | R |  | C | I | C |  |  | C |  |  |  |  |  |
| RACI-RSK-04 | Submit and deliver risk treatment plans within the deadlines in RSK-002 | RSK-002.5.7; RSK-001.5.4 |  |  |  |  |  |  |  | I |  |  |  |  |  |  | C |  |  |  |  |  |  | A |  | R |  |  |  |
| RACI-RSK-05 | Accept a Low residual Risk | RSK-001.5.5 |  |  |  |  |  |  |  | I |  |  |  |  |  |  | R |  |  |  |  |  |  | A |  |  |  |  |  |
| RACI-RSK-06 | Accept a Medium residual Risk | RSK-001.5.5 |  |  |  | I |  |  |  | A |  |  |  |  |  |  | R |  |  |  |  |  |  | R |  |  |  |  |  |
| RACI-RSK-07 | Accept a High residual Risk | RSK-001.5.5 |  |  |  | A |  |  |  | R |  |  |  |  |  |  | R |  |  |  |  |  |  | R |  |  |  |  |  |
| RACI-RSK-08 | Accept a Critical residual Risk | RSK-001.5.5; GOV-001 §6.1 |  | I | A | C |  | C | C | R | C | C |  | C |  |  | R |  |  | I |  |  |  | R |  |  |  |  |  |
| RACI-RSK-09 | Review the Risk Register and overdue treatment | RSK-001.5.6 |  | I |  | A |  |  |  | R |  |  |  |  |  |  | R |  |  |  |  |  |  |  |  |  |  |  |  |
| RACI-RSK-10 | Run third-party risk management | RSK-003; GOV-001 §6.1 |  |  |  | I |  | C | C | A | C | C |  | C |  |  | R |  |  | I |  |  | R |  |  |  |  |  |  |
| RACI-RSK-11 | Perform third-party due diligence before contract (TPL-004) | RSK-003.5.3 |  |  |  |  |  |  |  | C | C |  |  | C | C | C | A | C |  |  |  |  | R | R |  |  |  |  | R |
| RACI-RSK-12 | Include required security and privacy terms in third-party contracts | RSK-003.5.4; GOV-001.5.4.5 |  |  |  |  |  |  |  |  | C | R |  | C | C | C | C |  |  |  |  |  | A |  |  |  |  |  |  |
| RACI-RSK-13 | Reassess Third Parties and review assurance reports | RSK-003.5.5 |  |  |  |  | R |  |  | I |  |  |  |  |  |  | A | C |  |  | C |  |  | R |  |  |  |  |  |
| RACI-RSK-14 | Perform the business impact analysis and assign Recovery Tiers | RSK-004 |  |  |  | I | C | C |  |  |  |  |  |  | C |  | I |  |  |  | A |  | C | R |  | C |  |  |  |
| RACI-RSK-15 | Approve Recovery Tier 0 and Tier 1 assignments | RSK-004.5.7 |  |  |  | A |  | I |  |  |  |  |  |  |  |  |  |  |  |  | R |  |  | C |  |  |  |  |  |
| RACI-RSK-16 | Operate threat intelligence: intelligence requirements, sources, triage and reporting | RSK-005.5.1 – 5.5 |  |  |  |  |  |  |  | C |  | C |  |  |  |  | I | I | A |  |  |  |  |  |  |  |  |  |  |
| RACI-RSK-17 | Maintain the AI System inventory and classify AI use cases | RSK-006.5.2 – 5.3 |  |  |  |  |  |  |  | A | C | C |  | C |  |  | I |  |  |  |  |  |  |  |  | R |  |  |  |
| RACI-RSK-18 | Approve the approved Generative AI tools list and High-class AI Systems | RSK-006.5.3 – 5.4 |  |  |  | A |  |  |  | R | C | C |  |  |  |  |  | C |  |  |  |  |  |  | C |  |  |  |  |

#### 5.3.3 Compliance, audit and privacy

| ID | Activity | Source | Board of Directors | Audit Committee | Chief Executive Officer (CEO) | Information Security Steering Committee (ISSC) | Chief Financial Officer (CFO) | Chief Information Officer (CIO) | Chief Technology Officer (CTO) | Chief Information Security Officer (CISO) | Chief Privacy Officer (CPO) | General Counsel (GC) | Chief Human Resources Officer (CHRO) | Data Protection Officer (DPO) | HIPAA Security Officer | HIPAA Privacy Officer | Head of GRC | Head of Security Engineering | SOC Manager | Internal Audit Director | Business Continuity Manager | Head of Facilities | Head of Procurement | Asset Owner | Data Owner | System Owner | Data Custodian | Workforce Member | Third Party |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| RACI-CMP-01 | Maintain the Obligations Register | CMP-001.5.1 – 5.2; GOV-001 §6.1 |  | I |  | I |  |  |  | C | C | R |  | C |  |  | A |  |  | I |  |  |  |  |  |  |  |  |  |
| RACI-CMP-02 | Approve applicability determinations and legal interpretation of obligations | CMP-001.5.1.2, 5.3 |  |  |  |  | C |  |  | C | C | A |  | C |  |  | R |  |  |  |  |  |  |  |  |  |  |  |  |
| RACI-CMP-03 | Manage the SOC 2 Type II examination and sign management's assertion | CMP-001.5.1.3, 5.6 |  | I | R | I |  |  |  | A |  |  |  |  |  |  | R |  |  | C |  |  |  |  |  | R |  |  |  |
| RACI-CMP-04 | `[PCI]` Validate PCI DSS compliance and sign the Attestation of Compliance | CMP-001.5.6.15; SEC-019.5.11 |  | I |  |  |  |  |  | A |  | C |  |  |  |  | R | R |  | C |  |  |  |  |  |  |  |  |  |
| RACI-CMP-05 | `[HIPAA]` Perform the ePHI risk analysis, addressable decisions and Security Rule evaluation | CMP-008.5.3, 5.5, 5.11 |  |  |  | I |  |  |  | C |  | C |  |  | A | C | R |  |  | R |  |  |  |  |  |  |  |  |  |
| RACI-CMP-06 | `[SOX]` Scope ITGCs, test Key Controls and support management's assertion | CMP-009; GOV-001 §6.1 |  | I | C | I | A | C | C | C |  | C |  |  |  |  | R |  |  | C |  |  |  |  |  | R |  |  |  |
| RACI-CMP-07 | `[SOX]` Classify ITGC deficiencies and escalate Significant Deficiencies and Material Weaknesses | CMP-009.5.11; CMP-002 §6 |  | I | I |  | A |  |  |  |  | C |  |  |  |  | R |  |  | C |  |  |  |  |  |  |  |  |  |
| RACI-CMP-08 | Approve the internal audit plan and perform internal audits | CMP-002; GOV-001 §6.1 |  | A | I | I |  | C | C | C | C |  |  | C |  |  | C |  |  | R |  |  |  |  |  |  |  |  |  |
| RACI-CMP-09 | Perform second-line testing of Key Controls | CMP-002.5.3, 5.5 |  |  |  |  |  |  |  | I |  |  |  |  |  |  | A |  |  | I |  |  |  |  |  | R |  |  |  |
| RACI-CMP-10 | Track deficiencies to remediation and validate closure | CMP-002.5.8 |  | I |  | I |  |  |  | C |  |  |  |  |  |  | A |  |  |  |  |  |  |  |  | R |  |  |  |
| RACI-CMP-11 | Approve an Exception: Low residual Risk | CMP-003.5.4; RSK-001.5.5 |  |  |  |  |  |  |  | C |  |  |  |  |  |  | R |  |  | I |  |  |  | A |  |  |  | R |  |
| RACI-CMP-12 | Approve an Exception: Medium residual Risk | CMP-003.5.4; GOV-001 §6.1 |  | I |  |  |  | C | C | A | C |  |  | C |  |  | R |  |  | I |  |  |  |  |  |  |  | R |  |
| RACI-CMP-13 | Approve an Exception: High residual Risk | CMP-003.5.4; GOV-001 §6.1 |  | I |  | A |  | C | C | C | C |  |  | C |  |  | R |  |  | I |  |  |  |  |  |  |  | R |  |
| RACI-CMP-14 | Approve an Exception: Critical residual Risk | CMP-003.5.4; GOV-001 §6.1 |  | I | A | C |  | C | C | C | C |  |  | C |  |  | R |  |  | I |  |  |  |  |  |  |  | R |  |
| RACI-CMP-15 | Maintain the Exception register, expiry notices and Compensating Control testing | CMP-003.5.5, 5.8 – 5.9 |  |  |  | I |  |  |  |  |  |  |  |  |  |  | A |  |  | I |  |  |  |  |  | R |  |  |  |
| RACI-CMP-16 | Maintain the retention schedule and Evidence repository | CMP-004.5.1 – 5.2, 5.7 |  |  |  | I |  |  |  |  | C | C |  | C |  |  | A |  |  |  |  |  |  |  |  | R |  |  |  |
| RACI-CMP-17 | Issue, manage and release Legal Holds | CMP-004.5.4 |  |  |  |  |  | R |  |  |  | A |  |  |  |  | I |  |  |  |  |  |  |  |  | R |  | I |  |
| RACI-CMP-18 | Collect and preserve Evidence of Control operation | CMP-004.5.5 – 5.6 |  |  |  |  |  |  |  | C |  |  |  |  |  |  | A |  | R |  |  |  |  |  |  | R |  |  |  |
| RACI-CMP-19 | Run the privacy program and approve Privacy Notices | CMP-005.5.1 – 5.4 |  |  |  |  |  |  |  |  | A | R | R | C |  |  | I |  |  |  |  |  |  |  |  |  |  |  |  |
| RACI-CMP-20 | Maintain the Record of Processing Activities (TPL-010) `[GDPR]` | CMP-005.5.8 |  |  |  |  |  |  |  |  | A |  |  | R |  |  |  |  |  |  |  |  |  |  | R |  |  |  |  |
| RACI-CMP-21 | Perform and approve DPIAs (TPL-005) `[GDPR]` | CMP-005.5.9 |  |  |  |  |  |  |  | C | A | C |  | C |  |  |  |  |  |  |  |  |  |  | R | C |  |  |  |
| RACI-CMP-22 | Respond to Data Subject Requests `[GDPR]` `[CPRA]` | CMP-010 |  |  |  |  |  |  |  | C | I | C |  | A |  |  |  |  |  |  |  |  | R |  | R | R |  | R |  |
| RACI-CMP-23 | Operate whistleblower channels, triage and investigations | CMP-006.5.1 – 5.6 |  | I |  |  |  |  |  | R | R | A | C |  |  |  |  |  | R | R |  |  |  |  |  |  |  | R |  |
| RACI-CMP-24 | `[SOX]` Operate Audit Committee procedures for accounting and auditing complaints | CMP-006.5.7 |  | A |  |  | C |  |  |  |  | R |  |  |  |  |  |  |  | R |  |  |  |  |  |  |  |  |  |
| RACI-CMP-25 | Investigate and sanction violations of suite documents | CMP-007 |  |  |  | I |  |  |  | R | C | C | A | C | C | C |  |  |  | I |  |  |  |  |  | R |  |  |  |

#### 5.3.4 Security controls

| ID | Activity | Source | Board of Directors | Audit Committee | Chief Executive Officer (CEO) | Information Security Steering Committee (ISSC) | Chief Financial Officer (CFO) | Chief Information Officer (CIO) | Chief Technology Officer (CTO) | Chief Information Security Officer (CISO) | Chief Privacy Officer (CPO) | General Counsel (GC) | Chief Human Resources Officer (CHRO) | Data Protection Officer (DPO) | HIPAA Security Officer | HIPAA Privacy Officer | Head of GRC | Head of Security Engineering | SOC Manager | Internal Audit Director | Business Continuity Manager | Head of Facilities | Head of Procurement | Asset Owner | Data Owner | System Owner | Data Custodian | Workforce Member | Third Party |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| RACI-SEC-01 | Maintain the Asset Inventory, discovery and Shadow IT detection | SEC-001 |  |  |  |  |  | A |  | I |  |  |  |  |  |  |  | C | I |  |  |  | R | R |  |  | R |  |  |
| RACI-SEC-02 | Classify data and review classification | SEC-002.5.1 – 5.3, 5.6 |  |  |  |  | C |  |  | C | C | C |  |  |  |  |  |  |  |  |  |  |  |  | A |  | R | R |  |
| RACI-SEC-03 | Operate data loss prevention and data discovery | SEC-002.5.5 |  |  |  |  |  |  |  | A |  |  |  | C |  |  |  | R | R |  |  |  |  |  | I |  |  |  |  |
| RACI-SEC-04 | Record joiner, mover, leaver and leave events in the human resources system | SEC-003 §6; PPL-001 |  |  |  |  |  | I |  | I |  |  | A |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| RACI-SEC-05 | Provision and change access on an approved request (joiner and mover) | SEC-003.5.2 – 5.4 |  |  |  |  |  | R |  |  |  |  |  |  |  |  |  | C |  |  |  |  |  |  | R | A |  | R |  |
| RACI-SEC-06 | Revoke access on Separation | SEC-003.5.7 |  |  |  |  |  | R |  | A |  |  | R |  |  |  |  |  | I |  |  |  |  |  |  | R |  |  |  |
| RACI-SEC-07 | Perform User Access Reviews (TPL-008) | SEC-003.5.12; GOV-001.5.4.6 |  |  |  |  |  |  |  | I |  |  |  |  |  |  | R |  |  | I |  |  |  |  | R | A | R |  |  |
| RACI-SEC-08 | Configure identity provider, MFA, SSO and password controls | SEC-004 |  |  |  |  |  | R |  | C |  |  |  |  |  |  |  | A | I |  |  |  |  |  |  | R |  |  |  |
| RACI-SEC-09 | Operate privileged access management, JIT access and PAWs | SEC-005.5.1 – 5.6 |  |  |  |  |  | R | R |  |  |  |  |  |  |  |  | A | R |  |  |  |  |  |  | R |  |  |  |
| RACI-SEC-10 | Review privileged access | SEC-005.5.11 |  |  |  |  |  |  |  | I |  |  |  |  |  |  | R | A |  |  |  |  |  |  |  | R |  |  |  |
| RACI-SEC-11 | Manage cryptographic keys, certificates and the post-quantum migration plan | SEC-006 |  |  |  | I |  | R | R | C |  |  |  |  |  |  |  | A | I |  |  |  |  |  | C |  |  |  |  |
| RACI-SEC-12 | Maintain network architecture, zones, rules and rule reviews | SEC-007 |  |  |  |  |  | R |  | C |  |  |  |  |  |  |  | A | I |  |  |  |  |  |  | R |  |  |  |
| RACI-SEC-13 | Enrol, harden, encrypt and patch Endpoints and Mobile Devices | SEC-008 |  |  |  |  |  | A |  | I |  |  |  |  |  |  |  | C | I |  |  |  |  |  |  |  |  | R |  |
| RACI-SEC-14 | Operate EDR and respond to Endpoint alerts | SEC-008.5.3 |  |  |  |  |  | R |  |  |  |  |  |  |  |  |  | A | R |  |  |  |  |  |  |  |  |  |  |
| RACI-SEC-15 | Approve Cloud Services and onboard them | SEC-009.5.2 |  |  |  |  |  | R | A |  | C |  |  |  |  |  | R | R |  |  |  |  | R |  | C |  |  |  |  |
| RACI-SEC-16 | Operate CSPM/CNAPP and remediate cloud findings | SEC-009.5.5 |  |  |  |  |  |  | C | I |  |  |  |  |  |  |  | A | I |  |  |  |  |  |  | R |  |  |  |
| RACI-SEC-17 | Run the secure development lifecycle, code review and security testing gates | SEC-010.5.1 – 5.5 |  |  |  |  |  |  | A |  |  |  |  |  |  |  |  | R |  |  |  |  |  |  |  | R |  | R |  |
| RACI-SEC-18 | Scan for Vulnerabilities and reconcile scanner coverage | SEC-011.5.1 – 5.3 |  |  |  |  |  |  |  | I |  |  |  |  |  |  |  | A |  |  |  |  |  |  |  | C |  |  |  |
| RACI-SEC-19 | Remediate Vulnerabilities and patch within the SLA in SEC-011 | SEC-011.5.4 – 5.5; GOV-001.5.4.6 |  |  |  |  |  | R | R | I |  |  |  |  |  |  |  | C |  |  |  |  |  |  |  | A |  |  |  |
| RACI-SEC-20 | Declare and manage emergency Vulnerabilities | SEC-011 §6 |  |  |  | I |  | R | R | A |  |  |  |  |  |  |  | R | R |  |  |  |  |  |  |  |  |  |  |
| RACI-SEC-21 | Commission and supervise Penetration Tests | SEC-011.5.7 |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | A | I |  |  |  | R |  |  | R |  |  | R |
| RACI-SEC-22 | Onboard log sources and enable required logging | SEC-012.5.1 – 5.3 |  |  |  |  |  | R | R |  | C |  |  | C |  |  |  | R | A |  |  |  |  |  |  | R |  |  |  |
| RACI-SEC-23 | Maintain detection use cases; triage alerts 24×7; respond to log failures | SEC-012.5.7 – 5.8, 5.10 |  |  |  |  |  |  |  | I |  |  |  |  |  |  |  | C | A |  |  |  |  |  |  | R |  |  |  |
| RACI-SEC-24 | Review logs, including the `[HIPAA]` ePHI activity review | SEC-012.5.9 |  |  |  |  |  |  |  |  |  |  |  |  | I |  | I |  | A |  |  |  |  |  |  |  |  |  |  |
| RACI-SEC-25 | Raise, assess, test, implement and verify Changes | SEC-013.5.3 – 5.7; GOV-001.5.4.6 |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | C |  |  | C |  |  |  |  | A |  | R |  |
| RACI-SEC-26 | Approve Normal Changes and retrospectively approve Emergency Changes (CAB) | SEC-013.5.5 |  |  |  |  |  | A | C | C |  |  |  |  |  |  |  | C |  |  | C |  |  |  |  | R |  |  |  |
| RACI-SEC-27 | Maintain Configuration Baselines and detect drift and unauthorized Change | SEC-013.5.8 – 5.9 |  |  |  |  |  | I |  |  |  |  |  |  |  |  |  | A | R |  |  |  |  |  |  | R |  |  |  |
| RACI-SEC-28 | `[SOX]` Control program change for Financially Significant Systems | SEC-013.5.11; SEC-010.5.14 |  |  |  |  | C | A |  |  |  |  |  |  |  |  | C |  |  |  |  |  |  |  |  | R |  |  |  |
| RACI-SEC-29 | Operate email authentication and anti-phishing controls | SEC-014.5.1 – 5.3 |  |  |  |  |  | A |  | C |  |  |  |  |  |  |  | R | R |  |  |  |  |  |  |  |  |  |  |
| RACI-SEC-30 | Control physical access, visitors and CCTV | SEC-016.5.1 – 5.4 |  |  |  |  |  | R |  |  |  |  | R |  |  |  |  |  | I |  |  | A |  | R |  |  |  | R |  |
| RACI-SEC-31 | Sanitize and dispose of Media | SEC-017 |  |  |  |  |  | A |  | I |  | C |  |  |  |  | C |  |  |  |  | R | R | R |  |  | R |  |  |
| RACI-SEC-32 | Operate and monitor Backups | SEC-018.5.1 – 5.5, 5.7 |  |  |  |  |  | A |  |  |  |  |  |  |  |  |  | C | I |  | C |  |  |  |  | R |  |  |  |
| RACI-SEC-33 | Test restores and sign off the results | SEC-018.5.6 |  |  |  |  |  | A |  |  |  |  |  |  |  |  |  |  |  |  | I |  |  |  |  | R | R |  |  |
| RACI-SEC-34 | `[PCI]` Define and confirm CDE scope | SEC-019.5.1 – 5.2 |  |  |  |  |  |  |  | A |  | C |  |  |  |  | C | R |  |  |  |  |  |  |  |  |  |  |  |
| RACI-SEC-35 | `[PCI]` Inspect POI devices and respond to tampering | SEC-019.5.9 |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | A | R |  |  | R |  |  |  |  |  | R |  |

#### 5.3.5 Incident response, business continuity and disaster recovery

| ID | Activity | Source | Board of Directors | Audit Committee | Chief Executive Officer (CEO) | Information Security Steering Committee (ISSC) | Chief Financial Officer (CFO) | Chief Information Officer (CIO) | Chief Technology Officer (CTO) | Chief Information Security Officer (CISO) | Chief Privacy Officer (CPO) | General Counsel (GC) | Chief Human Resources Officer (CHRO) | Data Protection Officer (DPO) | HIPAA Security Officer | HIPAA Privacy Officer | Head of GRC | Head of Security Engineering | SOC Manager | Internal Audit Director | Business Continuity Manager | Head of Facilities | Head of Procurement | Asset Owner | Data Owner | System Owner | Data Custodian | Workforce Member | Third Party |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| RACI-RES-01 | Maintain the incident response capability | RES-001.5.1, 5.8 |  |  |  | I |  | C |  | A |  | C |  |  |  |  |  |  | R |  |  |  |  |  |  |  |  |  |  |
| RACI-RES-02 | Report suspected Security Incidents | RES-001.5.2 |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | A |  |  |  |  |  |  |  |  | R | R |
| RACI-RES-03 | Respond to Sev-1 and Sev-2 Security Incidents | RES-002; RES-001.5.3; GOV-001 §6.1 | I | I | I | I | I | C | I | A | C | C | C | C |  |  | C |  | R |  |  |  |  |  |  | R |  |  |  |
| RACI-RES-04 | Respond to Sev-3 and Sev-4 Security Incidents | RES-002.5.3 |  |  |  |  |  |  |  | I |  |  |  |  |  |  |  |  | A |  |  |  |  |  |  | R |  |  |  |
| RACI-RES-05 | Preserve evidence and conduct forensic investigation | RES-001.5.4 |  |  |  |  |  |  |  | I |  | C | C |  |  |  |  |  | A |  |  |  |  |  |  | R |  |  |  |
| RACI-RES-06 | Decide on any ransom or extortion payment | RES-001.5.7 | I | I | A |  | R |  |  | R |  | R |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| RACI-RES-07 | Complete post-incident reviews (TPL-007) | RES-002.5.10 |  |  |  |  |  |  |  | C |  |  |  |  |  |  | I |  | A |  |  |  |  |  |  | R |  |  |  |
| RACI-RES-08 | Exercise the incident response plan | RES-002.5.14 |  |  |  | I |  |  |  | C | C | C |  |  |  |  |  |  | A |  |  |  |  |  |  | R |  |  |  |
| RACI-RES-09 | Decide on breach notification | RES-003.5.2 – 5.6; GOV-001 §6.1 | I | I | C | I |  | C | C | C | A | R |  | R | C | R |  |  |  |  |  |  |  |  |  |  |  |  |  |
| RACI-RES-10 | `[SOX]` Determine materiality and file Form 8-K Item 1.05 | RES-003.5.5 |  | I | A |  | R |  |  | C |  | R |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| RACI-RES-11 | Run the business continuity program | RES-004.5.1 | I | I | A | C |  |  |  |  |  |  |  |  |  |  |  |  |  |  | R |  |  |  |  |  |  |  |  |
| RACI-RES-12 | Activate and run the Crisis Management Team | RES-004.5.4 |  |  | A |  | C | R | R | R | R | R | R |  |  |  |  |  |  |  | R | R |  |  |  |  |  |  |  |
| RACI-RES-13 | Develop, maintain and exercise business continuity plans | RES-004.5.5, 5.11 – 5.12 |  |  |  | C |  |  |  |  |  |  |  |  |  |  |  |  |  |  | A |  |  | R |  |  |  |  |  |
| RACI-RES-14 | Declare a disaster | RES-005.5.2 |  |  | I |  |  | A | C | C |  |  |  |  |  |  |  |  |  |  | I |  |  |  |  |  |  |  |  |
| RACI-RES-15 | Recover Information Systems by Recovery Tier | RES-005.5.3 – 5.7 |  |  |  |  |  | A |  |  |  |  |  |  |  |  |  | R | R |  | I |  |  | R |  | R | R |  |  |
| RACI-RES-16 | Test disaster recovery | RES-005.5.10; RES-004.5.11 |  |  |  |  |  | A |  |  |  |  |  |  | I |  |  |  |  |  | C |  |  |  |  | R | R |  |  |

#### 5.3.6 People

| ID | Activity | Source | Board of Directors | Audit Committee | Chief Executive Officer (CEO) | Information Security Steering Committee (ISSC) | Chief Financial Officer (CFO) | Chief Information Officer (CIO) | Chief Technology Officer (CTO) | Chief Information Security Officer (CISO) | Chief Privacy Officer (CPO) | General Counsel (GC) | Chief Human Resources Officer (CHRO) | Data Protection Officer (DPO) | HIPAA Security Officer | HIPAA Privacy Officer | Head of GRC | Head of Security Engineering | SOC Manager | Internal Audit Director | Business Continuity Manager | Head of Facilities | Head of Procurement | Asset Owner | Data Owner | System Owner | Data Custodian | Workforce Member | Third Party |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| RACI-PPL-01 | Designate position risk levels and complete screening | PPL-001.5.1 – 5.2 |  |  |  |  |  |  |  | C | C | C | A | C |  |  |  |  |  |  |  |  | R |  |  |  |  |  |  |
| RACI-PPL-02 | Obtain signed terms of employment and confidentiality | PPL-001.5.3 |  |  |  |  |  |  |  |  |  | C | A |  |  |  |  |  |  |  |  |  |  |  |  |  |  | R |  |
| RACI-PPL-03 | Recover assets and close access at Separation | PPL-001.5.7; GOV-004.5.15 |  |  |  |  |  | R |  | I |  |  | A |  |  |  |  |  |  |  |  |  |  |  |  | R |  | R |  |
| RACI-PPL-04 | Run the security awareness and training program | PPL-002.5.1 – 5.3, 5.6; GOV-001 §6.1 |  |  | I | C |  | C | C | A | C | C | C | C |  |  | C |  |  |  |  |  |  |  |  |  |  | R |  |
| RACI-PPL-05 | Provide role-based training content | PPL-002.5.4 |  |  |  |  | R | R | R | A |  |  |  | R | R | R | R | R | R |  | R |  |  |  |  |  |  | R |  |
| RACI-PPL-06 | Act on training non-completion | PPL-002.5.7 |  |  |  |  |  |  |  | R |  |  | A |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |

### 5.4 Role-to-document ownership

Owner and approver assignments as listed in the README document library. Roles not listed own
or approve no document.

| Role | Owns | Approves |
|---|---|---|
| Board of Directors | — | ISP-000 |
| Audit Committee | — | CMP-002, CMP-006 |
| Chief Executive Officer (CEO) | — | GOV-001 |
| Information Security Steering Committee (ISSC) | — | GOV-002, GOV-003, GOV-004, GOV-006, RSK-001, RSK-003, RSK-006, CMP-001, CMP-003, CMP-004, CMP-005, CMP-007, SEC-001, SEC-002, SEC-003, SEC-006, SEC-007, SEC-008, SEC-009, SEC-010, SEC-011, SEC-012, SEC-013, SEC-014, SEC-015, SEC-016, SEC-017, SEC-018, RES-001, RES-004, PPL-001, PPL-002, REF-002, REF-003 |
| Chief Financial Officer (CFO) | — | CMP-009 |
| Chief Information Officer (CIO) | SEC-001, SEC-008, SEC-013, SEC-014, SEC-017, SEC-018, RES-005 | — |
| Chief Technology Officer (CTO) | SEC-009, SEC-010 | — |
| Chief Information Security Officer (CISO) | ISP-000, GOV-001, GOV-003, GOV-004, RSK-006, SEC-002, SEC-003, SEC-015, RES-001, PPL-002, REF-003 | RSK-002, RSK-004, RSK-005, CMP-008, SEC-004, SEC-005, SEC-019, RES-002, RES-003, TPL-001, TPL-002, TPL-003, TPL-004, TPL-006, TPL-007, TPL-008, TPL-009, REF-001 |
| Chief Privacy Officer (CPO) | CMP-005, RES-003 | CMP-010, TPL-005, TPL-010 |
| General Counsel (GC) | CMP-006 | — |
| Chief Human Resources Officer (CHRO) | CMP-007, PPL-001 | — |
| Data Protection Officer (DPO) | CMP-010, TPL-005, TPL-010 | — |
| HIPAA Security Officer | CMP-008 | — |
| HIPAA Privacy Officer | — | — |
| Head of GRC | GOV-002, GOV-006, RSK-001, RSK-002, RSK-003, CMP-001, CMP-003, CMP-004, CMP-009, TPL-001, TPL-002, TPL-003, TPL-004, TPL-009, REF-001, REF-002 | — |
| Head of Security Engineering | SEC-004, SEC-005, SEC-006, SEC-007, SEC-011, SEC-019, TPL-008 | — |
| SOC Manager | RSK-005, SEC-012, RES-002, TPL-006, TPL-007 | — |
| Internal Audit Director | CMP-002 | — |
| Business Continuity Manager | RSK-004, RES-004 | RES-005 |
| Head of Facilities | SEC-016 | — |
| Head of Procurement | — | — |
| Asset Owner | — | — |
| Data Owner | — | — |
| System Owner | — | — |
| Data Custodian | — | — |
| Workforce Member | — | — |
| Third Party | — | — |

Notes: "Approves" lists the default approver. CMP-008 moves to the ISSC where the CISO is
designated HIPAA Security Officer (‡). Documents whose README approver carries a qualifier
(ISSC with Audit Committee ratification of Risk Appetite for RSK-001; GC concurrence for CMP-004
and RES-003) are listed under the approving body. The concurring or ratifying role is shown in
the matching activity rows of section 5.3.

### 5.5 Segregation-of-duties check: owner is not approver

The check applies SUITE-REGISTER section A ("A document's owner SHALL NOT be its approver") and
GOV-001 SOD-01 to all 61 documents.

| Document | Owner | Approver | Result | Conditions that must hold for the result |
|---|---|---|---|---|
| ISP-000 | CISO | Board of Directors (via Audit Committee) | Pass |  |
| GOV-001 | CISO | CEO † (creates the ISSC) | Pass |  |
| GOV-002 | Head of GRC | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| GOV-003 | CISO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| GOV-004 | CISO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| GOV-006 | Head of GRC | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| RSK-001 | Head of GRC | ISSC (appetite ratified by Audit Committee) | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| RSK-002 | Head of GRC | CISO | Pass | Depends on the CISO + Head of GRC combination being prohibited (GOV-001.5.8.3) |
| RSK-003 | Head of GRC | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| RSK-004 | Business Continuity Manager | CISO | Pass |  |
| RSK-005 | SOC Manager | CISO | Pass |  |
| RSK-006 | CISO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| CMP-001 | Head of GRC | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| CMP-002 | Internal Audit Director | Audit Committee † | Pass |  |
| CMP-003 | Head of GRC | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| CMP-004 | Head of GRC | ISSC (GC concurrence) | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| CMP-005 | CPO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| CMP-006 | GC | Audit Committee † (SOX §301) | Pass |  |
| CMP-007 | CHRO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| CMP-008 | HIPAA Security Officer | CISO ‡ | Pass | Where the CISO is designated HIPAA Security Officer, the owner and approver would coincide; approval moves to the ISSC (README ‡, GOV-001.5.8.3), and the CISO recuses |
| CMP-009 | Head of GRC | CFO † (SOX §404) | Pass | Depends on the CFO + Head of GRC combination being prohibited (GOV-001.5.8.3) |
| CMP-010 | DPO | CPO | Pass | Depends on the DPO not holding the CPO role (GOV-001.5.6.4) |
| SEC-001 | CIO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| SEC-002 | CISO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| SEC-003 | CISO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| SEC-004 | Head of Security Engineering | CISO | Pass |  |
| SEC-005 | Head of Security Engineering | CISO | Pass |  |
| SEC-006 | Head of Security Engineering | ISSC | Pass |  |
| SEC-007 | Head of Security Engineering | ISSC | Pass |  |
| SEC-008 | CIO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| SEC-009 | CTO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| SEC-010 | CTO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| SEC-011 | Head of Security Engineering | ISSC | Pass |  |
| SEC-012 | SOC Manager | ISSC | Pass |  |
| SEC-013 | CIO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| SEC-014 | CIO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| SEC-015 | CISO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| SEC-016 | Head of Facilities | ISSC | Pass |  |
| SEC-017 | CIO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| SEC-018 | CIO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| SEC-019 | Head of Security Engineering | CISO | Pass |  |
| RES-001 | CISO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| RES-002 | SOC Manager | CISO | Pass | If the CISO + SOC Manager combination is used (below 250 Workforce Members), approval passes to the ISSC (GOV-001.5.8.3) |
| RES-003 | CPO | CISO (GC concurrence) | Pass |  |
| RES-004 | Business Continuity Manager | ISSC | Pass |  |
| RES-005 | CIO | Business Continuity Manager | Pass | Depends on the CIO not also holding the Business Continuity Manager role (not a permitted combination in GOV-001.5.8.3) |
| PPL-001 | CHRO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| PPL-002 | CISO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| TPL-001 | Head of GRC | CISO | Pass | Depends on the CISO + Head of GRC combination being prohibited (GOV-001.5.8.3) |
| TPL-002 | Head of GRC | CISO | Pass | Depends on the CISO + Head of GRC combination being prohibited (GOV-001.5.8.3) |
| TPL-003 | Head of GRC | CISO | Pass | Depends on the CISO + Head of GRC combination being prohibited (GOV-001.5.8.3) |
| TPL-004 | Head of GRC | CISO | Pass | Depends on the CISO + Head of GRC combination being prohibited (GOV-001.5.8.3) |
| TPL-005 | DPO | CPO | Pass | Depends on the DPO not holding the CPO role (GOV-001.5.6.4) |
| TPL-006 | SOC Manager | CISO | Pass | If the CISO + SOC Manager combination is used (below 250 Workforce Members), approval passes to the ISSC (GOV-001.5.8.3) |
| TPL-007 | SOC Manager | CISO | Pass | If the CISO + SOC Manager combination is used (below 250 Workforce Members), approval passes to the ISSC (GOV-001.5.8.3) |
| TPL-008 | Head of Security Engineering | CISO | Pass |  |
| TPL-009 | Head of GRC | CISO | Pass | Depends on the CISO + Head of GRC combination being prohibited (GOV-001.5.8.3) |
| TPL-010 | DPO | CPO | Pass | Depends on the DPO not holding the CPO role (GOV-001.5.6.4) |
| REF-001 | Head of GRC | CISO | Pass | Depends on the CISO + Head of GRC combination being prohibited (GOV-001.5.8.3) |
| REF-002 | Head of GRC | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |
| REF-003 | CISO | ISSC | Pass | Owner sits on the ISSC and recuses from the decision (GOV-001.5.3.9) |

Result: 0 of 61 documents fail the check. Where a document is approved by the ISSC and its
owner is an ISSC voting member or the Chair, segregation is preserved by the recusal rule in
GOV-001.5.3.9. Several results depend on role combinations staying prohibited or
conditional as set in GOV-001.5.8.3. The Head of GRC SHALL repeat this check every time the
role-assignment register records a new role combination.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| Head of GRC | Owns this document; maintains the matrix, ownership table and SoD check; records discrepancies; submits corrections to Document Owners. |
| ISSC | Approves this document and material changes to activity assignments. |
| CISO | As GOV-001's owner, corrects GOV-001 section 6.1 for discrepancies recorded in appendix A. |
| Document Owners | Keep section 6 of their documents consistent with this matrix; consult roles marked R or A when revising documents. |
| CHRO | Uses this matrix when confirming role accountabilities in job descriptions (GOV-001.5.4.7). |
| Internal Audit Director | Uses this matrix to identify Control Owners and to test SoD under CMP-002. |
| All role holders | Perform the activities marked R or A for their role. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| REF-002.7.1 | Accountable roles per activity | Exactly 1 |
| REF-002.7.2 | Matrix update after approval of a new or revised suite document, or a change to GOV-001 section 5.4 | Within 10 business days |
| REF-002.7.3 | GOV-001 correction submitted to the CISO after a discrepancy is recorded | Within 10 business days |
| REF-002.7.4 | Column names matching SUITE-REGISTER section B | 100% |
| REF-002.7.5 | Documents passing the owner ≠ approver check | 61 of 61 |
| REF-002.7.6 | Roles with an A or R in an applicable activity that have a named holder in the role-assignment register | 100% |
| REF-002.7.7 | Document review | As set in GOV-002, and on approval of any new suite document |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Activities with other than one A | 0 | On each update | Head of GRC |
| Open discrepancies in appendix A older than 90 days | 0 | Quarterly | Head of GRC |
| Documents failing the owner ≠ approver check | 0 | On each update and each new role combination | Head of GRC |
| Roles with A or R and no named holder | 0 | Every 12 months, with the role-assignment register review | Head of GRC |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003. The single-A rule
(REF-002.5.1.1) and the owner ≠ approver rule (section 5.5) SHALL NOT receive an Exception.

## 10. Enforcement

Non-compliance is handled under CMP-007.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| REF-002.5.1 – 5.3 | 5.3; A.5.2, A.5.4 | GV.RR-01, GV.RR-02 | PM-2, PM-29 | — | CC1.3, CC1.5 | APO01.02, EDM01 | `[HIPAA]` §164.308(a)(2); `[GDPR]` Art. 24; `[PCI]` 12.4.1 |
| REF-002.5.4 – 5.5 | 5.3; A.5.3 | GV.RR-02 | AC-5, PM-2 | — | CC1.3, CC5.1 | APO01.02, DSS06 | `[SOX]` §404; `[PCI]` 12.1.3 |

## 12. Related documents

ISP-000, GOV-001, GOV-002, GOV-006, CMP-002, CMP-003, CMP-007, REF-001, REF-003, and every suite
document cited in section 5.3.

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Head of GRC | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |

## Appendix A. Discrepancies between GOV-001 and topic documents

Under REF-002.5.2.3 the matrix follows the topic document. D-01 to D-05 have been resolved in
GOV-001 section 6.1, which now matches this matrix. D-06 and D-07 are informational and need no
change.

| # | Activity | GOV-001 (as originally drafted) | Topic document | REF-002 assignment | Resolution |
|---|---|---|---|---|---|
| D-01 | Ratify Risk Appetite and Risk Tolerance (RACI-RSK-01) | GOV-001 §6.1: ISSC = C | RSK-001.5.3.7: changes "SHALL be approved by the ISSC and ratified by the Audit Committee" | ISSC = R | Resolved in GOV-001 |
| D-02 | Respond to Sev-1 and Sev-2 Security Incidents (RACI-RES-03) | GOV-001 §6.1: CIO / CTO = R; SOC Manager not shown | RES-002 §6 and 5.4: the SOC Manager owns the Plan and the Incident Commander leads; the CIO receives Sev-1 notification and decides disaster declaration under RES-005; the CTO has no Sev-1 role | SOC Manager = R; CIO = C; CTO = I | Resolved in GOV-001 |
| D-03 | Run the security awareness and training program (RACI-PPL-04) | GOV-001 §6.1: CHRO = R; ISSC = I | PPL-002 §6: the CISO runs the program; the CHRO provides HRIS data and acts on non-completion; the ISSC approves the annual program plan | CISO = A/R (with Workforce Member R for completion); CHRO = C (and A for non-completion, RACI-PPL-06); ISSC = C | Resolved in GOV-001 |
| D-04 | Approve Exceptions (RACI-CMP-11 to RACI-CMP-14) | GOV-001 §6.1: one row with three "A" entries (CEO, ISSC, CISO by level); Low residual Risk omitted | CMP-003.5.4 and RSK-001.5.5: four authority levels, with the Risk Owner approving Low | Four rows, one A each; Low = Risk Owner (Asset Owner column) | Resolved in GOV-001 |
| D-05 | Approve Tier 2 Standards (RACI-GOV-12) | GOV-001 §6.1: CISO = A for all Tier 2 Standards | README † and ‡; CMP-009 §1: CMP-009 is approved by the CFO (SOX §404); CMP-008 by the ISSC where the CISO is HIPAA Security Officer | CISO = A, with the two exceptions stated in the activity and in section 5.4 | Resolved in GOV-001 |
| D-06 | Breach notification decision (RACI-RES-09); Sev-1 response; others | GOV-001 §6.1 combines "CPO / DPO" and "CIO / CTO" in single columns (e.g. CPO / DPO = A for breach notification) | RES-003 §6 and 5.2–5.3: the CPO leads and owns the determination; the DPO performs the `[GDPR]` risk assessment and submits supervisory authority notifications | CPO = A; DPO = R. Combined columns split in all rows using the topic document | Informational: no change needed if GOV-001 §6.1 notes that REF-002 splits combined columns |
| D-07 | Change management (RACI-SEC-25, RACI-SEC-26) | GOV-001.5.4.6: System Owner "accountable for ... Change (SEC-013)" | SEC-013.5.5 and §6: the CAB, set up and chaired by the CIO, approves Normal Changes and retrospectively approves Emergency Changes | Two activities: the System Owner is A for raising, testing and verifying Changes; the CIO (CAB) is A for change approval. Both statements hold, so neither document needs to change | Informational: no change needed |
