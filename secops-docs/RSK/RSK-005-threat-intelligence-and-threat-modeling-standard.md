# RSK-005 — Threat Intelligence & Threat Modeling Standard

## 1. Document control

| Field | Value |
|---|---|
| Document ID | RSK-005 |
| Title | Threat Intelligence & Threat Modeling Standard |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 2 — Standard |
| Classification | Internal |
| Owner | SOC Manager |
| Approver | Chief Information Security Officer (CISO) |
| Effective date | [DECISION REQUIRED: Date of CISO approval] |
| Next review date | Effective date + 12 months |
| Parent document | RSK-001 Risk Management Policy |
| Related documents | RSK-002, RSK-003, RSK-006, SEC-002, SEC-010, SEC-011, SEC-012, RES-002 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | SOC Manager | Initial release |

## 3. Purpose

This Standard sets the requirements for collecting, analyzing, handling, sharing and acting
on threat intelligence, and for threat modeling Information Systems. It ensures that
decisions on risk, detection, Vulnerability prioritization and secure design are informed
by current knowledge of the Threats the Organization faces, expressed in a common taxonomy
(MITRE ATT&CK) so that intelligence, detections and Threat Models can be compared.

## 4. Scope

- **People:** the SOC Manager and the SOC Manager's team, the Head of Security Engineering, System Owners, development and architecture teams, and any Workforce Member or Third Party that receives or shares threat intelligence on the Organization's behalf.
- **Systems:** all Information Systems in ISP-000 scope, including Cloud Services, AI Systems (RSK-006) and the `[PCI]` CDE.
- **Data:** threat intelligence received from external sources, intelligence derived from the Organization's own telemetry, and Threat Model artifacts.
- **Locations:** all locations.
- **Third parties:** intelligence providers, information sharing communities, and managed security service providers operating under contract.

## 5. Requirements

### 5.1 Intelligence requirements and threat profile

- **RSK-005.5.1.1** The SOC Manager SHALL maintain a set of documented priority intelligence requirements (PIRs) stating the questions intelligence must answer for the Organization, covering at minimum: threat actors and campaigns targeting the Organization's sector and regions; Vulnerabilities being exploited in technologies in the Asset Inventory (SEC-001); threats to Recovery Tier 0 and Tier 1 services (RSK-004); threats to vendor Tier 1 Third Parties (RSK-003); and threats to AI Systems (RSK-006).
- **RSK-005.5.1.2** The PIRs SHALL be reviewed and approved by the CISO at least every 12 months and within 30 days of a merger, acquisition, entry into a new sector or region, or a Sev-1 incident.
- **RSK-005.5.1.3** The SOC Manager SHALL maintain a threat profile listing the threat actor categories relevant to the Organization (for example financially motivated crime, ransomware operators, nation-state actors, hacktivists, insiders, and supply chain compromise), their motivations, observed capabilities, and the MITRE ATT&CK tactics and techniques they use.
- **RSK-005.5.1.4** The threat profile SHALL identify a prioritized list of MITRE ATT&CK (Enterprise, and where relevant Cloud and Mobile matrices) techniques that represent the most likely and most damaging attack paths against the Organization. The prioritized list SHALL be updated at least every 6 months.

### 5.2 Intelligence sources

- **RSK-005.5.2.1** The Organization SHALL collect intelligence from at least one source in each of the following categories:

| Category | Examples (non-binding) |
|---|---|
| Government and public advisories | CISA advisories and the KEV catalog; national CERT/CSIRT advisories in each region of operation; sector regulator alerts |
| Sector sharing communities | The Information Sharing and Analysis Center (ISAC) or Organization (ISAO) for the Organization's sector |
| Commercial or open intelligence feeds | Indicator feeds and finished intelligence reports from a commercial provider or reputable open-source feed |
| Vendor security advisories | Security bulletins from suppliers of software, hardware and Cloud Services in the Asset Inventory |
| Internal telemetry | Security Events, Security Incidents, phishing reports, and Post-Incident Reviews (RES-002) |
| Open-source and dark-web monitoring | Monitoring for leaked Organization credentials, data, domains and brand impersonation |

- **RSK-005.5.2.2** Each source SHALL be recorded in a source register with its owner, type, format, reliability rating, cost, and the PIRs it supports. The SOC Manager SHALL review each source's value against the PIRs at least every 12 months and SHALL retire sources that do not contribute to any PIR.
- **RSK-005.5.2.3** Each source and each item of intelligence SHALL be rated for reliability and credibility using the Admiralty system (source reliability A–F; information credibility 1–6) or an equivalent two-axis scale documented by the SOC Manager.
- **RSK-005.5.2.4** Paid intelligence providers SHALL be engaged under RSK-003.

### 5.3 Processing, analysis and action

- **RSK-005.5.3.1** Machine-readable indicators of compromise SHALL be ingested into the SIEM, EDR and other detection tools operated under SEC-012, de-duplicated, and assigned an expiry date. Indicators rated reliability A–B and credibility 1–2 SHALL be deployed to detection tools within 24 hours of receipt. Other indicators SHALL be deployed within 5 business days or discarded with a recorded reason.
- **RSK-005.5.3.2** Indicators SHALL expire from blocking controls no later than 90 days after deployment unless re-validated by a member of the SOC Manager's team.
- **RSK-005.5.3.3** Advisories and finished intelligence relevant to a PIR SHALL be triaged by a member of the SOC Manager's team within 1 business day of receipt.
- **RSK-005.5.3.4** Where intelligence indicates active exploitation of a Vulnerability in a technology present in the Asset Inventory, the SOC Manager SHALL notify the Head of Security Engineering within 4 hours of triage. The Vulnerability SHALL then be remediated under SEC-011.
- **RSK-005.5.3.5** Where intelligence indicates that the Organization or one of its vendor Tier 1 Third Parties is targeted or compromised, the SOC Manager SHALL open a Security Event for investigation under RES-002 within 1 hour of triage.
- **RSK-005.5.3.6** Where intelligence indicates a new or materially changed Threat to the Organization, the SOC Manager SHALL submit it to the Head of GRC for risk assessment under RSK-002 within 5 business days.
- **RSK-005.5.3.7** The SOC Manager SHALL conduct at least one intelligence-led threat hunt per quarter, each based on a hypothesis derived from the prioritized technique list (RSK-005.5.1.4) or current intelligence. Each hunt SHALL be documented with its hypothesis, data sources, ATT&CK techniques, findings, and resulting detection or Control improvements.

### 5.4 Handling and sharing

- **RSK-005.5.4.1** Intelligence SHALL be handled according to its Traffic Light Protocol (TLP) 2.0 marking (TLP:RED, TLP:AMBER+STRICT, TLP:AMBER, TLP:GREEN, TLP:CLEAR) and the terms of the source. Where no TLP marking is present, intelligence SHALL be treated as TLP:AMBER.
- **RSK-005.5.4.2** Intelligence SHALL also be classified under SEC-002. Intelligence marked TLP:RED or TLP:AMBER+STRICT, and intelligence identifying Organization Vulnerabilities, SHALL be classified at least Confidential.
- **RSK-005.5.4.3** The Organization SHALL share intelligence externally only through the sector community or government channels recorded in the source register, and only with the approval of the SOC Manager. Sharing that includes information about a Security Incident affecting the Organization SHALL also be approved by the CISO and the GC.
- **RSK-005.5.4.4** Shared intelligence SHALL NOT include Personal Data except where necessary to describe a Threat (for example a malicious email address), and SHALL NOT include Restricted data. `[GDPR]` Where Personal Data is shared, the CPO SHALL confirm the lawful basis before sharing.
- **RSK-005.5.4.5** The SOC Manager SHALL keep a record of all external sharing, including date, recipient community, TLP marking and approver.

### 5.5 Reporting

- **RSK-005.5.5.1** The SOC Manager SHALL produce a threat landscape report at least quarterly for the CISO and ISSC, summarizing relevant threat activity, changes to the threat profile, exploited Vulnerabilities affecting the Organization's technologies, intelligence-led hunt results, and ATT&CK detection coverage (section 5.7).
- **RSK-005.5.5.2** The SOC Manager SHALL provide the annual threat landscape summary to the Head of GRC as an input to the enterprise risk assessment under RSK-002.
- **RSK-005.5.5.3** Intelligence of a Threat assessed by the SOC Manager as likely to cause a Sev-1 or Sev-2 incident within 30 days SHALL be briefed to the CISO within 1 business day.

### 5.6 Threat modeling

- **RSK-005.5.6.1** A Threat Model SHALL be produced for each of the following before design approval or, for existing systems, within 12 months of the effective date of this Standard:

| Trigger | Threat Model required |
|---|---|
| New Information System or Cloud Service that stores, processes or transmits Restricted data | Yes |
| New Information System supporting a Recovery Tier 0 or Tier 1 process (RSK-004) | Yes |
| New internet-facing application, API or service | Yes |
| Significant Change as defined in RSK-002 to any system above, including changes to trust boundaries, authentication, data flows or hosting | Yes (update existing model) |
| New integration with a vendor Tier 1 Third Party (RSK-003) | Yes |
| AI System classified High or Limited under RSK-006 | Yes, including AI-specific threats |
| `[PCI]` Any new system component in or connected to the CDE | Yes |
| Other systems | SHOULD, at System Owner discretion |

- **RSK-005.5.6.2** Threat Models SHALL use STRIDE (Spoofing, Tampering, Repudiation, Information disclosure, Denial of service, Elevation of privilege) applied to each element and trust boundary of a data flow diagram. Where the system processes Personal Data, the Threat Model SHALL also apply LINDDUN (or an equivalent privacy threat method approved by the CPO). AI Systems SHALL also be assessed against AI-specific threats, using MITRE ATLAS or the OWASP Top 10 for Large Language Model Applications as a reference set.
- **RSK-005.5.6.3** Each Threat Model SHALL contain at minimum: system scope and assumptions; a data flow diagram showing processes, data stores, external entities, data flows and trust boundaries; Classification Levels of data in each flow (SEC-002); identified threats per element; the MITRE ATT&CK technique(s) each threat maps to where a mapping exists; existing and required mitigations; and residual threats.
- **RSK-005.5.6.4** Each Threat Model SHALL be produced by the System Owner's team with participation of at least one member of the Head of Security Engineering's team, and SHALL be reviewed and approved by the Head of Security Engineering or a delegate.
- **RSK-005.5.6.5** Mitigations identified by a Threat Model SHALL be recorded as security requirements in the system's work-tracking system and implemented under SEC-010 before production release. Mitigations not implemented before release SHALL be scored under RSK-002, and residual threats rated Medium or above SHALL be recorded in the Risk Register.
- **RSK-005.5.6.6** Threat Models SHALL be reviewed and updated at least every 12 months for Recovery Tier 0 systems, systems holding Restricted data, and High-class AI Systems, and on every Significant Change for all systems requiring a Threat Model.
- **RSK-005.5.6.7** Threat Models SHALL be stored in a repository accessible to the Head of Security Engineering, the SOC Manager and the System Owner, classified Confidential, and retained as Evidence under CMP-004.
- **RSK-005.5.6.8** The SOC Manager SHALL review each new or updated Threat Model for Recovery Tier 0 and Tier 1 systems and SHALL confirm that detections exist, or are planned, for the mapped ATT&CK techniques.

### 5.7 MITRE ATT&CK mapping and detection coverage

- **RSK-005.5.7.1** Every detection rule operated under SEC-012 SHALL be tagged with the MITRE ATT&CK technique(s) or sub-technique(s) it detects.
- **RSK-005.5.7.2** The SOC Manager SHALL maintain an ATT&CK coverage map showing, for each technique on the prioritized list (RSK-005.5.1.4), whether a detection exists, whether it has been validated, and the data sources it depends on.
- **RSK-005.5.7.3** At least 80% of the techniques on the prioritized list SHALL have a validated detection. Each prioritized technique without a validated detection SHALL be recorded as a gap with a planned detection date or a Risk Register entry.
- **RSK-005.5.7.4** Detections for prioritized techniques SHALL be validated at least every 12 months, and within 30 days of a material change to the underlying data source, by adversary emulation, atomic testing, purple-team exercise or replay of recorded attack data.
- **RSK-005.5.7.5** Security Incidents and Penetration Test findings SHALL be mapped to ATT&CK techniques in the incident record (RES-002) and Penetration Test report (SEC-011), and the SOC Manager SHALL update the coverage map within 30 days of incident closure or report receipt.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CISO | Approves this Standard and the PIRs; approves external sharing about Organization incidents; receives threat landscape reports and urgent briefings. |
| SOC Manager | Owns this Standard; maintains PIRs, source register, threat profile, prioritized technique list and ATT&CK coverage map; runs intelligence triage, hunts and reporting; approves external sharing. |
| Head of Security Engineering | Receives exploited-Vulnerability notifications; approves Threat Models; provides security participation in threat modeling. |
| System Owner | Commissions and maintains Threat Models for owned systems; ensures mitigations are implemented. |
| Head of GRC | Assesses new Threats under RSK-002; uses threat landscape in the enterprise risk assessment. |
| CPO | Approves privacy threat method alternatives; confirms lawful basis for sharing Personal Data. |
| GC | Approves external sharing about Organization incidents. |
| CTO | Ensures threat modeling is embedded in the design phase of SEC-010. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| RSK-005.7.1 | PIR review | Every 12 months; within 30 days of M&A, new sector/region, or Sev-1 |
| RSK-005.7.2 | Prioritized ATT&CK technique list update | Every 6 months |
| RSK-005.7.3 | Source categories | At least one source in each of 6 categories in 5.2.1 |
| RSK-005.7.4 | High-confidence indicator deployment | Within 24 hours (A–B / 1–2); others within 5 business days or discarded |
| RSK-005.7.5 | Indicator expiry | 90 days unless re-validated |
| RSK-005.7.6 | Advisory triage | 1 business day |
| RSK-005.7.7 | Actively exploited Vulnerability notification to Head of Security Engineering | 4 hours from triage |
| RSK-005.7.8 | Targeting/compromise intelligence to Security Event | 1 hour from triage |
| RSK-005.7.9 | New Threat submitted for risk assessment | 5 business days |
| RSK-005.7.10 | Intelligence-led threat hunts | At least 1 per quarter |
| RSK-005.7.11 | Default TLP when unmarked | TLP:AMBER |
| RSK-005.7.12 | Threat landscape report | Quarterly to CISO and ISSC |
| RSK-005.7.13 | Threat Model method | STRIDE; plus LINDDUN for Personal Data; plus MITRE ATLAS or OWASP LLM Top 10 for AI Systems |
| RSK-005.7.14 | Threat Model review | Every 12 months for Recovery Tier 0, Restricted-data and High-class AI systems; on every Significant Change |
| RSK-005.7.15 | Validated detection coverage of prioritized techniques | ≥ 80% |
| RSK-005.7.16 | Detection validation | Every 12 months and within 30 days of data source change |
| RSK-005.7.17 | Vulnerability remediation | As set in SEC-011 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Advisories triaged within 1 business day | ≥ 95% | Monthly | SOC Manager |
| High-confidence indicators deployed within 24 hours | ≥ 95% | Monthly | SOC Manager |
| Prioritized ATT&CK techniques with validated detection | ≥ 80% | Quarterly | SOC Manager |
| Intelligence-led hunts completed | ≥ 1 per quarter | Quarterly | SOC Manager |
| Systems requiring a Threat Model that have a current one | 100% | Quarterly | Head of Security Engineering |
| Threat-model mitigations open past production release without Risk Register entry | 0 | Quarterly | Head of Security Engineering |
| Sources contributing to at least one PIR | 100% | Annually | SOC Manager |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

No Exception SHALL be granted to the TLP handling rules in RSK-005.5.4.1 where the source's terms of use require them.

## 10. Enforcement

Non-compliance is handled under CMP-007.

Disclosure of intelligence in breach of its TLP marking or source terms SHALL be handled as a Security Incident under RES-002.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| RSK-005.5.1 – 5.2 | A.5.7, A.5.6 | ID.RA-02, ID.RA-03 | PM-16, RA-3 | — | CC3.2 | APO12.01 | — |
| RSK-005.5.3 | A.5.7, A.8.8, A.8.16 | ID.RA-02, DE.AE-02, DE.CM-01 | SI-4, SI-5, RA-10 | 7.1, 13.1 | CC7.1, CC7.2 | DSS05.07 | `[PCI]` 6.3.1 |
| RSK-005.5.4 | A.5.6, A.5.14 | ID.RA-02, RS.CO-03 | PM-15, SI-5 | — | CC2.3 | APO08 | `[GDPR]` Art. 6(1)(f) |
| RSK-005.5.5 | A.5.7, 9.3 | GV.OV-01, ID.RA-03 | PM-16 | — | CC2.2, CC3.2 | MEA01 | — |
| RSK-005.5.6 | A.5.8, A.8.25, A.8.27 | ID.RA-03, ID.RA-05, PR.PS-06 | SA-8, SA-11, SA-15, RA-3 | 16.10, 16.14 | CC3.2, CC8.1 | BAI03.02 | `[GDPR]` Art. 25; `[PCI]` 6.2.1 |
| RSK-005.5.7 | A.8.16 | DE.CM-01, DE.AE-02, ID.IM-02 | SI-4, CA-8, RA-10 | 8.11, 18.1 | CC7.2, CC4.1 | DSS05.07 | — |

## 12. Related documents

RSK-001, RSK-002, RSK-003, RSK-004, RSK-006, SEC-001, SEC-002, SEC-010, SEC-011, SEC-012, RES-002, CMP-003, CMP-004, CMP-007, REF-001

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: SOC Manager | | | |
| Approver: CISO | | | |
