# CMP-009 — SOX IT General Controls Standard

## 1. Document control

| Field | Value |
|---|---|
| Document ID | CMP-009 |
| Title | SOX IT General Controls Standard |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 2 — Standard |
| Classification | Internal |
| Owner | Head of GRC |
| Approver | Chief Financial Officer (CFO) † (SOX §404) |
| Effective date | [DECISION REQUIRED: Date of CFO approval] |
| Next review date | Effective date + 12 months, and on the event-triggered reviews in GOV-002.7.4 |
| Parent document | CMP-001 Compliance Management Policy |
| Related documents | GOV-001, RSK-002, RSK-003, CMP-002, CMP-003, CMP-004, CMP-006, SEC-001, SEC-003, SEC-004, SEC-005, SEC-010, SEC-012, SEC-013, SEC-018, RES-002, RES-003, REF-001 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Head of GRC | Initial release |

## 3. Purpose

This Standard defines how the Organization scopes, designs, operates, tests and reports
IT general controls (ITGCs) over its Financially Significant Systems, so that management can
support:

- the CEO and CFO quarterly and annual certifications under SOX §302;
- management's annual assessment of internal control over financial reporting (ICFR) under
  SOX §404(a); and
- where applicable, the External Auditor's attestation under
  SOX §404(b).

ITGCs matter because automated application controls, IT-dependent manual controls and
system-generated reports can be relied on only if the systems that run them are protected from
unauthorized access and change and operate consistently.

## 4. Scope

**This entire document is a conditional module. It applies only where the Organization is
subject to SOX `[SOX]`**, that is, where it is an SEC registrant, as recorded in the Obligations
Register (CMP-001). Where SOX does not apply, the Organization removes this document and all
clauses tagged `[SOX]` (README "Conditional modules").

| Dimension | In scope |
|---|---|
| People | Workforce Members who administer, develop, change, operate or hold access to Financially Significant Systems; Control Owners of Key Controls in this Standard; finance personnel who own IPE |
| Systems | Every Financially Significant System, at each technology layer identified under section 5.2 (application, database, operating system, cloud platform, job scheduler, Identity Provider), and end-user computing tools used in Key Controls |
| Data | Financial transaction data, master data, configuration data that drives automated controls, and reports used in Key Controls |
| Locations | All locations from which Financially Significant Systems are administered or operated |
| Third parties | Service organizations that host, operate or process transactions for Financially Significant Systems, and their relevant subservice organizations |

Business-process (transaction-level) controls are owned by the CFO's finance function and are
outside this Standard, except for the IPE and automated-control dependencies in section 5.8.
[ASSUMPTION: Management assesses ICFR against the COSO Internal Control — Integrated Framework
(2013).]

## 5. Requirements

### 5.1 General

- **CMP-009.5.1.1** `[SOX]` The Head of GRC SHALL maintain an ITGC control matrix listing, for each Key Control in sections 5.4 to 5.7: control ID, control objective, control description, Control Owner, frequency, nature (manual, automated, IT-dependent manual), type (preventive or detective), Financially Significant Systems and layers covered, IPE used, and the Evidence produced.
- **CMP-009.5.1.2** `[SOX]` Each Key Control SHALL have one named Control Owner. A Control Owner SHALL NOT be the tester of their own control (section 5.10).
- **CMP-009.5.1.3** `[SOX]` The ITGC control matrix SHALL be approved by the CFO at the start of each fiscal year, together with the scoping memo (CMP-009.5.2.6), and SHALL be shared with the External Auditor.
- **CMP-009.5.1.4** `[SOX]` The underlying controls (access provisioning, Access Review, Change approval, Backup, and so on) are defined in their home documents, which are cited in each table. This Standard sets only the SOX-specific objectives, Key Control designations, Evidence, testing and reporting requirements. Where this Standard and a home document differ, the stricter requirement applies to Financially Significant Systems.

### 5.2 Scoping Financially Significant Systems

- **CMP-009.5.2.1** `[SOX]` The Head of GRC SHALL scope Financially Significant Systems using the top-down, risk-based method below, aligned with PCAOB AS 2201, every fiscal year and SHALL update the scope every fiscal quarter for changes.
- **CMP-009.5.2.2** `[SOX]` Scoping SHALL follow these steps, each documented in the scoping memo:
  1. **Significant accounts.** The CFO identifies significant accounts and disclosures and their relevant assertions, using quantitative materiality and qualitative factors. [DECISION REQUIRED: Quantitative threshold for a significant account. Recommended default: any account or disclosure whose balance or annual activity exceeds performance materiality set by the CFO, plus any account that is qualitatively significant]
  2. **Processes and controls.** For each significant account, the CFO's finance function identifies the significant business processes and the Key Controls in them, flagging automated controls, IT-dependent manual controls, system calculations, interfaces and IPE.
  3. **Applications.** The Head of GRC identifies every application that initiates, authorizes, records, processes or reports the transactions, or that runs a flagged control or produces flagged IPE. These are Financially Significant Systems.
  4. **Supporting layers.** For each Financially Significant System, the System Owner identifies each supporting layer (database, operating system, cloud platform account or subscription, job scheduler, middleware, Identity Provider) where an unauthorized access or change could affect the application's data, controls or reports. Each such layer is in scope.
  5. **Service organizations.** The Head of GRC identifies service organizations that host, operate or process transactions for any in-scope application or layer (section 5.9).
  6. **Risks arising from IT.** For each in-scope application and layer, the Head of GRC rates the risk arising from IT as High, Moderate or Low, based on the complexity of the system, degree of customization, volume of automated controls, number of privileged Users, frequency of change and history of deficiencies. The rating determines the testing extent in section 5.10.
  7. **Exclusions.** Systems considered and excluded are recorded with the rationale.
- **CMP-009.5.2.3** `[SOX]` Each Financially Significant System SHALL be flagged `[SOX]` in the Asset Inventory (SEC-001), with its System Owner, Data Owner, supporting layers and risk-arising-from-IT rating.
- **CMP-009.5.2.4** `[SOX]` A new information system, or a material upgrade of an existing one, that will meet the Financially Significant System test SHALL be added to scope before it goes live. The System Owner SHALL notify the Head of GRC at project initiation and no later than 60 days before go-live.
- **CMP-009.5.2.5** `[SOX]` The System Owner SHALL notify the Head of GRC within 10 business days of any change that may affect scope, including a new interface, migration to a new hosting platform, a change of service organization, or decommissioning.
- **CMP-009.5.2.6** `[SOX]` The scoping memo SHALL be approved by the CFO within 60 days after the start of each fiscal year, and each quarterly update SHALL be approved by the CFO before the quarterly ITGC report in CMP-009.5.10.6.

### 5.3 ITGC domains

- **CMP-009.5.3.1** `[SOX]` The Organization's ITGCs SHALL cover four domains, each with the control objectives and Key Controls in sections 5.4 to 5.7:

| Domain | Code | Overall objective |
|---|---|---|
| Access to programs and data | APD | Only authorized Users have access to Financially Significant Systems and financial data, limited to their job responsibilities, with Segregation of Duties enforced |
| Program change | PC | Changes to Financially Significant Systems are authorized, tested, approved and implemented as intended |
| Program development | PD | New Financially Significant Systems and material upgrades are acquired or developed, tested, converted and implemented so that they process data completely and accurately |
| Computer operations | CO | Financially Significant Systems are scheduled, monitored, backed up and recovered so that processing is complete and accurate and data are available |

- **CMP-009.5.3.2** `[SOX]` Every Key Control in sections 5.4 to 5.7 SHALL apply to every in-scope layer of every Financially Significant System, unless the scoping memo records why the control does not apply to a layer (e.g. a SaaS application where the layer is operated by a service organization covered under section 5.9).

### 5.4 Access to programs and data (APD)

- **CMP-009.5.4.1** `[SOX]` The following Key Controls SHALL operate over each Financially Significant System:

| Control ID | Control objective | Key Control | Nature / type | Frequency | Control Owner | Home of underlying requirement |
|---|---|---|---|---|---|---|
| ITGC-APD-01 | New access is authorized | Access to the application, database, operating system and cloud platform is granted only on a documented request approved by the Data Owner (or delegate) before provisioning | Manual / preventive | Each request | System Owner | SEC-003 |
| ITGC-APD-02 | Access is removed on Separation | Accounts of separated Workforce Members are disabled within the revocation time in SEC-003.7.3; a reconciliation of the HR Separation report to active accounts is performed every month and differences are resolved | Manual / preventive and detective | Each Separation; monthly reconciliation | System Owner | SEC-003 |
| ITGC-APD-03 | Access is adjusted on role change | Access no longer required after a transfer is removed within the role-change time in SEC-003.7.5 | Manual / preventive | Each transfer | System Owner | SEC-003 |
| ITGC-APD-04 | Access remains limited to job responsibilities | Access Reviews of all User and Privileged Accounts on each in-scope layer are performed by the Data Owner at the frequency in SEC-003.7.1 for Financially Significant Systems, using TPL-008; changes are actioned and verified | Manual / detective | Per SEC-003 | Data Owner | SEC-003; TPL-008 |
| ITGC-APD-05 | Privileged access is restricted | Privileged Accounts on each layer are limited to named administrators, granted through Just-in-Time Access where supported, and reviewed at the frequency in SEC-005.7.1 | Manual and automated / preventive and detective | Per SEC-005 | System Owner | SEC-005 |
| ITGC-APD-06 | Authentication is enforced | Password, MFA, lockout and session settings on each layer meet SEC-004; settings are compared to the Configuration Baseline every 12 months and after each change to authentication configuration | Automated / preventive | Continuous; comparison every 12 months | System Owner | SEC-004; SEC-013 |
| ITGC-APD-07 | Segregation of Duties is enforced | Application roles are checked against the financial SoD ruleset approved by the CFO; conflicts are prevented at provisioning or, where accepted, monitored by a documented mitigating control | Automated or manual / preventive and detective | Each request; ruleset review every 12 months | Data Owner | GOV-001 (SoD principles); this Standard (financial ruleset) |
| ITGC-APD-08 | Shared, generic and Service Accounts are controlled | Each shared, generic or Service Account has a named owner, documented purpose and interactive log-in disabled where feasible; these accounts are included in ITGC-APD-04 | Manual / preventive and detective | Per SEC-003 | System Owner | SEC-003; SEC-004; SEC-005 |
| ITGC-APD-09 | Direct data changes are authorized | Direct changes to production financial data outside the application (data fixes) are requested, approved by the Data Owner, performed by an authorized administrator, logged, and the log is reviewed by the Data Owner every month | Manual / preventive and detective | Each change; monthly log review | Data Owner | SEC-012 (logging) |
| ITGC-APD-10 | Privileged activity is monitored | Logs of privileged activity on Financially Significant Systems are retained under CMP-004 and reviewed under SEC-012; activity by Break-glass Accounts is reviewed within the time in SEC-005.7.3 | Automated and manual / detective | Per SEC-012 and SEC-005 | SOC Manager | SEC-005; SEC-012 |

- **CMP-009.5.4.2** `[SOX]` The CFO SHALL approve the financial SoD ruleset (the pairs of application roles or permissions that SHALL NOT be held by the same User) for each Financially Significant System, and SHALL re-approve it every 12 months.
- **CMP-009.5.4.3** `[SOX]` Evidence for ITGC-APD-04 SHALL include the complete User listing extracted from the system, validated under section 5.8, the reviewer's decision for each account, and proof that removals were completed.
- **CMP-009.5.4.4** `[SOX]` The SOC Manager SHALL provide the System Owner of each Financially Significant System with a privileged activity report (ITGC-APD-10) and an unauthorized-change report (supporting ITGC-PC-05) every month.

### 5.5 Program change (PC)

- **CMP-009.5.5.1** `[SOX]` The following Key Controls SHALL operate over each Financially Significant System:

| Control ID | Control objective | Key Control | Nature / type | Frequency | Control Owner | Home of underlying requirement |
|---|---|---|---|---|---|---|
| ITGC-PC-01 | Changes are authorized, tested and approved | Every Change to application code, configuration, database structure, infrastructure-as-code, job schedules or automated-control settings is recorded, tested, and approved under the Change class rules in SEC-013 before production deployment | Manual / preventive | Each Change | System Owner | SEC-013; SEC-010 |
| ITGC-PC-02 | Business approval of changes affecting financial processing | Changes that affect automated controls, calculations, interfaces or reports used in Key Controls are approved by the Data Owner after reviewing test results | Manual / preventive | Each Change | Data Owner | SEC-013 |
| ITGC-PC-03 | Development and production duties are segregated | Personnel who develop a Change cannot deploy it to production; access to deploy to production is restricted to authorized personnel or an automated pipeline that enforces approval | Automated or manual / preventive | Continuous | System Owner | SEC-010; SEC-013; SEC-005 |
| ITGC-PC-04 | Emergency Changes are controlled | Emergency Changes receive retrospective approval within the time in SEC-013.7.1, including Data Owner approval where ITGC-PC-02 applies | Manual / detective | Each Emergency Change | System Owner | SEC-013 |
| ITGC-PC-05 | All production changes are approved | Changes deployed to production (from deployment logs, version control or system change logs) are reconciled every month to approved Change records; unmatched Changes are investigated and treated as deficiencies | Manual / detective | Monthly | System Owner | SEC-013; SEC-012 |
| ITGC-PC-06 | Vendor-delivered changes are assessed | For SaaS and packaged applications, vendor release notes are reviewed before each release for effect on automated controls, reports and interfaces; affected functions are regression-tested | Manual / preventive | Each vendor release | System Owner | SEC-013 |

- **CMP-009.5.5.2** `[SOX]` Standard Changes to Financially Significant Systems SHALL NOT include changes to automated controls, calculations, interfaces or Key Control reports; such changes SHALL always be Normal Changes or Emergency Changes.
- **CMP-009.5.5.3** `[SOX]` Evidence for ITGC-PC-01 to ITGC-PC-05 SHALL include, for each Change: the change record identifier; requester; description; affected Financially Significant System and component; Change Class; test evidence and tester; Data Owner approval where ITGC-PC-02 applies; CAB approval or Emergency Change retrospective approval, with dates; the identity of the person or pipeline that deployed the Change, distinct from its developer (ITGC-PC-03); and the deployment date and time from system logs.

### 5.6 Program development (PD)

- **CMP-009.5.6.1** `[SOX]` The following Key Controls SHALL operate for each new Financially Significant System and each material upgrade:

| Control ID | Control objective | Key Control | Nature / type | Frequency | Control Owner | Home of underlying requirement |
|---|---|---|---|---|---|---|
| ITGC-PD-01 | Projects are authorized | Projects to implement or materially upgrade a Financially Significant System are approved by the Data Owner and the CFO (or delegate) before build starts, with financial control requirements documented | Manual / preventive | Each project | System Owner | SEC-010 |
| ITGC-PD-02 | New functionality is tested | User acceptance testing of financial functionality, automated controls, interfaces and reports is performed and signed off by the Data Owner before go-live | Manual / preventive | Each project | Data Owner | SEC-010 |
| ITGC-PD-03 | Data conversion is complete and accurate | Migrated balances and master data are reconciled (record counts, control totals, sample comparison) from source to target, and the reconciliation is approved by the Data Owner before go-live | Manual / preventive and detective | Each conversion | Data Owner | SEC-010 |
| ITGC-PD-04 | Go-live is approved | Go-live is approved by the Data Owner and System Owner after PD-02 and PD-03 are complete and ITGCs in sections 5.4, 5.5 and 5.7 are operating | Manual / preventive | Each project | System Owner | SEC-013 |
| ITGC-PD-05 | Implementation is confirmed | A post-implementation review is completed within 90 days after go-live, covering open defects, control operation and access | Manual / detective | Each project | System Owner | SEC-010 |

### 5.7 Computer operations (CO)

- **CMP-009.5.7.1** `[SOX]` The following Key Controls SHALL operate over each Financially Significant System:

| Control ID | Control objective | Key Control | Nature / type | Frequency | Control Owner | Home of underlying requirement |
|---|---|---|---|---|---|---|
| ITGC-CO-01 | Job schedules are controlled | The ability to create or change scheduled jobs and interfaces is restricted to authorized operators, and changes follow ITGC-PC-01 | Automated / preventive | Continuous | System Owner | SEC-013 |
| ITGC-CO-02 | Processing failures are resolved | Failed or incomplete scheduled jobs and interfaces are detected by automated alert, investigated, and resolved or escalated; resolution is recorded in a ticket | Automated and manual / detective | Each business day | System Owner | SEC-012 |
| ITGC-CO-03 | Interfaces are complete and accurate | Record counts or control totals of each interface that feeds financial data are reconciled between source and target, with exceptions resolved | Automated or manual / detective | Each interface run | Data Owner | — (this Standard) |
| ITGC-CO-04 | Data are backed up | Financially Significant Systems are backed up at the frequency in SEC-018.7.1; failures are resolved and a successful Backup is confirmed within 1 business day of a failure | Automated and manual / preventive and detective | Per SEC-018 | System Owner | SEC-018; CMP-004 (`[SOX]` year-end Backup retention) |
| ITGC-CO-05 | Data can be restored | Restores of Financially Significant System data are tested at the frequency in SEC-018.7.2 for the system's Recovery Tier | Manual / detective | Per SEC-018 | System Owner | SEC-018 |
| ITGC-CO-06 | Operational incidents are resolved | Security Incidents and operational incidents affecting a Financially Significant System are logged, resolved, and assessed by the Head of GRC for ICFR impact | Manual / detective | Each incident | System Owner | RES-002 |

### 5.8 Information Produced by the Entity (IPE) and report controls

- **CMP-009.5.8.1** `[SOX]` The Head of GRC SHALL maintain an inventory of every report, query, extract and end-user computing tool (e.g. a spreadsheet) used in the operation or testing of a Key Control (IPE), recording: name, source system, type (standard system report, custom report, ad hoc query, end-user computing tool), owner, the Key Controls that use it, and the method of validating it.
- **CMP-009.5.8.2** `[SOX]` The person performing a Key Control that uses IPE SHALL, each time the IPE is used, retain Evidence of its completeness and accuracy:
  1. **Standard (unmodified vendor) reports:** the report parameters used (screenshot or export), the run date and time, and a check that the output totals or record count agree to an independent source;
  2. **Custom reports:** as for standard reports, plus reliance on a baseline test of report logic performed when the report was created or last changed and controlled under ITGC-PC-01;
  3. **Ad hoc queries:** the query text, parameters, source, run date and time, and a reconciliation of the output to an independent source; and
  4. **End-user computing tools:** the version used, and evidence of the integrity checks in CMP-009.5.8.4.
- **CMP-009.5.8.3** `[SOX]` A custom report or query used in a Key Control SHALL be changed only under ITGC-PC-01 and ITGC-PC-02. The report logic SHALL be retested before the changed report is next used in a Key Control.
- **CMP-009.5.8.4** `[SOX]` End-user computing tools used in Key Controls SHALL be stored in a location with access restricted to authorized Users and version history enabled; formulas and links SHALL be locked or reviewed for integrity by a second person before each quarter-end use. The Head of GRC SHALL review the end-user computing inventory every fiscal quarter.
- **CMP-009.5.8.5** `[SOX]` Where an automated control has been tested once and the APD and PC Key Controls over its system have operated effectively throughout the period since, the Head of GRC MAY rely on that test (benchmarking) instead of retesting the automated control. The CFO SHALL approve the benchmarking plan, and the automated control SHALL be retested at least every 3 fiscal years and after any change to it.

### 5.9 Service organizations and SOC 1 reliance

- **CMP-009.5.9.1** `[SOX]` The Head of GRC SHALL maintain, as part of the scoping memo, a list of service organizations that host, operate or process transactions for any in-scope application or layer, flagged `[SOX]` in the Third Party inventory maintained under RSK-003.
- **CMP-009.5.9.2** `[SOX]` The Head of Procurement SHALL ensure that each contract with a `[SOX]`-flagged service organization requires it to provide a SOC 1 Type II report (SSAE 18 / ISAE 3402) every 12 months and a Bridge Letter on request, and gives the Organization a right of audit where no SOC 1 Type II report is available. Contract requirements otherwise follow RSK-003.
- **CMP-009.5.9.3** `[SOX]` The SOC 1 Type II report relied on SHALL cover at least 6 months of the Organization's fiscal year and SHALL end no more than 3 months before fiscal year-end. Where the report period ends before fiscal year-end, the Head of GRC SHALL obtain a Bridge Letter covering the gap. Where the gap exceeds 3 months, the Head of GRC SHALL perform and document additional procedures (e.g. inquiry of the service organization, testing of the Organization's monitoring controls over the service), approved by the CFO.
- **CMP-009.5.9.4** `[SOX]` The Head of GRC SHALL review each SOC 1 report within 30 days of receipt and document:
  1. the opinion type and any qualification;
  2. whether the systems, locations and control objectives described cover the services the Organization uses;
  3. the report period and its overlap with the fiscal year;
  4. each control exception noted and its effect on the Organization's ICFR;
  5. subservice organizations, whether they are carved out or included, and how carved-out subservice organizations are addressed (e.g. obtaining their SOC 1 report);
  6. complementary subservice organization controls the service organization relies on; and
  7. each complementary user entity control (CUEC) and the Organization control that addresses it.
- **CMP-009.5.9.5** `[SOX]` Each CUEC relevant to the services used SHALL be mapped to an Organization control in the ITGC control matrix or the business-process control matrix, with a named Control Owner, and SHALL be tested under section 5.10. A CUEC without a mapped, effective Organization control SHALL be treated as a Control Deficiency under section 5.11.
- **CMP-009.5.9.6** `[SOX]` A SOC 2 report SHALL NOT be used in place of a SOC 1 report unless the Head of GRC documents that its controls cover the relevant control objectives and the CFO approves the reliance after consulting the External Auditor.
- **CMP-009.5.9.7** `[SOX]` A qualified opinion, or an exception that affects a relevant control objective, SHALL be reported by the Head of GRC to the CFO within 5 business days of the review and evaluated under section 5.11.

### 5.10 Control testing and quarterly support for §302 certification

- **CMP-009.5.10.1** `[SOX]` Testing SHALL be performed under the method in CMP-002, by Internal Audit or by testers independent of the Control Owner. The Head of GRC SHALL prepare an annual ITGC testing plan, approved by the CFO within 60 days after the start of each fiscal year, covering every Key Control in sections 5.4 to 5.9.
- **CMP-009.5.10.2** `[SOX]` Each Key Control SHALL receive a walkthrough (design test) every fiscal year and after any material change to it, and an operating-effectiveness test with an interim test covering at least the first three fiscal quarters and a roll-forward test to fiscal year-end.
- **CMP-009.5.10.3** `[SOX]` Operating-effectiveness samples SHALL be no smaller than:

| Control frequency | Minimum sample (Low or Moderate risk arising from IT) | Minimum sample (High risk arising from IT) |
|---|---|---|
| Annual | 1 | 1 |
| Quarterly | 2 | 2 |
| Monthly | 2 | 3 |
| Weekly | 5 | 10 |
| Daily | 20 | 30 |
| Multiple times per day or event-driven, population ≥ 250 | 25 | 40 |
| Event-driven, population 53–249 | 10 | 15 |
| Event-driven, population 13–52 | 5 | 8 |
| Event-driven, population 5–12 | 2 | 3 |
| Event-driven, population 1–4 | 1 | All |
| Automated | 1 per configuration, with benchmarking under CMP-009.5.8.5 | 1 per configuration, with benchmarking under CMP-009.5.8.5 |

- **CMP-009.5.10.4** `[SOX]` Within 10 business days after each fiscal quarter-end, each Control Owner SHALL complete a quarterly sub-certification confirming that their Key Controls operated as designed during the quarter, listing any failures, and listing any changes to the control or to the Financially Significant Systems it covers.
- **CMP-009.5.10.5** `[SOX]` Within 10 business days after each fiscal quarter-end, each System Owner of a Financially Significant System SHALL report to the Head of GRC any new system, material upgrade, change of hosting or service organization, or Key Control design change made during the quarter.
- **CMP-009.5.10.6** `[SOX]` The Head of GRC SHALL deliver a quarterly ITGC report to the CFO no later than 10 business days before the planned filing date of each Form 10-Q and Form 10-K, stating: testing completed and results; open Control Deficiencies with classification and remediation status; sub-certification exceptions; scope changes; SOC 1 review results; and any change during the quarter that has "materially affected, or is reasonably likely to materially affect" ICFR (Regulation S-K Item 308(c)).
- **CMP-009.5.10.7** `[SOX]` The Head of GRC SHALL make testing workpapers available to the External Auditor on request within 5 business days, to support any reliance on management's testing.

### 5.11 Deficiency evaluation and escalation

- **CMP-009.5.11.1** `[SOX]` A Control Owner, tester or System Owner who identifies a failure of a Key Control SHALL report it to the Head of GRC within 2 business days of identification.
- **CMP-009.5.11.2** `[SOX]` The Head of GRC SHALL document each Control Deficiency within 10 business days of the report, including: the control, the failure, its Root Cause, the period affected, the Financially Significant Systems and dependent automated controls, IT-dependent manual controls and IPE affected, compensating controls, and a preliminary classification as Control Deficiency, Significant Deficiency or Material Weakness under PCAOB AS 2201.
- **CMP-009.5.11.3** `[SOX]` When evaluating an ITGC deficiency, the Head of GRC SHALL assess its effect on each dependent application control and report, and SHALL NOT conclude that a dependent control is unaffected unless a compensating control or direct testing of the dependent control's output over the affected period supports that conclusion.
- **CMP-009.5.11.4** `[SOX]` Escalation SHALL follow this table:

| Preliminary classification | Escalated to | Time limit |
|---|---|---|
| Control Deficiency | CFO, through the quarterly ITGC report | Next quarterly report (CMP-009.5.10.6) |
| Significant Deficiency (potential or confirmed) | CFO and Internal Audit Director; CFO informs the External Auditor | Within 2 business days of preliminary classification |
| Significant Deficiency (confirmed) | Audit Committee, by the CFO | At the next Audit Committee meeting and before the next periodic filing |
| Material Weakness (potential or confirmed) | CFO, CEO, GC and Internal Audit Director; CFO informs the External Auditor | Within 2 business days of preliminary classification |
| Material Weakness (potential or confirmed) | Audit Committee chair, by the CFO | Within 5 business days of preliminary classification |

- **CMP-009.5.11.5** `[SOX]` The CFO SHALL make the final classification of each Significant Deficiency and Material Weakness, after consulting the GC and the Internal Audit Director and discussing the classification with the External Auditor. Aggregation of deficiencies SHALL be evaluated at each fiscal quarter-end and at fiscal year-end. The CEO and CFO SHALL consider each Material Weakness for disclosure in the SOX §302 certifications and the SOX §404 management report.
- **CMP-009.5.11.6** `[SOX]` Where a deficiency may indicate fraud, intentional circumvention or a Security Incident, the Head of GRC SHALL also report it under RES-002 or CMP-006, as applicable, within the same 2 business days.
- **CMP-009.5.11.7** `[SOX]` The Head of GRC SHALL report all open Significant Deficiencies and Material Weaknesses, with remediation status, to the Audit Committee every fiscal quarter.

### 5.12 Remediation

- **CMP-009.5.12.1** `[SOX]` The Control Owner SHALL submit a remediation plan, with actions, owners and dates, to the Head of GRC within 30 days of the deficiency being documented. The CFO SHALL approve plans for Significant Deficiencies and Material Weaknesses.
- **CMP-009.5.12.2** `[SOX]` A remediated control SHALL operate for at least the following number of occurrences before it is retested and the deficiency closed:

| Control frequency | Minimum occurrences after remediation before retest |
|---|---|
| Annual | 1 |
| Quarterly | 2 |
| Monthly | 2 |
| Weekly | 5 |
| Daily | 20 |
| Multiple times per day or event-driven | 25 occurrences or 30 days, whichever is later |
| Automated | 1, after the corrected configuration is moved to production under ITGC-PC-01 |

- **CMP-009.5.12.3** `[SOX]` The Head of GRC SHALL schedule remediation so that Significant Deficiencies and Material Weaknesses can be retested before fiscal year-end. A deficiency not retested effective by fiscal year-end SHALL be reported to the CFO as open for management's §404(a) assessment.
- **CMP-009.5.12.4** `[SOX]` Exceptions under CMP-003 SHALL NOT be used to close or defer a Control Deficiency over a Key Control (section 9).

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CFO | Approves this Standard, the scoping memo, the ITGC control matrix, the testing plan, the financial SoD ruleset and remediation plans for Significant Deficiencies and Material Weaknesses; makes final deficiency classification; certifies under SOX §302 with the CEO; escalates to the Audit Committee |
| CEO | Co-certifies under SOX §302; receives Material Weakness escalations |
| Audit Committee | Oversees ICFR; receives Significant Deficiency and Material Weakness reports |
| Head of GRC | Owns this Standard; performs scoping; maintains the control matrix, IPE inventory and service organization list; reviews SOC 1 reports; prepares the quarterly ITGC report; documents and escalates deficiencies |
| Internal Audit Director | Performs or oversees independent testing under CMP-002; receives Significant Deficiency and Material Weakness escalations |
| GC | Advises on deficiency classification and disclosure; receives Material Weakness escalations |
| CIO | Ensures IT operations staff operate the CO and PC Key Controls on Financially Significant Systems |
| CISO | Ensures the security controls underlying the APD Key Controls operate on Financially Significant Systems |
| System Owners | Operate ITGCs for their systems; identify supporting layers; notify scope changes; complete quarterly reports |
| Data Owners | Approve access, data fixes and business-impacting changes; perform Access Reviews |
| Control Owners | Operate Key Controls; complete quarterly sub-certifications; report failures within 2 business days; deliver remediation plans |
| Head of Procurement | Includes SOC 1 and audit-right clauses in service organization contracts |
| SOC Manager | Operates privileged-activity monitoring for ITGC-APD-10 |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| CMP-009.7.1 | Scoping refresh | Every fiscal year, approved by the CFO within 60 days after fiscal year start; updated every fiscal quarter |
| CMP-009.7.2 | Notice of new or upgraded Financially Significant System | At project initiation and at least 60 days before go-live |
| CMP-009.7.3 | Notice of scope-affecting change | Within 10 business days |
| CMP-009.7.4 | User Access Review frequency for Financially Significant Systems | As set in SEC-003 |
| CMP-009.7.5 | Separation reconciliation | Monthly |
| CMP-009.7.6 | Direct data change log review | Monthly |
| CMP-009.7.7 | Production change-to-ticket reconciliation | Monthly |
| CMP-009.7.8 | Financial SoD ruleset re-approval | Every 12 months |
| CMP-009.7.9 | Post-implementation review | Within 90 days after go-live |
| CMP-009.7.10 | Failed Backup resolution | Successful Backup confirmed within 1 business day |
| CMP-009.7.11 | Automated control benchmark retest | At least every 3 fiscal years and after any change |
| CMP-009.7.12 | SOC 1 Type II coverage | At least 6 months of the fiscal year, ending no more than 3 months before fiscal year-end; Bridge Letter for any gap |
| CMP-009.7.13 | SOC 1 review | Within 30 days of receipt |
| CMP-009.7.14 | Testing plan approval | Within 60 days after fiscal year start |
| CMP-009.7.15 | Minimum test samples | Table in CMP-009.5.10.3 |
| CMP-009.7.16 | Control Owner quarterly sub-certification | Within 10 business days after quarter-end |
| CMP-009.7.17 | Quarterly ITGC report to CFO | At least 10 business days before each Form 10-Q / 10-K filing |
| CMP-009.7.18 | Control failure reported to Head of GRC | Within 2 business days |
| CMP-009.7.19 | Deficiency documented | Within 10 business days |
| CMP-009.7.20 | Significant Deficiency / Material Weakness escalation | Table in CMP-009.5.11.4 |
| CMP-009.7.21 | Remediation plan | Within 30 days of documentation |
| CMP-009.7.22 | Minimum operation before retest | Table in CMP-009.5.12.2 |
| CMP-009.7.23 | Year-end Backup retention for Financially Significant Systems | As set in CMP-004 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Financially Significant Systems with all in-scope layers mapped to Key Controls | 100% | Quarterly | Head of GRC |
| Key Controls tested per plan by quarter-end | 100% of planned tests | Quarterly | Internal Audit Director |
| Key Controls tested effective | ≥ 95% | Quarterly | Head of GRC |
| Control Owner sub-certifications received on time | 100% | Quarterly | Head of GRC |
| Production changes without an approved Change record (ITGC-PC-05) | 0 | Monthly | CIO |
| Separated Users with active access past the SEC-003 revocation time (ITGC-APD-02) | 0 | Monthly | CISO |
| `[SOX]` service organizations with a current, reviewed SOC 1 Type II report or documented alternative procedures | 100% | Quarterly | Head of GRC |
| CUECs mapped to a tested Organization control | 100% | Quarterly | Head of GRC |
| Open Significant Deficiencies / Material Weaknesses | 0 at fiscal year-end | Quarterly | CFO |
| Remediation plans delivered within 30 days | 100% | Quarterly | Head of GRC |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

In addition:

- No Exception MAY be granted that removes a Key Control, closes a Control Deficiency or
  defers its remediation. A Key Control that cannot operate is a Control Deficiency and is handled
  under sections 5.11 and 5.12.
- Exceptions to underlying requirements in home documents (e.g. SEC-003, SEC-013) that affect a
  Financially Significant System SHALL be reviewed by the Head of GRC for ICFR impact before
  approval and reported in the next quarterly ITGC report.

## 10. Enforcement

Non-compliance is handled under CMP-007.

Falsifying control Evidence, sub-certifications or test results, or knowingly circumventing a
Key Control, SHALL be reported under CMP-006 and may also constitute a violation of law,
including SOX §§802 and 1102.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| CMP-009.5.1 – 5.3 | 4.3, 6.1.3; A.5.9, A.5.31 | GV.OC-03, ID.AM-02 | PM-5, CM-8 | 1.1, 2.1 | CC1.4, CC2.1, CC3.1 | MEA03, APO01 | `[SOX]` §§302, 404; PCAOB AS 2201 |
| CMP-009.5.4 | A.5.3, A.5.15, A.5.16, A.5.18, A.8.2, A.8.5 | PR.AA-01, PR.AA-05 | AC-2, AC-5, AC-6, IA-2, AU-6 | 5.1, 5.3, 6.1, 6.2, 6.8 | CC6.1, CC6.2, CC6.3 | DSS05, DSS06 | `[SOX]` §404 |
| CMP-009.5.5 | A.8.9, A.8.31, A.8.32 | PR.PS-01 | CM-3, CM-5, CM-6 | 4.1, 16.1 | CC8.1 | BAI06, BAI07 | `[SOX]` §404 |
| CMP-009.5.6 | A.5.8, A.8.25, A.8.29, A.8.33 | PR.PS-06 | SA-3, SA-8, SA-11 | 16.1 | CC8.1 | BAI03, BAI07 | `[SOX]` §404 |
| CMP-009.5.7 | A.8.6, A.8.13, A.8.15 | PR.DS-11, DE.CM-09 | CP-9, CP-10, AU-6 | 11.2, 11.5 | CC7.2, A1.2, A1.3 | DSS01, DSS04 | `[SOX]` §404 |
| CMP-009.5.8 | A.5.33, A.8.32 | PR.DS-01 | SI-10, CM-3 | 3.1 | CC2.1, CC8.1 | DSS06 | `[SOX]` §404; PCAOB AS 1105 |
| CMP-009.5.9 | A.5.19, A.5.20, A.5.22 | GV.SC-07 | SA-9, SR-6 | 15.5, 15.6 | CC9.2 | APO10 | `[SOX]` §404; AICPA SSAE 18 (AT-C 320) |
| CMP-009.5.10 | 9.1, 9.2; A.5.35, A.5.36 | GV.OV-01, ID.IM-01 | CA-2, CA-7 | — | CC4.1 | MEA02 | `[SOX]` §302; §404(a); Reg. S-K Item 308 |
| CMP-009.5.11 – 5.12 | 10.2 | GV.OV-02, ID.IM-01 | CA-5, PM-4 | — | CC4.2, CC5.1 | MEA02, MEA03 | `[SOX]` §§302, 404; PCAOB AS 2201 |

## 12. Related documents

ISP-000, GOV-001, GOV-002, RSK-002, RSK-003, CMP-001, CMP-002, CMP-003, CMP-004, CMP-006,
CMP-007, SEC-001, SEC-003, SEC-004, SEC-005, SEC-010, SEC-012, SEC-013, SEC-018, RES-002,
TPL-008, REF-001, REF-002

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Head of GRC | | | |
| Approver: Chief Financial Officer (CFO) | | | |
