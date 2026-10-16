# RES-001 — Incident Response Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | RES-001 |
| Title | Incident Response Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Information Security Officer (CISO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | RES-002, RES-003, RES-004, RES-005, SEC-012, SEC-013, CMP-004, CMP-006, CMP-007, RSK-003, PPL-002, TPL-006, TPL-007 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CISO | Initial release |

## 3. Purpose

This Policy establishes the Organization's mandate and authority to detect, report,
respond to and learn from Security Incidents. It sets the obligation on every Workforce
Member and Third Party to report suspected Security Incidents, establishes the incident
response capability and the authority of the Incident Commander, and sets the rules for
evidence preservation, forensic investigation, law enforcement liaison and external
incident response support. The operational procedure, Severity Levels and response time
limits are in RES-002; breach determination and external notification are in RES-003.

## 4. Scope

- **People:** all Workforce Members; members of the Incident Response Team; executives and governance bodies with a role in incident escalation; Third Parties that access, process or support Organization Information Assets.
- **Systems:** all Information Systems, Cloud Services, Endpoints, networks, operational technology and facilities owned, operated or contracted by the Organization, in every environment (production, non-production, corporate and the CDE `[PCI]`).
- **Data:** all information at every Classification Level, including Personal Data, PHI `[HIPAA]`, CHD `[PCI]` and data in Financially Significant Systems `[SOX]`.
- **Locations:** all Organization sites, remote work locations, travel and Third-Party facilities that hold Organization information.
- **Third parties:** Third Parties whose services, staff or systems are involved in, cause or are affected by a Security Incident, and Third Parties that provide incident response services to the Organization.
- **Out of scope:** operational IT service outages with no security cause, which are handled under the IT incident process and, where recovery targets are threatened, under RES-004 and RES-005.

## 5. Policy statements

### 5.1 Incident response program

- **RES-001.5.1.1** The Organization SHALL maintain an incident response capability able to detect, analyze, contain, eradicate and recover from Security Incidents 24 hours a day, 7 days a week.
- **RES-001.5.1.2** The CISO SHALL be accountable for the incident response capability. The SOC Manager SHALL be responsible for its day-to-day operation.
- **RES-001.5.1.3** The SOC Manager SHALL maintain RES-002 Incident Response Plan, including the Severity Level criteria, response time limits, team roles, phase procedures, escalation matrix, communications plan and playbooks.
- **RES-001.5.1.4** The incident response capability SHALL align with NIST SP 800-61 Rev. 3 and the NIST CSF 2.0 Respond and Recover functions, and with ISO/IEC 27001:2022 Annex A 5.24 to 5.28.
- **RES-001.5.1.5** Every Security Incident SHALL be recorded in the incident register using TPL-006, assigned a Severity Level under RES-002, and tracked to closure.
- **RES-001.5.1.6** Security Events SHALL be triaged within the alert triage SLA in SEC-012. A Security Event that meets the Security Incident criteria in RES-002 SHALL be declared a Security Incident at the time those criteria are met.
- **RES-001.5.1.7** The CISO SHALL ensure that at least two trained Incident Commanders are on call at all times, with a published on-call rota maintained by the SOC Manager.
- **RES-001.5.1.8** Workforce Members assigned an incident response role SHALL complete the role-based training required by PPL-002 before taking an on-call or Incident Commander assignment.
- **RES-001.5.1.9** `[PCI]` The incident response capability SHALL include personnel available 24×7 to respond to suspected or confirmed Security Incidents affecting the CDE, and SHALL include the response to detection of stored PAN anywhere it is not expected, as specified in RES-002.
- **RES-001.5.1.10** `[HIPAA]` The incident response capability SHALL identify and respond to suspected or known Security Incidents involving ePHI, mitigate their harmful effects to the extent practicable, and document them and their outcomes.

### 5.2 Obligation to report suspected Security Incidents

- **RES-001.5.2.1** Every Workforce Member SHALL report any suspected or actual Security Incident, Security Event of concern, or violation of a suite document with security impact, through the security reporting channel, immediately on becoming aware of it and in any case within 1 hour.
- **RES-001.5.2.2** The SOC Manager SHALL operate a security reporting channel consisting of at minimum: (a) a monitored email address; (b) a telephone line answered 24×7; and (c) a reporting form or ticket category in the IT service portal. [DECISION REQUIRED: Channel identifiers (address, number, portal link). Recommended default: a dedicated security mailbox, a 24×7 SOC hotline and a "Report a security incident" service-portal form, published on the intranet home page.]
- **RES-001.5.2.3** The channel details SHALL be published on the intranet, included in the training required by PPL-002 and in GOV-004, and printed on or linked from every Endpoint lock screen or support page.
- **RES-001.5.2.4** Reportable events SHALL include at minimum: suspected phishing that was clicked or answered; disclosure of a password, MFA code or other Secret; loss or theft of an Endpoint, Mobile Device, Media or access badge; Malware alerts or unexplained system behavior; unauthorized access to, or disclosure of, Confidential or Restricted information; misdirected email containing Personal Data; suspected fraud or payment-redirection requests; unauthorized physical access; and suspected misuse of an AI System.
- **RES-001.5.2.5** Reports of lost or stolen Endpoints and Mobile Devices SHALL also be made to the IT Service Desk within the same 1-hour limit so that remote lock or wipe can be initiated under SEC-008.
- **RES-001.5.2.6** Workforce Members SHALL NOT investigate a suspected Security Incident themselves, alter or delete affected data or systems, confront a suspected insider, or discuss the incident with any external party, unless directed by the Incident Commander.
- **RES-001.5.2.7** Workforce Members SHALL preserve and not delete suspicious emails, messages or files, and SHALL follow the SOC's instructions for submitting them.
- **RES-001.5.2.8** A Workforce Member who suspects that the security reporting channel itself, or a member of the Incident Response Team, is involved in the incident SHALL report through the channels in CMP-006.
- **RES-001.5.2.9** The Organization SHALL NOT retaliate against any Workforce Member for reporting a suspected Security Incident in good faith, including a report of the reporter's own error. Protection against retaliation is governed by CMP-006.
- **RES-001.5.2.10** A Workforce Member's own good-faith error that is reported within the time limit in RES-001.5.2.1 SHALL be treated as a mitigating factor under CMP-007. Failure to report within that limit SHALL be treated as a separate violation under CMP-007.
- **RES-001.5.2.11** Third Parties SHALL report Security Incidents affecting Organization Information Assets within the time set in their contract under RSK-003. The Head of Procurement SHALL ensure that every contract with a Third Party that accesses Confidential or Restricted information names the security reporting channel as the reporting destination.
- **RES-001.5.2.12** The SOC SHALL acknowledge each report received through the security reporting channel within the alert triage SLA in SEC-012 for the Severity of the reported event, and SHALL tell the reporter whether further action is required of them.
- **RES-001.5.2.13** External reports of Vulnerabilities received through the VDP under SEC-011 that indicate active exploitation SHALL be forwarded to the SOC as Security Events within 1 hour of receipt.

### 5.3 Incident Commander and authority

- **RES-001.5.3.1** Every Security Incident SHALL have one named Incident Commander at all times. The Incident Commander SHALL be assigned within the response time limit in RES-002 for the Severity Level.
- **RES-001.5.3.2** The Incident Commander SHALL direct the response, assign team roles under RES-002, set priorities, approve containment actions and own the incident record until closure or formal hand-over.
- **RES-001.5.3.3** The Incident Commander SHALL have the authority, without prior approval of the System Owner, Asset Owner or Data Owner, to:
  - (a) isolate any Endpoint, server, container, virtual machine, network segment or Cloud Service account from the network;
  - (b) disable, suspend or force re-authentication of any User account, Service Account or Privileged Account, and revoke sessions, tokens and API keys;
  - (c) block IP addresses, domains, URLs, email senders and file hashes at any enforcement point;
  - (d) suspend a Third-Party connection or integration;
  - (e) take forensic images and memory captures of any Organization-owned system;
  - (f) suspend scheduled jobs, deployments or Changes affecting the systems in scope; and
  - (g) direct any Workforce Member to take or stop an action necessary for containment.
- **RES-001.5.3.4** Shutting down, or isolating in a way that causes an outage of, a system assigned Recovery Tier 0 or Tier 1 under RSK-004 SHALL require approval of the CISO, or the CIO if the CISO is unavailable, except where the Incident Commander determines that data exfiltration, destructive activity or ransomware propagation is in progress, in which case the Incident Commander MAY act first and SHALL obtain retrospective approval within 1 hour.
- **RES-001.5.3.5** The Incident Commander SHALL notify the System Owner of every action taken under RES-001.5.3.3 or RES-001.5.3.4 within 1 hour of the action.
- **RES-001.5.3.6** Containment actions that change production systems SHALL be recorded as Emergency Changes and approved retrospectively under SEC-013.
- **RES-001.5.3.7** Workforce Members, System Owners and Third Parties under contract SHALL comply with the Incident Commander's directions. A disagreement SHALL be escalated to the CISO, whose decision is final for the duration of the incident; it SHALL NOT delay a containment action already directed.
- **RES-001.5.3.8** For Sev-1 Security Incidents, the CISO SHALL act as executive sponsor and SHALL escalate to the Crisis Management Team when the activation criteria in RES-004 are met.
- **RES-001.5.3.9** The Incident Commander SHALL NOT be a person whose own actions or accounts are under investigation in the incident. Where an incident involves a member of the Incident Response Team, the CISO SHALL appoint an Incident Commander from outside the affected team. Where it involves the CISO, the GC SHALL appoint the Incident Commander and assume the CISO's decision rights under this Policy for that incident.
- **RES-001.5.3.10** Decisions to restore affected systems to production SHALL be made by the Incident Commander together with the System Owner, under RES-002, and, where a disaster has been declared, under RES-005.

### 5.4 Evidence preservation and forensics

- **RES-001.5.4.1** From the moment a Security Event is triaged as a potential Security Incident, the Incident Response Team SHALL preserve evidence. Where containment and evidence preservation conflict, the Incident Commander SHALL decide, record the reason, and give priority to stopping ongoing harm.
- **RES-001.5.4.2** Volatile evidence (memory, running processes, network connections) SHALL be captured before a system is powered off or reimaged, where it is technically possible and the Incident Commander does not determine that delay would cause further harm.
- **RES-001.5.4.3** Forensic images and evidence files SHALL be hashed using SHA-256 or a stronger algorithm permitted by SEC-006 at acquisition, and the hash SHALL be verified each time the evidence is accessed or transferred.
- **RES-001.5.4.4** Every evidence item SHALL have a chain-of-custody record in TPL-006 identifying: item description and unique identifier; source system; date and time of collection (UTC); collector; hash value; storage location; and every subsequent transfer, access and purpose.
- **RES-001.5.4.5** Evidence SHALL be stored in a dedicated evidence repository with access restricted to named incident response personnel, the GC and the GC's designees, with access logged under SEC-012 and data encrypted at rest under SEC-006. Evidence SHALL be classified Restricted.
- **RES-001.5.4.6** Analysis SHALL be performed on verified copies, not on original evidence.
- **RES-001.5.4.7** Physical evidence (devices, Media) SHALL be sealed in tamper-evident bags labeled with the evidence identifier and stored in a locked container in an access-controlled area under SEC-016.
- **RES-001.5.4.8** Logs relevant to a Security Incident SHALL be preserved beyond the retention period in CMP-004 for the life of the incident and any Legal Hold. The SOC Manager SHALL suspend automated log deletion for affected sources within 24 hours of the incident being declared.
- **RES-001.5.4.9** The GC SHALL decide within 1 business day of a Sev-1 or Sev-2 declaration whether to issue a Legal Hold. Where a Legal Hold is issued, evidence and incident records SHALL be retained until the GC releases it.
- **RES-001.5.4.10** Forensic investigation of a Workforce Member's activity, Endpoint or accounts SHALL be authorized in writing by the GC and the CHRO before it starts, except for automated controls under SEC-012 and containment actions under RES-001.5.3.3. Such investigations SHALL comply with applicable employment and privacy law, as advised by the GC, and with CMP-005.
- **RES-001.5.4.11** Forensic work on systems or data owned by a Third Party, or in a Cloud Service Provider's environment, SHALL be performed only within the rights granted by contract or with the Third Party's written consent.
- **RES-001.5.4.12** Where litigation, regulatory action or law enforcement involvement is anticipated, as determined by the GC, forensic investigation SHOULD be performed by, or under the direction of, the external incident response provider engaged through counsel under RES-001.5.6.3.
- **RES-001.5.4.13** Incident records and evidence SHALL be retained for the period in CMP-004, subject to any Legal Hold, and then disposed of under SEC-017.

### 5.5 Law enforcement and authority liaison

- **RES-001.5.5.1** Only the GC, or a person the GC designates in writing for a specific incident, SHALL authorize contact with law enforcement about a Security Incident. The CISO SHALL be the operational point of contact once contact is authorized.
- **RES-001.5.5.2** The GC SHALL decide within 24 hours of a Sev-1 declaration whether to notify law enforcement, and SHALL record the decision and its reasons in the incident record. For ransomware, extortion, Business Email Compromise with funds transferred, and threats to life or safety, the GC SHALL presume notification unless the GC records a reason not to notify.
- **RES-001.5.5.3** The SOC Manager SHALL maintain, and verify every 12 months, a contact list of the law enforcement agencies, national computer emergency response teams and government cyber agencies relevant to each country of operation (e.g. national police cybercrime units, federal investigative agencies, national CSIRTs). [DECISION REQUIRED: Primary law enforcement contacts per region. Recommended default: the national federal investigative agency's cyber division and the national cyber agency in each country of operation.]
- **RES-001.5.5.4** Evidence, data or system access SHALL be provided to law enforcement only as authorized by the GC, and only in response to a valid legal process or with the GC's recorded approval of voluntary disclosure. Disclosure of Personal Data to law enforcement SHALL comply with CMP-005.
- **RES-001.5.5.5** A request by law enforcement to delay notification SHALL be received in writing (or, where received orally, documented by the GC with the officer's identity and the date, and confirmed in writing within the period required by the applicable law) and handled under RES-003.
- **RES-001.5.5.6** Communications with regulators, supervisory authorities and payment brands about a Security Incident SHALL be made only as set out in RES-003.
- **RES-001.5.5.7** The SOC Manager MAY share indicators of compromise and threat information, stripped of Personal Data and Confidential or Restricted information, with information-sharing organizations approved under RSK-005, with the CISO's approval.

### 5.6 External incident response support

- **RES-001.5.6.1** The Organization SHALL maintain at all times a contracted incident response retainer with at least one external provider able to perform digital forensics, incident response, threat hunting and ransomware or extortion negotiation support.
- **RES-001.5.6.2** The retainer SHALL guarantee: remote engagement within 4 hours of a call-out, on any day; on-site deployment to any primary Organization location within 48 hours; and coverage of all regions in which the Organization operates. [DECISION REQUIRED: Retainer response commitments. Recommended default: remote within 4 hours, on-site within 48 hours.]
- **RES-001.5.6.3** The retainer SHOULD be structured so that the provider can be engaged by or through the GC or outside counsel, to support assertion of Legal Privilege over the investigation.
- **RES-001.5.6.4** The CISO SHALL confirm that the retainer provider is acceptable to the Organization's cyber insurer, where the insurance policy limits the choice of provider, and SHALL coordinate with the CFO on insurer notification under RES-003.
- **RES-001.5.6.5** The retainer provider SHALL be assessed and managed as a Tier 1 Third Party under RSK-003 (RSK-003.5.2.1), and SHALL be bound by confidentiality, data protection and, where applicable, Business Associate Agreement `[HIPAA]` terms before it receives any Organization data.
- **RES-001.5.6.6** The CISO or SOC Manager SHALL engage the retainer for every Sev-1 Security Incident within 4 hours of declaration, unless the CISO records that internal capability is sufficient. For Sev-2 Security Incidents, the Incident Commander MAY engage the retainer.
- **RES-001.5.6.7** `[PCI]` Where a compromise of CHD is suspected and a payment brand or acquirer requires a PCI Forensic Investigator (PFI), the Organization SHALL engage a PFI from the PCI SSC list within the time required by the brand or acquirer, as coordinated under RES-003.
- **RES-001.5.6.8** The SOC Manager SHALL verify every 12 months that the retainer contact details, activation procedure and pre-approved hours are current, and SHALL record the verification.

### 5.7 Ransom and extortion payments

- **RES-001.5.7.1** No Workforce Member SHALL pay, promise or negotiate a ransom or extortion demand, or engage directly with a threat actor, except as authorized under this section.
- **RES-001.5.7.2** A decision to pay a ransom or extortion demand SHALL be made only by the CEO, on the joint recommendation of the GC, CFO and CISO, and SHALL be reported to the Audit Committee within 24 hours of the decision.
- **RES-001.5.7.3** Before any payment, the GC SHALL confirm in writing that the payment does not breach sanctions or other applicable law (including screening of the recipient against applicable sanctions lists), and the CFO SHALL confirm insurer notification where the insurance policy requires it.
- **RES-001.5.7.4** Negotiation with a threat actor SHALL be conducted only by a specialist provider engaged under section 5.6.

### 5.8 Readiness, testing and improvement

- **RES-001.5.8.1** The incident response capability SHALL be tested through exercises at the frequency and in the form set in RES-002. The CISO SHALL ensure at least one exercise each year includes participants at executive level.
- **RES-001.5.8.2** Post-Incident Reviews SHALL be conducted for the Severity Levels and within the time set in RES-002, using TPL-007, in a blameless format.
- **RES-001.5.8.3** Corrective actions from Post-Incident Reviews and exercises SHALL be assigned an owner and due date and tracked to closure by the SOC Manager. Corrective actions that address a Risk SHALL be entered in the Risk Register and treated within the deadlines in RSK-002.
- **RES-001.5.8.4** A Sev-1 Security Incident whose Root Cause relates to a suite document SHALL trigger an event-driven review of that document under GOV-002.
- **RES-001.5.8.5** Sev-1 Security Incidents SHALL trigger the risk assessment and ISSC escalation set out in RSK-002 and GOV-001.
- **RES-001.5.8.6** The SOC Manager SHALL maintain detection and response tooling (e.g. SIEM, EDR, case management) such that incident data required by TPL-006 is captured, and SHALL ensure that Log Sources required by SEC-012 are available to responders.
- **RES-001.5.8.7** The CISO SHALL report incident metrics to the ISSC and Audit Committee at the cadence set in GOV-003.

### 5.9 Confidentiality of incident information

- **RES-001.5.9.1** Information about an active Security Incident SHALL be classified at least Confidential, and Restricted where it contains Restricted data, indicators that would aid an attacker or legal advice.
- **RES-001.5.9.2** Information about an active Security Incident SHALL be shared only with persons with a Need to Know, as determined by the Incident Commander, and through channels set out in RES-002. Where the Organization's primary collaboration or email systems are suspected to be compromised, the out-of-band communication channel in RES-002 SHALL be used.
- **RES-001.5.9.3** No Workforce Member SHALL make any public statement, social media post, or statement to customers, media or investors about a Security Incident except as authorized under RES-002 and RES-003.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CISO | Accountable for the incident response capability; executive sponsor of Sev-1 incidents; approves Tier 0/Tier 1 shutdowns (RES-001.5.3.4); resolves disputes over Incident Commander directions; appoints the Incident Commander where the response team is implicated; engages the retainer; reports metrics. |
| SOC Manager | Operates the capability and the security reporting channel; maintains RES-002 and the on-call rota; maintains law enforcement and retainer contacts; suspends log deletion; tracks corrective actions. |
| Incident Commander (IR role under RES-002) | Directs the response; exercises the authority in RES-001.5.3.3; decides containment versus evidence conflicts; notifies System Owners of actions taken. |
| GC | Authorizes law enforcement contact; decides on Legal Holds; authorizes forensic investigation of Workforce Members (with the CHRO); engages providers under privilege; confirms the lawfulness of any ransom payment; appoints the Incident Commander where the CISO is implicated. |
| CEO | Sole authority for any ransom or extortion payment decision; chairs the Crisis Management Team under RES-004. |
| CFO | Notifies the cyber insurer; co-recommends any ransom payment decision; confirms insurer requirements. |
| CIO | Approves Tier 0/Tier 1 shutdowns when the CISO is unavailable; provides infrastructure and IT Service Desk support to responders. |
| CHRO | Co-authorizes forensic investigation of Workforce Members; leads personnel actions arising from incidents under CMP-007. |
| CPO | Leads breach determination and notification under RES-003. |
| Head of Procurement | Ensures Third-Party contracts name the security reporting channel and incident reporting time limits under RSK-003. |
| System Owners | Comply with Incident Commander directions; support containment, recovery and evidence collection. |
| Workforce Members | Report suspected Security Incidents within the time limit in RES-001.5.2.1; preserve evidence; follow directions. |
| Third Parties | Report Security Incidents per contract; cooperate with investigations as contracted. |

Role names and accountabilities are established in GOV-001 and consolidated in REF-002.

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| RES-001.7.1 | Workforce Member reporting of a suspected Security Incident | Immediately, and within 1 hour of becoming aware |
| RES-001.7.2 | Security reporting channel availability | 24×7, at least three channels (email, telephone, portal) |
| RES-001.7.3 | Trained Incident Commanders on call | At least 2 at all times |
| RES-001.7.4 | Incident Commander assignment, executive notification and update cadence | As set in RES-002 |
| RES-001.7.5 | Retrospective approval of emergency Tier 0/Tier 1 shutdown | Within 1 hour of the action |
| RES-001.7.6 | System Owner notification of containment action | Within 1 hour of the action |
| RES-001.7.7 | Suspension of automated log deletion for affected sources | Within 24 hours of declaration |
| RES-001.7.8 | Legal Hold decision for Sev-1 and Sev-2 | Within 1 business day of declaration |
| RES-001.7.9 | Law enforcement notification decision for Sev-1 | Within 24 hours of declaration |
| RES-001.7.10 | Evidence integrity hash | SHA-256 or stronger, verified on each access or transfer |
| RES-001.7.11 | External IR retainer response | Remote within 4 hours; on-site within 48 hours |
| RES-001.7.12 | Retainer engagement for Sev-1 | Within 4 hours of declaration, unless CISO records internal capability is sufficient |
| RES-001.7.13 | Retainer and law enforcement contact verification | Every 12 months |
| RES-001.7.14 | VDP report indicating active exploitation forwarded to SOC | Within 1 hour of receipt |
| RES-001.7.15 | Ransom payment reported to Audit Committee | Within 24 hours of the decision |
| RES-001.7.16 | IR plan testing | As set in RES-002 |
| RES-001.7.17 | Post-Incident Review | As set in RES-002 |
| RES-001.7.18 | Incident record and evidence retention | As set in CMP-004 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Security Incidents reported by Workforce Members within 1 hour of awareness (where awareness time is determinable) | ≥ 90% | Monthly | SOC Manager |
| Security reporting channel test calls and emails answered within the SEC-012 triage SLA | 100% | Quarterly | SOC Manager |
| Days with fewer than 2 trained Incident Commanders on call | 0 | Monthly | SOC Manager |
| Containment actions with System Owner notified within 1 hour | 100% | Monthly | SOC Manager |
| Sev-1/Sev-2 incidents with a recorded Legal Hold decision within 1 business day | 100% | Quarterly | GC |
| Evidence items with complete chain-of-custody records (sampled) | 100% | Quarterly | SOC Manager |
| Sev-1 incidents with retainer engaged within 4 hours or a recorded CISO decision | 100% | Quarterly | CISO |
| Retainer and law enforcement contact verification completed | Within 12 months of the last | Annually | SOC Manager |
| Post-Incident Review corrective actions closed by due date | ≥ 90% | Quarterly | SOC Manager |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following SHALL NOT receive an Exception: the reporting obligation in RES-001.5.2.1; the
non-retaliation commitment in RES-001.5.2.9; the ransom payment authority in section 5.7;
and the GC's authority over law enforcement contact in RES-001.5.5.1.

## 10. Enforcement

Non-compliance is handled under CMP-007.

Failure to report a known Security Incident, destruction or alteration of evidence,
obstruction of the Incident Commander, unauthorized contact with a threat actor, or
unauthorized external disclosure of incident information SHALL be treated as serious
violations under CMP-007. Third-Party non-compliance is handled under the contract and
RSK-003.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| RES-001.5.1 | A.5.24, A.5.26 | RS.MA-01, RS.MA-02, ID.IM-04 | IR-1, IR-4, IR-8 | 17.1, 17.4 | CC7.3, CC7.4 | DSS02, DSS05 | `[PCI]` 12.10.1, 12.10.3, 12.10.7; `[HIPAA]` §164.308(a)(6) |
| RES-001.5.2 | A.6.8, A.5.25 | DE.AE-02, RS.MA-01 | IR-6, IR-7 | 17.2, 17.3 | CC2.2, CC2.3, CC7.3 | DSS02 | `[HIPAA]` §164.308(a)(6)(ii); `[PCI]` 12.10.1 |
| RES-001.5.3 | A.5.26 | RS.MA-01, RS.MA-03, RS.MI-01, RS.MI-02 | IR-4 | 17.5 | CC7.4 | DSS02, DSS05 | — |
| RES-001.5.4 | A.5.28 | RS.AN-03, RS.AN-07 | IR-4, AU-9, AU-11 | 17.4 | CC7.4 | DSS05 | `[GDPR]` Art. 33(5); `[HIPAA]` §164.308(a)(6)(ii) |
| RES-001.5.5 | A.5.5, A.5.6 | RS.CO-03 | IR-6, IR-7 | 17.2 | CC2.3 | APO08, MEA03 | `[GDPR]` Art. 33 |
| RES-001.5.6 | A.5.24, A.5.19 | RS.MA-01, GV.SC-01 | IR-7 | 17.5 | CC7.4, CC9.2 | APO10 | `[PCI]` 12.10.1 |
| RES-001.5.7 | A.5.26, A.5.31 | RS.MA-01 | IR-4 | — | CC7.4 | APO12, MEA03 | — |
| RES-001.5.8 | A.5.27, 10.2 | ID.IM-01, ID.IM-02, ID.IM-04 | IR-2, IR-3, IR-4 | 17.7, 17.8 | CC7.5, CC4.2 | DSS02, MEA01 | `[PCI]` 12.10.2, 12.10.4, 12.10.6 |
| RES-001.5.9 | A.5.14, A.5.26 | RS.CO-02, RS.CO-03 | IR-4, IR-6 | 17.6 | CC2.2, C1.1 | DSS05 | `[SOX]` Form 8-K Item 1.05 (via RES-003) |

## 12. Related documents

ISP-000, GOV-001, GOV-002, GOV-003, GOV-004, GOV-006, RSK-001, RSK-002, RSK-003, RSK-004, RSK-005, CMP-003, CMP-004, CMP-005, CMP-006, CMP-007, SEC-006, SEC-008, SEC-011, SEC-012, SEC-013, SEC-016, SEC-017, PPL-002, RES-002, RES-003, RES-004, RES-005, TPL-006, TPL-007, REF-001, REF-002

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CISO | | | |
| Approver: ISSC Vice-Chair, on behalf of the ISSC (CISO recused as Document Owner under GOV-001.5.3.9) | | | |
