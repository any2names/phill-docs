# RES-005 — Disaster Recovery Plan

## 1. Document control

| Field | Value |
|---|---|
| Document ID | RES-005 |
| Title | Disaster Recovery Plan |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 3 — Plan |
| Classification | Internal |
| Owner | Chief Information Officer (CIO) |
| Approver | Business Continuity Manager |
| Effective date | [DECISION REQUIRED: Date of Business Continuity Manager approval] |
| Next review date | Effective date + 12 months, and within 30 days after each DR test or real DR activation |
| Parent document | RES-004 Business Continuity Policy |
| Related documents | RSK-004, SEC-001, SEC-006, SEC-009, SEC-012, SEC-013, SEC-018, RES-001, RES-002, RES-003, RES-004, CMP-004, CMP-009 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CIO | Initial release |

## 3. Purpose

This Plan describes how the Organization restores Information Systems and data after a
disruption, within the Recovery Tier targets set in RSK-004. It defines the DR
organization, the criteria and authority for declaring a disaster, the recovery procedure
for each Recovery Tier, the order in which systems are recovered, failover and failback,
communications during recovery, and how the Plan is tested. It implements the technology
recovery strategy required by RES-004.

## 4. Scope

- **People:** the CIO, the DR organization in section 5.1, System Owners, Data Custodians and Third Parties that operate or host in-scope systems.
- **Systems:** every Information System recorded in the Asset Inventory (SEC-001) with a Recovery Tier under RSK-004, in on-premises data centers, colocation facilities and Cloud Services, including the shared infrastructure they depend on (identity, network, DNS, key management, logging, backup).
- **Data:** all data held in in-scope systems and their Backups under SEC-018.
- **Locations:** primary and recovery data centers, cloud regions and availability zones, and the locations from which the DR organization works.
- **Third parties:** Cloud Service Providers, hosting and colocation providers, and recovery service providers. Their obligations are set by contract under RSK-003.
- **Out of scope:** continuity of business processes (RES-004); the technical handling of Security Incidents (RES-002), except where RES-002 hands recovery to this Plan.

## 5. Procedure

### 5.1 DR organization

- **RES-005.5.1.1** The CIO SHALL lead disaster recovery and SHALL appoint, in writing, a DR Coordinator and an alternate. [ASSUMPTION: The DR Coordinator is a senior infrastructure or IT operations leader reporting to the CIO.]
- **RES-005.5.1.2** The DR organization SHALL consist of the following teams. The CIO SHALL name a team lead and alternate for each team in the DR contact register:

  | Team | Lead (appointed by the CIO) | Responsibilities |
  |---|---|---|
  | DR command | DR Coordinator | Runs the recovery, tracks status against RTOs, records the DR log, reports to the CIO |
  | Infrastructure recovery | Infrastructure lead | Data center, compute, storage, virtualization, cloud Landing Zones |
  | Network and connectivity | Network lead | WAN, LAN, DNS, load balancing, remote access, recovery-site connectivity |
  | Identity and security services | Head of Security Engineering (delegate) | Directory, SSO, MFA, privileged access, key management, security tooling |
  | Data recovery | Database and storage lead | Backup restoration, database recovery, data integrity validation |
  | Application recovery | System Owner of each application | Application restore, configuration, functional validation |
  | Security oversight | SOC Manager (delegate) | Monitoring of recovered systems, confirmation that recovery sources are clean |
  | Business liaison | BCP owners (RES-004) | Business acceptance testing; link to BCPs and Manual Workarounds |

- **RES-005.5.1.3** The DR contact register SHALL list, for every team lead and alternate, at least two contact methods, one of which does not depend on the Organization's primary Information Systems. The DR Coordinator SHALL verify it every 6 months.
- **RES-005.5.1.4** This Plan, the DR contact register, system runbooks, the recovery dependency map and the credentials or break-glass procedure needed to start recovery SHALL be available offline or from an independently hosted location accessible when primary systems, identity services and the corporate network are unavailable. Break-glass Accounts are governed by SEC-005.
- **RES-005.5.1.5** Each System Owner of a Tier 0, Tier 1 or Tier 2 system SHALL maintain a recovery runbook that a trained member of the DR organization other than the author can follow. Each runbook SHALL contain: Recovery Tier; upstream and downstream dependencies; recovery location; restore or failover steps; configuration and Secrets references; validation tests; failback steps; and the System Owner's contacts.
- **RES-005.5.1.6** Runbooks SHALL be reviewed at least every 12 months and after any change under SEC-013 that alters the system's architecture, hosting location or recovery method.

### 5.2 Activation and Disaster Declaration

- **RES-005.5.2.1** Any of the following SHALL notify the DR Coordinator immediately on becoming aware of an actual or projected outage of a Tier 0 or Tier 1 system: the SOC (through SEC-012 monitoring), the IT Service Desk, a System Owner, a Cloud Service Provider notice, or the Incident Commander under RES-002.
- **RES-005.5.2.2** The DR Coordinator SHALL start an impact assessment within 30 minutes of notification for a Tier 0 system and within 1 hour for a Tier 1 system. The assessment SHALL establish: affected systems and their Recovery Tiers; cause, if known; whether a Security Incident is suspected; the projected time to restore in the primary environment; and the state of the latest Backups or replicas.
- **RES-005.5.2.3** Where a Security Incident is suspected, the DR Coordinator SHALL report it under RES-001 and SHALL coordinate with the Incident Commander under RES-002 before taking any recovery action that could destroy evidence or reintroduce a Threat.
- **RES-005.5.2.4** The DR Coordinator SHALL recommend a Disaster Declaration to the declaration authority when restoration in the primary environment is not expected within 50% of the applicable RTO in RSK-004.
- **RES-005.5.2.5** Declaration authority: the CIO SHALL decide whether to declare a disaster. If the CIO cannot be reached within 30 minutes, the CTO SHALL decide; if the CTO cannot be reached within a further 30 minutes, the CISO SHALL decide.
- **RES-005.5.2.6** The declaration SHALL be recorded in the DR log with: time; declaring role; affected systems; Recovery Tiers; recovery location; and the expected recovery sequence.
- **RES-005.5.2.7** On declaration, the declaring role SHALL notify the CEO (or alternate CMT Chair) so that the Crisis Management Team is activated under RES-004, and SHALL notify the Business Continuity Manager.
- **RES-005.5.2.8** On declaration, the DR Coordinator SHALL: open a DR bridge; mobilize the teams in RES-005.5.1.2 needed for the affected systems; open an Emergency Change under SEC-013 covering the recovery actions; and start the DR log.
- **RES-005.5.2.9** Where the disruption is a Sev-1 Security Incident under RES-002, the Incident Commander SHALL confirm that containment is sufficient before the DR Coordinator restores affected systems to a network connected to production.
- **RES-005.5.2.10** The declaration authority MAY declare a disaster before the threshold in RES-005.5.2.4 is reached where waiting would make the RTO unachievable.

### 5.3 Recovery procedures by Recovery Tier

Recovery Tiers, RTOs and RPOs are set in RSK-004. Backup frequency and restore testing are
set in SEC-018. The following steps apply to each system being recovered; the tier-specific
requirements in RES-005.5.3.8 to RES-005.5.3.11 add to them.

- **RES-005.5.3.1** **Step 1 — Confirm recovery point.** The data recovery team SHALL identify the most recent Backup or replica that is complete, consistent and, where a Security Incident is involved, confirmed clean by the security oversight team. The DR Coordinator SHALL record the recovery point and the resulting data loss, and compare it with the RPO in RSK-004.
- **RES-005.5.3.2** **Step 2 — Prepare target environment.** The infrastructure and network teams SHALL prepare the recovery environment using the approved Configuration Baselines (SEC-013) and, for cloud workloads, the approved infrastructure-as-code templates (SEC-009).
- **RES-005.5.3.3** **Step 3 — Restore or fail over.** The application recovery team SHALL restore or fail over the system following its runbook.
- **RES-005.5.3.4** **Step 4 — Apply security controls.** Before the recovered system accepts production traffic, the identity and security services team SHALL confirm that: Encryption is in place under SEC-006; access is limited to authorized Users under SEC-003; logging to the SIEM is active under SEC-012; Endpoint protection is running where applicable; and patches required by SEC-011 are applied or tracked.
- **RES-005.5.3.5** **Step 5 — Validate.** The System Owner SHALL run the runbook's validation tests (technical health, data integrity checks, interface checks), and the business liaison SHALL perform business acceptance testing.
- **RES-005.5.3.6** **Step 6 — Release.** The DR Coordinator SHALL release the system to users only after Steps 4 and 5 pass, and SHALL record the release time and the achieved recovery time in the DR log.
- **RES-005.5.3.7** **Step 7 — Reconcile.** BCP owners SHALL reconcile transactions processed under Manual Workarounds (RES-004) and re-enter or recover data lost between the recovery point and the disruption.
- **RES-005.5.3.8** **Tier 0 — Mission-critical.** Tier 0 systems SHALL have pre-provisioned recovery capacity (active-active, hot standby or pre-built cloud environment) and continuous or near-continuous replication meeting SEC-018. Recovery SHALL be by automated or scripted failover. The DR Coordinator SHALL report recovery status to the CIO every hour until the system is released.
- **RES-005.5.3.9** **Tier 1 — Critical.** Tier 1 systems SHALL have warm-standby capacity or a tested, scripted rebuild able to complete within the RTO in RSK-004. Status SHALL be reported to the CIO every 4 hours until the system is released.
- **RES-005.5.3.10** **Tier 2 — Important.** Tier 2 systems MAY be recovered by rebuild and restore from Backup. Recovery SHALL start once all Tier 0 and Tier 1 systems sharing the same recovery resources are released, unless the CIO approves a different order. Status SHALL be reported daily.
- **RES-005.5.3.11** **Tier 3 — Deferrable.** Tier 3 systems SHALL be recovered by rebuild and restore from Backup after all higher tiers are released, in an order agreed by the CIO with the business unit leaders. Status SHALL be reported daily.
- **RES-005.5.3.12** `[SOX]` Recovery of a Financially Significant System SHALL preserve the integrity of financial data. The System Owner SHALL document the data integrity validation performed and any data lost, and SHALL provide it to the Head of GRC for assessment against CMP-009.
- **RES-005.5.3.13** `[PCI]` Systems in the CDE SHALL be recovered only into environments within the CDE scope and segmentation defined in SEC-019.
- **RES-005.5.3.14** `[HIPAA]` Recovery of ePHI systems SHALL restore exact copies of ePHI, as required by 45 CFR §164.308(a)(7)(ii)(B), and the System Owner SHALL record the integrity verification performed.
- **RES-005.5.3.15** Where a recovery will miss its RTO, the DR Coordinator SHALL inform the CIO and the CMT as soon as the miss is projected, with a revised estimate.

### 5.4 Recovery sequencing and dependencies

- **RES-005.5.4.1** The CIO SHALL maintain a recovery dependency map showing, for each Tier 0 and Tier 1 system, the Information Systems, shared services, Cloud Services and Third Parties it depends on. The map SHALL be derived from the Asset Inventory (SEC-001) and the BIA (RSK-004) and reviewed every 12 months and after each DR test.
- **RES-005.5.4.2** Recovery SHALL follow this sequence unless the DR Coordinator records a justified deviation in the DR log:

  | Phase | Systems | Rationale |
  |---|---|---|
  | 0 — Foundation | Recovery-site power, network, DNS and connectivity; identity services (directory, SSO, MFA, privileged access); key management and Secrets vaults; backup and replication platforms; logging and security monitoring | Every other system depends on them; recovery cannot be controlled or monitored without them |
  | 1 — Tier 0 | Tier 0 systems, in dependency order from the map | Highest business impact |
  | 2 — Tier 1 | Tier 1 systems, in dependency order | Critical processes |
  | 3 — Tier 2 | Tier 2 systems | Important processes |
  | 4 — Tier 3 | Tier 3 systems | Deferrable processes |

- **RES-005.5.4.3** Foundation services in Phase 0 SHALL be assigned a Recovery Tier under RSK-004 no lower than the highest Recovery Tier of the systems that depend on them.
- **RES-005.5.4.4** Where a dependency has a lower Recovery Tier than a system that depends on it, the System Owner SHALL report the mismatch to the Business Continuity Manager for correction in the next BIA refresh under RSK-004, and the CIO SHALL recover the dependency in the dependent system's phase.
- **RES-005.5.4.5** Where several systems in the same phase compete for recovery resources, the CMT SHALL set the priority under RES-004.

### 5.5 Failover

- **RES-005.5.5.1** Each Tier 0 and Tier 1 system SHALL have a documented failover method in its runbook: automatic (no human action), scripted (human-initiated, automated execution) or manual.
- **RES-005.5.5.2** Automatic failover within a site, cloud region or availability zone set MAY occur without a Disaster Declaration. The SOC SHALL alert the DR Coordinator, and the event SHALL be recorded as a change under SEC-013.
- **RES-005.5.5.3** Failover between sites or cloud regions that is not automatic SHALL require either a Disaster Declaration under section 5.2 or approval of the CIO under an Emergency Change.
- **RES-005.5.5.4** Before initiating a manual or scripted failover, the data recovery team SHALL confirm the replication state and record the expected data loss.
- **RES-005.5.5.5** After failover, the application recovery team SHALL complete Steps 4 to 6 of section 5.3 before production traffic is accepted.
- **RES-005.5.5.6** Cloud workloads SHALL be designed so that the failover target uses a separate availability zone or region approved under SEC-009.5.10.1, and the failover target SHALL be included in the Asset Inventory.

### 5.6 Failback

- **RES-005.5.6.1** Failback to the primary environment SHALL NOT begin until: the cause of the disruption is resolved; the primary environment is restored and, where a Security Incident was involved, confirmed clean by the SOC Manager; and the CIO has approved a written failback plan.
- **RES-005.5.6.2** The failback plan SHALL be submitted to the CIO within 10 business days of the last affected system being released in the recovery environment, and SHALL include: the failback sequence (normally the reverse of section 5.4 for application systems); data synchronization method; expected outage window; validation tests; and rollback criteria.
- **RES-005.5.6.3** Failback SHALL be performed as a Normal Change under SEC-013 approved by the CAB, scheduled in a window agreed with the affected BCP owners.
- **RES-005.5.6.4** Data written in the recovery environment SHALL be synchronized to the primary environment and its integrity verified before the recovery environment is decommissioned.
- **RES-005.5.6.5** Where failback will not be performed within 90 days of declaration, the CIO SHALL either designate the recovery environment as the new primary (with Asset Inventory, Configuration Baseline and SEC-018 Backup coverage updated) or record the resulting Risk under RSK-001.
- **RES-005.5.6.6** Media and storage released after failback SHALL be sanitized under SEC-017.

### 5.7 Recovery from destructive attack

- **RES-005.5.7.1** Where systems are affected by ransomware or another destructive attack, recovery SHALL be coordinated with the Incident Commander under RES-002 and SHALL NOT start for an affected system until the Incident Commander confirms containment for that system.
- **RES-005.5.7.2** Recovery SHALL use Backups from the immutable or logically isolated copies required by SEC-018. The security oversight team SHALL scan restored data and images for indicators of compromise supplied by RES-002 before release.
- **RES-005.5.7.3** Restoration SHALL first be performed into an isolated recovery environment with no connectivity to production, where the system is validated before being connected to production.
- **RES-005.5.7.4** All credentials, keys and Secrets for affected systems SHALL be rotated before release, under SEC-004, SEC-005 and SEC-006.
- **RES-005.5.7.5** Systems SHALL be rebuilt from Configuration Baselines rather than restored from system images where the integrity of the image cannot be confirmed.

### 5.8 Communications during recovery

- **RES-005.5.8.1** The DR Coordinator SHALL issue status updates to the CIO at the intervals set in section 5.3 for the highest Recovery Tier still being recovered, and the CIO SHALL brief the CMT at each CMT meeting under RES-004.
- **RES-005.5.8.2** Each status update SHALL state: systems released; systems in progress with estimated release time; RTO and RPO status against RSK-004; issues and decisions required.
- **RES-005.5.8.3** The IT Service Desk SHALL publish user-facing service status at least every 4 hours while a disaster is declared, using wording approved by the DR Coordinator.
- **RES-005.5.8.4** Communications to customers, regulators, media or other external parties SHALL be made only as authorized by the CMT under RES-004 and, where a Security Incident is involved, under RES-002 and RES-003.
- **RES-005.5.8.5** The DR Coordinator SHALL notify affected Third Parties (for example Cloud Service Providers and recovery service providers) of the declaration and the support required, using the contacts in the DR contact register.

### 5.9 Stand-down and post-recovery review

- **RES-005.5.9.1** The CIO SHALL stand down DR operations when all affected systems are released and stable for 24 hours, and SHALL record the stand-down in the DR log.
- **RES-005.5.9.2** The DR Coordinator SHALL complete a post-recovery review within 30 days of stand-down, recording: timeline; achieved recovery time and data loss for each system against RSK-004; deviations from this Plan; Root Causes of any missed RTO or RPO; and corrective actions with owners and due dates. Where the disaster was caused by a Security Incident, the review SHALL be combined with the Post-Incident Review under RES-002 using TPL-007.
- **RES-005.5.9.3** The post-recovery review SHALL be submitted to the Business Continuity Manager and counts as an After-Action Report under RES-004.

### 5.10 Testing

- **RES-005.5.10.1** DR testing SHALL be performed at the frequency set in RES-004. Restore testing of Backups is performed separately at the frequency set in SEC-018 and does not replace DR testing.
- **RES-005.5.10.2** The DR Coordinator SHALL use the following test types:

  | Test type | Description | Evidence of success |
  |---|---|---|
  | Tabletop | Facilitated walk-through of a disaster scenario with the DR organization, CMT liaison and System Owners, covering declaration, sequencing, roles and communications | Participants list, scenario, decisions, gaps found |
  | Partial | Recovery of one or more systems or components (for example a database restore, an application rebuild or a single-service failover) in the recovery environment, without affecting production | Measured recovery time and data loss against RSK-004, validation test results |
  | Full failover | Failover of a Tier 0 or Tier 1 system, or a defined group of systems, to the recovery site or region, operation from it, and failback | Measured recovery time and data loss, business acceptance results, failback results |

- **RES-005.5.10.3** The DR test of each Tier 0 system required by RES-004 SHALL be a full failover test, or a partial test that demonstrates recovery of every component of the system within its RTO and RPO. A tabletop SHALL NOT alone satisfy the test requirement for a Tier 0 or Tier 1 system.
- **RES-005.5.10.4** The DR test of each Tier 1 system required by RES-004 SHALL be at least a partial test. [DECISION REQUIRED: Whether Tier 1 systems also require a full failover test on a multi-year cycle. Recommended default: full failover of each Tier 1 system at least every 36 months.]
- **RES-005.5.10.5** Tier 2 and Tier 3 systems SHALL be included in at least one tabletop test every 24 months.
- **RES-005.5.10.6** At least one tabletop test every 12 months SHALL use a destructive-attack scenario exercising section 5.7, and MAY be combined with the IR plan exercise under RES-002.
- **RES-005.5.10.7** Each test SHALL have a written test plan approved by the CIO before the test, stating scope, objectives, success criteria, rollback plan and the change record under SEC-013. Tests that affect production SHALL be approved by the CAB.
- **RES-005.5.10.8** The DR Coordinator SHALL issue a test report within 30 days after each test, recording: systems tested; achieved recovery time and data loss against RSK-004; success criteria met or missed; issues; and corrective actions with owners and due dates.
- **RES-005.5.10.9** Results of each test SHALL be reviewed, and this Plan and affected runbooks updated, within 30 days after each test.
- **RES-005.5.10.10** A system that misses its RTO or RPO in a test SHALL be retested, after corrective action, within 90 days of the test report. Where the retest also fails, the CIO SHALL record a Risk under RSK-001.
- **RES-005.5.10.11** `[PCI]` DR tests SHALL be coordinated with the IR plan test so that the business recovery and continuity procedures in PCI DSS v4.0.1 Requirement 12.10.1 are tested at least once every 12 months (Requirement 12.10.2).
- **RES-005.5.10.12** `[HIPAA]` DR tests of ePHI systems SHALL be recorded as testing of the contingency plan under 45 CFR §164.308(a)(7)(ii)(D) and reported to the HIPAA Security Officer.

### 5.11 Plan maintenance and records

- **RES-005.5.11.1** The CIO SHALL review this Plan every 12 months and within 30 days after each DR test or real DR activation, and submit material changes to the Business Continuity Manager for approval.
- **RES-005.5.11.2** System Owners SHALL notify the DR Coordinator of any change that alters a system's Recovery Tier, hosting location, dependencies or recovery method, through SEC-013 change impact assessment, before the change is implemented.
- **RES-005.5.11.3** DR logs, declarations, test plans, test reports and post-recovery reviews SHALL be retained under CMP-004.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CIO | Owns this Plan; appoints the DR Coordinator and team leads; primary Disaster Declaration authority; approves test plans and failback plans; reports to the CMT. |
| CTO | First alternate declaration authority; supports recovery of product and engineering platforms. |
| CISO | Second alternate declaration authority; ensures security requirements are met during recovery. |
| Business Continuity Manager | Approves this Plan; receives test reports and post-recovery reviews; tracks DR test completion against RES-004. |
| DR Coordinator | Runs impact assessments and recovery; recommends declaration; maintains the DR log, contact register and test program; issues test reports and post-recovery reviews. |
| Head of Security Engineering | Leads (or delegates) identity and security services recovery; supports credential rotation. |
| SOC Manager | Leads (or delegates) security oversight; confirms recovery sources and environments are clean; monitors recovered systems. |
| System Owners | Maintain runbooks; lead application recovery; validate recovered systems; report Recovery Tier mismatches. |
| Data Custodians | Perform Backup restoration and data integrity validation. |
| BCP owners | Perform business acceptance testing and reconciliation after recovery. |
| Head of GRC | `[SOX]` Assesses data integrity evidence for Financially Significant Systems against CMP-009. |
| HIPAA Security Officer | `[HIPAA]` Receives DR test results for ePHI systems. |
| Third Parties | Provide recovery capability and support as set by contract under RSK-003. |

Role accountabilities are consolidated in REF-002.

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| RES-005.7.1 | RTO and RPO by Recovery Tier | As set in RSK-004 |
| RES-005.7.2 | Backup frequency and restore testing | As set in SEC-018 |
| RES-005.7.3 | DR test frequency | As set in RES-004 |
| RES-005.7.4 | Disaster Declaration threshold | Restoration in the primary environment not expected within 50% of the applicable RTO in RSK-004 |
| RES-005.7.5 | Declaration authority | CIO; then CTO if CIO unreachable for 30 minutes; then CISO if CTO unreachable for a further 30 minutes |
| RES-005.7.6 | Impact assessment start after notification | Tier 0: 30 minutes · Tier 1: 1 hour |
| RES-005.7.7 | Recovery status reporting to CIO | Tier 0: hourly · Tier 1: every 4 hours · Tier 2 and Tier 3: daily |
| RES-005.7.8 | User-facing service status while disaster declared | At least every 4 hours |
| RES-005.7.9 | Failback plan submitted to CIO | Within 10 business days of last affected system released |
| RES-005.7.10 | Failback or re-designation of primary | Within 90 days of declaration, or Risk recorded under RSK-001 |
| RES-005.7.11 | Stand-down condition | All affected systems released and stable for 24 hours |
| RES-005.7.12 | Post-recovery review | Within 30 days of stand-down |
| RES-005.7.13 | Test report and Plan update after each test | Within 30 days after each test |
| RES-005.7.14 | Retest after failed RTO/RPO in test | Within 90 days of the test report |
| RES-005.7.15 | Minimum test type, Tier 0 | Full failover, or partial covering every component |
| RES-005.7.16 | Minimum test type, Tier 1 | Partial |
| RES-005.7.17 | Tabletop coverage of Tier 2 and Tier 3 systems | At least every 24 months |
| RES-005.7.18 | Destructive-attack tabletop | At least every 12 months |
| RES-005.7.19 | Runbook review | Every 12 months and after any architecture or hosting change |
| RES-005.7.20 | DR contact register verification | Every 6 months |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Tier 0 and Tier 1 systems with a DR test in the period required by RES-004 | 100% | Quarterly | DR Coordinator |
| Tier 0–2 systems with a current runbook (reviewed within 12 months) | 100% | Quarterly | DR Coordinator |
| Tests meeting RTO (achieved recovery time ≤ RTO in RSK-004) | 100% | Per test | DR Coordinator |
| Tests meeting RPO (achieved data loss ≤ RPO in RSK-004) | 100% | Per test | DR Coordinator |
| Test reports issued and Plan updated within 30 days | 100% | Per test | DR Coordinator |
| Failed RTO/RPO tests retested within 90 days | 100% | Quarterly | CIO |
| Recovery Tier mismatches between dependencies and dependent systems | 0 open beyond next BIA refresh | Every 12 months | CIO |
| Real disasters with RTO met for all affected Tier 0/Tier 1 systems | 100% | Per activation | CIO |

Metrics are reported under GOV-003.

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The DR test of Tier 0 and Tier 1 systems at the frequency set in RES-004 SHALL NOT receive an Exception. A system that cannot be tested at the required test type SHALL be recorded as a Risk under RSK-001 instead.

## 10. Enforcement

Non-compliance is handled under CMP-007.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| RES-005.5.1 (DR organization, runbooks) | A.5.29, A.5.30, A.5.37 | GV.RR-02, RC.RP-01 | CP-2, CP-3 | 11.1 | A1.2, CC7.5 | DSS04.03 | `[HIPAA]` §164.308(a)(7)(ii)(B) |
| RES-005.5.2 (activation, declaration) | A.5.26, A.5.29 | RC.RP-01, RS.MA-01 | CP-2, CP-10, IR-4 | 17.4 | CC7.4, CC7.5 | DSS04.03 | — |
| RES-005.5.3 (recovery by tier) | A.5.30, A.8.13, A.8.14 | RC.RP-02, RC.RP-03, RC.RP-05, PR.DS-11 | CP-9, CP-10 | 11.1, 11.2, 11.3 | A1.2, CC7.5 | DSS04.03, BAI04 | `[HIPAA]` §164.308(a)(7)(ii)(A)–(B); `[PCI]` 12.10.1; `[SOX]` §404; `[GDPR]` Art. 32(1)(c) |
| RES-005.5.4 (sequencing, dependencies) | A.5.30, A.5.9 | GV.OC-04, ID.AM-01, RC.RP-01 | CP-2, CM-8 | 1.1 | A1.2 | DSS04.02 | `[HIPAA]` §164.308(a)(7)(ii)(E) |
| RES-005.5.5 – 5.6 (failover, failback) | A.8.14, A.8.32 | PR.IR-03, RC.RP-04 | CP-7, CP-10, CM-3 | 11.4 | A1.2, CC8.1 | DSS04.03, BAI06 | `[PCI]` 12.10.1 |
| RES-005.5.7 (destructive attack) | A.5.26, A.8.7, A.8.13 | RS.MI-01, RC.RP-03, RC.RP-04 | CP-9, CP-10, IR-4, SI-3 | 11.3, 11.4 | CC7.4, CC7.5 | DSS05, DSS04.03 | — |
| RES-005.5.8 – 5.9 (communications, review) | A.5.27, A.5.29 | RC.CO-03, RC.CO-04, RC.RP-06, ID.IM-03 | CP-2, IR-4 | 17.6, 17.8 | CC2.3, CC7.5 | DSS04.07, DSS04.08 | — |
| RES-005.5.10 – 5.11 (testing, maintenance) | 9.1, 10.2; A.5.30 | ID.IM-02, ID.IM-04 | CP-4, CP-2 | 11.5 | A1.3 | DSS04.04, DSS04.05, DSS04.06 | `[HIPAA]` §164.308(a)(7)(ii)(D); `[PCI]` 12.10.2 |

## 12. Related documents

ISP-000, GOV-003, GOV-006, RSK-001, RSK-003, RSK-004, CMP-003, CMP-004, CMP-007, CMP-009, SEC-001, SEC-003, SEC-004, SEC-005, SEC-006, SEC-009, SEC-011, SEC-012, SEC-013, SEC-017, SEC-018, SEC-019, RES-001, RES-002, RES-003, RES-004, TPL-007, REF-001, REF-002

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CIO | | | |
| Approver: Business Continuity Manager | | | |
