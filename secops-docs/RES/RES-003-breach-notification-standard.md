# RES-003 — Breach Notification Standard

## 1. Document control

| Field | Value |
|---|---|
| Document ID | RES-003 |
| Title | Breach Notification Standard |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 2 — Standard |
| Classification | Internal |
| Owner | Chief Privacy Officer (CPO) |
| Approver | Chief Information Security Officer (CISO), with General Counsel (GC) concurrence |
| Effective date | [DECISION REQUIRED: Date of CISO approval with GC concurrence] |
| Next review date | Effective date + 12 months, and within 30 days of any change to a notification obligation recorded in the Obligations Register (CMP-001) |
| Parent document | RES-001 Incident Response Policy |
| Related documents | RES-001, RES-002, CMP-001, CMP-004, CMP-005, CMP-008, CMP-009, RSK-003, TPL-006, TPL-007 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CPO | Initial release |

## 3. Purpose

This Standard sets how the Organization determines whether a Security Incident is a
notifiable breach, and how, when, by whom and to whom notification is made. It is the home
of every breach notification timeline in the suite: internal legal escalation, GDPR, HIPAA,
PCI DSS, SEC public disclosure, US state breach laws, and contractual notification to
customers. It also sets the process and decision rights for determining whether a Security
Incident is a Material Cybersecurity Incident `[SOX]`, and the documentation required when
the Organization decides not to notify.

## 4. Scope

- **People:** the CPO, GC, CISO, DPO, HIPAA Privacy Officer, HIPAA Security Officer, CFO, CEO, the Incident Response Team under RES-002, and every Workforce Member who handles a notification.
- **Systems:** all Information Systems and Cloud Services in scope of RES-001, and any Third-Party system that processes Organization Personal Data, PHI `[HIPAA]` or CHD `[PCI]`.
- **Data:** Personal Data (including Sensitive Personal Information), PHI `[HIPAA]`, CHD and SAD `[PCI]`, customer data processed under contract, and information about Security Incidents affecting Financially Significant Systems or the Organization's operations `[SOX]`.
- **Locations:** all jurisdictions recorded in the Obligations Register under CMP-001. The baseline covers the United States (federal and all states) and the EU/EEA. [DECISION REQUIRED: Additional jurisdictions in scope (decision #7). Recommended default: United States and EU/EEA; add UK GDPR and other local laws through the Obligations Register.]
- **Third parties:** Processors, Subprocessors, Business Associates `[HIPAA]` and other Third Parties that suffer a Security Incident involving Organization data, and Controllers and Covered Entities `[HIPAA]` to which the Organization owes notification as a Processor or Business Associate.
- **Out of scope:** the operational response to the Security Incident itself (RES-002), and Data Subject Requests (CMP-010).

## 5. Requirements

### 5.1 Internal escalation

- **RES-003.5.1.1** The Incident Commander under RES-002 SHALL notify the GC and the CPO within 24 hours of a Suspected Personal Data Breach (GOV-006).
- **RES-003.5.1.2** Because the GDPR Supervisory Authority deadline runs from awareness, the Incident Commander SHOULD notify the GC and CPO as soon as the suspicion arises and SHALL NOT wait for the end of the 24-hour limit where EU/EEA Personal Data may be involved `[GDPR]`.
- **RES-003.5.1.3** On receipt, the CPO SHALL notify: the DPO where EU/EEA Personal Data may be involved `[GDPR]`; the HIPAA Privacy Officer and HIPAA Security Officer where PHI may be involved `[HIPAA]`; and the account owner of any customer whose data may be involved.
- **RES-003.5.1.4** `[PCI]` The CISO SHALL notify the GC and CFO within 4 hours of any suspected compromise of CHD or SAD.
- **RES-003.5.1.5** `[SOX]` The CISO SHALL notify the GC and CFO within 24 hours of any Security Incident that is Sev-1 under RES-002, that affects a Financially Significant System, or that the CISO considers may be material, so that the materiality process in section 5.5 can begin.
- **RES-003.5.1.6** The CFO SHALL notify the Organization's cyber insurer within the time required by the insurance policy, and in any case within 72 hours of a Sev-1 declaration or a suspected Personal Data Breach affecting 500 or more individuals. [DECISION REQUIRED: Insurer notification target where the policy is silent. Recommended default: 72 hours.]
- **RES-003.5.1.7** Each escalation, its time and recipient SHALL be recorded in the TPL-006 incident record.

### 5.2 Breach determination process

- **RES-003.5.2.1** The CPO SHALL convene a breach determination group for every suspected Personal Data Breach within 24 hours of the CPO's notification under RES-003.5.1.1. The group SHALL comprise: the CPO (lead); the GC or Legal Lead; the CISO or Incident Commander; and, as applicable, the DPO `[GDPR]` and the HIPAA Privacy Officer `[HIPAA]`.
- **RES-003.5.2.2** The group SHALL establish and record: (a) the time of awareness or discovery under each applicable regime (RES-003.5.2.4); (b) the Organization's role for the affected data (Controller, Processor, Covered Entity, Business Associate, merchant or service provider); (c) the data elements and Classification Level involved; (d) the number of individuals and records, and their jurisdictions of residence; (e) whether the data was encrypted under SEC-006 and whether the key was also compromised; (f) the outcome of each applicable risk assessment in sections 5.3 to 5.5; and (g) the notifications required, with deadlines, under section 5.6.
- **RES-003.5.2.3** Where facts are incomplete, the group SHALL make a provisional determination based on the information available, set the earliest applicable deadline, and re-assess at least every 2 business days until a final determination is recorded. Incomplete facts SHALL NOT delay a notification whose deadline is approaching; the Organization SHALL notify in phases where the law permits (e.g. GDPR Art. 33(4)).
- **RES-003.5.2.4** The clock for each regime SHALL be recorded as follows:
  - `[GDPR]` Awareness: when the Organization has a reasonable degree of certainty that a Security Incident has occurred that has led to Personal Data being compromised, consistent with European Data Protection Board guidance. A short initial investigation to establish this SHALL NOT exceed 24 hours from the first indication.
  - `[HIPAA]` Discovery: the first day on which the breach is known to the Organization, or would have been known with the exercise of diligence, including knowledge of any Workforce Member or agent other than the person who committed the breach (45 CFR §164.404(a)(2)).
  - `[SOX]` The Form 8-K deadline runs from the date of the materiality determination under section 5.5, not from discovery.
  - US state laws: discovery or notification of the breach as defined by each applicable statute.
  - `[PCI]` Confirmation of compromise, as defined in section 5.6, or earlier suspicion where card brand rules or the acquirer agreement require it.
- **RES-003.5.2.5** Where the Organization is a Processor or Business Associate `[HIPAA]`, the group SHALL determine only the facts the Controller or Covered Entity needs, and SHALL NOT delay the notification to the Controller or Covered Entity in order to complete its own risk assessment.
- **RES-003.5.2.6** The final determination, signed by the CPO and GC, SHALL be recorded in the incident record and in the Breach Register maintained by the CPO.

### 5.3 GDPR risk to rights and freedoms `[GDPR]`

- **RES-003.5.3.1** `[GDPR]` For every Personal Data Breach where the Organization is Controller, the DPO SHALL assess the risk to the rights and freedoms of natural persons and classify it as: **no risk likely**, **risk**, or **high risk**.
- **RES-003.5.3.2** `[GDPR]` The assessment SHALL consider: the type of breach (Confidentiality, Integrity or Availability); the nature, sensitivity and volume of Personal Data, with special-category data, criminal offence data, government identifiers, financial account data and authentication Secrets treated as increasing risk; ease of identification of individuals; severity and permanence of consequences (e.g. identity theft, fraud, financial loss, discrimination, reputational damage, physical harm, loss of confidentiality of data protected by professional secrecy); special characteristics of the individuals (e.g. children, vulnerable persons); the number of individuals affected; and the special characteristics of the Controller.
- **RES-003.5.3.3** `[GDPR]` Outcomes:
  - **No risk likely:** no notification to the Supervisory Authority is required; the breach SHALL be documented under section 5.8.
  - **Risk:** the lead Supervisory Authority SHALL be notified under section 5.6.
  - **High risk:** the Supervisory Authority and the affected Data Subjects SHALL be notified under section 5.6, unless an exception in Art. 34(3) applies and is documented: the data was rendered unintelligible (e.g. encrypted with an uncompromised key); subsequent measures ensure the high risk is no longer likely to materialize; or individual communication would involve disproportionate effort, in which case a public communication SHALL be made instead.
- **RES-003.5.3.4** `[GDPR]` Where the assessment is uncertain between two outcomes, the higher-risk outcome SHALL be applied.
- **RES-003.5.3.5** `[GDPR]` Where processing is cross-border, the DPO SHALL notify the lead Supervisory Authority recorded under CMP-005.5.1.7, and SHALL notify the authorities of other affected Member States where no lead authority applies.

### 5.4 HIPAA four-factor risk assessment `[HIPAA]`

- **RES-003.5.4.1** `[HIPAA]` An acquisition, access, use or disclosure of PHI not permitted by the Privacy Rule SHALL be presumed to be a Breach unless one of the exclusions in 45 CFR §164.402(1) applies, or the HIPAA Privacy Officer documents a low probability that the PHI has been compromised based on a risk assessment of at least the following four factors:
  1. the nature and extent of the PHI involved, including the types of identifiers and the likelihood of re-identification;
  2. the unauthorized person who used the PHI or to whom the disclosure was made;
  3. whether the PHI was actually acquired or viewed; and
  4. the extent to which the risk to the PHI has been mitigated.
- **RES-003.5.4.2** `[HIPAA]` The exclusions in 45 CFR §164.402(1) (unintentional good-faith access by a Workforce Member within scope of authority; inadvertent disclosure between persons authorized at the same Covered Entity, Business Associate or organized health care arrangement; and a good-faith belief that the recipient could not reasonably have retained the information) SHALL be applied only with the HIPAA Privacy Officer's documented reasoning and the GC's concurrence.
- **RES-003.5.4.3** `[HIPAA]` PHI encrypted or destroyed in accordance with HHS guidance on rendering PHI unusable, unreadable or indecipherable is not Unsecured PHI, and its loss does not require notification, provided the key was not compromised. The HIPAA Security Officer SHALL confirm the Encryption status in writing.
- **RES-003.5.4.4** `[HIPAA]` Each factor SHALL be scored and reasoned in writing using the four-factor worksheet held in the Breach Register, and the overall conclusion (low probability of compromise / Breach) SHALL be signed by the HIPAA Privacy Officer and the GC.
- **RES-003.5.4.5** `[HIPAA]` Where the Organization is a Business Associate (decision #3 default), it SHALL notify the Covered Entity under section 5.6 regardless of its own four-factor conclusion unless the Business Associate Agreement assigns the risk assessment to the Organization; the four-factor assessment SHALL then be provided to the Covered Entity on request.

### 5.5 SEC materiality determination `[SOX]`

- **RES-003.5.5.1** `[SOX]` The Organization SHALL determine without unreasonable delay after discovery whether a Security Incident, or a series of related Security Incidents, is a Material Cybersecurity Incident.
- **RES-003.5.5.2** `[SOX]` A materiality assessment group SHALL be convened by the GC within 48 hours of an escalation under RES-003.5.1.5. It SHALL comprise the GC (chair), CFO, CISO and CPO, and SHALL be advised by outside securities counsel. The Internal Audit Director SHALL be informed of each convening.
- **RES-003.5.5.3** `[SOX]` The group SHALL assess, and record, both quantitative and qualitative factors, including: actual and reasonably likely impact on financial condition and results of operations; harm to reputation, customer and vendor relationships and competitiveness; the likelihood of litigation or regulatory investigation; operational disruption; the nature, scope and timing of the incident; the data involved; and whether there is a substantial likelihood that a reasonable investor would consider the information important in making an investment decision.
- **RES-003.5.5.4** `[SOX]` The materiality determination SHALL be made jointly by the CEO and the CFO, on the written recommendation of the materiality assessment group. The Audit Committee Chair SHALL be informed of the determination before any Form 8-K is filed, and in any case within 24 hours of the determination.
- **RES-003.5.5.5** `[SOX]` Where the group cannot yet make a recommendation, it SHALL re-convene at least every 5 business days, and SHALL record what further facts are needed. Lack of complete information SHALL NOT by itself postpone a determination where the available facts establish materiality.
- **RES-003.5.5.6** `[SOX]` A determination that an incident is not material SHALL record the reasons and SHALL be re-assessed if new facts emerge, including facts about related incidents that may be material in aggregate.
- **RES-003.5.5.7** `[SOX]` The materiality determination is distinct from the Severity Level under RES-002 and from the breach determinations in sections 5.3 and 5.4.
- **RES-003.5.5.8** `[SOX]` Disclosure of cybersecurity risk management, strategy and governance in the annual report (Regulation S-K Item 106) is outside the scope of this Standard and is coordinated by the GC and CFO with the CISO.

### 5.6 Notification requirements by regulation

- **RES-003.5.6.1** The Organization SHALL make each notification below that applies, as determined under section 5.2, within the deadline stated. Where more than one regime applies, each deadline SHALL be met independently.
- **RES-003.5.6.2** Notification table:

| # | Regime | Trigger | Recipient | Deadline | Required content | Responsible role | Approver |
|---|---|---|---|---|---|---|---|
| N1 | Internal legal escalation | Suspected Personal Data Breach | GC and CPO | Within 24 hours of suspicion | Facts known, data types, systems, estimated individuals | Incident Commander | — |
| N2 | `[GDPR]` Controller to Supervisory Authority (Art. 33) | Personal Data Breach assessed as "risk" or "high risk" | Lead Supervisory Authority | Within 72 hours of awareness; if later, with reasons for delay | Template A (section 5.7) | DPO | CPO and GC |
| N3 | `[GDPR]` Controller to Data Subjects (Art. 34) | Personal Data Breach assessed as "high risk", no Art. 34(3) exception | Affected Data Subjects | Without undue delay where risk is high | Template B | CPO | CPO and GC |
| N4 | `[GDPR]` Processor to Controller (Art. 33(2)) | Personal Data Breach in data processed for a Controller | Controller's designated contact | Within 24 hours of awareness, or sooner if the Data Processing Agreement requires | Template E | CPO | GC |
| N5 | `[HIPAA]` Covered Entity to individuals (§164.404) | Breach of Unsecured PHI | Affected individuals (or next of kin / personal representative) | Within 60 days of discovery | Template B (HIPAA elements) | HIPAA Privacy Officer | CPO and GC |
| N6 | `[HIPAA]` Covered Entity to HHS (§164.408) | Breach of Unsecured PHI | Secretary of HHS via the HHS breach portal | Concurrently with individual notice if ≥ 500 individuals; otherwise within 60 days after the end of the calendar year in which the breach was discovered | Template C | HIPAA Privacy Officer | CPO and GC |
| N7 | `[HIPAA]` Covered Entity to media (§164.406) | Breach of Unsecured PHI involving > 500 residents of a state or jurisdiction | Prominent media outlets serving that state or jurisdiction | Within 60 days of discovery | Template B (HIPAA elements) as a press release | Communications Lead (RES-002) with HIPAA Privacy Officer | CEO, CPO and GC |
| N8 | `[HIPAA]` Business Associate to Covered Entity (§164.410) | Breach of Unsecured PHI held as Business Associate | Covered Entity's designated contact | Within 10 business days of discovery, or sooner by contract | Template D | HIPAA Privacy Officer | GC |
| N9 | `[PCI]` Payment card compromise | Confirmed (or, where brand rules require, suspected) compromise of CHD or SAD | Acquirer(s) and each affected payment brand, per brand rules | Per brand rules; internal target within 24 hours of confirmed compromise | Template F | CISO | GC and CFO |
| N10 | `[SOX]` Public disclosure (Form 8-K Item 1.05) | Determination under section 5.5 that an incident is a Material Cybersecurity Incident | SEC (public filing) | Within 4 business days of determining the incident is material; Form 8-K/A within 4 business days after any required information that was not determined or available at filing becomes so | Template G | GC | CEO and CFO |
| N11 | US state breach laws `[CPRA]` | Breach of "personal information" as defined by each applicable state law, for residents of that state | Affected residents; state attorney general or regulator where required; consumer reporting agencies where required | Internal target 30 days from discovery, or the shortest applicable statutory deadline if shorter | Template B (state elements) | CPO | CPO and GC |
| N12 | Contractual — customers | Security Incident affecting a customer's data or services, as defined in the customer contract | Customer's designated contact | The contractual deadline; where the contract is silent, within 72 hours of confirming that the customer's data was affected [DECISION REQUIRED: Default customer notification time where the contract is silent. Recommended default: 72 hours of confirmation] | Template E | CPO with the customer account owner | GC |
| N13 | Contractual — cyber insurer | Incident that may give rise to a claim | Insurer's claims contact | Per RES-003.5.1.6 | Per policy | CFO | CFO |
| N14 | Contractual — other parties | Partners, financing parties, licensors or other Third Parties with notification clauses | As per contract | As per contract | As per contract | GC | GC |
| N15 | Other regimes in the Obligations Register | Any other notification obligation recorded under CMP-001 (e.g. NIS2 early warning within 24 hours and notification within 72 hours for in-scope entities; sector regulators; UK GDPR) | As recorded | As recorded | As recorded | As recorded in CMP-001 | CPO and GC |

- **RES-003.5.6.3** `[CPRA]` For US state breach laws, the CPO SHALL maintain a state law matrix in the Obligations Register listing, for each state: the definition of personal information; any encryption safe harbor; any risk-of-harm threshold; the statutory deadline; attorney general or regulator notification thresholds and forms; consumer reporting agency notification thresholds; required notice content; and any requirement to offer identity theft protection services. The matrix SHALL be reviewed every 12 months and within 30 days of any change in a state law.
- **RES-003.5.6.4** `[CPRA]` Where notification is required to residents of more than one state, the Organization SHALL notify all affected residents on the timeline of the shortest applicable deadline, using a notice whose content satisfies every applicable state, unless the GC approves state-specific notices.
- **RES-003.5.6.5** `[CPRA]` Notifications to California residents SHALL use the headings and content required by Cal. Civ. Code §1798.82(d), and a sample copy SHALL be submitted to the California Attorney General where more than 500 California residents are notified.
- **RES-003.5.6.6** `[CPRA]` Where a breach exposes government identifiers (e.g. Social Security numbers or driver's license numbers), the Organization SHALL offer identity theft prevention and mitigation services at no cost for at least the longest period required by any applicable state law. [DECISION REQUIRED: Standard offer period. Recommended default: 24 months.]
- **RES-003.5.6.7** `[HIPAA]` Individual notices SHALL be sent by first-class mail, or by email where the individual has agreed to electronic notice. Where contact information is insufficient or out of date for 10 or more individuals, substitute notice SHALL be given by a conspicuous posting on the Organization's website for 90 days or by major print or broadcast media, with a toll-free number active for at least 90 days (45 CFR §164.404(d)).
- **RES-003.5.6.8** `[HIPAA]` The HIPAA Privacy Officer SHALL maintain a log of all Breaches affecting fewer than 500 individuals and SHALL submit it to HHS within 60 days after the end of each calendar year.
- **RES-003.5.6.9** `[PCI]` On a Confirmed Compromise (GOV-006), the CISO SHALL comply with any instruction from the acquirer or payment brand on forensic investigation and reporting, as coordinated under RES-001.5.6.7.
- **RES-003.5.6.10** Notifications SHALL be sent by a channel that produces a record of sending and, where available, acknowledgement (e.g. regulator portal confirmation, registered mail, delivery receipts), and each SHALL be recorded in TPL-006.

### 5.7 Notification content templates

- **RES-003.5.7.1** The CPO SHALL maintain the following templates, pre-approved by the GC and reviewed every 12 months. Each notification SHALL be prepared from the applicable template and approved as set out in RES-003.5.6.2 before it is sent.
- **RES-003.5.7.2** Notices to individuals SHALL be written in plain language, SHALL NOT include information that would aid an attacker, and SHALL be available in the languages of the affected individuals' jurisdictions where the law requires.

**Template A — Supervisory Authority notification `[GDPR]` (Art. 33(3))**

| Element | Content |
|---|---|
| Controller | Legal entity name, registration, main establishment |
| Contact point | Name and contact details of the DPO or other contact point |
| Timing | Date and time of breach (or estimate), date and time of awareness; reasons for any delay beyond 72 hours |
| Nature of the breach | Description; Confidentiality / Integrity / Availability; how it occurred |
| Data subjects | Categories and approximate number of Data Subjects concerned |
| Personal Data | Categories and approximate number of Personal Data records concerned, including any special-category data |
| Likely consequences | Assessed consequences for Data Subjects and the risk level from section 5.3 |
| Measures | Measures taken or proposed to address the breach and mitigate adverse effects |
| Data Subject communication | Whether Data Subjects have been or will be informed, and if not, why |
| Cross-border | Other Member States concerned; other authorities notified |
| Phasing | Whether this is an initial, follow-up or final notification |

**Template B — Notice to individuals (`[GDPR]` Art. 34, `[HIPAA]` §164.404(c), state laws `[CPRA]`)**

| Heading | Content |
|---|---|
| What happened | Brief description, including the date of the breach and the date of discovery (if known) |
| What information was involved | The types of Personal Data or PHI involved (e.g. name, Social Security number, date of birth, diagnosis, account number) |
| What we are doing | Steps the Organization has taken to investigate, mitigate harm and protect against further breaches |
| What you can do | Steps the individual should take to protect themselves (e.g. password change, fraud alerts, credit freeze, monitoring statements); details of any identity protection service offered and how to enroll |
| Likely consequences `[GDPR]` | The likely consequences of the breach |
| For more information | Contact procedures, which SHALL include a toll-free telephone number, an email address, website or postal address `[HIPAA]`; the DPO's contact details `[GDPR]`; contact details for consumer reporting agencies and the relevant regulator where state law requires `[CPRA]` |

**Template C — HHS breach report `[HIPAA]`** — Prepared as the content of the HHS breach portal submission: Covered Entity details and contact; whether a Business Associate was involved and its details; date of breach and date of discovery; approximate number of individuals; type of breach (e.g. hacking/IT incident, unauthorized access or disclosure, theft, loss, improper disposal); location of breached information (e.g. network server, email, laptop, paper); types of PHI involved; safeguards in place before the breach; dates individual notice was provided; whether substitute notice and media notice were required; actions taken in response.

**Template D — Business Associate to Covered Entity notice `[HIPAA]` (§164.410)** — Identification of each individual whose Unsecured PHI has been, or is reasonably believed by the Organization to have been, accessed, acquired, used or disclosed (to the extent possible); date of breach and of discovery; description of what happened; types of PHI involved; mitigation steps taken; contact person; and any other information the Covered Entity needs for its notices under §164.404, supplied as it becomes available.

**Template E — Notice to Controller or customer (Processor or contractual notice)** — Nature of the incident; date and time of incident and of awareness; categories and approximate numbers of Data Subjects and records affected for that customer; systems and services involved; likely consequences; measures taken and proposed; Organization contact point (CPO or DPO); next update time; information the customer needs for its own regulatory notifications; any assistance offered under the contract or Data Processing Agreement.

**Template F — Acquirer and payment brand notice `[PCI]`** — Merchant or service provider identifiers; date of suspected or confirmed compromise and of detection; description of the incident and CDE components affected; estimated number of accounts and card brands involved; date range of potentially exposed transactions; whether SAD may have been exposed; containment actions taken; PFI engagement status; Organization contact point; and any additional fields required by the acquirer or brand.

**Template G — Form 8-K Item 1.05 disclosure outline `[SOX]`** — The material aspects of the nature, scope and timing of the incident; and the material impact or reasonably likely material impact on the Organization, including its financial condition and results of operations. The disclosure SHALL NOT include specific technical information about planned response or the Organization's systems, networks, devices or potential Vulnerabilities in such detail as would impede the response or remediation. Where required information is not determined or unavailable at filing, the filing SHALL say so and a Form 8-K/A SHALL follow under RES-003.5.6.2 (N10).

### 5.8 Documentation of decisions not to notify

- **RES-003.5.8.1** Every suspected Personal Data Breach, whether or not notified, SHALL be recorded in the Breach Register maintained by the CPO with: the facts; effects; remedial action; the determination under section 5.2; each risk assessment under sections 5.3 to 5.5; each notification made or not made; and the reasons.
- **RES-003.5.8.2** `[GDPR]` The Breach Register SHALL meet Art. 33(5), so that the Supervisory Authority can verify compliance with Art. 33, and SHALL be provided to the authority on request.
- **RES-003.5.8.3** `[HIPAA]` Where the Organization concludes that an impermissible use or disclosure is not a Breach, the four-factor assessment, exclusion reasoning or Encryption confirmation SHALL be documented to meet the burden of proof in 45 CFR §164.414.
- **RES-003.5.8.4** `[SOX]` Each non-materiality determination, its reasons, the attendees of the materiality assessment group and the CEO's and CFO's sign-off SHALL be documented and retained.
- **RES-003.5.8.5** A decision not to notify under any regime SHALL be signed by the CPO and the GC. A decision not to notify where the GC and CPO disagree SHALL be escalated to the CEO, whose decision SHALL be recorded.
- **RES-003.5.8.6** A decision to delay notification at the request of law enforcement SHALL be documented with the requesting agency, officer, date, the stated reason and the requested period, and SHALL be applied only to the extent the applicable law permits (e.g. 45 CFR §164.412 `[HIPAA]`; the Attorney General national security or public safety delay under Form 8-K Item 1.05 `[SOX]`). The GC SHALL diary the end of each delay period.
- **RES-003.5.8.7** Breach Register entries, determinations and notification records SHALL be retained for the period for incident records in CMP-004, and SHALL be subject to any Legal Hold.

### 5.9 Third-Party breaches

- **RES-003.5.9.1** Where a Processor, Business Associate or other Third Party notifies the Organization of a Security Incident involving Organization data, the Organization's notification clocks as Controller or Covered Entity SHALL be treated as starting from receipt of that notice, unless facts show the Organization was aware earlier.
- **RES-003.5.9.2** Contracts with Third Parties processing Personal Data, PHI `[HIPAA]` or CHD `[PCI]` SHALL require notification to the Organization within the time in the RSK-003.5.4.1 contract clauses, which the Head of Procurement SHALL confirm allows the Organization to meet its own deadlines in section 5.6.
- **RES-003.5.9.3** The Organization SHALL NOT rely on a Third Party to make notifications on its behalf unless the arrangement is written, approved by the GC, and the Organization reviews and approves the notice content before it is sent.

### 5.10 Readiness

- **RES-003.5.10.1** The CPO SHALL maintain, and verify every 12 months, the contact details and submission methods for: each Supervisory Authority in scope `[GDPR]`; the HHS breach portal `[HIPAA]`; each acquirer and payment brand `[PCI]`; state attorneys general and regulators `[CPRA]`; consumer reporting agencies; and the cyber insurer.
- **RES-003.5.10.2** The CPO SHALL maintain pre-arranged capacity for mass individual notification (e.g. a contracted notification mailing, call center and identity protection provider) able to begin mailing within 5 business days of a decision to notify. [DECISION REQUIRED: Whether to pre-contract notification services. Recommended default: yes, through outside counsel or the cyber insurer's panel.]
- **RES-003.5.10.3** The breach determination and notification process SHALL be exercised at least as part of the annual incident response exercise under RES-002, including at least one scenario involving Personal Data.
- **RES-003.5.10.4** Workforce Members in the roles listed in section 6 SHALL complete the role-based training required by PPL-002.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CPO | Owns this Standard; leads breach determination; maintains the Breach Register, state law matrix, templates and contacts; approves notifications as set out in section 5.6. |
| GC | Concurs in this Standard; member of the breach determination group; chairs the materiality assessment group `[SOX]`; approves notifications and decisions not to notify; handles law enforcement delay requests; leads Form 8-K preparation `[SOX]`. |
| CISO | Approves this Standard; provides incident facts; member of the breach determination and materiality assessment groups; leads `[PCI]` acquirer and brand notification. |
| DPO `[GDPR]` | Performs the risk to rights and freedoms assessment; identifies the lead Supervisory Authority; submits Supervisory Authority notifications; acts as contact point. |
| HIPAA Privacy Officer `[HIPAA]` | Performs the four-factor risk assessment; makes individual, HHS, media and Business Associate notifications; maintains the < 500 breach log. |
| HIPAA Security Officer `[HIPAA]` | Confirms Encryption status of PHI; supports the four-factor assessment. |
| CEO and CFO `[SOX]` | Jointly make the materiality determination; approve Form 8-K filings. |
| CFO | Member of the materiality assessment group `[SOX]`; notifies the cyber insurer; co-approves `[PCI]` notifications. |
| Audit Committee Chair `[SOX]` | Receives the materiality determination before filing. |
| Incident Commander (RES-002) | Makes the internal escalation in RES-003.5.1.1; supplies facts to the determination groups. |
| Head of Procurement | Ensures Third-Party contracts contain notification terms under RES-003.5.9.2. |
| Customer account owners | Provide customer contract notification terms and contacts; co-ordinate customer notices with the CPO. |

Role names and accountabilities are established in GOV-001 and consolidated in REF-002.

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| RES-003.7.1 | Internal legal escalation | GC and CPO notified within 24 hours of a suspected personal-data breach |
| RES-003.7.2 | `[GDPR]` notification | Supervisory authority within 72 hours of awareness; data subjects without undue delay where risk is high; as processor, notify controller within 24 hours |
| RES-003.7.3 | `[HIPAA]` notification | Individuals within 60 days of discovery; HHS concurrently if ≥ 500 individuals, otherwise within 60 days after calendar-year end; media if > 500 residents of a state or jurisdiction; as business associate, notify covered entity within 10 business days (or sooner by contract) |
| RES-003.7.4 | `[PCI]` notification | Acquirer and payment brands per brand rules, internal target within 24 hours of confirmed compromise |
| RES-003.7.5 | `[SOX]` public disclosure | Form 8-K Item 1.05 within 4 business days of determining an incident is material |
| RES-003.7.6 | US state breach laws `[CPRA]` | Internal target 30 days from discovery, or the shortest applicable statutory deadline if shorter |
| RES-003.7.7 | Breach determination group convened | Within 24 hours of the CPO's notification |
| RES-003.7.8 | `[GDPR]` Initial investigation to establish awareness | Not more than 24 hours from first indication |
| RES-003.7.9 | Provisional determination re-assessment | At least every 2 business days until final |
| RES-003.7.10 | `[PCI]` Internal escalation of suspected CHD compromise to GC and CFO | Within 4 hours |
| RES-003.7.11 | `[SOX]` Escalation of potentially material incidents to GC and CFO | Within 24 hours |
| RES-003.7.12 | `[SOX]` Materiality assessment group convened | Within 48 hours of escalation; re-convened at least every 5 business days until determination |
| RES-003.7.13 | `[SOX]` Audit Committee Chair informed of determination | Before any Form 8-K filing, and within 24 hours of the determination |
| RES-003.7.14 | Cyber insurer notification where the policy is silent | Within 72 hours of Sev-1 declaration or a suspected Personal Data Breach of ≥ 500 individuals |
| RES-003.7.15 | Customer notification where the contract is silent | Within 72 hours of confirming the customer's data was affected |
| RES-003.7.16 | Third-Party notification to the Organization (contract term) | Per the contract clauses in RSK-003.5.4.1 |
| RES-003.7.17 | `[CPRA]` Identity protection services offered when government identifiers are exposed | At least 24 months, or longer if required by state law |
| RES-003.7.18 | Mass notification capacity | Mailing able to begin within 5 business days of a decision to notify |
| RES-003.7.19 | Templates, state law matrix, regulator and insurer contacts review | Every 12 months; state law matrix also within 30 days of a law change |
| RES-003.7.20 | Breach Register and notification record retention | As set in CMP-004 for incident records |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Suspected Personal Data Breaches escalated to GC and CPO within 24 hours | 100% | Monthly | CPO |
| Breach determination group convened within 24 hours of CPO notification | 100% | Quarterly | CPO |
| Regulatory and individual notifications made within the deadlines in section 5.6 | 100% | Quarterly | CPO |
| `[GDPR]` Supervisory Authority notifications made after 72 hours (with reasons) | 0 | Quarterly | DPO |
| `[HIPAA]` Annual < 500 breach log submitted to HHS within 60 days of year end | Yes | Annually | HIPAA Privacy Officer |
| `[SOX]` Potentially material incidents with materiality group convened within 48 hours | 100% | Quarterly | GC |
| Suspected breaches with a complete Breach Register entry (sampled) | 100% | Quarterly | CPO |
| Decisions not to notify signed by both CPO and GC | 100% | Quarterly | GC |
| `[CPRA]` State law matrix reviewed within 12 months | Yes | Annually | CPO |
| Third-Party contracts (Personal Data, PHI, CHD) with the notification clause in RES-003.5.9.2 | 100% of new and renewed contracts | Quarterly | Head of Procurement |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

Statutory and regulatory notification deadlines in section 5.6 (N2 to N11) SHALL NOT
receive an Exception. Contractual deadlines (N12 to N14) may be varied only by contract
amendment approved by the GC.

## 10. Enforcement

Non-compliance is handled under CMP-007.

Concealing a suspected breach, delaying escalation beyond the limits in section 5.1, or
making an unauthorized notification or public statement SHALL be treated as serious
violations under CMP-007.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| RES-003.5.1 | A.5.24, A.5.26 | RS.MA-01, RS.CO-02 | IR-6 | 17.2, 17.6 | CC2.2, CC7.4 | DSS02 | `[GDPR]` Art. 33(1); `[HIPAA]` §164.404(a)(2) |
| RES-003.5.2 – 5.3 | A.5.25, A.5.34 | RS.AN-03, RS.MA-03 | IR-4, IR-6 | 17.9 | CC7.3, P6.6 | APO12, MEA03 | `[GDPR]` Arts. 4(12), 33, 34, 56 |
| RES-003.5.4 | A.5.25, A.5.34 | RS.AN-03 | IR-4, IR-6 | 17.9 | CC7.3, P6.6 | MEA03 | `[HIPAA]` §§164.402, 164.414 |
| RES-003.5.5 | A.5.31 | GV.OC-03, RS.CO-03 | IR-6 | — | CC2.3 | MEA03, EDM05 | `[SOX]` Form 8-K Item 1.05; Reg. S-K Item 106 (17 CFR 229.106); SOX §302 |
| RES-003.5.6 | A.5.5, A.5.26, A.5.31, A.5.34 | RS.CO-02, RS.CO-03, RC.CO-03, RC.CO-04 | IR-6 | 17.6 | CC2.3, P6.6 | MEA03 | `[GDPR]` Arts. 33, 34; `[HIPAA]` §§164.404–164.410; `[PCI]` 12.10.1; `[SOX]` Form 8-K Item 1.05; `[CPRA]` Cal. Civ. Code §1798.82 |
| RES-003.5.7 | A.5.26, A.5.34 | RS.CO-03 | IR-6 | 17.6 | CC2.3, P6.6 | MEA03 | `[GDPR]` Arts. 33(3), 34(2); `[HIPAA]` §§164.404(c), 164.410(c); `[CPRA]` Cal. Civ. Code §1798.82(d) |
| RES-003.5.8 | A.5.27, A.5.33 | ID.IM-01 | IR-4, IR-5 | 17.8 | CC7.4, P6.6 | MEA03 | `[GDPR]` Art. 33(5); `[HIPAA]` §§164.412, 164.414 |
| RES-003.5.9 | A.5.19, A.5.20 | GV.SC-05, GV.SC-08 | SR-8, IR-6 | 15.4 | CC9.2 | APO10 | `[GDPR]` Art. 28(3)(f), 33(2); `[HIPAA]` §164.504(e) |
| RES-003.5.10 | A.5.24, A.5.5 | ID.IM-04, PR.AT-02 | IR-2, IR-3 | 17.2, 17.7 | CC2.3 | DSS02 | `[PCI]` 12.10.2 |

## 12. Related documents

ISP-000, GOV-001, GOV-006, CMP-001, CMP-003, CMP-004, CMP-005, CMP-007, CMP-008, CMP-009, CMP-010, RSK-003, SEC-006, PPL-002, RES-001, RES-002, RES-004, TPL-006, TPL-007, REF-001, REF-002

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CPO | | | |
| Approver: CISO | | | |
| Concurrence: GC | | | |
