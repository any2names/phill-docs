# SEC-012 — Logging & Monitoring Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | SEC-012 |
| Title | Logging & Monitoring Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | SOC Manager |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months, and on the event-triggered reviews in GOV-002.7.4 |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | SEC-001, SEC-002, SEC-003, SEC-005, SEC-006, SEC-007, SEC-009, SEC-013, SEC-019, RSK-003, RSK-005, RES-001, RES-002, CMP-004, CMP-005, CMP-008, CMP-009 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | SOC Manager | Initial release |

## 3. Purpose

This policy sets the Organization's requirements for generating, collecting, protecting,
centralizing and reviewing security logs, and for monitoring Information Systems so that
Security Events are detected, triaged and escalated within defined time limits. It provides
the evidence base for incident response (RES-002), forensic investigation, and the
demonstration of Control operation to auditors.

## 4. Scope

- **People:** all Workforce Members and Third Parties who operate, administer or support Information Systems, and the SOC, whether staffed internally or by a managed security service provider engaged under RSK-003.
- **Systems:** every Information System, Cloud Service, network device, Endpoint, security tool and application listed in the Asset Inventory (SEC-001), in production and in any non-production environment that holds Confidential or Restricted data.
- **Data:** all security logs, audit trails, alerts and monitoring telemetry, and the Personal Data they contain.
- **Locations:** all Organization facilities, data centers, cloud regions and remote work locations.
- **Third parties:** Third Parties that host or operate Information Systems for the Organization SHALL meet this policy, or provide equivalent logs to the Organization, as a contractual requirement under RSK-003.

Retention periods for logs are set in CMP-004 and are not restated here.

## 5. Policy statements

### 5.1 Logging governance

- **SEC-012.5.1.1** The SOC Manager SHALL maintain a Log Source Register listing every Log Source required under section 5.2, its System Owner, its Recovery Tier where assigned under RSK-004, its ingestion status in the SIEM, and the date it was last verified.
- **SEC-012.5.1.2** Each System Owner SHALL ensure that logging is enabled and configured on their Information System in accordance with this policy before the system enters production. Onboarding to the SIEM SHALL be a release criterion recorded in the change record under SEC-013.
- **SEC-012.5.1.3** The SOC Manager SHALL reconcile the Log Source Register against the Asset Inventory (SEC-001) every month and SHALL raise a finding to the System Owner for each in-scope asset that is not sending logs.
- **SEC-012.5.1.4** A System Owner SHALL remediate a missing or misconfigured Log Source within 30 days of the finding, or request an Exception under CMP-003.
- **SEC-012.5.1.5** Changes to logging configuration, SIEM parsing rules, detection rules and alert routing SHALL follow SEC-013.

### 5.2 Required Log Sources

- **SEC-012.5.2.1** The following Log Sources SHALL be enabled and forwarded to the SIEM. "Critical" sources are those whose loss of logging triggers the 60-minute silence alert in SEC-012.5.10.2.

| # | Log Source category | Examples | Criticality |
|---|---|---|---|
| 1 | Identity Providers, directories and SSO | Directory services, SSO and MFA platforms, federation services | Critical |
| 2 | Privileged access management | Credential vaults, session brokers, JIT elevation systems (SEC-005) | Critical |
| 3 | Endpoint operating systems and EDR | Security event logs, EDR detections and tamper alerts on Endpoints and servers | Critical |
| 4 | Network security controls | Firewalls, segmentation gateways, IDS/IPS, WAF, network access control | Critical |
| 5 | Remote access | VPN, zero-trust network access gateways, remote desktop gateways (SEC-007) | Critical |
| 6 | Cloud control plane | IaaS/PaaS audit trails, identity and access management events, resource configuration changes (SEC-009) | Critical |
| 7 | SaaS administrative and audit logs | Administrative actions, sharing changes and sign-ins for every SaaS holding Confidential or Restricted data | Critical |
| 8 | DNS, web proxy and secure web gateway | Resolver queries, blocked categories, egress connections | Standard |
| 9 | Email security | Message trace, phishing and Malware verdicts, user-reported messages (SEC-014) | Standard |
| 10 | Databases holding Confidential or Restricted data | Authentication, privileged queries, schema and permission changes | Critical |
| 11 | Business applications | Authentication, authorization failures, administrative actions, access to Restricted records | Standard; Critical for `[PCI]` CDE and `[SOX]` Financially Significant Systems |
| 12 | Key management and HSMs | Key creation, use by privileged identities, rotation, destruction (SEC-006) | Critical |
| 13 | Source code repositories and CI/CD pipelines | Permission changes, branch protection changes, pipeline secret access, production deployments (SEC-010) | Standard |
| 14 | Container and orchestration platforms | API server audit logs, admission decisions, runtime alerts | Standard |
| 15 | Data Loss Prevention | Policy violations and overrides | Standard |
| 16 | File integrity and change detection | Change-detection alerts on critical files (SEC-013) | Critical |
| 17 | Backup platforms | Job status, deletion attempts, retention-lock changes (SEC-018) | Standard |
| 18 | Vulnerability management | Scanner start/stop, credential failures, scan coverage (SEC-011) | Standard |
| 19 | Physical access control systems | Badge grants, denials and forced-door alarms for Zone 2 and Zone 3 areas (SEC-016) | Standard |
| 20 | Security tooling itself | SIEM, EDR console and log pipeline audit logs, including rule and configuration changes | Critical |
| 21 | AI Systems classified High under RSK-006 | Prompts, outputs, tool calls and human-review decisions (RSK-006.5.8.6) | Standard |
| 22 | Evidence repositories (CMP-004) and incident evidence stores (RES-001) | Access, download, modification and deletion events (RES-001.5.4.5) | Standard |

- **SEC-012.5.2.2** Where a Log Source cannot forward to the SIEM, the System Owner SHALL provide an alternative collection method approved by the SOC Manager that meets SEC-012.5.4 and SEC-012.5.5.
- **SEC-012.5.2.3** `[PCI]` Every system component in, or connected to, the CDE as scoped under SEC-019 SHALL be a Log Source and SHALL be designated Critical.
- **SEC-012.5.2.4** `[HIPAA]` Every Information System that creates, receives, maintains or transmits ePHI SHALL record and forward activity logs, in support of the audit controls standard documented in CMP-008.
- **SEC-012.5.2.5** `[SOX]` Every Financially Significant System, including its database and operating-system layers, SHALL forward privileged activity and change events to the SIEM to support the ITGC monitoring defined in CMP-009.

### 5.3 Required event types and fields

- **SEC-012.5.3.1** Each Log Source SHALL record, at minimum, the following event types where the source is capable of generating them:

| # | Event type | `[PCI]` reference |
|---|---|---|
| E1 | Individual User access to Restricted data, including CHD and ePHI | 10.2.1.1 |
| E2 | All actions taken by any individual using a Privileged Account | 10.2.1.2 |
| E3 | All access to audit logs and the SIEM | 10.2.1.3 |
| E4 | Invalid or failed logical access attempts | 10.2.1.4 |
| E5 | Creation, modification, elevation and deletion of accounts and credentials, including MFA enrollment changes | 10.2.1.5 |
| E6 | Initialization, stopping or pausing of audit logs | 10.2.1.6 |
| E7 | Creation and deletion of system-level objects | 10.2.1.7 |
| E8 | Successful logons, logoffs and session establishment for remote and privileged access | — |
| E9 | Changes to security configuration, policies, firewall rules and access control lists | — |
| E10 | Security tool detections, quarantines and tamper events | — |
| E11 | Data export, bulk download and external sharing of Confidential or Restricted data | — |
| E12 | Key management operations (SEC-006) | — |

- **SEC-012.5.3.2** `[PCI]` Each logged event SHALL contain, at minimum, the fields required by PCI DSS 10.2.2. The Organization applies the same field set to all Log Sources:

| Field | Requirement |
|---|---|
| User or process identity | Unique User, Service Account or process identifier; shared identities SHALL NOT be the only identifier |
| Event type | Normalized category of the action |
| Date and time | Timestamp in UTC, ISO 8601 format, with millisecond precision where the source supports it |
| Outcome | Success or failure |
| Origination | Source IP address, hostname or device identifier |
| Affected resource | Identity or name of the data, system component, resource or service affected |
| Destination | Target host, service or tenant, where applicable |
| Log Source identifier | Hostname or unique asset identifier matching the Asset Inventory |

- **SEC-012.5.3.3** Logs SHALL NOT contain Secrets, SAD, full PAN, or passwords (including failed password values). Where an application must log a reference to such data, it SHALL log a token, truncated value or hash in accordance with SEC-002 and SEC-006.
- **SEC-012.5.3.4** `[GDPR]` `[CPRA]` Personal Data in logs SHALL be limited to the fields in SEC-012.5.3.2 and any additional fields documented as necessary for security purposes in the ROPA under CMP-005.

### 5.4 Time synchronization

- **SEC-012.5.4.1** `[PCI]` All Information Systems SHALL synchronize their clocks using a time-synchronization protocol (e.g. NTP or PTP) to designated Organization time sources or to the time service of the hosting Cloud Service Provider.
- **SEC-012.5.4.2** The Head of Security Engineering SHALL designate at least two internal time sources, each synchronized to at least two independent authoritative UTC references. Only designated time sources SHALL accept synchronization from external sources.
- **SEC-012.5.4.3** Clock drift on any Log Source SHALL NOT exceed 1 second from the designated time sources. The SOC Manager SHALL configure an alert for Log Sources whose timestamps deviate from SIEM receipt time by more than 60 seconds.
- **SEC-012.5.4.4** `[PCI]` Time data and time-synchronization settings SHALL be protected: changes SHALL be restricted to Privileged Accounts with a business need, and every change SHALL be logged (event type E9) and follow SEC-013.

### 5.5 Log integrity and protection

- **SEC-012.5.5.1** `[PCI]` Read access to logs SHALL be limited to Workforce Members with a job-related need, approved under SEC-003. Access to the SIEM SHALL be reviewed at the frequency set for systems holding Restricted data in SEC-003.
- **SEC-012.5.5.2** `[PCI]` Logs SHALL be protected from modification and deletion. Logs in the SIEM and central log storage SHALL be held on immutable (write-once) storage or protected by cryptographic integrity checks (e.g. hash chaining) for their full retention period under CMP-004.
- **SEC-012.5.5.3** `[PCI]` Logs SHALL be forwarded to the SIEM or central log storage within 5 minutes of generation for Critical Log Sources and within 60 minutes for Standard Log Sources, so that logs are not retained only on the originating system.
- **SEC-012.5.5.4** `[PCI]` File-integrity monitoring or change-detection mechanisms SHALL be applied to central log storage so that any change to existing log data generates an alert.
- **SEC-012.5.5.5** Administrators of a system SHALL NOT have the ability to modify or delete that system's logs in the SIEM or central log storage. SIEM administration SHALL be separated from the administration of monitored systems in accordance with GOV-001 Segregation of Duties rules.
- **SEC-012.5.5.6** Logs SHALL be encrypted in transit and at rest in accordance with SEC-006.
- **SEC-012.5.5.7** Log storage SHALL be monitored for capacity. An alert SHALL be raised at 80% of allocated capacity, and the SOC Manager SHALL expand capacity or adjust ingestion before 95% is reached.
- **SEC-012.5.5.8** Logs relevant to an open Security Incident or a Legal Hold SHALL be preserved beyond the CMP-004 retention period until the GC releases the hold or the incident record is closed under RES-002.

### 5.6 Centralization in a SIEM

- **SEC-012.5.6.1** The Organization SHALL operate a SIEM (or equivalent centralized log analytics platform) that collects, normalizes, correlates and retains logs from all sources in section 5.2.
- **SEC-012.5.6.2** The SIEM SHALL keep logs from the most recent period required by CMP-004 immediately available for search; older logs MAY be held in archive storage that can be restored within 5 business days.
- **SEC-012.5.6.3** The SIEM SHALL be deployed with resilience matching Recovery Tier 1 under RSK-004, at minimum.
- **SEC-012.5.6.4** The SIEM SHALL enrich events with asset criticality and Classification Level from the Asset Inventory (SEC-001), and with User identity attributes from the Identity Provider (SEC-003).
- **SEC-012.5.6.5** The SIEM SHALL ingest threat intelligence indicators produced under RSK-005 and match them against incoming events.
- **SEC-012.5.6.6** Where SIEM operation or monitoring is outsourced, the managed service provider SHALL be assessed as a Tier 1 Critical Vendor under RSK-003.5.2.1, and the Organization SHALL retain direct read access to all of its logs.

### 5.7 Detection Use Cases and coverage

- **SEC-012.5.7.1** The SOC Manager SHALL maintain a Detection Use Case Catalog. Each entry SHALL record the threat or behavior detected, the Log Sources required, the detection logic location, the alert severity, the response playbook reference (RES-002), and the MITRE ATT&CK technique tags required by RSK-005.5.7.1.
- **SEC-012.5.7.2** The catalog SHALL include, at minimum, detections for:
  1. brute-force, password-spraying and MFA-fatigue attempts;
  2. sign-ins from impossible travel, anonymizing networks or prohibited jurisdictions;
  3. creation of, or privilege grant to, a Privileged Account outside the PAM workflow (SEC-005);
  4. use of a Break-glass Account, or sign-in to a cloud root or owner account, at Critical alert severity (SEC-005.5.7.4, SEC-005.5.8.5);
  5. disabling, stopping or tampering with logging, EDR or other security tooling;
  6. Malware and ransomware behaviors, including mass file encryption or deletion;
  7. lateral movement and credential-dumping techniques;
  8. data exfiltration indicators, including large or unusual outbound transfers;
  9. changes to firewall rules, security groups or cloud identity policies outside an approved change (SEC-013);
  10. deletion or retention-lock changes on backups (SEC-018);
  11. access to Restricted data stores by a User without a recorded business need;
  12. matches against threat intelligence indicators (RSK-005);
  13. `[PCI]` unauthorized changes to CDE system components and Payment Pages, with Payment Page tamper alerts at Critical alert severity (SEC-019.5.8.5).
- **SEC-012.5.7.3** Each Detection Use Case SHALL be tested at least every 12 months, and within 30 days of a material change to its Log Sources, by simulation or replay of the targeted behavior. Test results SHALL be retained as Evidence under CMP-004.
- **SEC-012.5.7.4** The SOC Manager SHALL measure detection coverage against the ATT&CK coverage map in RSK-005.5.7.2 every quarter and report it to the ISSC under GOV-003.
- **SEC-012.5.7.5** New or revised Detection Use Cases SHALL be created within 30 days of: a Sev-1 or Sev-2 Post-Incident Review identifying a detection gap (RES-002); a threat assessment under RSK-005 identifying an uncovered technique; or onboarding of a new Critical Log Source.
- **SEC-012.5.7.6** The SOC Manager SHALL review each Detection Use Case with a false-positive rate above 90% over the prior 30 days and SHALL tune, retire or justify it within 30 days. A detection SHALL NOT be disabled without a change record under SEC-013.

### 5.8 Alert triage and escalation

- **SEC-012.5.8.1** The SOC SHALL monitor alerts 24 hours a day, 7 days a week, 365 days a year.
- **SEC-012.5.8.2** Each alert SHALL be assigned an alert severity of Critical, High, Medium or Low on creation, according to the criteria in the Detection Use Case Catalog.
- **SEC-012.5.8.3** The SOC SHALL complete triage of each alert, from alert creation to a documented triage decision, within the following SLAs:

| Alert severity | Triage SLA |
|---|---|
| Critical | 15 minutes (24×7) |
| High | 1 hour |
| Medium | 8 business hours |
| Low | 5 business days |

- **SEC-012.5.8.4** A triage decision SHALL be recorded for every alert as one of: Security Incident declared, benign true positive, false positive, or duplicate, with the analyst's rationale.
- **SEC-012.5.8.5** Where triage determines that a Security Event is a Security Incident, the SOC SHALL declare it and hand it to incident response under RES-002, which sets the Severity Level and response timelines.
- **SEC-012.5.8.6** Alert severity SHALL NOT be lowered after creation without a recorded justification by the analyst and review by the SOC Manager or a delegated shift lead.
- **SEC-012.5.8.7** The SOC Manager SHALL maintain an escalation roster that ensures a responder is reachable for Critical and High alerts at all times.

### 5.9 Log review

- **SEC-012.5.9.1** `[PCI]` The following SHALL be reviewed at least once daily using automated mechanisms (the SIEM correlation and alerting in section 5.7): all security events; logs of all system components that store, process or transmit CHD or SAD, or that could affect the security of CHD or SAD; logs of all critical system components; and logs of all servers and system components that perform security functions. The Organization applies this daily automated review to all Log Sources in section 5.2.
- **SEC-012.5.9.2** `[PCI]` The SOC SHALL complete a documented daily review of the alert queue, open exceptions and anomalies, and SHALL address each exception and anomaly identified under section 5.8.
- **SEC-012.5.9.3** `[HIPAA]` The SOC Manager SHALL produce a monthly information-system activity review report for ePHI systems covering access anomalies, failed log-in trends and privileged activity, and SHALL provide it to the HIPAA Security Officer.
- **SEC-012.5.9.4** `[SOX]` The SOC Manager SHALL provide privileged activity and unauthorized-change reports for Financially Significant Systems at the frequency in CMP-009.5.4.4.
- **SEC-012.5.9.5** Evidence of each daily review (reviewer, date, items reviewed, actions taken) SHALL be retained as Evidence under CMP-004.

### 5.10 Log failure alerting

- **SEC-012.5.10.1** `[PCI]` Failures of critical security control systems SHALL be detected, alerted and addressed. Critical security control systems are: network security controls, IDS/IPS, file-integrity monitoring, anti-Malware and EDR, physical access controls, logical access controls, audit logging mechanisms, segmentation controls, audit log review mechanisms, and automated security testing tools.
- **SEC-012.5.10.2** The SIEM SHALL raise a High-severity alert when a Critical Log Source sends no events for 60 consecutive minutes, and a Medium-severity alert when a Standard Log Source sends no events for 24 consecutive hours.
- **SEC-012.5.10.3** The SIEM SHALL raise a Critical-severity alert on any event of type E6 (stopping or pausing of audit logs) on a Critical Log Source.
- **SEC-012.5.10.4** `[PCI]` On a failure of a critical security control system, the System Owner, coordinated by the SOC, SHALL: restore the security function; identify and document the duration (start and end date and time) of the failure; identify and document the Root Cause and the remediation required; identify and address any security issues that arose during the failure; determine whether further action is required as a result; implement controls to prevent recurrence; and resume monitoring.
- **SEC-012.5.10.5** Logging for a Critical Log Source SHALL be restored within 24 hours of the failure alert. Failures exceeding 24 hours SHALL be escalated to the CISO and treated as a Security Incident candidate under RES-002.

### 5.11 Monitoring of Third Parties and cloud services

- **SEC-012.5.11.1** Contracts with Third Parties hosting Information Systems that hold Confidential or Restricted data SHALL require the Third Party to provide audit logs to the Organization, or to notify the Organization of Security Events affecting the Organization, within the timelines set in RSK-003.
- **SEC-012.5.11.2** Where a SaaS provider does not expose audit logs, the System Owner SHALL record the gap in the Log Source Register and the Risk Register (TPL-001).

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| SOC Manager | Owns this policy; maintains the Log Source Register and Detection Use Case Catalog; operates 24×7 monitoring and triage; reports coverage and SLA metrics; coordinates log failure response. |
| CISO | Oversees the policy; receives escalations of log failures exceeding 24 hours; presents monitoring metrics to the ISSC. |
| Head of Security Engineering | Designates time sources; engineers log pipelines and SIEM integrations; protects log integrity; administers the SIEM separately from monitored systems. |
| System Owner | Enables and maintains logging on their Information System; remediates Log Source gaps; restores failed logging; participates in root-cause analysis. |
| CIO / CTO | Ensure infrastructure, cloud and application teams onboard Log Sources before production. |
| HIPAA Security Officer | `[HIPAA]` Receives and acts on the monthly ePHI activity review. |
| Head of GRC | `[SOX]` Confirms that log reporting meets CMP-009; tests log review Controls as part of control testing. |
| CPO / DPO | Confirm that Personal Data in logs is limited under SEC-012.5.3.4. |
| GC | Issues and releases Legal Holds on logs. |
| ISSC | Approves this policy; reviews quarterly detection coverage and monitoring metrics. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| SEC-012.7.1 | Alert triage SLA | Critical 15 minutes (24×7) · High 1 hour · Medium 8 business hours · Low 5 business days |
| SEC-012.7.2 | SOC monitoring coverage | 24×7×365 |
| SEC-012.7.3 | Log forwarding latency to the SIEM | Critical sources ≤ 5 minutes · Standard sources ≤ 60 minutes |
| SEC-012.7.4 | Maximum clock drift | 1 second from designated time sources |
| SEC-012.7.5 | Designated internal time sources | At least 2, each synchronized to at least 2 independent UTC references |
| SEC-012.7.6 | Log silence alert | Critical sources: 60 minutes (High alert) · Standard sources: 24 hours (Medium alert) |
| SEC-012.7.7 | Restoration of logging for a Critical source | Within 24 hours of the failure alert |
| SEC-012.7.8 | Automated log review | At least daily, all Log Sources |
| SEC-012.7.9 | Log retention | As set for security logs in CMP-004 |
| SEC-012.7.10 | Archive restore time | Within 5 business days |
| SEC-012.7.11 | Log storage capacity alert | 80% of allocated capacity |
| SEC-012.7.12 | Detection Use Case testing | Every 12 months, and within 30 days of material change to its Log Sources |
| SEC-012.7.13 | Log Source gap remediation | Within 30 days of finding |
| SEC-012.7.14 | Log Source Register reconciliation with Asset Inventory | Monthly |
| SEC-012.7.15 | SIEM resilience | Recovery Tier 1 under RSK-004, at minimum |
| SEC-012.7.16 | `[HIPAA]` ePHI activity review report | Monthly |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Alerts triaged within SLA, by severity | ≥ 95% for each severity; 100% for Critical | Monthly | SOC Manager |
| In-scope assets in the Asset Inventory sending logs to the SIEM | ≥ 98%; 100% for `[PCI]` CDE components | Monthly | SOC Manager |
| Critical Log Source silence events restored within 24 hours | 100% | Monthly | SOC Manager |
| Log Sources with clock drift above 1 second | 0 | Monthly | Head of Security Engineering |
| Detection Use Cases tested within the last 12 months | 100% | Quarterly | SOC Manager |
| Adversary technique coverage by at least one tested detection | Target set annually by the CISO and reported to the ISSC | Quarterly | SOC Manager |
| Daily log review records complete | 100% of days | Monthly | SOC Manager |
| Mean time to detect for Sev-1 and Sev-2 Security Incidents | Reported trend; decreasing year on year | Quarterly | SOC Manager |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following requirements SHALL NOT receive an Exception: SEC-012.5.3.3 (no Secrets, SAD or full PAN in logs), SEC-012.5.5.2 (protection of logs from modification), and SEC-012.5.5.5 (administrators may not alter their own systems' logs). Where a Log Source cannot technically meet a requirement, the Exception request SHALL identify the Compensating Control.

## 10. Enforcement

Non-compliance is handled under CMP-007.

Deliberately disabling, bypassing or tampering with logging or monitoring, or deleting or altering logs without authorization, SHALL be investigated as a Security Incident under RES-002 in addition to disciplinary action under CMP-007.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| SEC-012.5.1 – 5.2 | A.8.15, A.8.16 | PR.PS-04, DE.CM-01, DE.CM-09 | AU-1, AU-2, AU-12 | 8.1, 8.2 | CC7.2 | DSS05.07 | PCI DSS 10.2.1; HIPAA §164.312(b) |
| SEC-012.5.3 | A.8.15 | PR.PS-04 | AU-2, AU-3 | 8.5 | CC7.2 | DSS05.07 | PCI DSS 10.2.1.1–10.2.1.7, 10.2.2, 3.3.1; GDPR Art. 5(1)(c) |
| SEC-012.5.4 | A.8.17 | PR.PS-04 | AU-8 | 8.4 | CC7.2 | DSS05.07 | PCI DSS 10.6.1–10.6.3 |
| SEC-012.5.5 | A.8.15 | PR.DS-01, PR.PS-04 | AU-4, AU-5, AU-9 | 8.3, 8.9 | CC7.2 | DSS05.07 | PCI DSS 10.3.1–10.3.4; HIPAA §164.312(b), §164.312(c)(1) |
| SEC-012.5.6 | A.8.15, A.8.16 | DE.AE-03, DE.AE-07 | AU-6, SI-4 | 8.9, 8.10, 13.1 | CC7.2 | DSS05.07 | PCI DSS 10.3.3, 10.5.1 |
| SEC-012.5.7 | A.8.16, A.5.7 | DE.CM-01, DE.CM-03, DE.AE-02, DE.AE-07 | SI-4, AU-6, RA-3 | 13.1, 13.3 | CC7.2, CC7.3 | DSS05.07, DSS02.01 | PCI DSS 10.4.1.1 |
| SEC-012.5.8 | A.5.25, A.6.8 | DE.AE-02, DE.AE-06, DE.AE-08, RS.MA-01 | IR-4, IR-5, IR-6, SI-4 | 13.1, 17.2 | CC7.3, CC7.4 | DSS02.02, DSS05.07 | PCI DSS 10.4.3, 12.10.5 |
| SEC-012.5.9 | A.8.15, A.8.16 | DE.AE-02, DE.CM-03 | AU-6 | 8.11 | CC4.1, CC7.2 | DSS05.07, MEA01 | PCI DSS 10.4.1, 10.4.1.1, 10.4.2, 10.4.3; HIPAA §164.308(a)(1)(ii)(D), §164.308(a)(5)(ii)(C); SOX §404 |
| SEC-012.5.10 | A.8.15, A.8.16 | DE.CM-09 | AU-5, SI-4 | 8.2 | CC7.2 | DSS05.07 | PCI DSS 10.7.2, 10.7.3 |
| SEC-012.5.11 | A.5.22, A.8.16 | DE.CM-06 | SA-9, AU-6 | 15.6 | CC9.2 | APO10.05 | HIPAA §164.314(a) |

## 12. Related documents

ISP-000, GOV-001, GOV-003, GOV-006, SEC-001, SEC-002, SEC-003, SEC-005, SEC-006, SEC-007, SEC-009, SEC-010, SEC-011, SEC-013, SEC-014, SEC-016, SEC-018, SEC-019, RSK-003, RSK-004, RSK-005, RES-001, RES-002, CMP-003, CMP-004, CMP-005, CMP-007, CMP-008, CMP-009, TPL-001, REF-001, REF-002

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: SOC Manager | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
