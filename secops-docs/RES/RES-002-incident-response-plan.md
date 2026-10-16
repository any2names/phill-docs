# RES-002 — Incident Response Plan

## 1. Document control

| Field | Value |
|---|---|
| Document ID | RES-002 |
| Title | Incident Response Plan |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 3 — Plan |
| Classification | Internal |
| Owner | SOC Manager |
| Approver | Chief Information Security Officer (CISO) |
| Effective date | [DECISION REQUIRED: Date of CISO approval] |
| Next review date | Effective date + 12 months, and within 30 days after the closure of each Sev-1 Security Incident |
| Parent document | RES-001 Incident Response Policy |
| Related documents | RES-001, RES-003, RES-004, RES-005, SEC-012, SEC-013, CMP-004, RSK-002, RSK-003, RSK-006, TPL-006, TPL-007 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | SOC Manager | Initial release |

## 3. Purpose

This Plan sets out how the Organization responds to Security Incidents under RES-001. It is
the home of the Severity Level criteria, response time limits, Incident Response Team
roles, phase-by-phase procedure, escalation matrix, communications plan, playbook index,
Post-Incident Review requirement and exercise requirement. The procedure is aligned with
NIST SP 800-61 Rev. 3, which organizes incident response around the NIST CSF 2.0 Functions:
preparation is carried out under Govern, Identify and Protect; detection under Detect; and
response and recovery under Respond and Recover.

Breach determination and regulatory, customer and individual notification are in RES-003.
Recovery of Information Systems after a declared disaster is in RES-005. Crisis management
of business disruption is in RES-004.

## 4. Scope

- **People:** the SOC; Workforce Members assigned an Incident Response Team role; executives in the escalation matrix; System Owners, Asset Owners and Data Owners of affected systems and data; Third Parties providing incident response services or affected by an incident.
- **Systems:** all Information Systems, Cloud Services, Endpoints, networks and facilities in scope of RES-001, including the CDE `[PCI]`, systems holding ePHI `[HIPAA]` and Financially Significant Systems `[SOX]`.
- **Data:** all data at every Classification Level.
- **Locations:** all Organization locations, remote work locations and Third-Party facilities holding Organization data.
- **Third parties:** the external incident response retainer provider (RES-001 section 5.6), Cloud Service Providers, managed service providers and any Third Party whose systems or data are involved in an incident.
- **Trigger:** this Plan applies from the moment a Security Event is triaged under SEC-012 as a potential Security Incident, or a suspected Security Incident is reported under RES-001 section 5.2, until the incident is closed and its Post-Incident Review (where required) is complete.

## 5. Procedure

### 5.1 Use of this Plan

- **RES-002.5.1.1** The SOC SHALL open an incident record using TPL-006 for every Security Event declared a Security Incident, and SHALL assign an incident identifier in the form INC-YYYY-NNNN.
- **RES-002.5.1.2** Every incident SHALL be assigned an initial Severity Level under section 5.2 at declaration, and SHALL be re-assessed at each phase transition and whenever new facts become known.
- **RES-002.5.1.3** The response SHALL follow the phases in sections 5.5 to 5.10 and the applicable playbook in section 5.13. Where no playbook applies, the Incident Commander SHALL follow the phase procedure alone and record that no playbook applied.
- **RES-002.5.1.4** Deviations from this Plan during a live incident MAY be directed by the Incident Commander where following the Plan would increase harm. Each deviation SHALL be recorded in TPL-006 with the reason and reviewed in the Post-Incident Review.
- **RES-002.5.1.5** All times in incident records SHALL be recorded in UTC.

### 5.2 Severity classification

- **RES-002.5.2.1** The Organization uses four Severity Levels: **Sev-1 Critical · Sev-2 High · Sev-3 Medium · Sev-4 Low**.
- **RES-002.5.2.2** An incident SHALL be assigned the highest Severity Level for which it meets at least one criterion in the matrix below.
- **RES-002.5.2.3** Where facts are insufficient to choose between two levels, the higher level SHALL be assigned until facts support downgrading.
- **RES-002.5.2.4** Severity matrix:

| Level | Classification criteria (any one is sufficient) |
|---|---|
| **Sev-1 Critical** | (a) Confirmed or highly probable unauthorized access to, or exfiltration of, Restricted data relating to 500 or more individuals, or of any Secret granting administrative access to production. (b) Ransomware or destructive Malware executing on more than one system, or on any system assigned Recovery Tier 0 under RSK-004. (c) A Tier 0 system unavailable, or a Tier 1 system unavailable and projected to exceed its RTO in RSK-004, because of a Security Incident. (d) Confirmed attacker control of an Identity Provider, directory, cloud organization or tenant-level administrative account, or of a Privileged Account with domain-wide rights. (e) `[PCI]` Confirmed or suspected compromise of CHD or SAD, or of any CDE system component. (f) `[SOX]` Confirmed unauthorized modification of data in a Financially Significant System, or any incident the CISO or GC considers potentially a Material Cybersecurity Incident. (g) Fraudulent transfer of funds at or above [DECISION REQUIRED: Sev-1 financial loss threshold. Recommended default: USD 250,000 or equivalent]. (h) A threat to the life or physical safety of any person. (i) Active, ongoing attacker presence with lateral movement across more than one network segment or cloud account. |
| **Sev-2 High** | (a) Confirmed unauthorized access to Restricted data relating to fewer than 500 individuals, or to Confidential data in any quantity. (b) Compromise of a single Privileged Account below tenant or domain level, or of 5 or more User accounts in one campaign. (c) Malware with confirmed command-and-control activity on any server, or on 2 or more Endpoints. (d) A Tier 1 system unavailable within its RTO, or a Tier 2 system unavailable, because of a Security Incident; or a DDoS attack degrading an external customer-facing service. (e) Business Email Compromise in which a mailbox was controlled by an attacker, or a fraudulent transfer of funds below the Sev-1 threshold. (f) Loss or theft of an Endpoint or Media holding Restricted data where Encryption under SEC-006 cannot be verified. (g) A confirmed Security Incident at a Third Party involving Organization Confidential or Restricted data. (h) Suspected deliberate exfiltration of Confidential or Restricted data by a Workforce Member. (i) Misuse of an AI System that disclosed Confidential or Restricted data outside the Organization. |
| **Sev-3 Medium** | (a) Compromise of a single standard User account with no evidence of access to Confidential or Restricted data. (b) Malware on a single Endpoint, contained by automated controls, with no command-and-control or lateral movement. (c) Unauthorized disclosure of Personal Data relating to fewer than 10 individuals to a known recipient who confirms deletion (e.g. misdirected email). (d) Degradation or unavailability of a Tier 2 or Tier 3 system within its RTO because of a Security Incident. (e) A violation of a suite document resulting in exposure of Internal or Confidential data to unauthorized internal persons only. (f) Use of an unapproved AI System or Shadow IT with Confidential data and no confirmed external disclosure. (g) A successful phishing interaction (credential entry or attachment opened) stopped before any account or system compromise. |
| **Sev-4 Low** | (a) Loss or theft of an Endpoint or Mobile Device with Encryption verified under SEC-006 and no indication of access. (b) A violation of a suite document with no data exposure (e.g. unapproved software, sharing of a non-privileged password with no misuse). (c) An unsuccessful but targeted attack attempt requiring follow-up action (e.g. blocked targeted spear-phishing, blocked exploitation attempt against a patched system). (d) Any other Security Incident not meeting Sev-1 to Sev-3 criteria. |

- **RES-002.5.2.5** The Incident Commander SHALL raise the Severity Level by one level where any of the following apply and the incident is not already Sev-1: the data involved includes PHI `[HIPAA]`, CHD `[PCI]` or Sensitive Personal Information; the incident has become publicly known or attracted media or regulator enquiry; or the attacker is assessed as still active after containment was reported complete.
- **RES-002.5.2.6** Only the Incident Commander SHALL change a Severity Level. A downgrade from Sev-1 or Sev-2 SHALL be approved by the CISO. Each change SHALL be recorded in TPL-006 with the criterion relied on.
- **RES-002.5.2.7** Severity Level determines operational response only. Whether an incident is a Personal Data Breach, a Breach under 45 CFR §164.402 `[HIPAA]`, or a Material Cybersecurity Incident `[SOX]` is determined separately under RES-003.

### 5.3 Response time limits

- **RES-002.5.3.1** The Incident Commander and SOC Manager SHALL meet the following time limits, measured from the time the incident is declared:

| Level | Incident Commander assigned | CISO notified | Executive notification | Status updates | Target closure |
|---|---|---|---|---|---|
| Sev-1 | Within 15 min | Within 30 min | Within 1 h | Hourly | — (managed by Incident Commander and CISO) |
| Sev-2 | Within 1 h | Within 2 h | At CISO's discretion | Every 4 h | — (managed by Incident Commander) |
| Sev-3 | Within 1 business day | In the weekly SOC report | Not required | Every business day | 10 business days |
| Sev-4 | Within 5 business days | In the monthly SOC report | Not required | At closure | 20 business days |

- **RES-002.5.3.2** Executive notification for Sev-1 SHALL be made to the CEO, CIO, GC, CPO and CFO by the CISO or, if the CISO cannot be reached within 30 minutes, by the SOC Manager.
- **RES-002.5.3.3** For Sev-3 and Sev-4, the Incident Commander SLA is met when a named responder has accepted the incident and begun analysis.
- **RES-002.5.3.4** Status update cadence applies until the Incident Commander declares containment complete; thereafter updates for Sev-1 and Sev-2 SHALL be issued at least every business day until closure.
- **RES-002.5.3.5** Upgrading an incident restarts the time limits of the new Severity Level from the time of upgrade.
- **RES-002.5.3.6** The internal escalation to the GC and CPO for a suspected Personal Data Breach, and all external notification deadlines, are set in RES-003 and run in parallel with this Plan.

### 5.4 Incident Response Team roles

- **RES-002.5.4.1** The Incident Commander SHALL assign, and record in TPL-006, the following roles. One person MAY hold more than one role for Sev-3 and Sev-4 incidents; for Sev-1 the Incident Commander, Scribe and Communications Lead SHALL be different persons.

| IR role | Assigned from | Responsibilities |
|---|---|---|
| Incident Commander | SOC Manager or a trained on-call Incident Commander under RES-001.5.1.7; for Sev-1, a senior Incident Commander designated by the CISO | Owns the incident end to end; exercises the authority in RES-001 section 5.3; assigns roles; sets objectives for each operational period; approves containment, eradication and recovery actions; decides Severity Level; issues status updates; declares closure. |
| Scribe | Workforce Member designated by the SOC Manager or the Head of GRC | Maintains the TPL-006 record, the timeline, decision log, action tracker and evidence register in real time; records attendees of each call; keeps the record suitable for legal review. Required for Sev-1 and Sev-2. |
| Communications Lead | For Sev-1: the corporate communications function [ASSUMPTION: the Organization has a corporate communications function]; otherwise a person designated by the CISO | Drafts and issues internal updates; prepares external holding statements, customer communications and media responses for approval under section 5.12; keeps the stakeholder notification log. |
| Legal Lead | GC or a lawyer designated by the GC | Advises on privilege, Legal Hold, law enforcement contact, contractual obligations and regulatory exposure; coordinates with the CPO on RES-003; approves all external wording. Required for Sev-1, Sev-2 and any incident involving Personal Data. |
| Technical Lead(s) | Security engineers, System Owners' engineers, cloud, identity, network, endpoint and application specialists, or the external retainer provider | Perform analysis, scoping, containment, eradication and recovery actions in their domain as directed by the Incident Commander; collect evidence under RES-001 section 5.4; report findings at each update. |
| Privacy Lead | CPO, DPO or HIPAA Privacy Officer `[HIPAA]`, as applicable | Joins whenever Personal Data, PHI or Sensitive Personal Information may be involved; runs breach determination under RES-003. |
| Business Liaison | System Owner or Asset Owner of the affected service | Assesses business impact; approves business-affecting actions where RES-001 requires; coordinates workarounds under RES-004. |
| HR Liaison | Delegate of the CHRO | Joins for Insider Threat and any incident involving investigation of a Workforce Member. |
| Executive Sponsor | CISO | For Sev-1 and Sev-2: provides resources, escalates to the executives and the Crisis Management Team, approves downgrades and decisions in RES-001 section 5.3. |

- **RES-002.5.4.2** The SOC Manager SHALL maintain a role roster naming at least two trained persons for each of the Incident Commander, Scribe, Communications Lead and Legal Lead roles, with contact details verified every 6 months.
- **RES-002.5.4.3** Hand-over of the Incident Commander role SHALL be made by a recorded verbal briefing, and the TPL-006 record SHALL show the time of hand-over and the incoming Incident Commander's acceptance. For Sev-1 incidents lasting more than 12 hours, the CISO SHALL ensure Incident Commander shifts do not exceed 12 hours.

### 5.5 Phase 1 — Preparation

Preparation is carried out continuously under the CSF 2.0 Govern, Identify and Protect Functions.

1. **RES-002.5.5.1** The SOC Manager SHALL maintain the on-call rota, the role roster (RES-002.5.4.2), and the contact directory of executives, System Owners, key Third Parties, the retainer provider, law enforcement contacts (RES-001.5.5.3) and regulators (RES-003).
2. **RES-002.5.5.2** The SOC Manager SHALL maintain an out-of-band communication capability independent of the Organization's primary Identity Provider, email and collaboration platforms (e.g. a separately hosted messaging workspace and a conference bridge with dial-in), tested every 6 months.
3. **RES-002.5.5.3** The SOC Manager SHALL maintain a responder toolkit, including forensic acquisition tools, write blockers, evidence storage, clean administrative workstations and pre-provisioned Break-glass Account procedures under SEC-005, verified every 6 months.
4. **RES-002.5.5.4** The SOC Manager SHALL ensure that Detection Use Cases under SEC-012 map to each playbook in section 5.13, and SHALL review the mapping every 12 months.
5. **RES-002.5.5.5** The SOC Manager SHALL maintain pre-approved holding statements and notification templates with the Communications Lead and Legal Lead, reviewed every 12 months, and SHALL coordinate the notification content templates in RES-003.
6. **RES-002.5.5.6** The SOC Manager SHALL ensure that every person on the role roster completes the role-based training required by PPL-002.
7. **RES-002.5.5.7** The SOC Manager SHALL confirm every 12 months that the Asset Inventory under SEC-001 identifies, for each Tier 0 and Tier 1 system, its System Owner, Recovery Tier and Classification Level, so that responders can scope incidents.

### 5.6 Phase 2 — Detection and analysis

1. **RES-002.5.6.1** **Intake.** A Security Event reaches the SOC by an alert under SEC-012, a report through the security reporting channel under RES-001 section 5.2, a Third-Party notice, a threat intelligence notice under RSK-005, or a VDP report under SEC-011. The SOC SHALL triage it within the alert triage SLA in SEC-012.
2. **RES-002.5.6.2** **Declaration.** If the Security Event meets any Severity Level criterion in section 5.2, the SOC SHALL declare a Security Incident, open TPL-006, assign the initial Severity Level and page the on-call Incident Commander. Events that do not meet any criterion SHALL be closed as Security Events with the reason recorded under SEC-012.
3. **RES-002.5.6.3** **Mobilization.** The Incident Commander SHALL accept the incident within the time limit in section 5.3, assign roles under section 5.4, and for Sev-1 and Sev-2 open an incident bridge on the out-of-band channel where compromise of primary collaboration tools cannot be ruled out.
4. **RES-002.5.6.4** **Initial assessment.** Within 1 hour of acceptance for Sev-1 and 4 hours for Sev-2, the Incident Commander SHALL record: what is known; affected systems, accounts and data; Classification Level of affected data; whether Personal Data, PHI `[HIPAA]`, CHD `[PCI]` or Financially Significant Systems `[SOX]` may be involved; whether the attacker may still be active; and the applicable playbook.
5. **RES-002.5.6.5** **Legal and privacy trigger.** Where Personal Data may be involved, the Incident Commander SHALL notify the GC and CPO within the time set in RES-003 and add the Privacy Lead to the team.
6. **RES-002.5.6.6** **Scoping.** Technical Leads SHALL identify the initial access vector, affected identities, systems and data, the time of first malicious activity, and indicators of compromise; and SHALL search all in-scope systems for those indicators using SIEM, EDR and cloud audit logs.
7. **RES-002.5.6.7** **Evidence.** Technical Leads SHALL collect and preserve evidence under RES-001 section 5.4 before any action that would alter it, unless the Incident Commander decides otherwise under RES-001.5.4.1.
8. **RES-002.5.6.8** **External support.** The Incident Commander SHALL engage the retainer provider for Sev-1 incidents under RES-001.5.6.6.
9. **RES-002.5.6.9** **Third-Party involvement.** Where a Third Party's service is the source or route of the incident, the Incident Commander SHALL notify the Third Party's designated security contact and request its incident details under the contract terms in RSK-003.
10. **RES-002.5.6.10** **Re-assessment.** The Incident Commander SHALL re-assess the Severity Level under section 5.2 at the end of the initial assessment and at each status update.

### 5.7 Phase 3 — Containment

1. **RES-002.5.7.1** The Incident Commander SHALL set a containment strategy within 2 hours of acceptance for Sev-1 and 8 hours for Sev-2, choosing short-term containment (stop the immediate harm) and long-term containment (hold the environment safely while eradication is prepared), and recording the decision and its business impact.
2. **RES-002.5.7.2** Containment actions MAY include any action in RES-001.5.3.3. Actions affecting Tier 0 or Tier 1 systems SHALL follow RES-001.5.3.4.
3. **RES-002.5.7.3** Where an attacker may be monitoring the Organization's response, the Incident Commander SHALL decide whether to delay visible containment actions until they can be executed together, and SHALL record the decision.
4. **RES-002.5.7.4** Credentials of every account confirmed or suspected compromised SHALL be reset or disabled and their sessions and tokens revoked. Where a Privileged Account, Identity Provider or Secrets store is compromised, Secrets accessible to it SHALL be rotated under SEC-006.
5. **RES-002.5.7.5** Containment actions on production SHALL be logged as Emergency Changes under SEC-013.
6. **RES-002.5.7.6** The Incident Commander SHALL declare containment complete only when no new malicious activity has been observed for at least 24 hours for Sev-1 and Sev-2 incidents, with monitoring for the indicators of compromise in place, and SHALL record the declaration in TPL-006.

### 5.8 Phase 4 — Eradication

1. **RES-002.5.8.1** Technical Leads SHALL remove every identified attacker artifact, persistence mechanism, unauthorized account, Malware and malicious configuration from affected systems.
2. **RES-002.5.8.2** Systems on which an attacker obtained administrative control SHALL be rebuilt from a trusted Configuration Baseline under SEC-013 or a known-good image, rather than cleaned in place, unless the Incident Commander and the CISO record a reason to clean in place.
3. **RES-002.5.8.3** The Vulnerability or control weakness exploited for initial access SHALL be remediated or mitigated before affected systems are reconnected. Remediation of related Vulnerabilities on other systems SHALL follow the remediation SLA in SEC-011.
4. **RES-002.5.8.4** Technical Leads SHALL re-scan all in-scope systems for the indicators of compromise after eradication and record the result.

### 5.9 Phase 5 — Recovery

1. **RES-002.5.9.1** The Incident Commander and the System Owner SHALL jointly approve the restoration of each affected system to production, after confirming eradication for that system.
2. **RES-002.5.9.2** Where restoration from Backup is needed, it SHALL use Backups taken before the earliest known malicious activity and verified free of indicators of compromise, under SEC-018.
3. **RES-002.5.9.3** Where restoration within the RTO in RSK-004 is not achievable in the primary environment, the Incident Commander SHALL notify the CIO, who SHALL consider a Disaster Declaration under RES-005. Ransomware and destructive-attack recovery SHALL follow RES-005 once the Incident Commander confirms containment.
4. **RES-002.5.9.4** Restored systems SHALL be placed under enhanced monitoring for the incident's indicators of compromise for at least 30 days for Sev-1 and Sev-2 incidents.
5. **RES-002.5.9.5** The Business Liaison SHALL confirm that the restored service is operating normally and that data Integrity has been validated, before the Incident Commander closes recovery.

### 5.10 Phase 6 — Post-incident activity and closure

1. **RES-002.5.10.1** The Incident Commander SHALL close an incident only when: containment, eradication and recovery are complete; the breach determination under RES-003 is recorded or marked not applicable; all notifications required by RES-003 are made or have a recorded decision not to notify; evidence is stored under RES-001 section 5.4; and the TPL-006 record is complete.
2. **RES-002.5.10.2** Closure of Sev-1 and Sev-2 incidents SHALL be approved by the CISO.
3. **RES-002.5.10.3** A Post-Incident Review SHALL be conducted for every Sev-1 and Sev-2 incident and completed within 10 business days of closure, using TPL-007.
4. **RES-002.5.10.4** A Post-Incident Review SHALL also be conducted where 3 or more Sev-3 incidents with the same Root Cause occur within 90 days, and MAY be required by the SOC Manager or CISO for any other incident.
5. **RES-002.5.10.5** The review SHALL be blameless: it SHALL identify causes in systems, processes and conditions, and SHALL NOT be used as evidence in disciplinary proceedings. Individual misconduct identified during a review SHALL be referred separately to the CHRO under CMP-007.
6. **RES-002.5.10.6** The review SHALL be facilitated by a person who was not the Incident Commander for the incident.
7. **RES-002.5.10.7** Corrective actions SHALL each have an owner and a due date, be tracked by the SOC Manager, and, where they address a Risk, be entered in the Risk Register and treated within the deadlines in RSK-002.
8. **RES-002.5.10.8** Where the Root Cause relates to a suite document, the CISO SHALL start an event-triggered review of that document under GOV-002, and SHALL update this Plan or its playbooks within 30 days of the review's completion where the review finds a gap in them.
9. **RES-002.5.10.9** `[PCI]` Lessons learned that affect the CDE SHALL be incorporated into this Plan and SEC-019 as required by PCI DSS 12.10.6.

### 5.11 Escalation matrix

- **RES-002.5.11.1** Escalation SHALL follow the matrix below. Each notification SHALL be recorded in TPL-006 with time and recipient.

| Recipient | Sev-1 | Sev-2 | Sev-3 | Sev-4 | Notified by |
|---|---|---|---|---|---|
| On-call Incident Commander | Immediately on declaration | Immediately on declaration | Next business day | Within 5 business days | SOC |
| SOC Manager | Within 15 min | Within 1 h | Weekly SOC report | Monthly SOC report | Incident Commander |
| CISO | Within 30 min | Within 2 h | Weekly SOC report | Monthly SOC report | Incident Commander or SOC Manager |
| CEO, CIO, GC, CPO, CFO | Within 1 h | Where the CISO decides | — | — | CISO |
| GC and CPO (Personal Data suspected) | Per RES-003 | Per RES-003 | Per RES-003 | Per RES-003 | Incident Commander |
| HIPAA Security Officer `[HIPAA]` | Within 1 h where ePHI may be involved | Within 4 h where ePHI may be involved | Weekly SOC report | Monthly SOC report | Incident Commander |
| CTO | Within 1 h where products or production platforms are affected | Within 4 h where products or production platforms are affected | — | — | CISO |
| CHRO | Within 4 h where a Workforce Member is suspected | Within 1 business day where a Workforce Member is suspected | — | — | CISO |
| Crisis Management Team | When the activation criteria in RES-004 are met | When the activation criteria in RES-004 are met | — | — | CISO |
| Audit Committee Chair | Within 24 h | Where the CISO and GC decide | — | — | CISO |
| ISSC | Extraordinary meeting under GOV-001.5.3.5 | Next scheduled meeting | Monthly metrics (GOV-003) | Monthly metrics (GOV-003) | CISO |
| Board of Directors | Via the Audit Committee, at the GC's and CEO's discretion | — | — | — | CEO |

- **RES-002.5.11.2** If a recipient cannot be reached within the time limit, the notifier SHALL contact the recipient's designated alternate and record both attempts.
- **RES-002.5.11.3** Any responder MAY escalate directly to the CISO if they believe an incident is under-classified or the response is stalled. The CISO SHALL respond within 1 hour for any escalation received outside the escalation matrix.

### 5.12 Communications plan

#### Internal communications

1. **RES-002.5.12.1** Status updates SHALL follow a standard format: incident ID; Severity Level; current phase; what is known; what is being done; decisions needed; next update time. The Communications Lead SHALL issue them at the cadence in section 5.3 to the distribution list set by the Incident Commander.
2. **RES-002.5.12.2** Incident communications SHALL be marked Confidential or Restricted under RES-001.5.9.1 and, where directed by the Legal Lead, marked as prepared at the direction of counsel.
3. **RES-002.5.12.3** Where compromise of the Identity Provider, email or collaboration platforms cannot be ruled out, all incident communications SHALL use the out-of-band channel in RES-002.5.5.2.
4. **RES-002.5.12.4** Workforce-wide notices (e.g. instructions to reset passwords or not to open a specific message) SHALL be approved by the Incident Commander and the Legal Lead before issue.

#### External communications

5. **RES-002.5.12.5** No external communication about an incident SHALL be issued unless approved as set out in the stakeholder notification matrix below. Regulatory, individual, payment brand, customer-contractual and public-disclosure notifications SHALL be decided and made under RES-003.
6. **RES-002.5.12.6** Media enquiries SHALL be referred to the Communications Lead. Only the CEO or a spokesperson the CEO designates SHALL speak to media about a Sev-1 incident.
7. **RES-002.5.12.7** Holding statements SHALL be prepared within 4 hours of a Sev-1 declaration, approved by the Legal Lead and the CISO, and held ready for release if the incident becomes public.
8. **RES-002.5.12.8** Communications SHALL state facts known at the time, SHALL NOT speculate on cause, attribution or impact, and SHALL be consistent across all audiences.

#### Stakeholder notification matrix

- **RES-002.5.12.9** External stakeholders SHALL be notified according to the following matrix:

| Stakeholder | Trigger | Timing | Prepared by | Approved by |
|---|---|---|---|---|
| Supervisory authorities, regulators, HHS `[HIPAA]`, state attorneys general | Per RES-003 determination | Per RES-003 | Privacy Lead | As set in RES-003 |
| Affected individuals | Per RES-003 determination | Per RES-003 | Privacy Lead with Communications Lead | As set in RES-003 |
| Acquirer and payment brands `[PCI]` | Suspected or confirmed CHD compromise | Per RES-003 | Legal Lead | As set in RES-003 |
| SEC / investors `[SOX]` | Material Cybersecurity Incident determination | Per RES-003 | Legal Lead with CFO | As set in RES-003 |
| Customers (contractual) | Incident affecting customer data or services, per contract | Per RES-003 | Communications Lead with Legal Lead | As set in RES-003 |
| Customers (service status) | Customer-facing service degraded by an incident, with no data impact | At least every 4 h while degraded | Communications Lead with Business Liaison | Incident Commander and CISO |
| Cyber insurer | Incident that may give rise to a claim | Per RES-003 | CFO | CFO |
| Law enforcement | Per GC decision under RES-001 section 5.5 | Per RES-001 | Legal Lead | GC |
| Affected Third Parties (source or route of the incident) | Incident involves the Third Party's service | Within 24 h of identifying involvement | Incident Commander | CISO |
| Media | Media enquiry, or incident becomes public | On enquiry, using approved holding statement | Communications Lead | CEO (Sev-1); CISO and Legal Lead (Sev-2) |
| Information-sharing organizations | Indicators of compromise useful to peers | After containment | Technical Lead | CISO (RES-001.5.5.7) |

### 5.13 Playbook index

- **RES-002.5.13.1** The SOC Manager SHALL maintain each playbook below as a controlled annex to this Plan in the incident response knowledge base. Each playbook SHALL contain at minimum: triggers and detection sources; default initial Severity Level; required IR roles; step-by-step actions for each phase; containment decision points and authority; evidence to collect; notification considerations by reference to RES-003; recovery hand-off criteria; and closure criteria.
- **RES-002.5.13.2** Each playbook SHALL be reviewed every 12 months and within 30 days after any Sev-1 or Sev-2 incident in which it was used.

| ID | Playbook | Typical triggers | Default Severity | Lead Technical Lead | Key actions beyond the phase procedure | Related documents |
|---|---|---|---|---|---|---|
| PB-01 | Ransomware | EDR ransomware detection; mass file encryption; ransom note; backup deletion attempts | Sev-1 | Endpoint and infrastructure | Isolate affected hosts and segments; disable compromised accounts; protect and verify isolated Backups; identify exfiltration (double extortion); no contact with the threat actor except under RES-001 section 5.7; recover under RES-005 | RES-001, RES-003, RES-005, SEC-018 |
| PB-02 | Business Email Compromise | Mailbox rule creation; anomalous mailbox login; payment-redirection request; customer report of fraudulent invoice | Sev-2 | Identity and email | Revoke sessions and reset credentials; remove malicious rules and OAuth grants; review sent items and mailbox access logs for data exposure; CFO to contact the bank for transfer recall within 1 h of discovery of a fraudulent transfer; notify counterparties | SEC-004, SEC-014, RES-003 |
| PB-03 | Credential compromise | Impossible travel; MFA fatigue; credential found in breach dump or on paste site; password spray success | Sev-3 (Sev-2 if privileged) | Identity | Disable or reset account; revoke tokens; review MFA enrollments; review access during compromise window; hunt for related accounts | SEC-003, SEC-004, SEC-005 |
| PB-04 | Data exfiltration | DLP alert; anomalous egress volume; data on leak site; extortion message; misdirected disclosure of Personal Data, including a DSR response sent to the wrong recipient (CMP-010) | Sev-1 or Sev-2 per section 5.2 | Network and data | Block egress channel; identify data sets and record counts; preserve egress logs; engage Privacy Lead early for RES-003 determination; monitor leak sites | SEC-002, SEC-007, RES-003 |
| PB-05 | Insider Threat | User behavior analytics alert; HR referral; bulk download before Separation; whistleblower report | Sev-2 | Security operations with HR Liaison | Restrict investigation to Need to Know; obtain GC and CHRO authorization under RES-001.5.4.10; preserve evidence covertly where authorized; coordinate access revocation with Separation under SEC-003 and PPL-001 | PPL-001, CMP-006, CMP-007 |
| PB-06 | Distributed denial of service | Traffic spike; provider DDoS alert; service degradation; extortion demand | Sev-2 (Sev-1 if Tier 0 unavailable) | Network | Engage DDoS mitigation provider and ISP; apply rate-limiting and geo-blocking; check for a concurrent intrusion used as a distraction; customer service status updates under section 5.12 | SEC-007, RES-005 |
| PB-07 | Cloud account compromise | Root or tenant admin login anomaly; new IAM users or keys; resource creation in unused regions; cryptomining; logging disabled | Sev-1 if tenant-level, otherwise Sev-2 | Cloud | Revoke keys and sessions; lock root/tenant admin using Break-glass Account procedures; preserve cloud audit logs; review and revert IAM changes; check for data snapshots shared externally; engage Cloud Service Provider support | SEC-005, SEC-009, SEC-012 |
| PB-08 | `[PCI]` Card data compromise | CDE intrusion; skimming code on Payment Page; acquirer or brand common-point-of-purchase notice; stored PAN found outside expected locations (SEC-019.5.5.4); POI Device tampering or substitution (SEC-019.5.9.6) | Sev-1 | CDE and application | Do not power off or rebuild CDE systems until evidence is preserved; isolate affected components; engage PFI under RES-001.5.6.7; notify acquirer and brands under RES-003; for unexpected stored PAN, locate, securely delete or migrate into the CDE and determine how it got there (PCI DSS 12.10.7) | SEC-019, RES-001, RES-003 |
| PB-09 | Lost or stolen device | Workforce Member report; asset not checked in; theft report | Sev-4 if Encryption verified, otherwise Sev-2 | Endpoint | Verify Encryption status from management console; remote lock and wipe under SEC-008; revoke device certificates and tokens; reset credentials stored on device; police report for theft where the GC requires | SEC-008, SEC-017, RES-003 |
| PB-10 | Third-party breach | Third Party notice; public disclosure of a vendor breach; threat intelligence | Sev-2 (Sev-1 if criteria met) | Third-party risk with Technical Lead | Determine Organization data and connections involved; suspend or restrict integrations and rotate shared Secrets; request incident details under contract; assess as Controller or Covered Entity notification duty under RES-003; reassess vendor under RSK-003 | RSK-003, RES-003 |
| PB-11 | AI System misuse | Prompt injection or jailbreak of an Organization AI System; Confidential data submitted to unapproved Generative AI; model output causing harm; model or training data tampering; AI agent acting outside authorization | Sev-3 (Sev-2 if Confidential or Restricted data disclosed externally) | Application and AI engineering | Suspend the affected AI System, agent credentials or integration; preserve prompts, outputs and logs; request deletion from the AI provider under contract; assess data exposure for RES-003; review guardrails with the AI System owner under RSK-006 | RSK-006, GOV-004, RES-003 |

- **RES-002.5.13.3** Incidents that do not fit a playbook (e.g. non-ransomware Malware, unauthorized physical access, web application compromise) SHALL be handled under the phase procedure in sections 5.5 to 5.10. Where the same incident type occurs 3 or more times in 12 months without a playbook, the SOC Manager SHALL create one within 90 days.

### 5.14 Testing and exercises

1. **RES-002.5.14.1** This Plan SHALL be tested by a tabletop or functional exercise every 12 months.
2. **RES-002.5.14.2** The SOC Manager SHALL plan the annual exercise so that, over each 24-month period, the exercises cover at least PB-01, PB-04 and PB-07, and `[PCI]` PB-08. A real Sev-1 incident handled under this Plan MAY substitute for the annual exercise where the CISO records that it exercised the Plan's escalation and communications sections.
3. **RES-002.5.14.3** Exercises SHALL include the Incident Commander, Scribe, Communications Lead, Legal Lead and Privacy Lead roles, and at least one executive in the Sev-1 executive notification list.
4. **RES-002.5.14.4** Each exercise SHALL produce a report within 30 days, recording objectives, participants, observations, gaps and corrective actions with owners and due dates. Corrective actions SHALL be tracked under RES-002.5.10.7.
5. **RES-002.5.14.5** The annual exercise MAY be combined with the destructive-attack DR tabletop required under RES-005, provided the objectives of both are recorded and met.
6. **RES-002.5.14.6** The SOC Manager SHALL test the out-of-band channel and the role roster contact details every 6 months, by a call-out test with recorded response times.

### 5.15 Plan maintenance

1. **RES-002.5.15.1** The SOC Manager SHALL review this Plan every 12 months, and within 30 days after the closure of each Sev-1 incident, and SHALL submit changes to the CISO for approval.
2. **RES-002.5.15.2** The SOC Manager SHALL update this Plan within 30 days of a change in IR role holders' functions, the retainer provider, the out-of-band channel, or a notification obligation in RES-003.
3. **RES-002.5.15.3** The current approved version of this Plan and its playbooks SHALL be available offline to every person on the role roster (e.g. printed copy or encrypted offline copy), refreshed within 10 business days of each approved change.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| SOC Manager | Owns this Plan and playbooks; maintains the on-call rota, role roster, out-of-band channel and toolkit; ensures time limits are met; tracks corrective actions; runs exercises. |
| CISO | Approves this Plan; Executive Sponsor for Sev-1 and Sev-2; makes executive notifications; approves downgrades from Sev-1/Sev-2 and closure of Sev-1/Sev-2; escalates to the Crisis Management Team, Audit Committee Chair and ISSC. |
| Incident Commander (IR role) | Leads each incident under section 5.4 and RES-001 section 5.3. |
| Scribe, Communications Lead, Legal Lead, Technical Lead, Privacy Lead, Business Liaison, HR Liaison (IR roles) | As set out in section 5.4. |
| GC | Provides or designates the Legal Lead; approves external wording; decides Legal Hold and law enforcement contact under RES-001. |
| CPO | Provides or designates the Privacy Lead; owns breach determination under RES-003. |
| CEO | Receives Sev-1 executive notification; designates the media spokesperson; chairs the Crisis Management Team under RES-004. |
| CIO | Receives Sev-1 executive notification; decides on Disaster Declaration under RES-005. |
| CFO | Receives Sev-1 executive notification; leads bank recall for fraudulent transfers and insurer notification. |
| CHRO | Provides the HR Liaison; co-authorizes Workforce Member investigations. |
| HIPAA Security Officer `[HIPAA]` | Receives escalation for incidents involving ePHI; ensures documentation under CMP-008. |
| System Owners | Act as Business Liaison; approve restoration of their systems with the Incident Commander. |

Role names and accountabilities are established in GOV-001 and consolidated in REF-002.

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| RES-002.7.1 | Severity Levels | Sev-1 Critical · Sev-2 High · Sev-3 Medium · Sev-4 Low |
| RES-002.7.2 | Incident response SLAs | Sev-1: incident commander within 15 min, executive notification within 1 h, updates hourly · Sev-2: commander within 1 h, updates every 4 h · Sev-3: within 1 business day · Sev-4: within 5 business days |
| RES-002.7.3 | CISO notification | Sev-1 within 30 min · Sev-2 within 2 h |
| RES-002.7.4 | Sev-3 / Sev-4 status updates and target closure | Sev-3: every business day, closure within 10 business days · Sev-4: at closure, closure within 20 business days |
| RES-002.7.5 | Initial assessment recorded | Sev-1 within 1 h of acceptance · Sev-2 within 4 h |
| RES-002.7.6 | Containment strategy set | Sev-1 within 2 h of acceptance · Sev-2 within 8 h |
| RES-002.7.7 | Containment complete criterion (Sev-1, Sev-2) | No new malicious activity for at least 24 h with IOC monitoring in place |
| RES-002.7.8 | Enhanced monitoring after recovery (Sev-1, Sev-2) | At least 30 days |
| RES-002.7.9 | Post-incident review | Required for Sev-1 and Sev-2, completed within 10 business days of closure; also for 3 or more Sev-3 incidents with the same root cause within 90 days |
| RES-002.7.10 | IR plan testing | Tabletop or functional exercise every 12 months |
| RES-002.7.11 | Exercise report | Within 30 days of the exercise |
| RES-002.7.12 | Audit Committee Chair notification of Sev-1 | Within 24 h of declaration |
| RES-002.7.13 | Sev-1 holding statement prepared | Within 4 h of declaration |
| RES-002.7.14 | Trained persons per key IR role | At least 2 for Incident Commander, Scribe, Communications Lead and Legal Lead |
| RES-002.7.15 | Out-of-band channel, roster contacts and toolkit verification | Every 6 months |
| RES-002.7.16 | Playbook review | Every 12 months and within 30 days after use in a Sev-1 or Sev-2 incident |
| RES-002.7.17 | Maximum Incident Commander shift (Sev-1) | 12 hours |
| RES-002.7.18 | Plan review | Every 12 months and within 30 days after closure of each Sev-1 incident |
| RES-002.7.19 | Alert triage | As set in SEC-012 |
| RES-002.7.20 | Breach notification deadlines and internal legal escalation | As set in RES-003 |
| RES-002.7.21 | Incident record retention | As set in CMP-004 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Incidents with Incident Commander assigned within the RES-002.7.2 limit, by Severity Level | 100% Sev-1/Sev-2; ≥ 95% Sev-3/Sev-4 | Monthly | SOC Manager |
| Sev-1 incidents with executive notification within 1 h | 100% | Monthly | CISO |
| Status updates issued at the required cadence (sampled) | ≥ 95% | Monthly | SOC Manager |
| Mean time to detect (first malicious activity to declaration), Sev-1/Sev-2 | Trend decreasing quarter on quarter | Quarterly | SOC Manager |
| Mean time to contain (declaration to containment complete), Sev-1/Sev-2 | Trend decreasing quarter on quarter | Quarterly | SOC Manager |
| Sev-3/Sev-4 incidents closed within target closure time | ≥ 90% | Monthly | SOC Manager |
| Post-Incident Reviews completed within 10 business days of closure | 100% | Quarterly | SOC Manager |
| Post-incident corrective actions closed by due date | ≥ 90% | Quarterly | SOC Manager |
| Severity downgrades from Sev-1/Sev-2 with CISO approval recorded | 100% | Quarterly | CISO |
| Annual exercise completed within 12 months of the last | Yes | Annually | SOC Manager |
| Playbooks reviewed within 12 months | 100% | Quarterly | SOC Manager |
| Recurrence: incidents with the same Root Cause as a closed Post-Incident Review within 12 months | 0 | Quarterly | CISO |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

Deviations during a live incident are governed by RES-002.5.1.4 and do not require an
Exception. The following SHALL NOT receive an Exception: the Sev-1 time limits in section
5.3; the Post-Incident Review requirement for Sev-1 and Sev-2; and the annual exercise.

## 10. Enforcement

Non-compliance is handled under CMP-007.

Failures by IR role holders to meet the time limits in section 5.3 SHALL be reviewed in the
Post-Incident Review before any referral under CMP-007, consistent with the blameless
principle in RES-002.5.10.5.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| RES-002.5.1 – 5.3 | A.5.24, A.5.25 | RS.MA-01, RS.MA-02, RS.MA-03, RS.MA-04, DE.AE-08 | IR-4, IR-5, IR-8 | 17.4, 17.9 | CC7.3, CC7.4 | DSS02.02, DSS02.03 | `[PCI]` 12.10.1; `[HIPAA]` §164.308(a)(6)(ii) |
| RES-002.5.4 | A.5.24, A.5.2 | GV.RR-02, RS.MA-01 | IR-4, IR-7, IR-8 | 17.1, 17.5 | CC7.4, CC1.3 | APO07, DSS02 | `[PCI]` 12.10.3 |
| RES-002.5.5 | A.5.24, A.5.5, A.5.6 | ID.IM-04, PR.AT-02 | IR-2, IR-8, IR-7 | 17.2, 17.6 | CC7.3, CC7.4 | DSS02, DSS05 | `[PCI]` 12.10.4, 12.10.5 |
| RES-002.5.6 | A.5.25, A.6.8, A.8.16 | DE.AE-02, DE.AE-03, DE.AE-07, RS.AN-03, RS.AN-06, RS.AN-07, RS.AN-08 | IR-4, IR-5, SI-4 | 17.4, 17.9 | CC7.2, CC7.3 | DSS02, DSS05 | `[HIPAA]` §164.308(a)(6)(ii) |
| RES-002.5.7 – 5.8 | A.5.26 | RS.MI-01, RS.MI-02 | IR-4 | 17.4 | CC7.4 | DSS02, DSS05 | `[HIPAA]` §164.308(a)(6)(ii) |
| RES-002.5.9 | A.5.26, A.5.29, A.8.13 | RC.RP-01, RC.RP-02, RC.RP-03, RC.RP-05, RC.RP-06 | IR-4, CP-10 | 11.5, 17.4 | CC7.5 | DSS02, DSS04 | `[GDPR]` Art. 32(1)(c) |
| RES-002.5.10 | A.5.27, 10.1, 10.2 | ID.IM-01, ID.IM-02, ID.IM-03, ID.IM-04, RS.MA-05 | IR-4, IR-8 | 17.8 | CC7.5, CC4.2 | DSS02.06, MEA01 | `[PCI]` 12.10.6 |
| RES-002.5.11 – 5.12 | A.5.24, A.5.26, A.5.5 | RS.CO-02, RS.CO-03, RC.CO-03, RC.CO-04 | IR-6, IR-4 | 17.2, 17.6 | CC2.2, CC2.3, CC7.4 | APO08, DSS02 | `[SOX]` Form 8-K Item 1.05 (via RES-003); `[GDPR]` Art. 33 (via RES-003) |
| RES-002.5.13 | A.5.24, A.5.26 | RS.MA-01, RS.MI-01, RS.MI-02 | IR-4, IR-8, IR-9 | 17.4 | CC7.4 | DSS02 | `[PCI]` 12.10.1, 12.10.7 |
| RES-002.5.14 – 5.15 | A.5.24, A.5.27 | ID.IM-02, ID.IM-04 | IR-3, IR-8 | 17.7 | CC7.4, CC7.5 | DSS02, DSS04 | `[PCI]` 12.10.2; `[HIPAA]` §164.308(a)(6) |

## 12. Related documents

ISP-000, GOV-001, GOV-002, GOV-003, GOV-004, GOV-006, RSK-002, RSK-003, RSK-004, RSK-005, RSK-006, CMP-003, CMP-004, CMP-006, CMP-007, CMP-008, SEC-001, SEC-002, SEC-003, SEC-004, SEC-005, SEC-006, SEC-007, SEC-008, SEC-009, SEC-011, SEC-012, SEC-013, SEC-014, SEC-017, SEC-018, SEC-019, PPL-001, PPL-002, RES-001, RES-003, RES-004, RES-005, TPL-006, TPL-007, REF-001, REF-002

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: SOC Manager | | | |
| Approver: CISO | | | |
