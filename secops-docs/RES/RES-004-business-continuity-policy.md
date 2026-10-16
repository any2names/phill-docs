# RES-004 — Business Continuity Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | RES-004 |
| Title | Business Continuity Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Business Continuity Manager |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | RSK-001, RSK-002, RSK-003, RSK-004, RES-001, RES-002, RES-003, RES-005, SEC-001, SEC-016, SEC-018, PPL-001, PPL-002, CMP-004 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Business Continuity Manager | Initial release |

## 3. Purpose

This Policy establishes the Organization's business continuity management (BCM) program,
aligned to ISO 22301:2019. It sets the requirements for continuing critical business
processes during and after a disruption, for the Crisis Management Team that directs the
Organization's response to a major disruption, for the Business Continuity Plans (BCPs) that
each critical business process maintains, and for the exercises that prove those
arrangements work. Recovery of Information Systems is carried out under RES-005; recovery
targets are set by the Business Impact Analysis under RSK-004.

## 4. Scope

- **People:** all Workforce Members, with specific duties for Crisis Management Team members, BCP owners and the Business Continuity Manager.
- **Processes:** every business process assigned a Recovery Tier under RSK-004. BCP requirements in section 5.6 apply to every process assigned Tier 0, Tier 1 or Tier 2.
- **Systems and data:** Information Systems and data that support in-scope processes. Technical recovery is governed by RES-005 and Backup by SEC-018.
- **Locations:** all offices, data centers, operations sites and remote-work arrangements from which in-scope processes are performed.
- **Third parties:** Third Parties on which an in-scope process depends, through RSK-003.
- **Exclusions:** none. Life-safety response (evacuation, first aid) is governed by SEC-016 and local emergency procedures; this Policy governs business continuation once life-safety actions are complete.

## 5. Policy statements

### 5.1 BCM program and scope

- **RES-004.5.1.1** The Organization SHALL operate a BCM program covering the elements of ISO 22301:2019 clauses 4 to 10: context, leadership, planning, support, operation (BIA, risk assessment, strategies, plans, exercises), performance evaluation and improvement.
- **RES-004.5.1.2** The Business Continuity Manager SHALL maintain a written BCM program scope statement listing the business units, locations, processes and products in scope, and any exclusions with justification. The scope statement SHALL be approved by the ISSC with this Policy and reviewed every 12 months.
- **RES-004.5.1.3** The Business Continuity Manager SHALL maintain a BCM program register listing every in-scope process, its Recovery Tier (from RSK-004), its BCP owner, its BCP version and review date, and the date and result of its last exercise.
- **RES-004.5.1.4** The CEO SHALL be the executive accountable for the BCM program. The Business Continuity Manager SHALL be responsible for its operation.
- **RES-004.5.1.5** Each business unit leader SHALL nominate, in writing, a BCP owner for each in-scope process in their unit within 30 days of the process being assigned a Recovery Tier.
- **RES-004.5.1.6** The Business Continuity Manager SHALL report BCM program status to the ISSC at least quarterly, covering: BCP currency, exercise completion, open corrective actions, and plan activations since the last report.

### 5.2 Business impact analysis and risk assessment

- **RES-004.5.2.1** BIAs SHALL be performed, and Recovery Tiers, RTOs and RPOs assigned, under RSK-004. This Policy SHALL NOT set or vary those values.
- **RES-004.5.2.2** Each BCP SHALL use the Recovery Tier, RTO and RPO recorded for its process in the current BIA. Where the BIA is refreshed under RSK-004, the BCP owner SHALL update the BCP within 30 days of the BIA approval.
- **RES-004.5.2.3** Risks of disruption to in-scope processes (including loss of site, loss of systems, loss of workforce, loss of supplier and loss of utilities) SHALL be assessed under RSK-002 and recorded in the Risk Register (TPL-001).
- **RES-004.5.2.4** Where a BCP cannot meet its RTO with the current strategy, the BCP owner SHALL record the gap as a Risk under RSK-001 within 10 business days of identifying it.

### 5.3 Continuity strategies

- **RES-004.5.3.1** For each in-scope process, the BCP owner SHALL select and document a continuity strategy that is capable of meeting the process RTO, covering each of the following resource categories: people, premises, technology and data, information and records, suppliers, and equipment.
- **RES-004.5.3.2** Continuity strategies SHALL be selected from, or combine, the following options: workload transfer to another site or team; remote working; alternate premises; Manual Workaround; reciprocal or contracted recovery services; alternate supplier; and technology recovery under RES-005.
- **RES-004.5.3.3** Manual Workarounds for a Tier 0 or Tier 1 process SHALL be documented step by step, SHALL identify the forms, records and reference data required, and SHALL describe how transactions processed manually are reconciled into Information Systems after recovery.
- **RES-004.5.3.4** `[SOX]` Manual Workarounds affecting a financially significant process SHALL be reviewed by the Head of GRC to confirm that compensating controls preserve the Key Controls identified under CMP-009.
- **RES-004.5.3.5** `[PCI]` Continuity strategies SHALL NOT process, store or transmit CHD outside the CDE defined under SEC-019, including on paper, unless the alternate arrangement has been brought into CDE scope before use.
- **RES-004.5.3.6** `[HIPAA]` Continuity strategies for processes that create, receive, maintain or transmit ePHI SHALL include an Emergency Mode Operation plan that preserves the security of ePHI while operating in emergency mode, as required by 45 CFR §164.308(a)(7)(ii)(C).
- **RES-004.5.3.7** Alternate premises used for a Tier 0 or Tier 1 process SHALL meet SEC-016 and SHALL be located so that a single regional event does not affect both the primary and alternate site. [DECISION REQUIRED: Minimum separation between primary and alternate premises. Recommended default: different utility grid and flood zone, and at least 50 km apart.]
- **RES-004.5.3.8** The Business Continuity Manager SHALL review every continuity strategy for a Tier 0 or Tier 1 process at least every 12 months and confirm that the cost of the strategy is approved by the business unit leader.

### 5.4 Crisis Management Team

- **RES-004.5.4.1** The Organization SHALL maintain a Crisis Management Team (CMT) to provide strategic direction during any disruption that meets the activation criteria in RES-004.5.4.4.
- **RES-004.5.4.2** The CMT SHALL be composed as follows:

  | CMT role | Primary | Alternate |
  |---|---|---|
  | Chair | CEO | CFO |
  | Members | CIO, CTO, CISO, CPO, GC, CFO, CHRO, Head of Facilities | Each member SHALL name one alternate in writing |
  | Coordinator and secretary | Business Continuity Manager | Delegate named by the Business Continuity Manager |
  | Communications | [ASSUMPTION: The Organization has a corporate communications function; its leader attends the CMT as a non-voting member and leads external and workforce messaging.] | Named delegate |

- **RES-004.5.4.3** Where the CFO acts as Chair, the CFO's alternate as a member SHALL attend in the CFO's place.
- **RES-004.5.4.4** The CEO, or any CMT member, SHALL activate the CMT when any of the following occurs:
  1. a disruption is projected to exceed the RTO of a Tier 0 or Tier 1 process under RSK-004;
  2. a Sev-1 Security Incident, as classified under RES-002, causes or is projected to cause business disruption;
  3. a disaster is declared under RES-005;
  4. a life-safety event affects Workforce Members or premises.
- **RES-004.5.4.5** The CMT SHALL convene, in person or virtually, within 1 hour of activation.
- **RES-004.5.4.6** A CMT meeting is quorate when the Chair (or alternate) and at least three members (or their alternates) are present. Where quorum cannot be reached within 1 hour of activation, the Chair (or alternate) SHALL act alone and the decisions SHALL be ratified at the next quorate meeting.
- **RES-004.5.4.7** The CMT SHALL have authority to: invoke any BCP; authorize emergency spending up to the limit in RES-004.7.5; relocate Workforce Members and operations; authorize external communications in coordination with RES-002 and RES-003; and direct priorities for technology recovery under RES-005.
- **RES-004.5.4.8** While a Security Incident is being handled under RES-002, the Incident Commander under RES-002 SHALL retain command of technical response. The CMT SHALL set business priorities, and the CISO SHALL be the link between the CMT and the Incident Commander.
- **RES-004.5.4.9** The Business Continuity Manager SHALL maintain a decision log for each CMT activation recording each decision, its time, its rationale and the decision maker.
- **RES-004.5.4.10** The CMT SHALL meet at an interval set at its first meeting and no less often than every 24 hours until the Chair stands it down.
- **RES-004.5.4.11** The Chair SHALL stand down the CMT only when all affected Tier 0 and Tier 1 processes are operating normally or under a stable BCP, and SHALL record the stand-down in the decision log.
- **RES-004.5.4.12** The Business Continuity Manager SHALL maintain a CMT handbook containing contact details for members and alternates, the activation and convening process, the meeting agenda template, the decision log template, and the locations of virtual and physical command centers. Contact details SHALL be verified every 6 months.
- **RES-004.5.4.13** The CMT handbook and all BCPs SHALL be accessible during an outage of the Organization's primary Information Systems, through at least one offline or independently hosted copy available to every CMT member and BCP owner.

### 5.5 Business continuity plans

- **RES-004.5.5.1** Each process assigned Tier 0, Tier 1 or Tier 2 under RSK-004 SHALL have a documented BCP. Tier 3 processes MAY be covered by a shared BCP for their business unit.
- **RES-004.5.5.2** Each BCP SHALL contain at least:
  1. process name, BCP owner and alternate, Recovery Tier, RTO and RPO (by reference to the BIA);
  2. activation criteria and the person authorized to activate the BCP;
  3. the continuity strategy selected under section 5.3 and step-by-step recovery actions;
  4. minimum staffing, named critical roles and their alternates;
  5. dependencies on Information Systems (with their Recovery Tiers), other processes, Third Parties, premises and equipment;
  6. Manual Workarounds and the reconciliation steps required after recovery;
  7. internal and external contact lists, including Third Party contacts;
  8. communication actions, cross-referenced to the CMT communications lead and, where a Security Incident is involved, to RES-002 and RES-003;
  9. resumption and return-to-normal steps;
  10. version, approval date and next review date.
- **RES-004.5.5.3** Each BCP SHALL be approved by the business unit leader accountable for the process and accepted by the Business Continuity Manager for completeness against RES-004.5.5.2.
- **RES-004.5.5.4** BCP owners SHALL activate their BCP when the activation criteria in the BCP are met or when directed by the CMT, and SHALL notify the Business Continuity Manager within 1 hour of activation.
- **RES-004.5.5.5** BCPs SHALL NOT contain Restricted information. Where a BCP needs Restricted information (for example Secrets), it SHALL reference the controlled location where that information is held.

### 5.6 Pandemic and widespread illness

- **RES-004.5.6.1** The Business Continuity Manager SHALL maintain a pandemic annex to the CMT handbook, using a planning assumption of 40% workforce absenteeism sustained for 8 weeks, with waves of absence over 12 months.
- **RES-004.5.6.2** The pandemic annex SHALL define staged response levels, triggered by public health authority alert levels, with predetermined actions at each level, including: remote working, site access restrictions, travel restrictions, hygiene measures and the suspension of non-essential activities.
- **RES-004.5.6.3** Each Tier 0 and Tier 1 BCP SHALL show how the process continues at the planning assumption in RES-004.5.6.1, including the use of cross-trained staff and remote working.
- **RES-004.5.6.4** The CIO SHALL confirm, every 12 months, that remote access capacity supports at least the number of concurrent remote users required by all Tier 0 and Tier 1 BCPs. Remote access security requirements are in SEC-015 and SEC-008.
- **RES-004.5.6.5** The CHRO SHALL maintain workforce health, leave and site-access measures for the pandemic annex, consistent with applicable employment and privacy law and CMP-005.

### 5.7 Workforce unavailability

- **RES-004.5.7.1** Each Tier 0 and Tier 1 BCP SHALL identify critical roles (roles whose absence would prevent the process meeting its RTO) and SHALL name at least 2 trained alternates for each critical role.
- **RES-004.5.7.2** Alternates SHALL be trained on the critical role's continuity tasks before being named, and SHALL perform or rehearse those tasks at least once every 12 months, which MAY be in a BC exercise.
- **RES-004.5.7.3** The CHRO SHALL maintain succession arrangements for each CMT member and for each role named as a single point of knowledge in a BCP.
- **RES-004.5.7.4** Critical knowledge held by one individual SHALL be documented in a runbook or BCP annex accessible to that individual's alternates. BCP owners SHALL confirm this every 12 months.
- **RES-004.5.7.5** Travel by more than 50% of the members of the CMT, or of the named staff for any Tier 0 process, on the same flight or conveyance SHALL NOT occur without the approval of the CEO.
- **RES-004.5.7.6** Workforce welfare and accountability during a disruption (locating and confirming the safety of Workforce Members) SHALL be led by the CHRO. The CHRO SHALL be able to start a workforce accountability check within 1 hour of CMT activation for a life-safety event.
- **RES-004.5.7.7** Access changes required to let alternates act in critical roles SHALL follow SEC-003 and SEC-005. Emergency access SHALL use the break-glass arrangements in SEC-005.

### 5.8 Supplier and Third Party failure

- **RES-004.5.8.1** Each BCP SHALL list the Third Parties on which the process depends, with their vendor tier under RSK-003.
- **RES-004.5.8.2** For every Third Party that supports a Tier 0 or Tier 1 process, the BCP owner SHALL document a supplier failure strategy, being one or more of: an approved alternate supplier; an in-house fallback; a contractual continuity commitment from the Third Party (verified under RSK-003); or an exit plan with a defined transition time.
- **RES-004.5.8.3** Supplier failure strategies for Critical Vendors SHALL be reviewed with the Head of Procurement every 12 months and at contract renewal.
- **RES-004.5.8.4** Assessment of a Third Party's own business continuity and disaster recovery capability, and the related contract terms, SHALL be performed under RSK-003. This Policy does not restate those requirements.
- **RES-004.5.8.5** Where a Third Party's continuity capability cannot meet the RTO of a dependent process and no supplier failure strategy closes the gap, the BCP owner SHALL record the gap as a Risk under RSK-001.
- **RES-004.5.8.6** When a Critical Vendor reports or suffers a disruption that is projected to affect a Tier 0 or Tier 1 process, the BCP owner SHALL notify the Business Continuity Manager within 1 hour of becoming aware. Where the disruption is a Security Incident at the Third Party, the BCP owner SHALL also report it under RES-001.

### 5.9 Loss of premises and utilities

- **RES-004.5.9.1** Each BCP SHALL describe how the process continues on loss of its primary premises, using the strategy selected under section 5.3.
- **RES-004.5.9.2** Physical protection, environmental controls and supporting utilities for premises are governed by SEC-016.
- **RES-004.5.9.3** The Head of Facilities SHALL maintain, for each premises hosting a Tier 0 or Tier 1 process, a site emergency plan covering evacuation, shelter-in-place, utility failure and building access restoration, and SHALL make it available to the CMT.

### 5.10 Communications during disruption

- **RES-004.5.10.1** The Organization SHALL maintain an emergency notification capability able to reach all Workforce Members by at least two independent channels (for example SMS and voice, in addition to email). The Business Continuity Manager SHALL test it every 6 months.
- **RES-004.5.10.2** External statements about a disruption SHALL be authorized by the CMT Chair. Where a Security Incident or Personal Data Breach is involved, statements SHALL also follow RES-002 and RES-003.
- **RES-004.5.10.3** Customer and regulator notifications triggered by a disruption SHALL follow contractual commitments recorded under CMP-001 and, for Security Incidents, RES-003.

### 5.11 Exercises

- **RES-004.5.11.1** The Organization SHALL conduct a BC exercise every 12 months; and a DR test of Tier 0 and Tier 1 every 12 months.
- **RES-004.5.11.2** The BC exercise in RES-004.5.11.1 SHALL include the CMT and SHALL exercise at least one scenario from: loss of premises, loss of a Tier 0 system, pandemic or workforce unavailability, Critical Vendor failure, or a Sev-1 Security Incident with business disruption. The scenario SHALL differ from the previous year's.
- **RES-004.5.11.3** Every Tier 0 and Tier 1 BCP SHALL be exercised at least every 12 months; Tier 2 BCPs at least every 24 months. A BCP exercise MAY be a tabletop walk-through, a functional exercise or a live test, and MAY be combined with the BC exercise in RES-004.5.11.1.
- **RES-004.5.11.4** DR testing types, procedures and success criteria are defined in RES-005.
- **RES-004.5.11.5** An actual activation of the CMT or of a BCP MAY count as the exercise for the plans activated, where the After-Action Report under RES-004.5.11.7 is completed.
- **RES-004.5.11.6** Each exercise SHALL have written objectives and success criteria agreed by the Business Continuity Manager before the exercise.
- **RES-004.5.11.7** The Business Continuity Manager SHALL issue an After-Action Report within 30 days of each exercise or real activation, recording objectives met or missed, issues found, and corrective actions with owners and due dates.
- **RES-004.5.11.8** Corrective actions from exercises SHALL be tracked to closure. Corrective actions that are not closed by their due date SHALL be reported to the ISSC at the next quarterly report under RES-004.5.1.6.
- **RES-004.5.11.9** The exercise schedule for the next 12 months SHALL be approved by the ISSC at the start of each fiscal year.
- **RES-004.5.11.10** `[PCI]` Exercises SHALL include the business recovery and continuity procedures required by PCI DSS v4.0.1 Requirement 12.10.1, coordinated with the IR plan test under RES-002.
- **RES-004.5.11.11** `[HIPAA]` Testing and revision of contingency plans for ePHI systems SHALL be performed as part of the exercises in this section, satisfying 45 CFR §164.308(a)(7)(ii)(D).

### 5.12 Plan maintenance

- **RES-004.5.12.1** Each BCP, the CMT handbook and the pandemic annex SHALL be reviewed and re-approved at least every 12 months.
- **RES-004.5.12.2** Each BCP SHALL also be reviewed within 30 days of any of the following: an exercise or real activation of the plan; a BIA refresh under RSK-004 affecting the process; a material change to the process, its systems, its premises or its Critical Vendors; or an organizational change affecting named roles.
- **RES-004.5.12.3** Contact lists in BCPs SHALL be verified every 6 months.
- **RES-004.5.12.4** The Business Continuity Manager SHALL keep superseded versions of BCPs and all exercise and activation records under CMP-004.
- **RES-004.5.12.5** Changes to Information Systems that affect a BCP's dependencies SHALL be identified through SEC-013 change impact assessment, and the change requester SHALL notify the affected BCP owner before implementation.

### 5.13 Training and awareness

- **RES-004.5.13.1** CMT members, alternates and BCP owners SHALL complete BCM role training before taking on the role and every 12 months thereafter.
- **RES-004.5.13.2** All Workforce Members SHALL be informed of how they will be contacted in a disruption and what is expected of them, as part of the awareness program under PPL-002.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| Board of Directors / Audit Committee | Receive the annual program report under GOV-003, which includes BCM status. |
| ISSC | Approves this Policy, the BCM scope and the annual exercise schedule; reviews quarterly BCM status and overdue corrective actions. |
| CEO | Executive accountable for the BCM program; chairs the CMT; may activate the CMT. |
| CFO | Alternate CMT Chair; approves emergency spending above the CMT limit. |
| CIO | CMT member; owns technology recovery through RES-005; confirms remote access capacity (RES-004.5.6.4). |
| CTO | CMT member; supports recovery of product and engineering platforms. |
| CISO | CMT member; link between the CMT and the Incident Commander under RES-002 during Security Incidents. |
| CPO / GC | CMT members; advise on privacy, legal and regulatory obligations, including RES-003. |
| CHRO | CMT member; leads workforce welfare and accountability, succession and pandemic workforce measures. |
| Head of Facilities | CMT member; maintains site emergency plans; leads premises recovery. |
| Head of Procurement | Supports supplier failure strategies and alternate supplier arrangements. |
| Business Continuity Manager | Owns this Policy; operates the BCM program; coordinates and records the CMT; maintains the program register, CMT handbook and pandemic annex; runs exercises; issues After-Action Reports. |
| Business unit leaders | Nominate BCP owners; approve BCPs and the cost of continuity strategies. |
| BCP owners | Develop, maintain, exercise and activate BCPs; record continuity gaps as Risks. |
| Workforce Members | Know how they will be contacted; follow BCP instructions and CMT direction during a disruption. |

Role accountabilities are consolidated in REF-002.

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| RES-004.7.1 | BC exercise frequency | BC exercise every 12 months; DR test of Tier 0 and Tier 1 every 12 months |
| RES-004.7.2 | CMT convening time | Within 1 hour of activation |
| RES-004.7.3 | CMT meeting cadence while active | At least every 24 hours |
| RES-004.7.4 | BCP coverage | Every Tier 0, Tier 1 and Tier 2 process |
| RES-004.7.5 | CMT emergency spending authority | [DECISION REQUIRED: CMT emergency spending limit per activation. Recommended default: the CEO's delegated spending authority; above that, CFO approval] |
| RES-004.7.6 | BCP exercise frequency | Tier 0 and Tier 1: every 12 months · Tier 2: every 24 months |
| RES-004.7.7 | After-Action Report | Within 30 days of each exercise or activation |
| RES-004.7.8 | BCP, CMT handbook, pandemic annex review | Every 12 months, and within 30 days of a trigger in RES-004.5.12.2 |
| RES-004.7.9 | BCP update after BIA refresh | Within 30 days of BIA approval |
| RES-004.7.10 | Contact list verification | Every 6 months |
| RES-004.7.11 | Emergency notification test | Every 6 months, at least two independent channels |
| RES-004.7.12 | Trained alternates per critical role (Tier 0 and Tier 1) | At least 2 |
| RES-004.7.13 | Pandemic planning assumption | 40% absenteeism for 8 weeks |
| RES-004.7.14 | BCP owner notification of activation to Business Continuity Manager | Within 1 hour |
| RES-004.7.15 | BCM role training | Before taking the role and every 12 months |
| RES-004.7.16 | Recovery Tiers, RTO, RPO | As set in RSK-004 |
| RES-004.7.17 | Retention of BCPs, exercise and activation records | As set in CMP-004 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Tier 0–2 processes with a current, approved BCP | 100% | Quarterly | Business Continuity Manager |
| BCPs reviewed within 12 months | 100% | Quarterly | Business Continuity Manager |
| BCPs exercised within the frequency in RES-004.7.6 | 100% | Quarterly | Business Continuity Manager |
| BC exercise and Tier 0/Tier 1 DR test completed in the last 12 months | Yes | Quarterly | Business Continuity Manager |
| After-Action Reports issued within 30 days | 100% | Per exercise | Business Continuity Manager |
| Exercise corrective actions overdue | 0 | Quarterly | Business Continuity Manager |
| CMT convened within 1 hour of activation (exercises and real events) | 100% | Per activation | Business Continuity Manager |
| Critical roles (Tier 0/1) with at least 2 trained alternates | 100% | Every 6 months | BCP owners |
| Emergency notification test reach (Workforce Members confirming receipt) | ≥ 90% | Every 6 months | Business Continuity Manager |
| Critical Vendors supporting Tier 0/1 processes with a documented supplier failure strategy | 100% | Every 12 months | Head of Procurement |

Metrics are reported under GOV-003.

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following requirements SHALL NOT receive an Exception: the BC exercise and DR test frequency in RES-004.5.11.1; the existence of a BCP for each Tier 0 and Tier 1 process (RES-004.5.5.1); and `[PCI]` RES-004.5.3.5.

## 10. Enforcement

Non-compliance is handled under CMP-007.

A BCP owner whose plan is more than 90 days past its review date SHALL be reported by the Business Continuity Manager to the ISSC.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| RES-004.5.1 (program, scope) | 4.3, 5.1, 6.1; A.5.29, A.5.30 | GV.OC-04, GV.RR-02 | CP-1, CP-2, PM-8 | — | CC9.1, A1.2 | DSS04.01 | ISO 22301:2019 cl. 4–6 |
| RES-004.5.2 (BIA, risk) | 6.1.2, 8.2; A.5.30 | GV.OC-04, ID.RA-01 | CP-2, RA-3 | — | CC3.2, CC9.1 | APO12, DSS04.02 | `[HIPAA]` §164.308(a)(7)(ii)(E) |
| RES-004.5.3 (strategies) | A.5.29, A.5.30, A.7.11, A.8.14 | PR.IR-03 | CP-2, CP-6, CP-7, CP-8 | — | A1.2, CC9.1 | DSS04.02, DSS04.03 | `[HIPAA]` §164.308(a)(7)(ii)(C); `[PCI]` 12.10.1; `[SOX]` §404 |
| RES-004.5.4 (CMT) | 5.3; A.5.29 | GV.RR-02, RS.MA-01 | CP-2, IR-4 | 17.4 | CC7.4, CC7.5 | DSS04.03 | — |
| RES-004.5.5 (BCPs) | A.5.29, A.5.30 | ID.IM-04, RC.RP-01 | CP-2, CP-10 | — | A1.2, CC7.5 | DSS04.03 | `[HIPAA]` §164.308(a)(7)(i); `[PCI]` 12.10.1 |
| RES-004.5.6 – 5.7 (pandemic, workforce) | A.5.29 | GV.OC-04, GV.RR-02 | CP-2, CP-3 | — | CC9.1 | DSS04.03 | — |
| RES-004.5.8 (supplier failure) | A.5.19, A.5.21, A.5.22, A.5.30 | GV.SC-08, GV.OC-05 | SA-9, SR-2, CP-2 | 15.1 | CC9.2 | APO10, DSS04.03 | — |
| RES-004.5.9 – 5.10 (premises, communications) | A.7.5, A.7.11; A.5.29 | RC.CO-03, RC.CO-04 | CP-2, PE-1, CP-8 | 17.6 | CC2.3, A1.2 | DSS04.03 | — |
| RES-004.5.11 (exercises) | 9.1; A.5.30 | ID.IM-02, ID.IM-04 | CP-4, CP-3 | 17.7 | A1.3, CC7.5 | DSS04.04, DSS04.05 | `[HIPAA]` §164.308(a)(7)(ii)(D); `[PCI]` 12.10.2 |
| RES-004.5.12 – 5.13 (maintenance, training) | 7.2, 7.3, 10.2; A.5.29 | ID.IM-04, PR.AT-02 | CP-2, CP-3 | — | A1.3 | DSS04.06, DSS04.08 | `[HIPAA]` §164.308(a)(7)(ii)(D) |

## 12. Related documents

ISP-000, GOV-001, GOV-003, GOV-006, RSK-001, RSK-002, RSK-003, RSK-004, CMP-001, CMP-003, CMP-004, CMP-005, CMP-007, CMP-009, SEC-003, SEC-005, SEC-008, SEC-013, SEC-015, SEC-016, SEC-018, SEC-019, RES-001, RES-002, RES-003, RES-005, PPL-001, PPL-002, TPL-001, REF-001, REF-002

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Business Continuity Manager | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
