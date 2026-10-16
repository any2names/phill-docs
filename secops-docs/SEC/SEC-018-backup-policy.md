# SEC-018 — Backup Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | SEC-018 |
| Title | Backup Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Information Officer (CIO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months, and on the event-triggered reviews in GOV-002.7.4 |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | SEC-001, SEC-002, SEC-005, SEC-006, SEC-009, SEC-012, SEC-013, SEC-016, SEC-017, RSK-003, RSK-004, RES-002, RES-004, RES-005, CMP-004, CMP-008, CMP-009 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CIO | Initial release |

## 3. Purpose

This policy sets the Organization's requirements for creating, protecting, monitoring and
testing Backups so that data, configurations and systems can be restored within the
Recovery Point Objective and Recovery Time Objective of their Recovery Tier, including
after a ransomware attack or the compromise of administrative credentials.

## 4. Scope

- **People:** all Workforce Members and Third Parties who administer Backup systems, perform restores, or own Information Systems whose data is backed up.
- **Systems:** all Information Systems in the Asset Inventory (SEC-001) that hold data or configuration of value to the Organization, including on-premises servers, virtual machines, databases, file shares, Cloud Services (IaaS, PaaS and SaaS), source code repositories, Infrastructure as Code, identity directories, network and security device configurations, and key management systems.
- **Data:** all production data and configuration, at every Classification Level, and the Backups themselves.
- **Locations:** all Organization facilities, data centers, cloud regions and Third-Party Backup storage locations.
- **Third parties:** Third Parties that host Organization data or provide Backup services SHALL meet this policy as a contractual condition under RSK-003.

Recovery Tier assignment, RTO and RPO are set in RSK-004. Recovery procedures are in
RES-005. Retention periods for Backups are set in CMP-004 and are not restated here.
Endpoints are backed up only where SEC-008 requires it; Organization data on Endpoints
SHALL be stored in approved repositories that are backed up under this policy.

## 5. Policy statements

### 5.1 Backup scope and governance

- **SEC-018.5.1.1** Each System Owner SHALL ensure their Information System has a documented Backup specification recording: its Recovery Tier from RSK-004; the data, configuration and system images to be backed up; the Backup method; frequency; copy locations; Encryption; and the restore procedure reference in RES-005.
- **SEC-018.5.1.2** The CIO SHALL maintain a Backup Register reconciling the Asset Inventory (SEC-001) with Backup specifications. Any Information System holding data without a Backup specification SHALL be reported to its System Owner and remediated within 30 days.
- **SEC-018.5.1.3** A new Information System SHALL NOT enter production until its Backup specification is approved by the CIO or delegate and its first successful Backup has completed. This SHALL be a release criterion in the change record under SEC-013.
- **SEC-018.5.1.4** Backups SHALL include, in addition to data: system and application configuration; Infrastructure as Code and deployment pipelines; identity directory and SSO configuration; network and security device configurations; and the information needed to restore Encryption keys under SEC-006.
- **SEC-018.5.1.5** Where a Recovery Tier changes under RSK-004, the System Owner SHALL update the Backup specification within 30 days.

### 5.2 Backup frequency

- **SEC-018.5.2.1** Backups SHALL be taken at the following minimum frequencies, which match the RPO set for each Recovery Tier in RSK-004:

| Recovery Tier | Minimum Backup frequency |
|---|---|
| Tier 0 Mission-critical | Continuous replication or ≤ 15 min |
| Tier 1 Critical | Every 4 h |
| Tier 2 Important | Daily |
| Tier 3 Deferrable | Weekly |

- **SEC-018.5.2.2** Replication alone SHALL NOT satisfy this policy for Tier 0 systems. Tier 0 systems SHALL also have point-in-time Backups at least daily that meet section 5.3, so that logical corruption or ransomware encryption replicated to secondary copies can be reversed.
- **SEC-018.5.2.3** Systems without an assigned Recovery Tier SHALL be backed up as Tier 2 until a tier is assigned under RSK-004.
- **SEC-018.5.2.4** A full Backup SHALL be taken at least weekly for Tier 0 – Tier 2 systems where the Backup method uses incremental or differential Backups, or the Backup platform SHALL provide synthetic full Backups at the same frequency.

### 5.3 The 3-2-1-1-0 rule

- **SEC-018.5.3.1** Backups of Tier 0, Tier 1 and Tier 2 systems, and of any system holding Restricted data, SHALL meet the 3-2-1-1-0 rule:

| Element | Requirement |
|---|---|
| **3** copies | At least three copies of the data: the production copy and two Backup copies |
| **2** media or storage types | Backup copies on at least two different storage types or platforms (e.g. disk and object storage, or two independent cloud storage services), so that a single platform failure or vulnerability cannot affect both |
| **1** off-site | At least one copy in a different geographic location from production: a separate facility at least 100 km away, or a separate cloud region |
| **1** immutable or offline | At least one copy that is immutable (write-once, with a retention lock that cannot be shortened or removed by any administrator, including the Backup administrator) or offline (air-gapped, with no network path from production) |
| **0** errors | Zero unresolved errors: every Backup job verified as complete, and every restore test passed, with each failure remediated under section 5.7 |

- **SEC-018.5.3.2** Tier 3 systems holding no Restricted data SHALL meet at least the "3", "1 off-site" and "0" elements.
- **SEC-018.5.3.3** The retention lock on the immutable copy SHALL equal the retention period set for that Backup in CMP-004. The lock mode SHALL be compliance mode (or equivalent) so that it cannot be shortened by the Organization's administrators or the provider's support staff at the Organization's request.
- **SEC-018.5.3.4** The immutable or offline copy SHALL be held in a separate security domain from production: a separate cloud account or tenant, or a separate identity directory, so that compromise of production administrative credentials does not grant the ability to delete or alter it.
- **SEC-018.5.3.5** Physical Backup Media held on site SHALL be stored in accordance with SEC-016. Backup Media in transit SHALL be tracked and protected in accordance with SEC-016 and SEC-015.

### 5.4 Backup Encryption

- **SEC-018.5.4.1** All Backups SHALL be encrypted at rest and in transit using algorithms and key lengths approved in SEC-006.
- **SEC-018.5.4.2** Backup Encryption keys SHALL be managed under SEC-006 and SHALL be stored separately from the Backups they protect. Keys needed to restore the immutable or offline copy SHALL remain available if the production key management system is unavailable or compromised.
- **SEC-018.5.4.3** Loss of a Backup Encryption key SHALL be treated as loss of the Backup; the CIO SHALL test key recovery as part of the restore tests in section 5.6.
- **SEC-018.5.4.4** `[PCI]` Backups containing CHD SHALL render PAN unreadable in accordance with SEC-006 and SEC-019.

### 5.5 Access to Backups

- **SEC-018.5.5.1** Administrative access to Backup systems SHALL be granted, used and reviewed as Privileged Account access under SEC-005.
- **SEC-018.5.5.2** Backup administration SHALL be performed with accounts that are separate from production administrative accounts and from the Organization's primary directory administrative accounts. No single account SHALL have administrative rights over both a production system and the immutable copy of its Backups.
- **SEC-018.5.5.3** Deletion of Backups before the end of their retention period, reduction of a retention period, disabling of a Backup job, or modification of immutability settings SHALL require approval by two authorized individuals (dual authorization) and SHALL generate an alert to the SOC under SEC-012.
- **SEC-018.5.5.4** Restores SHALL be performed only on an approved request: for production restores, by the System Owner; for restores of Confidential or Restricted data to any other location, by the Data Owner. Restores to non-production environments SHALL meet SEC-010 requirements on the use of production data.
- **SEC-018.5.5.5** Every restore SHALL be logged with requester, approver, data restored, destination and timestamp.
- **SEC-018.5.5.6** `[HIPAA]` Restores of ePHI SHALL be recorded so that the HIPAA Security Officer can confirm that the data backup and disaster recovery specifications documented in CMP-008 are met.

### 5.6 Restore testing

- **SEC-018.5.6.1** Restores SHALL be tested at the following minimum frequencies:

| Recovery Tier | Minimum restore testing |
|---|---|
| Tier 0 and Tier 1 | Quarterly |
| Tier 2 and Tier 3 | Every 12 months |

- **SEC-018.5.6.2** Each restore test SHALL restore data from a Backup to an isolated environment and SHALL verify that: the data is complete and readable; application-level integrity checks pass (e.g. database consistency checks, record counts, checksum comparison); the restored data is within the RPO for the system's Recovery Tier; and the restore completed within the RTO for that tier.
- **SEC-018.5.6.3** At least once every 12 months, each Tier 0 and Tier 1 system's restore test SHALL be performed from the immutable or offline copy, without use of production credentials or the production key management system.
- **SEC-018.5.6.4** Restore tests SHALL rotate through the systems of each tier so that every system in Tier 0 and Tier 1 is tested at least every 12 months, and every system in Tier 2 and Tier 3 at least every 24 months, in addition to the minimum frequencies in SEC-018.5.6.1.
- **SEC-018.5.6.5** Restore test results (system, date, Backup used, success or failure, RPO and RTO achieved, tester) SHALL be recorded and retained as Evidence under CMP-004, and SHALL be provided to the Business Continuity Manager for use in RES-004 and RES-005.
- **SEC-018.5.6.6** Backups SHALL be scanned for Malware and indicators of compromise before restore into production after a Security Incident, in accordance with RES-002.

### 5.7 Monitoring of Backup jobs

- **SEC-018.5.7.1** Every Backup job SHALL report success or failure automatically to a monitored console. Failures SHALL generate alerts to the Backup operations team.
- **SEC-018.5.7.2** The Backup operations team SHALL review all Backup job results each business day, and for Tier 0 and Tier 1 systems the alerts SHALL be monitored 24×7.
- **SEC-018.5.7.3** A failed Backup SHALL be re-run successfully: for Tier 0 and Tier 1 systems, within the RPO for the system's tier; for Tier 2 and Tier 3 systems, before the next scheduled Backup.
- **SEC-018.5.7.4** Two consecutive failed Backups of the same system, or any failure that leaves a Tier 0 or Tier 1 system outside its RPO, SHALL be escalated to the System Owner and the CIO within 4 hours.
- **SEC-018.5.7.5** Backup systems SHALL forward job status, administrative actions, deletion attempts and immutability changes to the SIEM under SEC-012. Anomalies indicating possible ransomware (e.g. sudden changes in data change rate, compression ratio or Backup size) SHOULD generate alerts to the SOC.
- **SEC-018.5.7.6** The CIO SHALL verify monthly that every system in the Backup Register has a successful Backup within its required frequency and that each 3-2-1-1-0 element is in place.

### 5.8 SaaS and Cloud Service data

- **SEC-018.5.8.1** For each SaaS application that holds Confidential or Restricted data, or that supports a Tier 0 or Tier 1 process, the System Owner SHALL document the provider's native Backup and restore capability, its retention, and whether the Organization can restore individual items and whole tenants to a point in time.
- **SEC-018.5.8.2** Where the provider's native capability does not meet the frequency in section 5.2, the restore testing in section 5.6, and at least the "1 off-site" and "1 immutable or offline" elements of section 5.3 under the Organization's control, the Organization SHALL back up the SaaS data to Organization-controlled storage or to an approved Third-Party Backup service.
- **SEC-018.5.8.3** Contracts for SaaS and Cloud Services holding Confidential or Restricted data SHALL require the provider to return all Organization data in a usable format on request and on termination, under RSK-003.
- **SEC-018.5.8.4** Cloud-native snapshots SHALL NOT be the only Backup copy unless they are copied to a separate account or region with immutability under SEC-018.5.3.4. Cloud Backup configuration SHALL also meet SEC-009.

### 5.9 Retention, Legal Hold and disposal

- **SEC-018.5.9.1** Backups SHALL be retained for the periods set for Backups in CMP-004 and SHALL be deleted or expired at the end of those periods unless a Legal Hold applies.
- **SEC-018.5.9.2** The CIO SHALL implement Legal Holds on affected Backups within 2 business days of notice from the GC.
- **SEC-018.5.9.3** `[GDPR]` `[CPRA]` Where Personal Data is deleted from production in response to a DSR or retention requirement, the CIO SHALL ensure that it is not restored to production from a Backup: either by deletion from Backups where technically feasible, or by recording the deletion and re-applying it after any restore, in accordance with CMP-005 and CMP-010.
- **SEC-018.5.9.4** Backup Media at end of life SHALL be sanitized or destroyed under SEC-017.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CIO | Owns this policy; maintains the Backup Register; operates Backup platforms; verifies 3-2-1-1-0 compliance monthly; implements Legal Holds; reports metrics. |
| System Owner | Maintains the Backup specification for their system; approves production restores; participates in restore tests; remediates Backup gaps. |
| Data Owner | Approves restores of Confidential or Restricted data to locations other than production. |
| Business Continuity Manager | Provides Recovery Tiers from RSK-004; uses restore test results in RES-004 and RES-005. |
| Head of Security Engineering | Approves the security architecture of Backup systems, including separation of security domains and Encryption key separation. |
| SOC Manager | Monitors Backup security alerts (deletion, immutability changes, ransomware indicators) under SEC-012. |
| CTO | Ensures Cloud Service and IaC Backups meet this policy and SEC-009. |
| GC | Issues and releases Legal Holds on Backups. |
| DPO / CPO | `[GDPR]` `[CPRA]` Confirm the handling of deleted Personal Data in Backups. |
| HIPAA Security Officer | `[HIPAA]` Confirms ePHI Backups and restores meet CMP-008. |
| Head of GRC | `[SOX]` Confirms that Backups of Financially Significant Systems meet CMP-009. |
| ISSC | Approves this policy. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| SEC-018.7.1 | Backup frequency | Tier 0 continuous replication or ≤ 15 min · Tier 1 every 4 h · Tier 2 daily · Tier 3 weekly (matches RSK-004 RPO) |
| SEC-018.7.2 | Restore testing | Tier 0 and Tier 1 quarterly · Tier 2 and Tier 3 every 12 months |
| SEC-018.7.3 | Tier 0 point-in-time Backups in addition to replication | At least daily |
| SEC-018.7.4 | Full or synthetic full Backup (Tier 0 – Tier 2) | At least weekly |
| SEC-018.7.5 | Copy rule | 3-2-1-1-0 for Tier 0 – Tier 2 and Restricted data; 3-1-0 elements for other Tier 3 |
| SEC-018.7.6 | Off-site separation | ≥ 100 km or a separate cloud region |
| SEC-018.7.7 | Immutable copy retention lock | Equal to the CMP-004 Backup retention period; compliance mode |
| SEC-018.7.8 | Restore test from immutable or offline copy | Every 12 months per Tier 0 and Tier 1 system |
| SEC-018.7.9 | Restore test coverage per system | Tier 0/1 every 12 months · Tier 2/3 every 24 months |
| SEC-018.7.10 | Backup job review | Each business day; Tier 0/1 alerts 24×7 |
| SEC-018.7.11 | Failed Backup re-run | Tier 0/1 within RPO · Tier 2/3 before next scheduled Backup |
| SEC-018.7.12 | Escalation of repeated or RPO-breaching failures | Within 4 hours |
| SEC-018.7.13 | Backup gap remediation | Within 30 days of finding |
| SEC-018.7.14 | Backup retention | As set in CMP-004 |
| SEC-018.7.15 | Legal Hold applied to Backups | Within 2 business days of GC notice |
| SEC-018.7.16 | Backup Encryption | Per SEC-006, at rest and in transit |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Backup job success rate | ≥ 99% | Monthly | CIO |
| Systems with a successful Backup within required frequency | 100% Tier 0/1; ≥ 98% Tier 2/3 | Monthly | CIO |
| Systems in the Asset Inventory with an approved Backup specification | 100% | Monthly | CIO |
| Tier 0/1 and Restricted-data systems meeting 3-2-1-1-0 | 100% | Monthly | CIO |
| Restore tests completed on schedule | 100% | Quarterly | CIO |
| Restore tests meeting RTO and RPO | 100%; each failure remediated and retested within 30 days | Quarterly | CIO |
| SaaS applications in scope with verified Backup coverage | 100% | Quarterly | CIO |
| Unauthorized Backup deletion or immutability change attempts | 0 successful; all alerted | Monthly | SOC Manager |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following requirements SHALL NOT receive an Exception: the "1 immutable or offline" element of SEC-018.5.3.1 for Tier 0 and Tier 1 systems, SEC-018.5.3.4 (separate security domain), and SEC-018.5.5.3 (dual authorization of Backup deletion). A restore test that fails SHALL be remediated and repeated within 30 days; it is not an Exception.

## 10. Enforcement

Non-compliance is handled under CMP-007.

Unauthorized deletion or alteration of Backups, or disabling of Backup jobs without an approved change under SEC-013, SHALL be investigated as a Security Incident under RES-002.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| SEC-018.5.1 | A.8.13, A.5.30 | PR.DS-11, ID.AM-08 | CP-9, CP-2 | 11.1 | A1.2 | DSS04.07 | HIPAA §164.308(a)(7)(ii)(A) |
| SEC-018.5.2 | A.8.13, A.8.14 | PR.DS-11 | CP-9, CP-10 | 11.2 | A1.2 | DSS04.07 | HIPAA §164.308(a)(7)(ii)(A) |
| SEC-018.5.3 | A.8.13 | PR.DS-11 | CP-6, CP-9 | 11.3, 11.4 | A1.2 | DSS04.07 | PCI DSS 9.4.1, 9.4.1.1; HIPAA §164.310(d)(2)(iv) |
| SEC-018.5.4 | A.8.13, A.8.24 | PR.DS-01, PR.DS-11 | CP-9, SC-28 | 11.3 | CC6.1, A1.2 | DSS05.02 | PCI DSS 3.5.1; HIPAA §164.312(a)(2)(iv) |
| SEC-018.5.5 | A.8.2, A.8.13 | PR.AA-05 | AC-6, CP-9 | 5.4, 11.3 | CC6.1, CC6.3 | DSS05.04 | HIPAA §164.308(a)(7)(ii)(A) |
| SEC-018.5.6 | A.8.13, A.5.30 | PR.DS-11, RC.RP-03 | CP-4, CP-9 | 11.5 | A1.3 | DSS04.04, DSS04.07 | HIPAA §164.308(a)(7)(ii)(D) |
| SEC-018.5.7 | A.8.13, A.8.16 | PR.DS-11, DE.CM-09 | CP-9, SI-4 | 11.2 | A1.2, CC7.2 | DSS04.07, DSS01.03 | — |
| SEC-018.5.8 | A.5.23, A.8.13 | PR.DS-11, GV.SC-07 | CP-9, SA-9 | 11.1, 15.4 | A1.2, CC9.2 | APO10.04, DSS04.07 | HIPAA §164.314(a) |
| SEC-018.5.9 | A.5.33, A.8.10 | PR.DS-11 | CP-9, SI-12, MP-6 | 3.4, 3.5 | C1.2 | DSS04.07, APO14 | GDPR Art. 17; Cal. Civ. Code §1798.105; SOX §404 |

## 12. Related documents

ISP-000, GOV-006, SEC-001, SEC-002, SEC-005, SEC-006, SEC-008, SEC-009, SEC-010, SEC-012, SEC-013, SEC-015, SEC-016, SEC-017, SEC-019, RSK-003, RSK-004, RES-002, RES-004, RES-005, CMP-003, CMP-004, CMP-005, CMP-007, CMP-008, CMP-009, CMP-010, REF-001, REF-002

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CIO | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
