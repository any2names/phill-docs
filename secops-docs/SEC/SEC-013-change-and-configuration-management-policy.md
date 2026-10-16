# SEC-013 — Change & Configuration Management Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | SEC-013 |
| Title | Change & Configuration Management Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Information Officer (CIO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months, and on the event-triggered reviews in GOV-002.7.4 |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-001, SEC-001, SEC-005, SEC-009, SEC-010, SEC-011, SEC-012, SEC-019, RSK-002, RSK-004, RES-002, RES-005, CMP-004, CMP-009 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CIO | Initial release |

## 3. Purpose

This policy sets the Organization's requirements for controlling Changes to Information
Systems and for establishing, hardening and maintaining their configurations. It ensures
that every Change is authorized, risk-assessed, tested, approved, recorded and reversible,
and that system components run on approved Configuration Baselines whose drift is detected
and corrected.

## 4. Scope

- **People:** all Workforce Members and Third Parties who request, approve, build, test, deploy or administer Changes to Information Systems.
- **Systems:** all production Information Systems and Cloud Services in the Asset Inventory (SEC-001), including infrastructure, network devices, operating systems, databases, applications, SaaS configuration, security tools, Infrastructure as Code, and Endpoint management policies. Non-production environments are in scope for Configuration Baselines (section 5.8 – 5.10) and for Changes that affect Confidential or Restricted data held there.
- **Data:** change records, Configuration Baselines, configuration-state data and drift reports.
- **Locations:** all Organization facilities, data centers and cloud regions.
- **Third parties:** Changes made by Third Parties to Organization-managed Information Systems follow this policy. Changes by Cloud Service Providers to their own platforms are managed through RSK-003.

Secure coding, code review and pipeline controls for software are in SEC-010. Vulnerability
remediation timelines are in SEC-011. This policy governs how those Changes are authorized
and deployed.

## 5. Policy statements

### 5.1 Change management governance

- **SEC-013.5.1.1** Every Change to a production Information System SHALL be recorded in the Organization's designated change management system before implementation, except Emergency Changes, which SHALL be recorded within 1 business day of implementation.
- **SEC-013.5.1.2** Each change record SHALL include: a unique identifier; requester; System Owner; affected Information Systems from the Asset Inventory; description and business reason; Change Class; Change Risk Rating (section 5.3); security impact assessment; test evidence; implementation plan; rollback plan; approvals; scheduled and actual implementation window; implementer; outcome; and `[PCI]` the CDE scope-impact flag required by SEC-019.5.1.5.
- **SEC-013.5.1.3** The CIO SHALL publish a change management procedure implementing this policy, including the change calendar and the blackout periods in SEC-013.5.6.6.
- **SEC-013.5.1.4** No Change SHALL be implemented in production by a person who lacks an approved change record, other than within an Emergency Change under section 5.2.
- **SEC-013.5.1.5** The individual who implements a Normal Change SHALL NOT be the sole approver of that Change.
- **SEC-013.5.1.6** `[HIPAA]` The change record for any Change that moves equipment holding ePHI SHALL record confirmation, before the move, that a retrievable exact copy of the ePHI exists under SEC-018 (45 CFR §164.310(d)(2)(iv)).

### 5.2 Change classes

- **SEC-013.5.2.1** Every Change SHALL be assigned one of the following Change Classes:

| Change Class | Definition reference | Approval |
|---|---|---|
| Standard | Low-risk, repeatable change on the approved Standard Change catalog | Pre-approved; no per-instance CAB approval |
| Normal | Any change not on the Standard Change catalog and not an Emergency Change | CAB approval before implementation |
| Emergency | Change needed to restore service or remediate an active threat | Implemented on authorization by an Emergency approver (SEC-013.5.2.6); retrospective approval within 2 business days |

- **SEC-013.5.2.2** The CAB SHALL approve each Standard Change type before it is added to the Standard Change catalog. `[SOX]` The catalog SHALL NOT include the change types excluded by CMP-009.5.5.2. Each catalog entry SHALL include a documented, tested procedure, its rollback steps, and the Information Systems to which it applies.
- **SEC-013.5.2.3** The CAB SHALL review the Standard Change catalog at least every 12 months, and SHALL remove a Standard Change type from the catalog after any instance of that type causes a Sev-1 or Sev-2 Security Incident or a failed change requiring rollback in production.
- **SEC-013.5.2.4** Standard Changes SHALL still be recorded in the change management system, automatically or manually, before implementation.
- **SEC-013.5.2.5** An Emergency Change SHALL be used only to restore service within the Recovery Tier targets in RSK-004, or to contain or remediate an active Security Incident or a vulnerability in the CISA KEV catalog under SEC-011. Convenience or missed deadlines SHALL NOT justify an Emergency Change.
- **SEC-013.5.2.6** An Emergency Change SHALL be authorized before implementation by one of: the CIO, the CTO, the CISO, or a delegate named in writing by one of them; or, during a declared Security Incident, by the Incident Commander under RES-002. The authorization SHALL be recorded (e.g. in the incident ticket or chat log) at the time it is given.
- **SEC-013.5.2.7** Every Emergency Change SHALL receive retrospective approval by the CAB within 2 business days of implementation. An Emergency Change that is not approved retrospectively SHALL be reviewed under section 5.7 and either regularized through a Normal Change or rolled back.
- **SEC-013.5.2.8** The CIO SHALL report the number of Emergency Changes per System Owner to the ISSC monthly. More than 10% Emergency Changes in any month for a system SHALL trigger a review by the CAB of that system's change practices.

### 5.3 Risk assessment of changes

- **SEC-013.5.3.1** The requester SHALL assign each Normal and Emergency Change a Change Risk Rating of High, Medium or Low using the following criteria. The highest criterion met determines the rating:

| Rating | Criteria (any one) |
|---|---|
| High | Affects a Recovery Tier 0 or Tier 1 system; affects authentication, authorization, Encryption, logging, network segmentation or perimeter controls; affects the `[PCI]` CDE or a `[SOX]` Financially Significant System; requires an outage of customer-facing services; has no tested rollback |
| Medium | Affects a Recovery Tier 2 system; affects systems holding Confidential or Restricted data; affects more than one Information System; involves a Third Party implementer |
| Low | Affects a single Recovery Tier 3 system or non-production environment holding no Confidential or Restricted data, with a tested rollback |

- **SEC-013.5.3.2** Each Normal and Emergency Change SHALL include a security impact assessment answering, at minimum: whether the Change alters access controls, network exposure, data flows, Encryption, logging or Configuration Baselines; whether it introduces new Third Parties or Cloud Services; and whether it affects in-scope systems for `[PCI]`, `[HIPAA]` or `[SOX]`.
- **SEC-013.5.3.3** Changes rated High SHALL be reviewed by the Head of Security Engineering, or a delegate, before CAB approval.
- **SEC-013.5.3.4** A Change that introduces a new Information System, a new Cloud Service or a new external connection SHALL trigger a risk assessment under RSK-002 before CAB approval. A Change that introduces new processing of Personal Data SHALL be referred to the DPO for DPIA screening under CMP-005.

### 5.4 Testing

- **SEC-013.5.4.1** Every Normal Change SHALL be tested in a non-production environment that is representative of production before CAB approval. Test evidence (test cases, results, tester, date) SHALL be attached to the change record.
- **SEC-013.5.4.2** Testing SHALL verify functional outcome, absence of adverse impact on security Controls, and that the rollback plan works. For High-rated Changes, the rollback SHALL be executed at least once in test.
- **SEC-013.5.4.3** Where a representative non-production environment does not exist, the System Owner SHALL document the reason and the alternative verification (e.g. canary or staged deployment) in the change record, and the CAB SHALL explicitly accept it.
- **SEC-013.5.4.4** `[PCI]` Changes to bespoke and custom software SHALL be tested for compliance with the secure development requirements in SEC-010 before deployment to production.
- **SEC-013.5.4.5** Production data SHALL NOT be used for testing except under the conditions set in SEC-010.

### 5.5 Approval and the Change Advisory Board

- **SEC-013.5.5.1** The CIO SHALL establish the CAB. Its membership SHALL be: the CIO or a delegate (chair); the Head of Security Engineering or a delegate; representatives of infrastructure, network, cloud and application operations; the Business Continuity Manager or a delegate for Changes to Recovery Tier 0 and Tier 1 systems; and the System Owner of each Change under review.
- **SEC-013.5.5.2** The CAB SHALL meet at least weekly. Quorum is the chair or delegate, the security representative, and at least two operations representatives.
- **SEC-013.5.5.3** The CAB SHALL approve, reject or defer each Normal Change and SHALL record its decision, the approvers' identities and the date in the change record.
- **SEC-013.5.5.4** Low-rated Normal Changes MAY be approved outside a CAB meeting by the System Owner and one CAB member, provided both approvals are recorded in the change management system before implementation.
- **SEC-013.5.5.5** The CAB SHALL NOT approve a High-rated Change without a security review under SEC-013.5.3.3 and a rollback plan tested under SEC-013.5.4.2.
- **SEC-013.5.5.6** Approval SHALL expire if the Change is not implemented within 30 days of approval; the Change SHALL then be resubmitted.
- **SEC-013.5.5.7** `[PCI]` Each Change to a system component in the CDE SHALL document the reason for the Change, the security impact, authorized approval, testing to verify no adverse impact on security, and the procedures to address failure and return to a secure state.

### 5.6 Implementation and rollback

- **SEC-013.5.6.1** Changes SHALL be implemented only within the approved window and only by Users whose access to production is authorized under SEC-003 and, for privileged actions, SEC-005.
- **SEC-013.5.6.2** Where feasible, Changes SHALL be deployed through automated pipelines or Infrastructure as Code (SEC-009, SEC-010) so that the deployed artifact is the tested and approved artifact.
- **SEC-013.5.6.3** The implementer SHALL execute the rollback plan if the Change fails its acceptance checks, causes an unplanned outage, or degrades a security Control, unless the System Owner and a CAB member jointly decide in writing to fix forward.
- **SEC-013.5.6.4** A rollback SHALL restore the system to its last approved Configuration Baseline and SHALL be recorded in the change record.
- **SEC-013.5.6.5** A failed Change that causes a disruption to a Recovery Tier 0 or Tier 1 system, or a security impact, SHALL be reported to the SOC and assessed under RES-002.
- **SEC-013.5.6.6** The CIO SHALL define blackout periods (e.g. financial period close, peak trading periods) during which only Emergency Changes and CAB-approved exceptions MAY be implemented. `[SOX]` Blackout periods SHALL include the financial close windows defined by the CFO for Financially Significant Systems.

### 5.7 Post-implementation review

- **SEC-013.5.7.1** The System Owner SHALL verify and record the outcome of every Change (successful, successful with issues, failed, rolled back) within 2 business days of implementation.
- **SEC-013.5.7.2** A post-implementation review SHALL be completed within 5 business days for: every Emergency Change; every High-rated Change; every failed or rolled-back Change; and every Change linked to a Security Incident.
- **SEC-013.5.7.3** The review SHALL record the Root Cause of any failure, any deviation from the approved plan, and corrective actions with owners and due dates. Corrective actions SHALL be tracked to closure.
- **SEC-013.5.7.4** `[PCI]` On completion of a Significant Change, the System Owner SHALL confirm that all applicable PCI DSS requirements are in place on all new or changed systems and networks, and that documentation, including the CDE scope under SEC-019, is updated.

### 5.8 Configuration Baselines and hardening

- **SEC-013.5.8.1** The Head of Security Engineering SHALL maintain a Configuration Baseline for each class of system component, including operating systems, network devices, databases, container images, hypervisors, Cloud Service accounts and subscriptions, SaaS tenants holding Confidential or Restricted data, and Endpoint images.
- **SEC-013.5.8.2** Each Configuration Baseline SHALL be derived from the current CIS Benchmark Level 1 profile for that technology, or, where none exists, from vendor hardening guidance or a DISA STIG. Level 2 profile settings SHALL be applied to systems that hold Restricted data or are internet-facing, where the System Owner has confirmed operational compatibility.
- **SEC-013.5.8.3** Every deviation from the source benchmark SHALL be documented in the Configuration Baseline with its justification and approved by the Head of Security Engineering.
- **SEC-013.5.8.4** Configuration Baselines SHALL, at minimum:
  1. remove or disable unnecessary services, protocols, ports, daemons, accounts and functions;
  2. change all vendor default passwords and remove or disable default accounts before connection to any network;
  3. enable logging in accordance with SEC-012;
  4. enforce Encryption settings from SEC-006 and authentication settings from SEC-004;
  5. enable host firewall and EDR in accordance with SEC-007 and SEC-008;
  6. synchronize time in accordance with SEC-012;
  7. `[PCI]` implement only one primary function per server, or isolate functions with different security levels on the same system component.
- **SEC-013.5.8.5** Configuration Baselines SHALL be reviewed and updated at least every 12 months, within 90 days of a new CIS Benchmark major version for that technology, and when a vulnerability under SEC-011 requires a configuration change.
- **SEC-013.5.8.6** New system components SHALL be built from an approved Configuration Baseline (e.g. a golden image or IaC template) and SHALL be verified against it before entering production.
- **SEC-013.5.8.7** Changes to a Configuration Baseline are Normal Changes and SHALL follow sections 5.3 – 5.7.
- **SEC-013.5.8.8** Configuration Baselines and the Organization's IaC templates SHALL be stored under version control with change history retained under CMP-004.

### 5.9 Drift detection and unauthorized change

- **SEC-013.5.9.1** The Head of Security Engineering SHALL deploy automated configuration assessment that compares each system component in production against its Configuration Baseline at least daily for Recovery Tier 0 and Tier 1 systems, `[PCI]` CDE components and internet-facing systems, and at least weekly for all others.
- **SEC-013.5.9.2** Drift findings SHALL be remediated, or the deviation approved through a Normal Change, within 30 days. Drift that disables a security Control (e.g. logging, EDR, MFA, Encryption, host firewall) SHALL be treated as a High-severity alert under SEC-012.
- **SEC-013.5.9.3** `[PCI]` A change-detection mechanism (e.g. file-integrity monitoring) SHALL alert on unauthorized modification, including changes, additions and deletions, of critical system files, configuration files and content files, and SHALL perform critical file comparisons at least once weekly.
- **SEC-013.5.9.4** `[PCI]` Change- and tamper-detection for HTTP headers and Payment Page contents (PCI DSS 11.6.1) is set in SEC-019.5.8.4 and SEC-019.5.8.5.
- **SEC-013.5.9.5** The CIO SHALL reconcile production changes detected by deployment, configuration and change-detection tooling against approved change records at least monthly. Each detected Change without a change record is an unauthorized Change and SHALL be investigated by the SOC under RES-002.
- **SEC-013.5.9.6** `[HIPAA]` The change-detection mechanism in SEC-013.5.9.3 SHALL also cover critical system, configuration and content files of Information Systems that store ePHI, supporting the integrity decisions documented in CMP-008.

### 5.10 Configuration items and records

- **SEC-013.5.10.1** Configuration items and their relationships SHALL be recorded in the Asset Inventory under SEC-001. Each change record SHALL reference the affected configuration items.
- **SEC-013.5.10.2** The System Owner SHALL update architecture diagrams and operating documentation within 10 business days of a Change that alters them. Network and data-flow diagrams SHALL be updated under SEC-007.5.8.3 and, for the `[PCI]` CDE, before the change record is closed under SEC-019.5.3.4.
- **SEC-013.5.10.3** Change records, CAB minutes, Configuration Baselines and drift reports SHALL be retained as Evidence under CMP-004.

### 5.11 `[SOX]` Program change for Financially Significant Systems

- **SEC-013.5.11.1** `[SOX]` Changes to Financially Significant Systems SHALL follow this policy and SHALL additionally meet the program change and configuration ITGCs, including Segregation of Duties between developers and production deployment, defined in CMP-009.
- **SEC-013.5.11.2** `[SOX]` The change record for a Financially Significant System SHALL capture the evidence attributes in CMP-009.5.5.3 so that each Change can be tested by the Internal Audit Director or External Auditor without additional records.

### 5.12 Capacity management

- **SEC-013.5.12.1** The CIO SHALL be accountable for capacity management, and the System Owner of each Recovery Tier 0, Tier 1 and Tier 2 Information System SHALL be responsible for it. The System Owner SHALL define capacity thresholds for the system's critical resources (for example compute, memory, storage, network bandwidth, licence counts and Cloud Service quotas). Unless the System Owner documents a different value, the threshold SHALL be the default in SEC-013.7.16.
- **SEC-013.5.12.2** Utilization of the resources in SEC-013.5.12.1 SHALL be monitored automatically, and a breach of a threshold SHALL generate an alert to the System Owner and the CIO. Alerts that indicate an imminent Availability impact SHALL also be forwarded to the SOC under SEC-012.
- **SEC-013.5.12.3** The System Owner SHALL produce a capacity forecast for each system in SEC-013.5.12.1 at the frequency in SEC-013.7.17, and before each major launch or other planned increase in demand, covering expected demand over at least the following 12 months, planned business changes and the Recovery Tier targets in RSK-004, and SHALL record the actions needed to keep utilization below the threshold.
- **SEC-013.5.12.4** Capacity increases and other actions arising from SEC-013.5.12.2 or SEC-013.5.12.3 SHALL be implemented as Changes under this Policy. Forecasts and threshold breaches SHALL be retained as Evidence under CMP-004.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CIO | Owns this policy; accountable for capacity management (section 5.12); establishes and chairs (or delegates the chair of) the CAB; publishes the change procedure and blackout calendar; reports Emergency Change metrics; reconciles unauthorized changes. |
| CTO | Ensures engineering pipelines and IaC enforce approved-artifact deployment; may authorize Emergency Changes. |
| CISO | May authorize Emergency Changes; oversees security impact of Changes; escalates unauthorized Changes. |
| Head of Security Engineering | Maintains Configuration Baselines and hardening; reviews High-rated Changes; operates drift and change-detection tooling. |
| CAB | Approves Normal Changes and Standard Change types; retrospectively approves Emergency Changes; reviews the Standard Change catalog. |
| System Owner | Requests or sponsors Changes; assesses risk; ensures testing and rollback; verifies outcomes; leads post-implementation reviews; remediates drift; sets capacity thresholds and produces capacity forecasts (section 5.12). |
| Business Continuity Manager | Reviews Changes to Recovery Tier 0 and Tier 1 systems for recovery impact. |
| SOC Manager | Investigates unauthorized Changes and drift alerts under SEC-012 and RES-002. |
| Head of GRC | `[SOX]` Confirms alignment with CMP-009; tests change Controls. |
| CFO | `[SOX]` Defines financial close blackout windows. |
| Workforce Member | Makes Changes only within an approved change record. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| SEC-013.7.1 | Change classes | Standard (pre-approved) · Normal (CAB approval) · Emergency (retrospective approval within 2 business days) |
| SEC-013.7.2 | Recording of an Emergency Change | Within 1 business day of implementation |
| SEC-013.7.3 | CAB meeting cadence | At least weekly |
| SEC-013.7.4 | Change approval validity | 30 days from approval |
| SEC-013.7.5 | Change outcome recorded | Within 2 business days of implementation |
| SEC-013.7.6 | Post-implementation review | Within 5 business days for Emergency, High-rated, failed or rolled-back, and incident-linked Changes |
| SEC-013.7.7 | Standard Change catalog review | Every 12 months |
| SEC-013.7.8 | Emergency Change review trigger | > 10% of a system's Changes in a month |
| SEC-013.7.9 | Configuration Baseline source | CIS Benchmark Level 1 (Level 2 for Restricted-data or internet-facing systems where compatible) |
| SEC-013.7.10 | Configuration Baseline review | Every 12 months, and within 90 days of a new CIS Benchmark major version |
| SEC-013.7.11 | Drift assessment frequency | Daily for Tier 0/Tier 1, `[PCI]` CDE and internet-facing systems; weekly for all others |
| SEC-013.7.12 | Drift remediation | Within 30 days; security-Control drift handled as a High alert under SEC-012 |
| SEC-013.7.13 | `[PCI]` Critical file comparison | At least weekly |
| SEC-013.7.14 | Unauthorized change reconciliation | Monthly |
| SEC-013.7.15 | Documentation update after Change | Within 10 business days |
| SEC-013.7.16 | Default capacity alert threshold | 80% sustained utilization of a critical resource (Tier 0 and Tier 1 systems; also the default for Tier 2) |
| SEC-013.7.17 | Capacity forecast | At least every 12 months, and before each major launch or planned increase in demand |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Production Changes with a complete, approved change record | 100% | Monthly | CIO |
| Emergency Changes retrospectively approved within 2 business days | 100% | Monthly | CIO |
| Emergency Changes as a share of all Changes | ≤ 5% | Monthly | CIO |
| Change success rate (not failed or rolled back) | ≥ 95% | Monthly | CIO |
| Unauthorized Changes detected | 0; each investigated | Monthly | CIO |
| System components compliant with Configuration Baseline | ≥ 95%; 100% for `[PCI]` CDE | Monthly | Head of Security Engineering |
| Drift findings remediated within 30 days | ≥ 95% | Monthly | Head of Security Engineering |
| Configuration Baselines reviewed within 12 months | 100% | Quarterly | Head of Security Engineering |
| Post-implementation reviews completed within 5 business days | 100% | Monthly | CIO |
| Tier 0–2 systems with a capacity forecast completed within 12 months | 100% | Quarterly | CIO |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following requirements SHALL NOT receive an Exception: SEC-013.5.1.4 (no production Change without an approved record or Emergency authorization), SEC-013.5.2.7 (retrospective approval of Emergency Changes), and `[SOX]` SEC-013.5.11.1. A deviation from a Configuration Baseline setting is approved under SEC-013.5.8.3 and does not require a separate Exception.

## 10. Enforcement

Non-compliance is handled under CMP-007.

An unauthorized Change to production SHALL be investigated as a potential Security Incident under RES-002. Repeated unauthorized Changes by the same team SHALL be reported to the ISSC.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| SEC-013.5.1 – 5.2 | 6.3; A.8.32, A.5.37 | ID.RA-07, PR.PS-01 | CM-3 | 4.1 | CC8.1 | BAI06.01, BAI06.02 | PCI DSS 6.5.1; SOX §404 |
| SEC-013.5.3 | A.8.32 | ID.RA-07 | CM-4, RA-3 | 4.1 | CC3.4, CC8.1 | BAI06.01 | PCI DSS 6.5.1; GDPR Art. 35 |
| SEC-013.5.4 | A.8.29, A.8.31, A.8.32 | PR.PS-06 | CM-4, SA-11 | 16.1 | CC8.1 | BAI07.05 | PCI DSS 6.5.1, 6.5.3 |
| SEC-013.5.5 – 5.6 | A.8.32, A.8.19 | ID.RA-07, PR.PS-01 | CM-3, CM-5 | 4.1 | CC8.1 | BAI06.01, BAI07.06 | PCI DSS 6.5.1; SOX §404 |
| SEC-013.5.7 | 10.2; A.8.32 | ID.IM-03 | CM-3, CM-4 | — | CC8.1 | BAI06.04 | PCI DSS 6.5.2 |
| SEC-013.5.8 | A.8.9 | PR.PS-01 | CM-2, CM-6, CM-7 | 4.1, 4.2 | CC7.1 | BAI10.02 | PCI DSS 2.2.1–2.2.7; HIPAA §164.308(a)(1)(ii)(B) |
| SEC-013.5.9 | A.8.9, A.8.16 | DE.CM-09, PR.PS-01 | CM-3, CM-6, SI-7 | 4.1 | CC7.1 | BAI10.05, DSS05.07 | PCI DSS 11.5.2, 11.6.1 |
| SEC-013.5.10 | A.5.9, A.5.37, A.8.9 | ID.AM-08 | CM-8, CM-9 | 1.1 | CC8.1 | BAI10.03 | PCI DSS 1.2.3, 1.2.4 |
| SEC-013.5.11 | A.8.32, A.5.3 | GV.OV-01 | CM-3, CM-5, AC-5 | — | CC8.1 | BAI06.01, MEA04 | SOX §§302, 404 |
| SEC-013.5.12 | A.8.6 | PR.IR-04 | CP-2(2), AU-4 | — | A1.1 | BAI04 | — |

## 12. Related documents

ISP-000, GOV-001, GOV-006, SEC-001, SEC-003, SEC-004, SEC-005, SEC-006, SEC-007, SEC-008, SEC-009, SEC-010, SEC-011, SEC-012, SEC-019, RSK-002, RSK-003, RSK-004, RES-002, RES-005, CMP-003, CMP-004, CMP-005, CMP-007, CMP-009, REF-001, REF-002

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CIO | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
