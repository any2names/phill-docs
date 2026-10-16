# RSK-004 — Business Impact Analysis Standard

## 1. Document control

| Field | Value |
|---|---|
| Document ID | RSK-004 |
| Title | Business Impact Analysis Standard |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 2 — Standard |
| Classification | Internal |
| Owner | Business Continuity Manager |
| Approver | Chief Information Security Officer (CISO) |
| Effective date | [DECISION REQUIRED: Date of CISO approval] |
| Next review date | Effective date + 12 months |
| Parent document | RES-004 Business Continuity Policy |
| Related documents | RSK-001, RSK-002, RSK-003, SEC-001, SEC-018, RES-004, RES-005, CMP-009 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Business Continuity Manager | Initial release |

## 3. Purpose

This Standard sets how the Organization performs its Business Impact Analysis (BIA): the
method, the criteria for assigning each business process and Information System a Recovery
Tier, the RTO and RPO of each Recovery Tier, the maximum tolerable period of disruption, and
the mapping of dependencies. It is the single source of RTO and RPO values used by the
Backup Policy (SEC-018), the Disaster Recovery Plan (RES-005) and third-party contracts
(RSK-003).

## 4. Scope

- **Business processes:** every business process of the Organization, including customer-facing services, internal operations, `[SOX]` financial reporting processes, and `[HIPAA]` processes creating, receiving, maintaining or transmitting ePHI.
- **Systems and data:** every Information System, Cloud Service, data set and facility recorded in the Asset Inventory (SEC-001) that supports an in-scope process.
- **People:** process owners (acting as Asset Owners for the process), System Owners, Data Owners, the Business Continuity Manager and BIA participants.
- **Locations:** all Organization sites and the hosting locations of in-scope systems.
- **Third parties:** Third Parties on which an in-scope process or system depends.

## 5. Requirements

### 5.1 BIA method

- **RSK-004.5.1.1** The Business Continuity Manager SHALL perform the BIA using the following steps: (1) identify business processes from the organizational structure and the Asset Inventory; (2) interview or survey the Asset Owner of each process using a standard BIA questionnaire; (3) assess impact over time (section 5.2); (4) determine the maximum tolerable period of disruption (section 5.4); (5) assign a Recovery Tier (section 5.3); (6) map dependencies (section 5.5); (7) identify minimum resources for recovery (section 5.6); (8) validate results with the Asset Owner and executive owner; (9) obtain approval (section 5.7).
- **RSK-004.5.1.2** The BIA questionnaire SHALL capture, for each process: purpose and outputs; Asset Owner; peak periods and calendar dependencies (for example month-end close, open enrollment, seasonal peaks); minimum staffing; Manual Workarounds and how long they can be sustained; regulatory and contractual deadlines (with reference to the Obligations Register, CMP-001); upstream and downstream processes; supporting Information Systems, data, facilities and Third Parties; and data-loss tolerance.
- **RSK-004.5.1.3** Each process SHALL be analyzed at its peak period. Where impact differs materially by period, the BIA SHALL record the peak-period result and use it for tier assignment.
- **RSK-004.5.1.4** The Asset Owner of each process SHALL validate the BIA output in writing within 10 business days of receiving the draft.
- **RSK-004.5.1.5** Where an Asset Owner does not respond within 10 business days, the Business Continuity Manager SHALL escalate to the Asset Owner's executive, and the draft SHALL be treated as validated after a further 5 business days.

### 5.2 Impact over time

- **RSK-004.5.2.1** For each process, the BIA SHALL score the impact of total loss of the process at each of the following points after disruption: 1 hour, 4 hours, 24 hours, 72 hours, 7 days and 30 days.
- **RSK-004.5.2.2** Impacts SHALL be scored using the five impact dimensions and the 1–5 scale in RSK-002 (Financial, Regulatory & legal, Operational, Reputational, Safety & privacy). For the purposes of the BIA, the Operational dimension SHALL be scored on the effect on the process's outputs and downstream processes, not on Recovery Tier criteria, to avoid circular scoring.
- **RSK-004.5.2.3** The impact at each point SHALL be the highest dimension score at that point, consistent with RSK-002.
- **RSK-004.5.2.4** The BIA SHALL also record data-loss tolerance: the maximum period of transactions or data changes the process can lose and recreate, and the effort required to recreate them.

### 5.3 Recovery Tiers and assignment criteria

- **RSK-004.5.3.1** Every in-scope process and Information System SHALL be assigned one of the following Recovery Tiers:

| Recovery Tier | Name | RTO | RPO | Maximum tolerable period of disruption |
|---|---|---|---|---|
| Tier 0 | Mission-critical | 4 hours | 15 minutes | 24 hours |
| Tier 1 | Critical | 24 hours | 4 hours | 72 hours |
| Tier 2 | Important | 72 hours | 24 hours | 7 days |
| Tier 3 | Deferrable | 7 days | 7 days | 30 days |

- **RSK-004.5.3.2** A process SHALL be assigned the Recovery Tier corresponding to the earliest point in its impact-over-time profile at which impact reaches 4 (Major) on any dimension:

| Earliest point at which impact reaches 4 (Major) | Recovery Tier assigned |
|---|---|
| At or before 4 hours | Tier 0 |
| After 4 hours, at or before 24 hours | Tier 1 |
| After 24 hours, at or before 72 hours | Tier 2 |
| After 72 hours, or never within 30 days | Tier 3 |

- **RSK-004.5.3.3** Notwithstanding RSK-004.5.3.2, the following processes SHALL be assigned no lower than the tier shown: processes whose loss would cause injury or loss of life: Tier 0; processes subject to a regulatory or contractual availability commitment shorter than the RTO of the tier otherwise assigned: the tier whose RTO meets the commitment; `[SOX]` processes supporting financial close and reporting: Tier 1 during close periods; `[HIPAA]` processes on which emergency access to ePHI depends: Tier 1.
- **RSK-004.5.3.4** A process SHALL be assigned the RPO of its Recovery Tier unless the data-loss tolerance recorded under RSK-004.5.2.4 is shorter, in which case the process SHALL be assigned the Recovery Tier whose RPO meets the tolerance.
- **RSK-004.5.3.5** An Information System SHALL inherit the most critical (lowest-numbered) Recovery Tier of any process it supports.
- **RSK-004.5.3.6** An Asset Owner MAY request a more critical Recovery Tier than the criteria produce, with a business justification approved by the Business Continuity Manager. A less critical tier than the criteria produce SHALL require a Risk Acceptance under RSK-001.
- **RSK-004.5.3.7** The Recovery Tier SHALL be recorded in the Asset Inventory (SEC-001) within 10 business days of BIA approval.
- **RSK-004.5.3.8** Backup frequency and restore testing by Recovery Tier are set in SEC-018. Recovery procedures and DR testing are set in RES-005 and RES-004.

### 5.4 Maximum tolerable period of disruption

- **RSK-004.5.4.1** For each process, the BIA SHALL record the maximum tolerable period of disruption (MTPD) as the earliest point in its impact-over-time profile at which impact reaches 5 (Severe) on any dimension, or 30 days if impact does not reach 5 within 30 days.
- **RSK-004.5.4.2** The MTPD recorded for a process SHALL NOT exceed the MTPD of its Recovery Tier in RSK-004.5.3.1. Where the analyzed MTPD is shorter than the tier's MTPD, the analyzed value SHALL apply to that process.
- **RSK-004.5.4.3** The RTO of each process SHALL be shorter than its MTPD. Where the analyzed MTPD is less than or equal to the RTO of the assigned tier, the process SHALL be moved to the next more critical tier; a Recovery Tier 0 process in this position SHALL be recorded under RSK-004.5.4.4.
- **RSK-004.5.4.4** A process that cannot be recovered within its MTPD with current capabilities SHALL be recorded in the Risk Register in category C5 (RSK-001) and scored under RSK-002.

### 5.5 Dependency mapping

- **RSK-004.5.5.1** For each Recovery Tier 0, Tier 1 and Tier 2 process, the BIA SHALL map upstream and downstream dependencies on: other business processes; Information Systems and Cloud Services; data sets; infrastructure services (identity, DNS, network, certificates, key management, logging); facilities; key personnel and skills; and Third Parties (with their vendor tier under RSK-003).
- **RSK-004.5.5.2** Dependency maps SHALL be recorded in, or linked from, the Asset Inventory (SEC-001), and SHALL identify single points of failure.
- **RSK-004.5.5.3** Each dependency of a process SHALL have a Recovery Tier at least as critical as the process, or a documented workaround that allows the process to meet its RTO without the dependency. Dependencies that meet neither condition SHALL be recorded in the Risk Register.
- **RSK-004.5.5.4** Shared infrastructure services on which any Recovery Tier 0 system depends (for example Identity Providers, DNS, network core, key management) SHALL be assigned Recovery Tier 0.
- **RSK-004.5.5.5** Third Parties supporting a Recovery Tier 0 or Tier 1 process SHALL have contractual recovery commitments meeting the process RTO and RPO, as required by RSK-003, or the gap SHALL be recorded in the Risk Register.
- **RSK-004.5.5.6** Dependency maps for Recovery Tier 0 and Tier 1 processes SHALL be updated within 30 days of any Change that adds, removes or replaces a dependency.

### 5.6 Minimum resources for recovery

- **RSK-004.5.6.1** For each Recovery Tier 0 and Tier 1 process, the BIA SHALL record the minimum resources required to operate at an acceptable reduced level until full recovery: staff numbers and skills, workspace, Endpoints, systems, data, Third Party services and vital records.
- **RSK-004.5.6.2** The minimum resource records SHALL be provided to the owners of RES-004 and RES-005 for use in continuity and recovery plans within 10 business days of BIA approval.

### 5.7 Approval, refresh and records

- **RSK-004.5.7.1** The BIA SHALL be refreshed every 12 months and on Significant Change.
- **RSK-004.5.7.2** For the purpose of RSK-004.5.7.1, Significant Change (GOV-006) SHALL include at minimum: a new or discontinued business process or product line; a merger, acquisition or divestiture; a new Recovery Tier 0 or Tier 1 Information System; relocation of a facility or hosting region; a change of a vendor Tier 1 Third Party supporting a Recovery Tier 0 or Tier 1 process; and a Sev-1 incident (RES-002) that caused an outage exceeding the RTO of the affected tier. The BIA for the affected processes SHALL be updated within 30 days of the change.
- **RSK-004.5.7.3** The Business Continuity Manager SHALL present the BIA results, including all Recovery Tier assignments and gaps, to the ISSC within 30 days of completion. Recovery Tier 0 and Tier 1 assignments SHALL be approved by the ISSC.
- **RSK-004.5.7.4** BIA records, including questionnaires, impact-over-time profiles, tier assignments, dependency maps and approvals, SHALL be retained as Evidence under CMP-004.
- **RSK-004.5.7.5** BIA results SHALL be classified Confidential under SEC-002.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CISO | Approves this Standard. |
| ISSC | Receives BIA results; approves Recovery Tier 0 and Tier 1 assignments (5.7.3). |
| Business Continuity Manager | Owns this Standard; performs the BIA; approves upward tier requests (5.3.6); maintains dependency maps; escalates non-responses (5.1.5). |
| Asset Owner (process owner) | Completes the BIA questionnaire; validates results within 10 business days (5.1.4); requests tier changes with justification. |
| System Owner | Provides system dependency information; confirms technical recovery capability against the assigned tier. |
| CIO | Ensures Recovery Tiers are reflected in the Asset Inventory and in RES-005 recovery sequencing. |
| Head of GRC | Records BIA gaps and Risk Acceptances in the Risk Register. |
| Head of Procurement | Provides Third Party information for dependency mapping. |
| CFO | `[SOX]` Confirms Recovery Tiers for financial close and reporting processes. |
| HIPAA Security Officer | `[HIPAA]` Confirms the applications and data criticality analysis for ePHI systems. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| RSK-004.7.1 | Recovery Tiers | Tier 0 Mission-critical: RTO 4 h / RPO 15 min · Tier 1 Critical: RTO 24 h / RPO 4 h · Tier 2 Important: RTO 72 h / RPO 24 h · Tier 3 Deferrable: RTO 7 days / RPO 7 days |
| RSK-004.7.2 | BIA refresh | Every 12 months and on significant change |
| RSK-004.7.3 | Maximum tolerable period of disruption by tier | Tier 0 24 hours · Tier 1 72 hours · Tier 2 7 days · Tier 3 30 days |
| RSK-004.7.4 | Impact-over-time assessment points | 1 h, 4 h, 24 h, 72 h, 7 days, 30 days |
| RSK-004.7.5 | Tier assignment threshold | Earliest point at which impact reaches 4 (Major) on RSK-002 scale |
| RSK-004.7.6 | MTPD threshold | Earliest point at which impact reaches 5 (Severe), capped at the tier MTPD |
| RSK-004.7.7 | Asset Owner validation | Within 10 business days of draft; escalation then deemed validated after a further 5 business days |
| RSK-004.7.8 | Recording of tier in Asset Inventory | Within 10 business days of BIA approval |
| RSK-004.7.9 | BIA update after Significant Change | Within 30 days |
| RSK-004.7.10 | Dependency map update for Tier 0/1 | Within 30 days of dependency Change |
| RSK-004.7.11 | BIA results to ISSC | Within 30 days of completion |
| RSK-004.7.12 | Backup frequency and restore testing | As set in SEC-018 |
| RSK-004.7.13 | BC/DR exercise frequency | As set in RES-004 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| In-scope processes with a current BIA (≤ 12 months) | 100% | Quarterly | Business Continuity Manager |
| Information Systems in the Asset Inventory with an assigned Recovery Tier | 100% | Quarterly | CIO |
| Recovery Tier 0/1 processes with a complete dependency map | 100% | Quarterly | Business Continuity Manager |
| Dependencies less critical than their process without workaround or Risk Register entry | 0 | Quarterly | Business Continuity Manager |
| Recovery Tier 0/1 processes whose tested recovery time (RES-005) exceeded RTO | 0 | After each test | Business Continuity Manager |
| Asset Owner validations within 10 business days | ≥ 90% | Each BIA cycle | Business Continuity Manager |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

A Recovery Tier less critical than the criteria in section 5.3 produce is handled as a Risk Acceptance under RSK-001, not as an Exception.

## 10. Enforcement

Non-compliance is handled under CMP-007.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| RSK-004.5.1 – 5.2 | 6.1.2; A.5.29, A.5.30 | GV.OC-04, GV.OC-05, ID.RA-04 | CP-2, RA-9, PM-11 | — | CC9.1, A1.2 | DSS04.02 | `[HIPAA]` §164.308(a)(7)(ii)(E) |
| RSK-004.5.3 – 5.4 | A.5.30, A.8.14 | ID.AM-05, RC.RP-01 | CP-2, CP-10 | 11.1 | A1.2, A1.3 | DSS04.02, DSS04.03 | `[HIPAA]` §164.308(a)(7)(ii)(E); `[SOX]` §404 |
| RSK-004.5.5 | A.5.29, A.5.30, A.8.14 | GV.OC-05, ID.AM-03, GV.SC-04 | CP-2, CP-8, RA-9, SA-9 | 15.1 | CC9.1, CC9.2 | DSS04.02, APO10 | — |
| RSK-004.5.6 – 5.7 | 7.5, A.5.30 | GV.OC-04, ID.IM-01 | CP-2 | — | A1.2 | DSS04.01 | `[HIPAA]` §164.308(a)(7)(i) |

## 12. Related documents

RES-004, RES-005, RSK-001, RSK-002, RSK-003, SEC-001, SEC-002, SEC-018, CMP-001, CMP-003, CMP-004, CMP-007, CMP-009, RES-002, REF-001

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Business Continuity Manager | | | |
| Approver: CISO | | | |
