# PPL-002 — Security Awareness & Training Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | PPL-002 |
| Title | Security Awareness & Training Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Information Security Officer (CISO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-001, GOV-002, GOV-003, GOV-004, CMP-004, CMP-005, CMP-007, CMP-008, PPL-001, RSK-003, SEC-019 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CISO | Initial release |

## 3. Purpose

This Policy establishes the Organization's security awareness and training program. It sets
who must be trained, on what, and when; the role-based training required for higher-risk
roles; the phishing simulation program; how training effectiveness is measured; and how
non-completion is handled, so that every Workforce Member can recognize and respond to threats
and meet their obligations under the policy suite.

## 4. Scope

- **People:** every Workforce Member; members of the Board of Directors; Third Party personnel who hold Organization accounts; and the managers and functions that assign, track and enforce training.
- **Systems:** the learning management system, the phishing simulation platform, and the communication channels used for awareness.
- **Data:** training content, completion records, assessment scores and phishing simulation results.
- **Locations:** all Organization sites and regions in the scope of ISP-000, including remote workers.
- **Third parties:** providers of training content or platforms, and Third Parties whose personnel are required by contract (RSK-003) to complete equivalent training.

## 5. Policy statements

### 5.1 Program governance

- **PPL-002.5.1.1** The CISO SHALL maintain a security awareness and training program and SHALL present an annual program plan to the ISSC for approval before the start of each fiscal year. The plan SHALL set the curriculum, role-based courses, phishing simulation schedule, communications calendar and targets.
- **PPL-002.5.1.2** The CISO SHALL review training content every 12 months, and within 30 days of: a change to GOV-004 or another document in an Attestation Set (GOV-002); a Sev-1 Security Incident whose Post-Incident Review identifies a human factor; or a material change in the threat landscape reported under RSK-005.
- **PPL-002.5.1.3** The CPO SHALL review privacy content, and the GC SHALL review content describing legal obligations, before each annual release.
- **PPL-002.5.1.4** Training SHALL be delivered in the primary working languages of the Organization's work locations and in formats that meet accessibility needs disclosed by Workforce Members. [DECISION REQUIRED: Languages in which training is provided. Recommended default: every language that is the primary working language of at least 50 Workforce Members.]
- **PPL-002.5.1.5** All training SHALL be assigned and recorded in the learning management system, which SHALL take its population of Workforce Members from the HRIS (PPL-001).

### 5.2 Training at hire

- **PPL-002.5.2.1** Every Workforce Member SHALL complete security awareness training within 30 days of start, and before access to Restricted data.
- **PPL-002.5.2.2** Training at hire SHALL cover, at a minimum:
  1. The Information Security Program and where to find suite documents (ISP-000, GOV-002).
  2. Acceptable use, including credentials, personal use, Generative AI tools, social media and monitoring (GOV-004).
  3. Classification Levels and handling rules (SEC-002).
  4. Phishing and social engineering recognition, including payment and credential fraud.
  5. Password, MFA and account security (SEC-004).
  6. Endpoint, Mobile Device and remote work security (SEC-008, SEC-015).
  7. Physical security, clear desk and visitor handling (GOV-004, SEC-016).
  8. How and when to report Security Incidents and concerns, the reporting channels, and protection against Retaliation (RES-001, CMP-006).
  9. Privacy principles and handling of Personal Data (CMP-005).
  10. Consequences of non-compliance (CMP-007).
- **PPL-002.5.2.3** `[PCI]` Training SHALL include awareness of threats and vulnerabilities that could affect the security of the CDE, including phishing and social engineering, and acceptable use of end-user technologies.
- **PPL-002.5.2.4** `[HIPAA]` Training SHALL include the HIPAA security topics in 45 CFR §164.308(a)(5)(ii): security reminders, protection from malicious software, log-in monitoring and password management.

### 5.3 Annual training

- **PPL-002.5.3.1** Every Workforce Member SHALL complete security awareness training every 12 months, completed within 30 days of assignment.
- **PPL-002.5.3.2** Annual training SHALL refresh the topics in PPL-002.5.2.2 and SHALL include changes to suite documents and lessons learned from Security Incidents in the preceding 12 months, without identifying individuals.
- **PPL-002.5.3.3** Each annual course SHALL end with an assessment. The pass mark SHALL be 80%. A Workforce Member who fails 3 attempts SHALL complete an instructor-led session arranged by the CISO within 30 days.
- **PPL-002.5.3.4** The CISO SHALL deliver a cyber-risk oversight briefing to the Board of Directors or the Audit Committee every 12 months, satisfying the director training requirement in ISP-000.5.7.6.

### 5.4 Role-based training

- **PPL-002.5.4.1** Role-based training SHALL be completed every 12 months for developers, privileged users, incident responders, and staff handling PHI or cardholder data.
- **PPL-002.5.4.2** Initial role-based training SHALL be completed within 30 days of assignment to the role and before first use of a Privileged Account or first access to the CDE or ePHI.
- **PPL-002.5.4.3** Role-based curricula SHALL include, at a minimum:

| Audience | Minimum content | Owner of content |
|---|---|---|
| Developers and engineers who commit code | Secure coding practices for the languages in use, OWASP Top 10, secrets handling, software supply chain and SBOM, secure use of Generative AI coding assistants (SEC-010) | CTO |
| Privileged users | Privileged access rules, JIT and break-glass procedures, administrative workstation security, detection of misuse (SEC-005) | Head of Security Engineering |
| Incident responders | RES-002 procedures, evidence handling, communication protocols, breach notification roles (RES-003), tabletop participation | SOC Manager |
| `[HIPAA]` Staff handling PHI | Minimum Necessary, permitted uses and disclosures, ePHI safeguards, breach reporting (CMP-008) | HIPAA Security Officer, with the HIPAA Privacy Officer |
| `[PCI]` Staff handling cardholder data, with CDE access, or at locations with POI Devices | Cardholder data handling, SAD prohibition, point-of-interaction device inspection where applicable (SEC-019) | Head of Security Engineering |

- **PPL-002.5.4.4** The following roles SHALL also complete role-based training every 12 months:

| Audience | Minimum content | Owner of content |
|---|---|---|
| Executives and members of the ISSC | Governance accountabilities (GOV-001), Risk Acceptance (RSK-001), incident escalation and disclosure (RES-003) | CISO |
| IT Service Desk staff | Caller identity verification before password or MFA resets, social engineering targeting help desks | CIO |
| Finance staff with payment authority | Business Email Compromise, payment change verification (GOV-004.5.6.2) | CFO |
| `[GDPR]` `[CPRA]` Staff handling Data Subject Requests | CMP-010 procedure, identity verification, statutory deadlines | DPO |
| Asset Owners, Data Owners and System Owners | Their accountabilities in GOV-001, Access Reviews (SEC-003), classification (SEC-002) | Head of GRC |
| Business Continuity and DR team members | RES-004 and RES-005 roles and exercises | Business Continuity Manager |
| Workforce Members who build, procure or oversee AI Systems | AI Risk Classes, Human Oversight Modes, evaluation and monitoring, AI incident reporting (RSK-006) | CISO |
| Risk Owners and Workforce Members who perform risk assessments | Risk method, scoring, treatment and Risk Acceptance (RSK-001, RSK-002); required before first performing the role | Head of GRC |

- **PPL-002.5.4.5** Content owners SHALL provide or approve role-based content and SHALL review it every 12 months. The CISO SHALL assign role-based training based on role data from the HRIS and from the access groups that define privileged, CDE and ePHI access.

### 5.5 Phishing simulation

- **PPL-002.5.5.1** The CISO SHALL run phishing simulations at least quarterly, covering every Workforce Member with an Organization email account at least once in each quarter.
- **PPL-002.5.5.2** Simulations SHALL vary in difficulty and technique (for example credential harvesting, malicious attachments, QR codes, callback and SMS lures) and SHALL reflect current threats reported under RSK-005.
- **PPL-002.5.5.3** A Workforce Member who clicks a simulated lure or submits credentials SHALL be shown brief training at the time of the failure.
- **PPL-002.5.5.4** A Workforce Member who fails 3 or more simulations within 12 months SHALL complete remedial training within 14 days of the third failure, and their manager SHALL be informed.
- **PPL-002.5.5.5** Phishing simulation results SHALL NOT, on their own, be the basis for disciplinary action. Repeated failure after remedial training MAY be referred by the CISO to the CHRO for handling under CMP-007 as a Category 1 Violation.
- **PPL-002.5.5.6** Simulations using themes concerning compensation, benefits, health or Separation SHALL be approved in advance by the CHRO.
- **PPL-002.5.5.7** Individual simulation results SHALL be classified Confidential and accessible only to the security awareness team, the individual and their manager. Results reported under GOV-003 SHALL be aggregated.
- **PPL-002.5.5.8** Excluding any Workforce Member or group from simulations SHALL require written approval of the CISO, recorded with the reason and reviewed every 12 months.
- **PPL-002.5.5.9** `[GDPR]` The processing of simulation results SHALL be described in the Workforce Privacy Notice issued under CMP-005.

### 5.6 Ongoing awareness

- **PPL-002.5.6.1** The CISO SHALL issue security awareness communications to all Workforce Members at least monthly.
- **PPL-002.5.6.2** Where an active phishing or social engineering campaign is targeting the Organization, the SOC Manager SHALL issue an alert to affected Workforce Members within 1 business day of confirmation.
- **PPL-002.5.6.3** `[HIPAA]` Ongoing communications SHALL include security reminders as required by 45 CFR §164.308(a)(5)(ii)(A), issued at least quarterly to Workforce Members with access to ePHI.
- **PPL-002.5.6.4** The CISO SHALL run at least one awareness campaign per year on a theme selected from Security Incident trends or GOV-003 metrics.

### 5.7 Non-completion

- **PPL-002.5.7.1** The learning management system SHALL send reminders to the Workforce Member 7 days and 1 day before each training due date.
- **PPL-002.5.7.2** Overdue training SHALL be escalated: to the manager at 1 day overdue; to the relevant executive at 15 days overdue; and to the CHRO for action under CMP-007 at 30 days overdue.
- **PPL-002.5.7.3** A Workforce Member who has not completed training at hire SHALL NOT be granted access to Restricted data until it is completed.
- **PPL-002.5.7.4** [DECISION REQUIRED: Access consequence of overdue annual or role-based training. Recommended default: suspend access to Restricted data and Privileged Accounts at 30 days overdue until completion.] Access to Restricted data and Privileged Accounts SHALL be suspended for any Workforce Member whose annual or role-based training is more than 30 days overdue, until the training is completed.
- **PPL-002.5.7.5** Training due during an approved leave of absence SHALL be completed within 30 days of return (PPL-001).

### 5.8 Third Parties

- **PPL-002.5.8.1** Third Party personnel who hold Organization accounts SHALL complete the Organization's training at hire and annual training on the same timeframes as Workforce Members, unless the Head of GRC accepts Evidence of equivalent training provided by the Third Party.
- **PPL-002.5.8.2** Contracts with Third Parties whose personnel access Restricted data SHALL require security awareness training equivalent to this Policy, with Evidence available on request (RSK-003).

### 5.9 Records and effectiveness

- **PPL-002.5.9.1** Training records SHALL record the Workforce Member, course, course version, assignment date, completion date and assessment score, and SHALL be retained under CMP-004.
- **PPL-002.5.9.2** The CISO SHALL measure program effectiveness using the GOV-003 training and phishing metrics, and SHALL report to the ISSC every 12 months on trends, including Security Incidents attributed to human error.
- **PPL-002.5.9.3** The CISO SHALL survey a sample of Workforce Members every 12 months on training quality and relevance and SHALL use the results in the content review under PPL-002.5.1.2.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CISO | Owns this Policy; runs the program, phishing simulations and communications; assigns role-based training; reports effectiveness |
| ISSC | Approves this Policy and the annual program plan |
| CHRO | Provides HRIS data; acts on non-completion and repeated failures under CMP-007; approves sensitive simulation themes |
| CPO / GC | Review privacy and legal content before release |
| Content owners (CTO, CIO, CFO, Head of Security Engineering, SOC Manager, HIPAA Security Officer, HIPAA Privacy Officer, DPO, Head of GRC, Business Continuity Manager) | Provide and review role-based content every 12 months |
| SOC Manager | Issues alerts on active campaigns |
| Head of GRC | Accepts equivalent Third Party training Evidence |
| Managers | Ensure their teams complete training; act on escalations |
| Workforce Members | Complete assigned training on time; report phishing |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| PPL-002.7.1 | Training at hire | Within 30 days of start, and before access to Restricted data |
| PPL-002.7.2 | Annual training | Every 12 months, completed within 30 days of assignment |
| PPL-002.7.3 | Phishing simulation | At least quarterly |
| PPL-002.7.4 | Role-based training | Every 12 months for developers, privileged users, incident responders, and staff handling PHI or cardholder data |
| PPL-002.7.5 | Initial role-based training | Within 30 days of role assignment, and before first privileged, CDE or ePHI access |
| PPL-002.7.6 | Assessment pass mark | 80% |
| PPL-002.7.7 | Remedial training after 3 simulation failures in 12 months | Within 14 days of the third failure |
| PPL-002.7.8 | Awareness communications | At least monthly |
| PPL-002.7.9 | Alert on active campaign | Within 1 business day of confirmation |
| PPL-002.7.10 | `[HIPAA]` Security reminders to ePHI users | At least quarterly |
| PPL-002.7.11 | Overdue escalation | Manager at 1 day; executive at 15 days; CHRO at 30 days |
| PPL-002.7.12 | Access suspension for overdue training | Restricted data and Privileged Accounts at > 30 days overdue |
| PPL-002.7.13 | Content review | Every 12 months, and within 30 days of a trigger in PPL-002.5.1.2 |
| PPL-002.7.14 | Cyber-risk oversight briefing to the Board of Directors or Audit Committee | Every 12 months |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Annual training completion within the window (GOV-003 KPI-10) | GOV-003 thresholds | Monthly | CISO |
| New-hire training completion within 30 days (GOV-003 KPI-11) | GOV-003 thresholds | Monthly | CISO |
| Phishing click rate and report rate (GOV-003 KPI-12, KPI-13) | GOV-003 thresholds | Per campaign | CISO |
| Repeat phishing failures (GOV-003 KRI-11) | GOV-003 thresholds | Quarterly | CISO |
| Role-based training completion for each audience in section 5.4 | 100% | Quarterly | CISO |
| Workforce Members with Restricted data access before completing training at hire | 0 | Monthly | CISO |
| First-attempt assessment pass rate | ≥ 90% | Every 12 months | CISO |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003. No Exception MAY be
granted to PPL-002.5.2.1 (training before access to Restricted data) or to training required
by PCI DSS 12.6 `[PCI]` or 45 CFR §164.308(a)(5) `[HIPAA]`. Exclusions from phishing
simulations under PPL-002.5.5.8 are not Exceptions.

## 10. Enforcement

Non-compliance is handled under CMP-007. Failure to complete required training is escalated
under section 5.7 before referral under CMP-007.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| PPL-002.5.1 | 7.2, 7.3; A.6.3 | PR.AT-01 | AT-1, PM-13, PM-14 | 14.1 | CC1.4, CC2.2 | APO07.03 | `[PCI]` 12.6.1, 12.6.2 |
| PPL-002.5.2 – 5.3 | 7.3; A.6.3 | PR.AT-01 | AT-2, AT-4 | 14.1–14.8 | CC1.4, CC2.2 | APO07.03 | `[PCI]` 12.6.3, 12.6.3.2; `[HIPAA]` §164.308(a)(5); `[GDPR]` Art. 39(1)(b) |
| PPL-002.5.4 | 7.2; A.6.3 | PR.AT-02 | AT-3 | 14.9, 16.9 | CC1.4 | APO07.03 | `[PCI]` 6.2.2; `[HIPAA]` §164.308(a)(5); `[CPRA]` Cal. Civ. Code §1798.130(a)(6) |
| PPL-002.5.5 | A.6.3 | PR.AT-01 | AT-2(3) | 14.2 | CC1.4 | APO07.03 | `[PCI]` 12.6.3.1 |
| PPL-002.5.6 | A.6.3 | PR.AT-01 | AT-2 | 14.1 | CC2.2 | APO07.03 | `[HIPAA]` §164.308(a)(5)(ii)(A) |
| PPL-002.5.7 – 5.8 | 7.2; A.5.19, A.6.3 | GV.SC-05, PR.AT-01 | AT-2, PS-7 | 14.1 | CC1.4, CC9.2 | APO07 | — |
| PPL-002.5.9 | 7.2, 9.1 | PR.AT-01, ID.IM-01 | AT-4 | — | CC1.4 | APO07.03, MEA01 | — |

## 12. Related documents

ISP-000, GOV-001, GOV-002, GOV-003, GOV-004, RSK-003, RSK-005, CMP-004, CMP-005, CMP-006,
CMP-007, CMP-008, CMP-010, SEC-002, SEC-004, SEC-005, SEC-008, SEC-010, SEC-015, SEC-016,
SEC-019, RES-001, RES-002, RES-004, RES-005, PPL-001

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CISO | | | |
| Approver: ISSC Vice-Chair, on behalf of the ISSC (CISO recused as Document Owner under GOV-001.5.3.9) | | | |
