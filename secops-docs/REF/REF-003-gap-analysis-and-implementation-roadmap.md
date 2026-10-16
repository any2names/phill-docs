# REF-003 — Gap Analysis & Implementation Roadmap

## 1. Document control

| Field | Value |
|---|---|
| Document ID | REF-003 |
| Title | Gap Analysis & Implementation Roadmap |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | Ref — Master reference |
| Classification | Internal |
| Owner | Chief Information Security Officer (CISO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 3 months, then every 3 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-001, GOV-002, GOV-003, CMP-001, CMP-002, REF-001, REF-002, SUITE-REGISTER |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CISO | Initial release |

## 3. Purpose

This document tells an adopting Organization how to assess its current state against the suite
and how to implement the suite in phases. It is written for an Organization that has no formal
program and whose first assurance target is a SOC 2 Type II examination, followed by `[PCI]`,
`[HIPAA]` and `[SOX]` validation and, later, ISO/IEC 27001 certification. It gives a gap-assessment
method, a self-assessment table, a phased roadmap with entry and exit criteria, the document approval
sequence, dependencies, resourcing, tooling, program risks, tailoring guidance and pointers to the
adopter decisions.

The ISSC approves this roadmap and tracks it (GOV-001.5.3.10). The CISO refreshes it quarterly.

## 4. Scope

- **Organization:** the whole Organization within the scope set by ISP-000, at the design baseline in the README (enterprise, 1,000+ Workforce Members, hybrid cloud and on-premises, United States and EU/EEA, all conditional modules in force). Smaller adopters use section 5.9 and the role combinations in GOV-001.5.8.
- **Documents:** all 61 suite documents.
- **Starting point:** no formal program. Where artifacts already exist, they are mapped to suite IDs during the gap assessment (section 5.1) and reused if they meet the requirement.
- **Time horizon:** about 30 months from Phase 0 start to the end of Phase 5. Phase durations are targets, not requirements; phase exit criteria are requirements.
- **Out of scope:** detailed project plans, budgets and procurement, which the CISO maintains as working documents under this roadmap.

## 5. Gap analysis and roadmap

### 5.1 Gap-assessment method

- **REF-003.5.1.1** The CISO SHALL run a baseline gap assessment during Phase 0 and complete it by the Phase 1 exit. The Head of GRC SHALL refresh it every 3 months until the Phase 4 exit, and every 12 months after that.
- **REF-003.5.1.2** The assessment SHALL follow these steps:

| Step | Activity | Output | Responsible |
|---|---|---|---|
| 1 | Record the adopter decisions in SUITE-REGISTER section E and the conditional modules that apply (section 5.9) | Decision record; tailored document list | CISO, with GC and CFO |
| 2 | Collect existing policies, procedures, contracts, tool configurations and records, and map each to the suite document ID it would satisfy | Artifact-to-ID map | Head of GRC |
| 3 | For each key requirement in section 5.2, interview the accountable role (REF-002), inspect the artifact and sample Evidence | Status per row, with Evidence references | Head of GRC, with each owner |
| 4 | Rate each gap by the residual Risk it leaves, using the RSK-002 method, and by its priority (P1/P2/P3) | Rated gap list | Head of GRC |
| 5 | Assign each gap to a roadmap phase (section 5.3), respecting dependencies (section 5.5), with an owner and a target date | Gap remediation plan | CISO |
| 6 | Record gaps rated High or Critical in the Risk Register (RSK-001) until closed | Risk Register entries | Head of GRC |
| 7 | Report status and phase readiness to the ISSC | Quarterly roadmap report | CISO |

- **REF-003.5.1.3** Status SHALL be assigned using these definitions:

| Status | Definition |
|---|---|
| Not started | No documented requirement and no consistent practice exists. |
| Partial | A practice exists but is undocumented, inconsistent, or covers only part of the scope in the suite document. |
| Implemented | The requirement is documented in an approved suite document and operates across its full scope, but Evidence covering one full cycle of the control's frequency is not yet retained. |
| Evidenced | Implemented, with Evidence of operation retained under CMP-004 for at least one full cycle of the control's frequency, in a form that can be tested under CMP-002. |

- **REF-003.5.1.4** Only "Evidenced" counts toward a phase exit criterion that requires a control to be operating. A status SHALL NOT be raised without the Evidence reference recorded in the table.
- **REF-003.5.1.5** Where an existing artifact conflicts with a suite requirement, the suite requirement prevails once the suite document is approved. A deviation needed during transition SHALL be handled as an Exception under CMP-003, within the transition period set in GOV-002.

### 5.2 Self-assessment

#### 5.2.1 Self-assessment table

The table lists the key requirements per document that most affect the SOC 2 Type II examination
and the regulatory modules. "Target phase" is the phase by which the row SHOULD reach "Evidenced"
(or "Implemented" for documents approved in that phase). The Status, Evidence and Owner columns
are for the adopter to complete.

| ID | Document | Pri | Target phase | Requirement | Key requirement | Status | Evidence | Owner |
|---|---|---|---|---|---|---|---|---|
| SA-001 | ISP-000 | P1 | Phase 0 | ISP-000.5.1, 5.7 | Charter approved by the Board of Directors; Board oversight and reporting lines in place | | | |
| SA-002 | ISP-000 | P1 | Phase 0 | ISP-000.5.5, 5.8 | Risk appetite stated; annual management review performed | | | |
| SA-003 | GOV-001 | P1 | Phase 0 | GOV-001.5.1 | Every applicable role assigned to a named holder and deputy in the role-assignment register | | | |
| SA-004 | GOV-001 | P1 | Phase 0 | GOV-001.5.3 | ISSC constituted, meeting at the required cadence, with minutes | | | |
| SA-005 | GOV-001 | P1 | Phase 2 | GOV-001.5.7 | Segregation of Duties matrix enforced in system roles | | | |
| SA-006 | GOV-002 | P1 | Phase 0 | GOV-002.5.5, 5.7 | Documents approved by the correct approver and reviewed on schedule | | | |
| SA-007 | GOV-002 | P1 | Phase 1 | GOV-002.5.9 | Workforce attestation at hire and annually | | | |
| SA-008 | GOV-003 | P2 | Phase 2 | GOV-003.5.3, 5.5 | KPI/KRI catalogue defined; reports issued at the cadence in GOV-003 | | | |
| SA-009 | GOV-004 | P1 | Phase 1 | GOV-004.5.1 – 5.15 | Acceptable Use Policy published and attested by all Workforce Members | | | |
| SA-010 | GOV-006 | P1 | Phase 0 | GOV-006.5.1 | Glossary approved; suite documents use defined terms only | | | |
| SA-011 | RSK-001 | P1 | Phase 1 | RSK-001.5.2, 5.6 | Risk Register established with a Risk Owner per Risk; ISSC review held | | | |
| SA-012 | RSK-001 | P1 | Phase 1 | RSK-001.5.5 | Risk Acceptances approved at the correct authority using TPL-002 | | | |
| SA-013 | RSK-002 | P1 | Phase 1 | RSK-002.5.1 – 5.6 | Enterprise risk assessment performed with the RSK-002 method and approved | | | |
| SA-014 | RSK-002 | P1 | Phase 1 | RSK-002.5.10 | Fraud risk, including management override of Controls, assessed and fraud scenarios recorded in the Risk Register | | | |
| SA-015 | RSK-002 | P1 | Phase 2 | RSK-002.5.8 | `[PCI]` Targeted risk analyses documented | | | |
| SA-016 | RSK-003 | P1 | Phase 2 | RSK-003.5.1 – 5.3 | Third-party inventory tiered; due diligence completed before contract | | | |
| SA-017 | RSK-003 | P1 | Phase 2 | RSK-003.5.4 – 5.5 | Contract security terms in place; reassessment at tier frequency | | | |
| SA-018 | RSK-004 | P1 | Phase 2 | RSK-004.5.1 – 5.7 | BIA completed; Recovery Tiers assigned and Tier 0/1 approved by ISSC | | | |
| SA-019 | RSK-005 | P3 | Phase 5 | RSK-005.5.1, 5.6 | Threat profile maintained; threat models produced for in-scope systems | | | |
| SA-020 | RSK-006 | P2 | Phase 5 | RSK-006.5.2 – 5.5 | AI System inventory, risk classes and approved Generative AI tools list | | | |
| SA-021 | CMP-001 | P1 | Phase 1 | CMP-001.5.2 – 5.3 | Obligations Register populated with GC-approved applicability determinations | | | |
| SA-022 | CMP-001 | P1 | Phase 1 | CMP-001.5.6 | External assessment calendar (SOC 2, `[PCI]`, `[HIPAA]`, `[SOX]`) scoped and approved | | | |
| SA-023 | CMP-002 | P2 | Phase 2 | CMP-002.5.3, 5.5 | Key Control self-assessment and second-line testing operating | | | |
| SA-024 | CMP-002 | P2 | Phase 2 | CMP-002.5.8 | Issue register with remediation tracking | | | |
| SA-025 | CMP-003 | P1 | Phase 1 | CMP-003.5.4, 5.8 | Exceptions approved at the correct authority and recorded in the register | | | |
| SA-026 | CMP-004 | P1 | Phase 1 | CMP-004.5.2, 5.7 | Retention schedule approved; Evidence repository in use | | | |
| SA-027 | CMP-004 | P1 | Phase 1 | CMP-004.5.4 | Legal Hold process and register operating | | | |
| SA-028 | CMP-005 | P1 | Phase 1 | CMP-005.5.8, 5.9 | `[GDPR]` ROPA complete; DPIAs performed when required | | | |
| SA-029 | CMP-005 | P1 | Phase 1 | CMP-005.5.11 – 5.13 | Processor agreements and transfer mechanisms in place; `[CPRA]` opt-outs honored | | | |
| SA-030 | CMP-006 | P1 | Phase 2 | CMP-006.5.2 – 5.4 | Reporting channels operating; reports triaged and investigated | | | |
| SA-031 | CMP-006 | P1 | Phase 2 | CMP-006.5.7 | `[SOX]` Audit Committee complaint procedures operating | | | |
| SA-032 | CMP-007 | P1 | Phase 1 | CMP-007.5.3 – 5.4 | Sanctions matrix and due process applied and recorded | | | |
| SA-033 | CMP-008 | P1 | Phase 1 | CMP-008.5.2 – 5.5 | `[HIPAA]` Security Officer designated; ePHI risk analysis and addressable decisions documented | | | |
| SA-034 | CMP-008 | P1 | Phase 4 | CMP-008.5.11 | `[HIPAA]` Security Rule evaluation completed | | | |
| SA-035 | CMP-009 | P1 | Phase 1 | CMP-009.5.2 | `[SOX]` Financially Significant Systems scoped and approved by the CFO | | | |
| SA-036 | CMP-009 | P1 | Phase 2 | CMP-009.5.4 – 5.7 | `[SOX]` ITGC Key Controls operating and tested | | | |
| SA-037 | CMP-010 | P1 | Phase 1 | CMP-010.5.1 – 5.3, 5.13 | `[GDPR]` `[CPRA]` DSR intake, logging and deadline tracking operating | | | |
| SA-038 | SEC-001 | P1 | Phase 1 | SEC-001.5.1 – 5.4 | Asset Inventory complete with owners, classification and Recovery Tier | | | |
| SA-039 | SEC-001 | P1 | Phase 2 | SEC-001.5.9 | Inventory reconciled against discovery sources | | | |
| SA-040 | SEC-002 | P1 | Phase 1 | SEC-002.5.1 – 5.4 | Classification Levels applied by Data Owners; handling matrix enforced | | | |
| SA-041 | SEC-002 | P1 | Phase 2 | SEC-002.5.5 | DLP and data discovery operating | | | |
| SA-042 | SEC-003 | P1 | Phase 2 | SEC-003.5.2 – 5.7 | Joiner, mover and leaver access processes driven by HR events | | | |
| SA-043 | SEC-003 | P1 | Phase 2 | SEC-003.5.12 | User Access Reviews performed at the SEC-003 frequency (TPL-008) | | | |
| SA-044 | SEC-004 | P1 | Phase 2 | SEC-004.5.4 – 5.5 | MFA and SSO enforced for all required access | | | |
| SA-045 | SEC-004 | P1 | Phase 2 | SEC-004.5.10 | Secrets removed from code and configuration | | | |
| SA-046 | SEC-005 | P1 | Phase 2 | SEC-005.5.1 – 5.4 | Privileged Accounts inventoried, vaulted and granted Just-in-Time | | | |
| SA-047 | SEC-005 | P1 | Phase 2 | SEC-005.5.7, 5.11 | Break-glass Accounts tested; privileged access reviewed | | | |
| SA-048 | SEC-006 | P1 | Phase 2 | SEC-006.5.2 | Approved algorithms and protocols enforced at rest and in transit | | | |
| SA-049 | SEC-006 | P1 | Phase 2 | SEC-006.5.3 – 5.9 | Key and certificate inventory; key lifecycle managed | | | |
| SA-050 | SEC-007 | P1 | Phase 2 | SEC-007.5.1 – 5.3 | Trust zones, default deny and rule reviews in place | | | |
| SA-051 | SEC-007 | P1 | Phase 2 | SEC-007.5.4, 5.8 | Remote access controlled; network diagrams current | | | |
| SA-052 | SEC-008 | P1 | Phase 2 | SEC-008.5.1 – 5.4 | Endpoints enrolled, hardened, encrypted and running EDR | | | |
| SA-053 | SEC-008 | P1 | Phase 2 | SEC-008.5.5 – 5.6 | Endpoint patching and no standing local administrator rights | | | |
| SA-054 | SEC-009 | P1 | Phase 2 | SEC-009.5.2 – 5.5 | Approved Cloud Services, landing zone, guardrails and CSPM operating | | | |
| SA-055 | SEC-010 | P1 | Phase 2 | SEC-010.5.4 – 5.6 | Code review, security testing gates and pipeline integrity enforced | | | |
| SA-056 | SEC-011 | P1 | Phase 2 | SEC-011.5.2, 5.4 | Vulnerability scanning and remediation within the SEC-011 SLA | | | |
| SA-057 | SEC-011 | P1 | Phase 3 | SEC-011.5.7 | Penetration Test completed and findings tracked | | | |
| SA-058 | SEC-012 | P1 | Phase 2 | SEC-012.5.2, 5.6 | Required log sources centralized in the SIEM | | | |
| SA-059 | SEC-012 | P1 | Phase 2 | SEC-012.5.8 – 5.9 | Alert triage within SLA; log review operating | | | |
| SA-060 | SEC-013 | P1 | Phase 2 | SEC-013.5.2 – 5.7 | Change classes, CAB approval and post-implementation review operating | | | |
| SA-061 | SEC-013 | P1 | Phase 2 | SEC-013.5.8 – 5.9 | Configuration Baselines and drift detection | | | |
| SA-062 | SEC-013 | P1 | Phase 2 | SEC-013.5.12 | Capacity thresholds monitored and capacity forecasts produced for in-scope systems | | | |
| SA-063 | SEC-014 | P2 | Phase 5 | SEC-014.5.1 – 5.3 | SPF, DKIM and DMARC enforced; anti-phishing controls | | | |
| SA-064 | SEC-015 | P3 | Phase 5 | SEC-015.5.1 – 5.5 | Remote work and high-risk travel controls | | | |
| SA-065 | SEC-016 | P1 | Phase 2 | SEC-016.5.1 – 5.5 | Physical zones, badge access, visitors and CCTV | | | |
| SA-066 | SEC-016 | P1 | Phase 2 | SEC-016.5.7 | Environmental controls monitored and tested | | | |
| SA-067 | SEC-017 | P1 | Phase 2 | SEC-017.5.2 – 5.5 | Media Sanitization by method with Certificates of Destruction | | | |
| SA-068 | SEC-018 | P1 | Phase 2 | SEC-018.5.2 – 5.4 | Backups at Recovery Tier frequency, 3-2-1-1-0 and encrypted | | | |
| SA-069 | SEC-018 | P1 | Phase 2 | SEC-018.5.6 | Restore tests at the SEC-018 frequency | | | |
| SA-070 | SEC-019 | P1 | Phase 2 | SEC-019.5.1 – 5.4 | `[PCI]` CDE scope confirmed; diagrams and segmentation tested | | | |
| SA-071 | SEC-019 | P1 | Phase 2 | SEC-019.5.8 – 5.9 | `[PCI]` Payment page script integrity and POI inspections | | | |
| SA-072 | RES-001 | P1 | Phase 2 | RES-001.5.1 – 5.3 | Incident response capability, reporting channel and Incident Commander roster | | | |
| SA-073 | RES-002 | P1 | Phase 2 | RES-002.5.2 – 5.10 | Incidents classified, handled within SLA and reviewed (TPL-006, TPL-007) | | | |
| SA-074 | RES-002 | P1 | Phase 3 | RES-002.5.14 | Incident response exercise completed | | | |
| SA-075 | RES-003 | P1 | Phase 2 | RES-003.5.1 – 5.2, 5.6 | Breach escalation, determination group and notification matrix ready | | | |
| SA-076 | RES-004 | P1 | Phase 2 | RES-004.5.4 – 5.5 | Crisis Management Team and business continuity plans in place | | | |
| SA-077 | RES-004 | P1 | Phase 3 | RES-004.5.11 | Business continuity exercise completed | | | |
| SA-078 | RES-005 | P1 | Phase 2 | RES-005.5.1 – 5.4 | DR organization, runbooks and recovery sequencing by tier | | | |
| SA-079 | RES-005 | P1 | Phase 3 | RES-005.5.10 | DR test of Tier 0 and Tier 1 systems completed | | | |
| SA-080 | PPL-001 | P1 | Phase 1 | PPL-001.5.2 – 5.3 | Screening and signed terms before access | | | |
| SA-081 | PPL-001 | P1 | Phase 1 | PPL-001.5.7 | Separation process: asset return and access closure | | | |
| SA-082 | PPL-002 | P1 | Phase 1 | PPL-002.5.2 – 5.3 | Training at hire and annual training completed | | | |
| SA-083 | PPL-002 | P1 | Phase 2 | PPL-002.5.4 – 5.5 | Role-based training and phishing simulations | | | |
| SA-084 | TPL-001, 002, 003, 009 | P1 | Phase 1 | TPL-001 – TPL-003, TPL-009 | Risk register, risk acceptance, exception and acknowledgement templates in use | | | |
| SA-085 | TPL-005, 008, 010 | P1 | Phase 1 | TPL-005, TPL-008, TPL-010 | DPIA, access review and ROPA templates in use | | | |
| SA-086 | TPL-004, 006, 007 | P1 | Phase 2 | TPL-004, TPL-006, TPL-007 | Vendor questionnaire, incident report and post-incident review templates in use | | | |
| SA-087 | REF-001 | P1 | Phase 3 | REF-001.5.1.4 | Key Control list approved by the CISO | | | |
| SA-088 | REF-002 | P1 | Phase 1 | REF-002.5.2 | RACI approved; every A/R role has a named holder | | | |

#### 5.2.2 Suite-level gaps carried from REF-001

REF-001 section 5.11 found the following gaps in the suite itself. G-01 and G-02 are closed in the
suite documents; G-03 to G-05 remain open until the documents named are revised.

| Gap | Summary | Close by | Owner |
|---|---|---|---|
| G-01 | Capacity management (ISO A.8.6; SOC 2 A1.1). **Closed in the suite:** SEC-013 section 5.12 added. Adopters SHALL still implement and evidence it (self-assessment row for SEC-013.5.12) | Closed in suite; implementation by Phase 2 exit | CIO; System Owners |
| G-02 | Fraud risk in risk assessment (SOC 2 CC3.3). **Closed in the suite:** RSK-002 section 5.10 added. Adopters SHALL still implement and evidence it (self-assessment row for RSK-002.5.10) | Closed in suite; implementation by Phase 1 exit | Head of GRC, CFO consulted |
| G-03 | Labelling relies on one subsection (ISO A.5.13) | Before an ISO/IEC 27001 Stage 2 audit (Phase 5) | CISO |
| G-04 | Five NIST CSF 2.0 subcategories not cited | Next revision of RSK-001, RSK-003, RES-002 | Head of GRC |
| G-05 | ISO A.8.34 mapped only in REF-001 | Next revision of CMP-002 and SEC-011 | Head of GRC |

### 5.3 Phased roadmap

- **REF-003.5.3.1** The program SHALL be delivered in the six phases below. A phase starts when its entry criteria are met, and the ISSC SHALL confirm its exit criteria before the phase is closed. Phases MAY overlap where entry criteria allow it.
- **REF-003.5.3.2** Phase targets are counted from the date the CEO approves the start of Phase 0. [ASSUMPTION: The Organization funds the roles in section 5.6 and the tooling in section 5.7 by the start of the phase that needs them.]

| Phase | Name | Target window | Entry criteria | Exit criteria (ISSC-confirmed) |
|---|---|---|---|---|
| 0 | Mobilize | Day 0 – 30 | CEO sponsorship recorded; interim CISO or program lead named; mobilization budget approved | ISP-000 approved by the Board of Directors; GOV-001 approved by the CEO; ISSC constituted and first meeting held with quorum; GOV-002, GOV-006 and REF-003 approved by the ISSC; CISO, Head of GRC and ISSC members named in the role-assignment register; statutory officer designations decided (GOV-001.5.5); adopter decisions #1–#8 recorded (section 5.10); baseline gap assessment started |
| 1 | Foundation | Day 30 – 90 | Phase 0 exit criteria met | Phase 1 documents in section 5.4 approved; REF-002 approved; baseline gap assessment complete; Obligations Register and applicability determinations complete (CMP-001); first enterprise risk assessment approved and Risk Register established (RSK-001, RSK-002); Asset Inventory covers all production Information Systems with owners and Classification Levels (SEC-001, SEC-002); Exception and Risk Acceptance processes operating; Workforce attestation and awareness training launched (GOV-002, PPL-002); identity provider and MFA rollout plan approved; GRC platform and Evidence repository live (CMP-004) |
| 2 | Control implementation | Month 3 – 6 | Phase 1 exit criteria met for the dependencies in section 5.5 | Phase 2 documents in section 5.4 approved; tooling in section 5.7 marked "Phase 2" in production; SSO and MFA enforced (SEC-004); PAM for Tier 0 privilege (SEC-005); EDR and endpoint encryption at the coverage set in SEC-008; SIEM with required log sources and 24×7 triage (SEC-012); vulnerability scanning and remediation tracking (SEC-011); CAB operating (SEC-013); BIA approved before Backup and DR implementation (RSK-004); restore test performed (SEC-018); third-party due diligence for existing Tier 1 and Tier 2 vendors (RSK-003); first User Access Review completed (SEC-003); every Key Control in REF-001 section 5.4 at least "Implemented" |
| 3 | SOC 2 readiness and observation start | Month 6 – 9 | Phase 2 exit criteria met; service auditor selected | Readiness Assessment (independent of the control operators) completed and High findings remediated; Key Control list approved by the CISO (REF-001.5.1.4); system description drafted; every Key Control "Evidenced" for one full cycle of its frequency; annual controls (Penetration Test, IR exercise, BC exercise, DR test, enterprise risk assessment) scheduled inside the Observation Period; Observation Period started on the date agreed with the service auditor |
| 4 | Type II period, report and regulatory validation | Month 9 – 18 | Observation Period started | SOC 2 Type II report issued for the first period set in CMP-001; exceptions noted by the service auditor remediated under CMP-002; `[PCI]` PCI DSS validation completed and AOC submitted (CMP-001, SEC-019); `[HIPAA]` ePHI risk analysis and Security Rule evaluation completed (CMP-008); `[SOX]` ITGC assessment completed for the fiscal year (CMP-009); next continuous 12-month SOC 2 period started (CMP-001) |
| 5 | Optimize | Month 18 – 30 | Phase 4 exit criteria met | P2 and P3 documents not already approved are approved (SEC-014, SEC-015, RSK-005, RSK-006 where not done earlier); REF-001 gaps G-03 to G-05 closed; ISO/IEC 27001 decision taken by the ISSC and, if pursued, Statement of Applicability derived from REF-001 and Stage 1 audit passed; metric targets in GOV-003 met for 2 consecutive quarters |

#### 5.3.1 Phase 0 — Mobilize (day 0 – 30)

1. The CEO names the CISO (or an interim lead) and approves the mobilization budget.
2. The CISO and the Head of GRC (once named) tailor the suite (section 5.9) and propose adopter decisions (section 5.10).
3. The CISO presents ISP-000 to the Audit Committee for recommendation and to the Board of Directors for approval.
4. The CEO approves GOV-001, which creates the ISSC, designates statutory officers and records role combinations.
5. The ISSC holds its first meeting. It approves GOV-002, GOV-006 and this roadmap, and records the adopter decisions.
6. The Head of GRC opens the role-assignment register, the suite repository (GOV-002) and the baseline gap assessment (section 5.1).

#### 5.3.2 Phase 1 — Foundation (day 30 – 90)

1. Approve the Phase 1 documents in the order in section 5.4.
2. Build the Obligations Register and compliance calendar (CMP-001). Confirm PCI DSS entity type and level, HIPAA status and SOX scope.
3. Build the Asset Inventory and apply Classification Levels (SEC-001, SEC-002). Scope the `[SOX]` Financially Significant Systems (CMP-009) and the `[PCI]` CDE (SEC-019) from it.
4. Run the first enterprise risk assessment (RSK-002) and set up the Risk Register (RSK-001, TPL-001).
5. Turn on the Exception (CMP-003, TPL-003), Risk Acceptance (TPL-002) and enforcement (CMP-007) processes.
6. Launch the attestation campaign (GOV-002, GOV-004, TPL-009) and awareness training (PPL-002). Align screening and separation with HR (PPL-001).
7. Select and deploy the GRC platform and Evidence repository (CMP-004). Start the identity provider and MFA rollout (SEC-004).
8. `[GDPR]` `[CPRA]` Complete the ROPA (TPL-010). Set up DSR intake (CMP-010) and the DPIA process (TPL-005).

#### 5.3.3 Phase 2 — Control implementation (month 3 – 6)

1. Approve the Phase 2 documents in the order in section 5.4, including the pulled-forward documents GOV-003, CMP-002 and TPL-007.
2. Deploy the Phase 2 tooling (section 5.7) and implement the SEC-series controls.
3. Complete the BIA (RSK-004) before setting Backup schedules (SEC-018) and DR runbooks (RES-005).
4. Run the first User Access Review (SEC-003, TPL-008) after SSO consolidation, and the first privileged access review (SEC-005).
5. Assess existing vendors by tier (RSK-003, TPL-004). Put security terms into contracts at renewal or by amendment.
6. Set up the incident response roster and run a tabletop (RES-001, RES-002). Prepare breach notification templates (RES-003).
7. Start Key Control self-assessment and second-line testing (CMP-002). Collect Key Control Evidence into the repository (CMP-004).

#### 5.3.4 Phase 3 — SOC 2 readiness and observation start (month 6 – 9)

1. Commission a Readiness Assessment. It is performed by a Third Party, or by the Internal Audit Director under CMP-002, and not by anyone who operates the controls (GOV-001 SOD-07).
2. Remediate High readiness findings; record others with remediation plans under CMP-002.
3. The CISO approves the Key Control list (REF-001.5.1.4). The Head of GRC drafts the system description and the complementary user entity control list for Cloud Services (SEC-009).
4. Engage the service auditor under CMP-001. Agree scope (SUITE-REGISTER decision #2) and the Observation Period start date.
5. Schedule the annual controls inside the Observation Period so that each operates at least once in it.

#### 5.3.5 Phase 4 — Type II period, report and regulatory validation (month 9 – 18)

1. Operate all Key Controls and collect Evidence continuously. Test them at the frequency in CMP-002.
2. Respond to service auditor requests within the times set in CMP-002. Remediate exceptions.
3. `[PCI]` Complete the PCI DSS assessment (ROC or SAQ per SUITE-REGISTER decision #4) and submit the AOC.
4. `[HIPAA]` Complete the ePHI risk analysis and the Security Rule evaluation (CMP-008).
5. `[SOX]` Test ITGC Key Controls and support the CFO's assessment (CMP-009).
6. Issue the SOC 2 Type II report and start the next continuous period (CMP-001).

#### 5.3.6 Phase 5 — Optimize (month 18 – 30)

1. Approve the remaining P2 and P3 documents (section 5.4).
2. Close REF-001 gaps G-03 to G-05.
3. The ISSC decides on ISO/IEC 27001 certification. If pursued: define the ISMS scope, derive the Statement of Applicability from REF-001 section 5.5 (REF-001.5.1.7), run an internal audit of the ISMS (CMP-002), hold a management review, and complete the Stage 1 and Stage 2 audits.
4. Move metrics from coverage to effectiveness (GOV-003). Consider adding Privacy to SOC 2 scope.

### 5.4 Document approval sequence

The README build order is the drafting order. The approval order differs only where an approving
body is created by a later document (the ISSC is created by GOV-001) or where a P2 document
underpins a Key Control. Within a phase, documents SHOULD be approved in the order shown. Approvers
are as listed in the README.

| Seq. | ID | Title | Tier | Approver | Pri | Build # | Target phase | Notes |
|---|---|---|---|---|---|---|---|---|
| 1 | ISP-000 | Information Security Program Charter | 0 | Board of Directors (via Audit Committee) | P1 | 2 | Phase 0 | Approved by the Board of Directors on Audit Committee recommendation |
| 2 | GOV-001 | Security Governance & Organization Policy | 1 | CEO † (creates the ISSC) | P1 | 3 | Phase 0 | Approval by the CEO creates the ISSC |
| 3 | GOV-002 | Policy Management Policy | 1 | ISSC | P1 | 4 | Phase 0 | First ISSC approval |
| 4 | GOV-006 | Glossary & Definitions | 1 (Ref) | ISSC | P1 | 1 | Phase 0 | Drafted first (build 1) but approved by the ISSC, so approval follows GOV-001 |
| 5 | REF-003 | Gap Analysis & Implementation Roadmap | Ref | ISSC | P1 | 61 | Phase 0 | Approved by the ISSC at its first meeting as the program plan; refreshed quarterly |
| 6 | RSK-001 | Risk Management Policy | 1 | ISSC (appetite ratified by Audit Committee) | P1 | 5 | Phase 1 |  |
| 7 | RSK-002 | Risk Assessment Standard | 2 | CISO | P1 | 6 | Phase 1 |  |
| 8 | CMP-003 | Policy Exception & Waiver Policy | 1 | ISSC | P1 | 7 | Phase 1 |  |
| 9 | CMP-007 | Enforcement & Disciplinary Policy | 1 | ISSC | P1 | 8 | Phase 1 |  |
| 10 | TPL-001 | Risk Register Template | T | CISO | P1 | 9 | Phase 1 |  |
| 11 | TPL-002 | Risk Acceptance Form | T | CISO | P1 | 10 | Phase 1 |  |
| 12 | TPL-003 | Policy Exception Request Form | T | CISO | P1 | 11 | Phase 1 |  |
| 13 | SEC-002 | Data Classification & Handling Policy | 1 | ISSC | P1 | 12 | Phase 1 | Approved before SEC-006, SEC-014, SEC-017 and CMP-004 handling rules are implemented |
| 14 | SEC-001 | Asset Management Policy | 1 | ISSC | P1 | 13 | Phase 1 |  |
| 15 | CMP-001 | Compliance Management Policy | 1 | ISSC | P1 | 14 | Phase 1 |  |
| 16 | CMP-004 | Evidence Management & Records Retention Policy | 1 | ISSC (GC concurrence) | P1 | 15 | Phase 1 |  |
| 17 | CMP-005 | Data Privacy & Protection Policy | 1 | ISSC | P1 | 16 | Phase 1 |  |
| 18 | CMP-010 | Data Subject Request Procedure | 3 | CPO | P1 | 17 | Phase 1 |  |
| 19 | TPL-005 | Data Protection Impact Assessment Template | T | CPO | P1 | 18 | Phase 1 |  |
| 20 | TPL-010 | Record of Processing Activities Template | T | CPO | P1 | 19 | Phase 1 |  |
| 21 | CMP-008 | HIPAA Security Rule Implementation Standard | 2 | CISO ‡ | P1 | 20 | Phase 1 |  |
| 22 | CMP-009 | SOX IT General Controls Standard | 2 | CFO † (SOX §404) | P1 | 21 | Phase 1 |  |
| 23 | GOV-004 | Acceptable Use Policy (absorbs GOV-005) | 1 | ISSC | P1 | 22 | Phase 1 |  |
| 24 | PPL-001 | Human Resources Security Policy | 1 | ISSC | P1 | 23 | Phase 1 |  |
| 25 | PPL-002 | Security Awareness & Training Policy | 1 | ISSC | P1 | 24 | Phase 1 |  |
| 26 | TPL-009 | Policy Acknowledgement Form | T | CISO | P1 | 25 | Phase 1 |  |
| 27 | SEC-003 | Identity & Access Management Policy | 1 | ISSC | P1 | 26 | Phase 1 |  |
| 28 | SEC-004 | Password & Authentication Standard | 2 | CISO | P1 | 27 | Phase 1 | IdP and MFA configuration standard; implementation is on the critical path for SEC-003 Access Reviews |
| 29 | SEC-005 | Privileged Access Management Standard | 2 | CISO | P1 | 28 | Phase 1 |  |
| 30 | TPL-008 | Access Review Template | T | CISO | P1 | 29 | Phase 1 |  |
| 31 | REF-002 | Master RACI Matrix | Ref | ISSC | P1 | 59 | Phase 1 | Needed by Document Owners for consultation under GOV-002.5.4.1 |
| 32 | SEC-006 | Cryptography & Key Management Policy | 1 | ISSC | P1 | 30 | Phase 2 |  |
| 33 | SEC-007 | Network Security Policy | 1 | ISSC | P1 | 31 | Phase 2 |  |
| 34 | SEC-019 | Cardholder Data Environment Standard | 2 | CISO | P1 | 32 | Phase 2 |  |
| 35 | SEC-008 | Endpoint & Mobile Device Security Policy (incl. BYOD) | 1 | ISSC | P1 | 33 | Phase 2 |  |
| 36 | SEC-009 | Cloud Security Policy | 1 | ISSC | P1 | 34 | Phase 2 |  |
| 37 | SEC-010 | Secure Software Development Lifecycle Policy | 1 | ISSC | P1 | 35 | Phase 2 |  |
| 38 | SEC-011 | Vulnerability & Patch Management Policy | 1 | ISSC | P1 | 36 | Phase 2 |  |
| 39 | SEC-012 | Logging & Monitoring Policy | 1 | ISSC | P1 | 37 | Phase 2 |  |
| 40 | SEC-013 | Change & Configuration Management Policy | 1 | ISSC | P1 | 38 | Phase 2 |  |
| 41 | RSK-004 | Business Impact Analysis Standard | 2 | CISO | P1 | 39 | Phase 2 | Approved before SEC-018 and RES-005 so Recovery Tiers have one source |
| 42 | SEC-018 | Backup Policy | 1 | ISSC | P1 | 40 | Phase 2 |  |
| 43 | SEC-016 | Physical & Environmental Security Policy | 1 | ISSC | P1 | 41 | Phase 2 |  |
| 44 | SEC-017 | Media Sanitization & Secure Disposal Policy | 1 | ISSC | P1 | 42 | Phase 2 |  |
| 45 | RSK-003 | Third-Party & Supply Chain Risk Management Policy | 1 | ISSC | P1 | 43 | Phase 2 |  |
| 46 | TPL-004 | Vendor Security Questionnaire | T | CISO | P1 | 44 | Phase 2 |  |
| 47 | RES-001 | Incident Response Policy | 1 | ISSC | P1 | 45 | Phase 2 |  |
| 48 | RES-002 | Incident Response Plan | 3 | CISO | P1 | 46 | Phase 2 |  |
| 49 | RES-003 | Breach Notification Standard | 2 | CISO (GC concurrence) | P1 | 47 | Phase 2 |  |
| 50 | TPL-006 | Incident Report Template | T | CISO | P1 | 48 | Phase 2 |  |
| 51 | TPL-007 | Post-Incident Review Template | T | CISO | P2 | 49 | Phase 2 | P2 in README; pulled forward because the post-incident review Key Control (RES-002.5.10) uses it |
| 52 | RES-004 | Business Continuity Policy | 1 | ISSC | P1 | 50 | Phase 2 |  |
| 53 | RES-005 | Disaster Recovery Plan | 3 | Business Continuity Manager | P1 | 51 | Phase 2 |  |
| 54 | CMP-006 | Whistleblower & Security Concern Reporting Policy | 1 | Audit Committee † (SOX §301) | P1 | 52 | Phase 2 |  |
| 55 | GOV-003 | Security Metrics & Reporting Policy | 1 | ISSC | P2 | 53 | Phase 2 | P2 in README; pulled forward because KC-08 (metrics reporting) and the CISO reports in GOV-001.5.2.2 depend on it |
| 56 | CMP-002 | Internal Audit & Control Testing Policy | 1 | Audit Committee † | P2 | 54 | Phase 2 | P2 in README; pulled forward because Key Control testing and deficiency tracking (CC4.1, CC4.2) depend on it |
| 57 | RSK-006 | AI & Emerging Technology Risk Policy | 1 | ISSC | P2 | 58 | Phase 2 | Phase 2 where Generative AI tools are in use (README); otherwise Phase 5 |
| 58 | REF-001 | Control Mapping Matrix | Ref | CISO | P1 | 60 | Phase 3 | Key Control list approved before the Observation Period (REF-001.5.1.4); draft mapping used from Phase 1 |
| 59 | SEC-014 | Email & Communications Security Policy | 1 | ISSC | P2 | 55 | Phase 5 |  |
| 60 | SEC-015 | Remote Work & Travel Security Policy | 1 | ISSC | P3 | 56 | Phase 5 |  |
| 61 | RSK-005 | Threat Intelligence & Threat Modeling Standard | 2 | CISO | P3 | 57 | Phase 5 |  |

Documents per target phase: Phase 0: 5 · Phase 1: 26 · Phase 2: 26 · Phase 3: 1 · Phase 5: 3. No document approval is planned for Phase 4.

### 5.5 Dependencies and critical path

#### 5.5.1 Dependencies

| # | Predecessor | Successor | Why |
|---|---|---|---|
| D1 | GOV-006 terms; GOV-001 (creates the ISSC) | Every Tier 1 approval | Tier 1 Policies are approved by the ISSC (GOV-002) |
| D2 | RSK-001 and RSK-002 (risk levels, acceptance authority) | CMP-003 Exceptions; all Risk Acceptances | Exception authority follows residual Risk level (CMP-003) |
| D3 | SEC-001 Asset Inventory | SEC-011 scan coverage; SEC-012 log source register; RSK-004 BIA; CMP-009 scoping; SEC-019 CDE scope | All these populations come from the inventory |
| D4 | SEC-002 classification | SEC-006 encryption; SEC-014 email encryption; SEC-017 sanitization; SEC-002.5.5 DLP; CMP-004 retention; SEC-003 access approval for Restricted data | Handling controls are set by Classification Level |
| D5 | RSK-004 BIA (Recovery Tiers, RTO/RPO) | SEC-018 Backup frequency and restore testing; RES-004 continuity strategies; RES-005 DR runbooks and tests | Recovery values have one source (README build order) |
| D6 | PPL-001 HR events in the HR system of record | SEC-003 joiner, mover, leaver automation | Revocation timing in SEC-003 depends on HR events being recorded by their effective date (SEC-003 §6) |
| D7 | SEC-004 identity provider, SSO and MFA | SEC-003 Access Reviews; SEC-005 PAM; TPL-008; SEC-009 identity federation | Reviews need a central, authoritative account source |
| D8 | SEC-012 SIEM and log sources | RES-002 detection and analysis; SEC-005 privileged session monitoring; SEC-012.5.9 log review | Detection and review depend on centralized logs |
| D9 | SEC-013 change management | SEC-010 pipeline approvals; `[SOX]` CMP-009 program change; `[PCI]` SEC-019 change controls | Change Evidence must exist before it can be tested |
| D10 | RSK-003 due diligence | SEC-009 Cloud Service approval; CMP-005 Processor agreements | Vendors are assessed before onboarding |
| D11 | CMP-004 Evidence repository | Phase 3 readiness; the Observation Period | Evidence must be retained from the first day of the period |
| D12 | CMP-002 testing; GOV-003 metrics; TPL-007 | Phase 3 readiness | These support Key Controls (CC4.1, CC4.2, CC2.2, CC7.5) despite P2 priority |
| D13 | REF-001 Key Control list | Observation Period start | The list cannot change during a period (REF-001.5.1.5) |
| D14 | CMP-001 applicability; GC confirmation of PCI entity type | SEC-019; CMP-008; CMP-009 | Conditional modules are confirmed before implementation |

#### 5.5.2 Critical path

The critical path to the start of the SOC 2 Observation Period is:

1. **Governance:** GOV-001 approval → ISSC → Tier 1 approvals (D1).
2. **Inventory and classification:** SEC-001 and SEC-002 → scoping of everything downstream (D3, D4).
3. **Identity:** HR system of record events (PPL-001) and identity provider, SSO and MFA (SEC-004) → joiner, mover and leaver automation → first User Access Review (D6, D7). Identity consolidation usually has the longest lead time.
4. **Detection:** SIEM onboarding of required log sources → 24×7 triage → log review Evidence (D8).
5. **Resilience:** BIA → Backup configuration → restore test → DR test scheduled inside the Observation Period (D5).
6. **Assurance:** Evidence repository → Key Control Evidence for one full cycle → Readiness Assessment → Key Control list approval → Observation Period start (D11–D13).

The CISO SHALL report progress on each critical-path item to the ISSC every quarter. A slip of
more than 30 days on any of them SHALL be escalated with a recovery plan.

### 5.6 Resourcing by role

The table shows the expected effort of each role by phase. [ASSUMPTION: Effort is sized for the
design baseline (1,000+ Workforce Members). Smaller adopters scale down and MAY combine roles as
permitted by GOV-001.5.8.] Levels: **L** lead (drives the phase, more than 50% of time);
**H** high (25–50%); **M** medium (10–25%); **S** support (under 10%).

| Role | Ph 0 | Ph 1 | Ph 2 | Ph 3 | Ph 4 | Ph 5 | Main contributions |
|---|---|---|---|---|---|---|---|
| Board of Directors | S | — | — | — | S | S | Approves ISP-000; receives annual report |
| Audit Committee | S | S | S | S | S | S | Recommends ISP-000; ratifies Risk Appetite; approves CMP-002 and CMP-006 |
| Chief Executive Officer (CEO) | M | S | S | S | S | S | Sponsors; approves GOV-001; co-signs management's assertion |
| Information Security Steering Committee (ISSC) | M | M | M | M | S | S | Approves Tier 1 Policies and this roadmap; confirms phase exits |
| Chief Information Security Officer (CISO) | L | L | L | L | H | H | Program lead; owner of this roadmap |
| Head of GRC | H | L | L | L | L | H | Gap assessment, risk, compliance, evidence, REF-001/REF-002 |
| Head of Security Engineering | S | M | L | H | M | M | IAM, PAM, cryptography, network, vulnerability management, CDE |
| SOC Manager | — | S | L | H | M | M | SIEM, detection, incident response, threat intelligence |
| Chief Information Officer (CIO) | S | M | L | H | M | M | Asset Inventory, endpoints, change, Backup, DR |
| Chief Technology Officer (CTO) | S | M | H | M | S | M | Cloud, SDLC, product security |
| Chief Privacy Officer (CPO) | S | H | M | S | S | S | Privacy program, ROPA, breach notification |
| Data Protection Officer (DPO) | — | H | M | S | S | S | `[GDPR]` ROPA, DPIA, DSR |
| General Counsel (GC) | M | M | S | S | S | S | Applicability, contracts, Legal Holds, whistleblower channels |
| Chief Financial Officer (CFO) | S | M | M | S | M | S | Budget; `[SOX]` scoping and assessment |
| Chief Human Resources Officer (CHRO) | S | M | M | S | S | S | Screening, HR events, training enforcement |
| HIPAA Security Officer | S | H | M | S | M | S | `[HIPAA]` risk analysis, addressable decisions, evaluation |
| HIPAA Privacy Officer | — | M | S | S | S | S | `[HIPAA]` Privacy Rule coordination |
| Internal Audit Director | — | S | M | H | M | M | Readiness (if not outsourced), CMP-002 audits |
| Business Continuity Manager | — | S | L | M | M | S | BIA, BCPs, exercises |
| Head of Facilities | — | S | M | S | S | S | Physical and environmental controls |
| Head of Procurement | S | M | M | S | S | S | Vendor inventory, contract terms |
| Asset Owner, Data Owner, System Owner | — | M | H | M | M | S | Classification, access approvals, reviews, remediation |
| Workforce Member | — | S | S | S | S | S | Attestation, training |

Indicative dedicated security and GRC staffing at the design baseline. [ASSUMPTION: Figures are
indicative and are confirmed in the staffing plan under GOV-001.5.9.1.]

| Function | Indicative staffing | Note |
|---|---|---|
| GRC (under the Head of GRC) | 3–4 analysts | Risk, compliance, Evidence, third-party assessment |
| Security engineering (under the Head of Security Engineering) | 4–6 engineers | IAM/PAM, cloud and network security, vulnerability management |
| Security operations (under the SOC Manager) | 24×7 coverage | In-house 24×7 coverage typically needs 8–10 analysts; a managed detection and response Third Party under RSK-003 is an alternative |
| Privacy operations (under the DPO) | 1–2 analysts | DSR handling, ROPA, DPIA support |
| Business continuity | 1 coordinator | Supports the Business Continuity Manager |
| External | Readiness assessor, service auditor, `[PCI]` QSA and ASV, Penetration Testers, external counsel | Engaged under CMP-001 and RSK-003 |

### 5.7 Tooling capabilities

The capabilities below are needed to operate the suite. They are described generically. Selection
follows RSK-003 due diligence, and each tool is recorded in the Asset Inventory (SEC-001).

| Capability | Supports | Needed by | Selection notes |
|---|---|---|---|
| GRC platform (policy repository, risk and Exception registers, control library, Evidence collection, testing workflow) | GOV-002, RSK-001, CMP-001 – CMP-004, REF-001 | Phase 1 | Imports the REF-001 matrix; automated Evidence collection from the tools below |
| Identity provider with SSO and MFA, including phishing-resistant MFA | SEC-003, SEC-004 | Phase 1 (rollout through Phase 2) | Integrates with the HR system of record for joiner, mover and leaver events |
| Identity governance (access requests, certifications, SoD rules) | SEC-003.5.12, GOV-001.5.7, `[SOX]` CMP-009 | Phase 2 | Produces TPL-008 Evidence; MAY be part of the GRC platform or identity provider |
| Privileged access management (vaulting, JIT elevation, session recording) | SEC-005 | Phase 2 | Covers cloud root/owner accounts and Break-glass Accounts |
| Endpoint detection and response (EDR) | SEC-008.5.3 | Phase 2 | Feeds the SIEM; supports remote isolation |
| Unified endpoint / mobile device management (UEM/MDM) | SEC-008 | Phase 2 | Enforces encryption, patching and BYOD separation |
| SIEM (with optional SOAR) | SEC-012, RES-002 | Phase 2 | Meets SEC-012 retention and integrity; supports detection use case catalog |
| Vulnerability scanning (internal authenticated, external, container and cloud) | SEC-011 | Phase 2 | `[PCI]` ASV scans from an approved scanning vendor |
| Cloud security posture management (CSPM/CNAPP) | SEC-009.5.5 | Phase 2 | Covers every cloud account in the landing zone |
| Application security testing (SAST, SCA, DAST, secret scanning) and SBOM generation | SEC-010, SEC-004.5.10 | Phase 2 | Enforced as pipeline gates |
| Data loss prevention, data discovery and labelling | SEC-002.5.4 – 5.5 | Phase 2 | Covers email, endpoints and Cloud Services |
| Email security (anti-phishing, attachment and link protection, DMARC reporting) | SEC-014 | Phase 2 | SEC-014 is P2 (Phase 5); deploy the capability in Phase 2 and approve SEC-014 early if the Readiness Assessment relies on it for CC6.8 |
| Backup with immutable or offline copies | SEC-018 | Phase 2 | Supports the 3-2-1-1-0 rule and restore testing per Recovery Tier |
| Key management service, HSM and certificate lifecycle management | SEC-006 | Phase 2 | Validated modules for Restricted data |
| IT service management and configuration management database (change, incident, asset records) | SEC-001, SEC-013, RES-002 | Phase 1 | Single record of Changes and assets for audit sampling |
| Asset discovery | SEC-001.5.5, 5.9 | Phase 1 | Reconciles the inventory |
| Network security (next-generation firewall, IDS/IPS, DDoS protection, DNS filtering, secure remote access) | SEC-007 | Phase 2 | Supports default deny and rule review |
| Configuration and drift monitoring; `[PCI]` file integrity monitoring and payment page tamper detection | SEC-013.5.9, SEC-019.5.8 | Phase 2 | — |
| Security awareness and phishing simulation platform | PPL-002 | Phase 1 | Integrates with the HR system of record |
| Third-party risk questionnaire and monitoring | RSK-003, TPL-004 | Phase 2 | MAY be part of the GRC platform |
| Privacy management (ROPA, DPIA, DSR workflow, consent and opt-out preference signals) | CMP-005, CMP-010 | Phase 1 | `[GDPR]` `[CPRA]` |
| Ethics and whistleblower hotline (independent Third Party) and case management | CMP-006, CMP-007 | Phase 2 | Anonymous reporting |
| Physical access control and CCTV | SEC-016 | Phase 2 | Feeds Zone 3 events to the SIEM |

### 5.8 Program risks

- **REF-003.5.8.1** The CISO SHALL record the program risks below in the Risk Register under RSK-001, with a named Risk Owner, and SHALL review them with the roadmap every quarter.

| # | Risk to the roadmap | Likely effect | Mitigation | Risk Owner |
|---|---|---|---|---|
| PR-01 | Executive sponsorship weakens after Phase 0 | Approvals stall; budget cut | ISSC quarterly roadmap review; CISO reports to the Audit Committee (GOV-001.5.2.2) | CEO |
| PR-02 | Key roles not filled (Head of GRC, Head of Security Engineering, SOC Manager) | Phase 1–2 slip | Interim or Third-Party resources; vacancies over 90 days reported to the Audit Committee (GOV-001.5.9.2) | CISO |
| PR-03 | Identity consolidation takes longer than planned (critical path) | First Access Review and SOC 2 window slip | Start IdP/MFA in Phase 1; prioritize Tier 0, Tier 1 and Financially Significant Systems; Exceptions under CMP-003 for legacy systems | CIO |
| PR-04 | 24×7 monitoring cannot be staffed | Alert triage SLA in SEC-012 not met | Managed detection and response Third Party assessed under RSK-003 | SOC Manager |
| PR-05 | Evidence not retained from the first day of the Observation Period | Qualified opinion or exceptions | GRC platform live in Phase 1; Evidence pilot in Phase 2; Key Control "Evidenced" status before Phase 3 exit | Head of GRC |
| PR-06 | P2 documents that underpin Key Controls (CMP-002, GOV-003, TPL-007) left to Phase 5 | Gaps under CC2.2, CC4.1, CC4.2, CC7.5 | Pulled forward to Phase 2 (section 5.4) | Head of GRC |
| PR-07 | Annual controls (Penetration Test, DR test, BC exercise, IR exercise, risk assessment) fall outside the Observation Period | Controls untestable in the first report | Schedule them in Phase 3 inside the period | CISO |
| PR-08 | Requirements added to close suite gaps G-01 (capacity, SEC-013.5.12) and G-02 (fraud risk, RSK-002.5.10) not implemented before readiness | Findings under A1.1 and CC3.3 | Track as self-assessment rows; their Key Controls must be "Evidenced" before Phase 3 exit | Head of GRC |
| PR-09 | Parallel `[PCI]`, `[HIPAA]` and `[SOX]` work competes with SOC 2 for the same people | All programs slip | Sequence validation in Phase 4; reuse REF-001 mappings so one control serves all frameworks | CISO |
| PR-10 | Role combinations in smaller adopters break Segregation of Duties | Owner approves own document or tests own control | Use only combinations permitted by GOV-001.5.8; repeat the REF-002 section 5.5 check on each combination | Head of GRC |
| PR-11 | Cloud Service Providers' assurance reports do not cover required complementary controls | Carve-out gaps in the SOC 2 report | Map complementary user entity controls under SEC-009 and RSK-003 in Phase 3 | CTO |
| PR-12 | Policy fatigue: low attestation and training completion | CC1.1, CC1.4, CC2.2 exceptions | Role-based attestation sets (GOV-002); enforcement under CMP-007 | CHRO |
| PR-13 | New or changed legal obligation during the program | Rework of documents | Regulatory change process in CMP-001; event-triggered review under GOV-002 | GC |
| PR-14 | Tool deployments create unmanaged Change or new attack surface | Incidents during rollout | All deployments as Normal Changes under SEC-013; security review under SEC-009 and SEC-010 | Head of Security Engineering |

### 5.9 Tailoring the suite

- **REF-003.5.9.1** The CISO SHALL propose, and the ISSC SHALL approve in Phase 0, which conditional modules apply. The decision SHALL be based on the applicability determinations recorded by the GC in the Obligations Register (CMP-001).
- **REF-003.5.9.2** Where a module does not apply, the Head of GRC SHALL tailor the suite as follows:

| Applies only if the Organization… | Remove | Also update |
|---|---|---|
| Stores, processes or transmits payment card data | SEC-019; clauses tagged `[PCI]` | REF-001 PCI entries and section 5.8; RSK-002.5.8 TRAs; REF-002 `[PCI]` activities; this roadmap's `[PCI]` items |
| Is a HIPAA covered entity or business associate | CMP-008; clauses tagged `[HIPAA]` | RES-003 HIPAA rows; REF-001 HIPAA entries and section 5.9; HIPAA Security Officer and HIPAA Privacy Officer columns in REF-002; GOV-001.5.5.1 – 5.5.3 |
| Is publicly listed (SEC registrant) | CMP-009; SOX §301 elements of CMP-006 (CMP-006.5.7); clauses tagged `[SOX]` | REF-001 SOX entries and section 5.10; REF-002 `[SOX]` activities; CFO approval of CMP-009 |
| Processes personal data of EU/EEA residents or California consumers | CMP-010, TPL-005, TPL-010; clauses tagged `[GDPR]` / `[CPRA]` | DPO column in REF-002 where GDPR Art. 37(1) does not apply; CMP-005 sections tagged accordingly |
| Develops or deploys AI systems | RSK-006 (recommended for all adopters that use third-party AI tools) | SEC-002 Generative AI handling row; GOV-004.5.8 |

- **REF-003.5.9.3** Removed document IDs SHALL NOT be reused. The Head of GRC SHALL mark each removed document "Not adopted" in SUITE-REGISTER section D, with the reason.
- **REF-003.5.9.4** Tagged clauses SHALL be found by searching for the tag text. Where removing a clause leaves a subsection empty, the subsection heading SHALL be kept with the text "Not applicable to the Organization", so that numbering and REF-001 references stay stable.
- **REF-003.5.9.5** Smaller adopters MAY combine roles only as permitted by GOV-001.5.8. They MAY defer P3 documents (RSK-005, SEC-015) beyond Phase 5, but SHALL NOT defer documents that support a Key Control.
- **REF-003.5.9.6** Every tailoring decision SHALL be approved by the ISSC, recorded in the minutes and retained under CMP-004. Removing a P1 document for a reason other than a conditional module SHALL be handled as an Exception under CMP-003.

### 5.10 Adopter decisions

The adopter decisions, their recommended defaults and the documents they affect are listed in
SUITE-REGISTER section E and are not repeated here. Their timing in this roadmap:

| SUITE-REGISTER section E decision # | Decide by | Decided by |
|---|---|---|
| 1, 6 | Phase 0 exit (before ISP-000 and GOV-001 approval) | Board of Directors (via ISP-000) and CEO (via GOV-001); Risk Appetite ratified by the Audit Committee |
| 2 | Phase 0 exit; confirmed at Phase 3 entry with the service auditor | ISSC |
| 3, 5 | Phase 0 exit (GOV-001 designations) | CEO, on GC advice |
| 4 | Phase 1 exit (Obligations Register) | CISO, on GC confirmation of entity type and level |
| 7, 8 | Phase 0 exit (scope of CMP-001, CMP-005 and RES-003; DPO appointment) | GC, then CEO |

- **REF-003.5.10.1** Every other `[DECISION REQUIRED]` placeholder in a suite document SHALL be resolved, or its recommended default confirmed, by the approver of that document at approval. The Head of GRC SHALL keep a decision log listing each placeholder, the decision, the approver and the date.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CISO | Owns this roadmap; leads the gap assessment and the program; reports progress, critical-path status and program risks to the ISSC quarterly. |
| ISSC | Approves this roadmap and every quarterly refresh; confirms phase exits; approves tailoring decisions. |
| CEO | Sponsors the program; approves Phase 0 start and GOV-001. |
| Head of GRC | Runs the self-assessment and refreshes it; keeps the decision log; tracks document approvals and REF-001 gaps. |
| Document Owners | Draft and present their documents for approval in the sequence in section 5.4. |
| Owners of key requirements (accountable roles in REF-002) | Complete the Status, Evidence and Owner columns in section 5.2 and deliver remediation. |
| Internal Audit Director | Performs or oversees the Readiness Assessment where it is not outsourced; gives independent assurance on phase-exit Evidence. |
| CFO | Funds the roadmap within the financial plan; leads `[SOX]` work in Phase 4. |

Activity-level assignments are consolidated in REF-002.

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| REF-003.7.1 | Roadmap refresh and report to the ISSC | Every 3 months |
| REF-003.7.2 | Baseline gap assessment complete | By Phase 1 exit |
| REF-003.7.3 | Self-assessment refresh | Every 3 months until Phase 4 exit; every 12 months after |
| REF-003.7.4 | Phase exit | Confirmed by the ISSC before the phase is closed |
| REF-003.7.5 | Key Control status before Observation Period start | 100% "Evidenced" for one full cycle of each control's frequency |
| REF-003.7.6 | Critical-path slip escalated to the ISSC with a recovery plan | Slip greater than 30 days |
| REF-003.7.7 | Open REF-001 gaps (G-03 to G-05) | Closed by the time shown in section 5.2.2 |
| REF-003.7.8 | Annual controls scheduled inside the first Observation Period | 100% of annual Key Controls |
| REF-003.7.9 | Gaps rated High or Critical recorded in the Risk Register | 100%, within 10 business days of rating |
| REF-003.7.10 | `[DECISION REQUIRED]` placeholders resolved or default confirmed | 100% at approval of each document |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| P1 documents approved vs. plan (section 5.4) | 100% by Phase 2 exit | Monthly | Head of GRC |
| Key requirements in section 5.2 at "Evidenced" | 100% of target-phase rows at each phase exit | Quarterly | Head of GRC |
| Key Controls (REF-001 section 5.4) at "Evidenced" | 100% by Phase 3 exit | Monthly in Phase 3 | Head of GRC |
| Critical-path items on schedule (section 5.5.2) | 100% | Quarterly | CISO |
| Program risks (section 5.8) rated High or Critical without an active treatment plan | 0 | Quarterly | CISO |
| Readiness Assessment High findings open at Observation Period start | 0 | Phase 3 | CISO |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003. Phase exit criteria
that require a Key Control to be "Evidenced" (REF-003.7.5) SHALL NOT receive an Exception. A
Key Control that cannot meet them SHALL be removed from the Key Control list under
REF-001.5.1.4, and the resulting coverage gap SHALL be accepted under RSK-001, before the
Observation Period starts.

## 10. Enforcement

Non-compliance is handled under CMP-007.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| REF-003.5.1 – 5.2 | 6.1.2, 9.1; A.5.36 | GV.OV-01, ID.IM-01 | CA-2, PM-14 | — | CC3.2, CC4.1 | MEA01, MEA02 | `[HIPAA]` §164.308(a)(8) |
| REF-003.5.3 – 5.5 | 6.2, 6.3, 8.1 | GV.OC-01, GV.RM-01 | PM-1, PM-3 | — | CC3.1, CC5.1 | APO02, APO05, BAI01 | — |
| REF-003.5.6 – 5.7 | 7.1, 7.2 | GV.RR-03 | PM-3, PM-13 | — | CC1.4 | APO07, BAI03 | — |
| REF-003.5.8 | 6.1.1, 6.1.3 | GV.RM-01, ID.RA-05 | PM-9, RA-3 | — | CC3.2 | APO12 | — |
| REF-003.5.9 – 5.10 | 4.3; A.5.31 | GV.OC-03 | PM-1, PL-1 | — | CC2.1, CC5.3 | APO01, MEA03 | `[PCI]` 12.5.2 |

## 12. Related documents

ISP-000, GOV-001, GOV-002, GOV-003, GOV-006, RSK-001, RSK-002, RSK-003, RSK-004, CMP-001,
CMP-002, CMP-003, CMP-004, CMP-007, CMP-008, CMP-009, SEC-001 to SEC-019, RES-001 to RES-005,
PPL-001, PPL-002, REF-001, REF-002; README; SUITE-REGISTER.

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CISO | | | |
| Approver: ISSC Vice-Chair, on behalf of the ISSC (the CISO, as owner, recuses as Chair under GOV-001.5.3.9) | | | |
