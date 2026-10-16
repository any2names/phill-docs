# CMP-004 — Evidence Management & Records Retention Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | CMP-004 |
| Title | Evidence Management & Records Retention Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Head of GRC |
| Approver | Information Security Steering Committee (ISSC), with General Counsel (GC) concurrence |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-002, CMP-001, CMP-002, CMP-003, CMP-005, CMP-006, CMP-007, CMP-008, CMP-009, CMP-010, SEC-002, SEC-003, SEC-006, SEC-012, SEC-016, SEC-017, SEC-018, SEC-019, RES-002, RES-003 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Head of GRC | Initial release |

## 3. Purpose

This Policy is the single home of every records retention period in the Information
Security & GRC Policy Suite. It sets how long each class of record is kept, when and how it
is destroyed, and how retention is suspended by Legal Hold. It also sets the requirements for
collecting, storing, protecting and producing Evidence, so that Evidence can be relied on by
Internal Audit, External Auditors, QSAs and regulators, and forensic Evidence remains
admissible.

## 4. Scope

- **People:** All Workforce Members who create, collect, store, access or dispose of records
  or Evidence, and in particular Control Owners, Data Owners, System Owners, Data Custodians,
  incident responders and Internal Audit.
- **Records:** All records created or received in the course of the Information Security
  Program, the compliance program and privacy program, in any format (electronic, paper,
  audio, video), including policy documents, Evidence, logs, registers, assessments,
  contracts, case files, Backups and Personal Data held in Information Systems.
- **Systems:** All Information Systems and Cloud Services that store such records, including
  the Evidence repository, the GRC tool, log platforms (SEC-012), Backup systems (SEC-018),
  ticketing systems, HR case-management systems and physical archives.
- **Locations:** All Organization sites, remote work locations and Third-Party facilities.
- **Third Parties:** Third Parties that hold records on the Organization's behalf, through
  contractual flow-down under RSK-003.
- **Not covered:** General business records with no security, privacy or compliance purpose
  (for example, sales or marketing records) are retained under the Organization's corporate
  records schedule maintained by the GC, except that Personal Data in them is governed by
  CMP-004.5.2 row R-12 and CMP-005.

## 5. Policy statements

### 5.1 Retention governance

- **CMP-004.5.1.1** Every record within scope SHALL be assigned to a record class in the retention schedule (CMP-004.5.2). A record that fits more than one class SHALL be retained for the longest applicable period, except that Personal Data SHALL NOT be retained beyond its class period solely because it appears in another record.
- **CMP-004.5.1.2** Retention periods in this Policy are minimums for compliance and audit purposes and, for Personal Data and Cardholder Data, also maximums. Records SHALL NOT be retained beyond the stated period unless a Legal Hold applies or the GC approves a longer period in writing, recorded in the retention schedule with its legal basis.
- **CMP-004.5.1.3** Where an applicable law, regulation or binding contract recorded in the Obligations Register (CMP-001) requires a longer period than this Policy, the longer period SHALL apply. The Head of GRC SHALL add the requirement to the schedule within 30 days of it being recorded in the Obligations Register.
- **CMP-004.5.1.4** Retention periods SHALL start from the trigger event stated in the schedule. Where no trigger is stated, the period starts on the date the record was created.
- **CMP-004.5.1.5** Each record class SHALL have a Record Owner, being the role named in the schedule. The Record Owner is accountable for retention, protection and disposal of records in that class.
- **CMP-004.5.1.6** The Head of GRC SHALL review the retention schedule every 12 months and within 30 days of a new or changed legal obligation affecting retention. Changes SHALL require GC concurrence before approval under GOV-002.
- **CMP-004.5.1.7** No other suite document SHALL set a retention period. Suite documents SHALL cite this Policy and the record class.

### 5.2 Retention schedule

- **CMP-004.5.2.1** Records SHALL be retained for the periods in the following schedule.

| Row | Record class | Examples | Retention period | Trigger / notes | Record Owner |
|---|---|---|---|---|---|
| R-01 | Policy documents and prior versions | ISP, GOV, RSK, CMP, SEC, RES, PPL, TPL and REF documents; approval records; Privacy Notices; Configuration Baselines | 7 years after superseded | From the date the version is superseded or retired | Head of GRC |
| R-02 | Control evidence, audit workpapers, access reviews | Control operation Evidence; Internal Audit plans, workpapers, reports and Issue Register (CMP-002); External Auditor and QSA requests and responses; Access Reviews (TPL-008); change records (SEC-013); vulnerability scan and Penetration Test reports (SEC-011); restore test results (SEC-018); `[HIPAA]` risk analyses and evaluations (CMP-001, CMP-008) | 7 years | From the end of the period the Evidence relates to (for audits, from the report date) | Control Owner; Internal Audit Director for audit records |
| R-03 | Security logs | Information System, network, security tool, authentication and audit logs (SEC-012) | 12 months minimum, of which the most recent 90 days immediately available; `[HIPAA]` logs from ePHI systems 6 years | From log event time | SOC Manager |
| R-04 | Incident records and Post-Incident Reviews | Incident tickets, TPL-006, TPL-007, forensic images and chain-of-custody records, `[GDPR]` Art. 33(5) breach record, notification records (RES-003) | 7 years after closure | From incident closure | SOC Manager; CPO for notification records |
| R-05 | Risk register entries, risk acceptances, exceptions | TPL-001 entries, TPL-002, TPL-003 and the Exception Register (CMP-003) | 7 years after closure or expiry | From closure, expiry or revocation | Head of GRC |
| R-06 | Training records and policy acknowledgements | Training completion, phishing simulation results, TPL-009 | Employment or engagement + 7 years | From Separation | CHRO (training: CISO) |
| R-07 | Third-party assessments and contracts | TPL-004, due-diligence files, contracts, Data Processing Agreements, `[HIPAA]` BAAs, `[GDPR]` executed SCCs, `[PCI]` service provider AOCs | Contract term + 7 years | From contract end | Head of Procurement; Head of GRC for assessments |
| R-08 | Data subject request records | DSR tickets, identity verification records, responses (CMP-010) | 3 years after closure | From DSR closure. Identity documents collected solely for verification are deleted within 30 days of closure (CMP-004.5.2.3) | DPO |
| R-09 | Whistleblower reports | Reports, case files, investigation reports, decisions (CMP-006) | 7 years after closure | From case closure. Personal Data unrelated to the report is deleted on receipt (CMP-004.5.2.4) | GC |
| R-10 | Backups | Backup sets (SEC-018) | Daily 35 days · monthly 13 months · `[SOX]` year-end backups of financially significant systems 7 years | From Backup creation | CIO |
| R-11 | CCTV recordings / visitor logs | Site CCTV footage; visitor registers (SEC-016) | 90 days / 12 months | From recording / visit date | Head of Facilities |
| R-12 | Personal data | Personal Data held in any Information System | Per the purpose in the ROPA; deleted or anonymized within 30 days after the purpose ends, unless under legal hold | Purpose and period recorded per processing activity in TPL-010 (CMP-005) | Data Owner |
| R-13 | `[PCI]` Cardholder data | PAN and associated CHD | Only as long as the documented business need; purge process run at least every 3 months; sensitive authentication data never stored after authorization | Business need documented in SEC-019 | Head of Security Engineering |
| R-14 | Compliance program records | Obligations Register and versions, regulatory change log and impact assessments, Compliance Calendar, certification register, management assertions, regulator correspondence (CMP-001) | 7 years after superseded or closed | From supersession (registers) or closure (correspondence) | Head of GRC |
| R-15 | Assurance reports | SOC 2 Type II reports, Bridge Letters, `[PCI]` ROCs, SAQs and AOCs, ASV reports, ISO/IEC 27001 audit reports | 7 years | From report date | Head of GRC |
| R-16 | Governance minutes and decisions | ISSC minutes and decision records; metrics reports (GOV-003) | 7 years | From meeting date | Head of GRC |
| R-17 | Board of Directors and Audit Committee minutes and papers | Minutes, approvals of ISP-000 and CMP-002/CMP-006, `[SOX]` §301 complaint reports to the Audit Committee | Permanent | — | GC |
| R-18 | Privacy accountability records | ROPA versions (TPL-010), DPIAs (TPL-005), Legitimate Interests Assessments, Transfer Impact Assessments | Life of the processing activity + 7 years | From the end of the processing activity; superseded versions per R-01 | DPO |
| R-19 | Consent and preference records | Consent records, withdrawals, `[CPRA]` opt-out and limit-use records, Opt-out Preference Signal records (CMP-005) | Life of the consent or preference + 3 years | From withdrawal, expiry or end of the processing relying on it | DPO |
| R-20 | HR disciplinary and enforcement case records | CMP-007 case files, sanctions, appeals | Employment or engagement + 7 years | From Separation. `[HIPAA]` sanction documentation is never kept less than 6 years from creation (45 CFR §164.316(b)(2)(i)) | CHRO |
| R-21 | Asset, media and disposal records | Asset Inventory history (SEC-001), certificates of Media Sanitization and destruction (SEC-017), disposal logs | 7 years | From disposal or decommissioning date | CIO |
| R-22 | Cryptographic key management records | Key inventory, key ceremony records, Key Custodian acknowledgements (SEC-006) | 7 years after key destruction | From key destruction. Key material itself is destroyed at end of cryptoperiod under SEC-006 | Head of Security Engineering |
| R-23 | Identity and access provisioning records | Access requests and approvals, joiner/mover/leaver tickets, privileged elevation and break-glass records (SEC-003, SEC-005) | 7 years | From the date access is removed | Head of Security Engineering |
| R-24 | Business continuity and DR records | BIAs (RSK-004), BCP and DR exercise reports (RES-004, RES-005) | 7 years | From report date | Business Continuity Manager |
| R-25 | Legal Hold records | Hold notices, custodian acknowledgements, scope, release notices | 7 years after release | From hold release | GC |
| R-26 | Personnel screening records | Background check results (PPL-001) | Employment or engagement + 7 years, or the shorter period required by applicable law | From Separation, or from decision if the candidate is not hired, for the period set by the GC per jurisdiction [DECISION REQUIRED: Retention of screening results for candidates not hired. Recommended default: 12 months from decision] | CHRO |
| R-27 | Transitory records | Drafts, working copies, duplicate convenience copies, chat messages with no record value | Until the final record is filed, max 90 days | From creation | Creator |

- **CMP-004.5.2.2** `[HIPAA]` Any record required by 45 CFR §164.316(b)(1) or §164.530(j) SHALL be retained for no less than 6 years from the date of its creation or the date when it was last in effect, whichever is later, regardless of the period stated in the schedule.
- **CMP-004.5.2.3** Copies of identity documents collected only to verify a Data Subject's identity SHALL be deleted within 30 days of DSR closure; the DSR record SHALL retain only a statement of the verification method and outcome.
- **CMP-004.5.2.4** `[GDPR]` Personal Data in a whistleblower report that is manifestly not relevant to the handling of the report SHALL NOT be collected or, if accidentally collected, SHALL be deleted within 30 days of identification, consistent with Directive (EU) 2019/1937 Art. 17.
- **CMP-004.5.2.5** `[PCI]` The quarterly purge process for Cardholder Data SHALL identify and securely delete stored CHD that exceeds the defined retention period, and its execution SHALL be retained as Evidence under row R-02.
- **CMP-004.5.2.6** `[PCI]` Audit logs of CDE system components SHALL meet row R-03, which satisfies PCI DSS Requirement 10.5.1.
- **CMP-004.5.2.7** `[SOX]` Records relevant to an audit or review of financial statements, including Evidence of Key Controls in Financially Significant Systems (CMP-009), SHALL be retained under row R-02 and SHALL NOT be destroyed, altered or falsified (SOX §802).
- **CMP-004.5.2.8** Personal Data contained in Backups is retained for the Backup period in row R-10. Where Personal Data must be erased under CMP-010 and is held in Backups, the Data Custodian SHALL ensure it is not restored to production use and that any restore re-applies the erasure before the restored data is made available.
- **CMP-004.5.2.9** [DECISION REQUIRED: Retention of a former Workforce Member's mailbox and files. Recommended default: 90 days after Separation.] The CIO SHALL preserve the mailbox and files of a former Workforce Member for 90 days after Separation. During that period the Line Manager SHALL identify records of business value and have them moved to an approved repository, where they are retained under the applicable row of the schedule. The remainder SHALL be deleted at the end of the period unless under Legal Hold (CMP-004.5.4.10).

### 5.3 Secure deletion at end of retention

- **CMP-004.5.3.1** Records SHALL be disposed of within 30 days after their retention period ends, unless under Legal Hold. Row R-12 (Personal Data) and row R-13 (`[PCI]` CHD) apply their own deadlines.
- **CMP-004.5.3.2** Each System Owner SHALL implement automated deletion or anonymization for each record class held in their Information System, where the system supports it. Where automation is not possible, the Record Owner SHALL run a documented manual disposal at least every 3 months.
- **CMP-004.5.3.3** Before any manual disposal, the Record Owner SHALL confirm with the GC that no Legal Hold covers the records. Automated deletion jobs SHALL check a Legal Hold flag or exclusion list before deletion.
- **CMP-004.5.3.4** Disposal SHALL use the methods SEC-017 section 5.2 specifies for the Classification Level and Media type. Logical deletion (flagging a record as deleted while the data remains recoverable) SHALL NOT be treated as disposal of Restricted or Confidential records.
- **CMP-004.5.3.5** Each disposal run SHALL be logged with the record class, volume or record range, date, method, and the person or job that performed it. Disposal logs and SEC-017 certificates SHALL be retained under row R-21.
- **CMP-004.5.3.6** Third Parties that hold the Organization's records SHALL return or destroy them at the end of the contract or retention period, and SHALL provide a written Certificate of Destruction, under the contract terms in RSK-003.5.7.4.
- **CMP-004.5.3.7** Anonymization used in place of deletion SHALL prevent re-identification by any means likely to be used (GDPR Recital 26), using techniques approved by the DPO under CMP-005. Pseudonymized data SHALL NOT be treated as anonymized.

### 5.4 Legal Hold

- **CMP-004.5.4.1** Only the GC, or a lawyer in the GC's office acting under written delegation, SHALL issue or release a Legal Hold.
- **CMP-004.5.4.2** Any Workforce Member who becomes aware of actual or threatened litigation, a regulatory investigation or inquiry, a subpoena, or an audit finding that may lead to proceedings SHALL notify the GC within 1 business day.
- **CMP-004.5.4.3** The GC SHALL issue a written Legal Hold notice to each identified custodian, Record Owner and affected System Owner within 1 business day of deciding a hold is required. The notice SHALL state the matter, the scope (record classes, date ranges, custodians and systems), and the prohibition on deletion or alteration.
- **CMP-004.5.4.4** Each System Owner named in a hold SHALL suspend automated deletion for the records in scope, including Backup rotation where the records exist only in Backups, within 2 business days of the notice and SHALL confirm suspension to the GC in writing.
- **CMP-004.5.4.5** Each custodian SHALL acknowledge the notice in writing within 5 business days. The GC SHALL escalate non-acknowledgement to the custodian's executive on the next business day.
- **CMP-004.5.4.6** The GC SHALL re-issue a reminder to custodians of each open hold every 6 months and on any change of scope, and SHALL issue the hold to new custodians within 1 business day of identifying them.
- **CMP-004.5.4.7** A Legal Hold overrides every retention period and disposal requirement in this Policy, including rows R-12 and R-13 and DSR erasure under CMP-010. Where an erasure request concerns held data, the DPO SHALL record the legal basis for refusal under CMP-010.
- **CMP-004.5.4.8** The GC SHALL maintain a Legal Hold Register recording each hold, its scope, custodians, acknowledgements, system suspensions and release date. The register SHALL be classified Restricted.
- **CMP-004.5.4.9** On release, the GC SHALL notify custodians and System Owners in writing. Normal retention SHALL resume from release; records whose period expired during the hold SHALL be disposed of within 30 days of release.
- **CMP-004.5.4.10** On departure of a custodian under hold, the CHRO SHALL notify the GC before Separation, and the CIO SHALL preserve the custodian's mailbox, files and devices in scope before deprovisioning under SEC-003.

### 5.5 Evidence collection and quality

- **CMP-004.5.5.1** Each Control Owner SHALL collect Evidence of each Control they own at the Control's operating frequency, and SHALL store it in the Evidence repository within 10 business days of the Control's operation (or of the end of the period for continuous Controls).
- **CMP-004.5.5.2** Each Evidence item SHALL record: Control ID (as mapped in REF-001); period covered; date and time of collection; collector; source system; method of extraction (system-generated, query, screenshot, attestation); and, for reports and queries, the parameters used.
- **CMP-004.5.5.3** System-generated Evidence SHALL be preferred over screenshots. Screenshots SHALL show the system clock or another date indicator and the system or environment identity.
- **CMP-004.5.5.4** Reports and queries used as Evidence SHALL be accompanied by the query, report definition or saved filter used, so that completeness and accuracy can be tested under CMP-002.
- **CMP-004.5.5.5** Evidence SHALL NOT be created, back-dated or altered after the fact. Where Evidence is missing, the Control Owner SHALL record the gap as a control failure under CMP-002, not reconstruct it.
- **CMP-004.5.5.6** Evidence SHALL contain the minimum Personal Data, CHD or PHI necessary. Restricted data elements not needed to demonstrate the Control SHALL be masked or redacted before storage. `[PCI]` PAN SHALL NOT appear in Evidence unless rendered unreadable under SEC-019.
- **CMP-004.5.5.7** Evidence provided to External Auditors, QSAs or regulators SHALL be logged in the Evidence repository with recipient, date, item and transfer method, and SHALL be transferred using protocols approved in SEC-006 section 5.2.

### 5.6 Evidence integrity and Chain of Custody

- **CMP-004.5.6.1** Every Evidence item SHALL have a cryptographic hash, using an algorithm approved in SEC-006, computed at ingestion and recorded in the Evidence repository metadata.
- **CMP-004.5.6.2** Evidence for rows R-02, R-03, R-04 and R-15 SHALL be stored in write-once-read-many (WORM) or immutable storage, or in storage with object-lock, for the full retention period.
- **CMP-004.5.6.3** The repository SHALL log every access to, export of, and attempted modification or deletion of Evidence, and those logs SHALL be retained under row R-03.
- **CMP-004.5.6.4** Forensic Evidence collected during a Security Incident or investigation (RES-002, CMP-006) SHALL be acquired following ISO/IEC 27037 principles: acquisition by trained personnel named in RES-002, write-blocking or read-only acquisition, hashing at acquisition and verification at each transfer, and working only on verified copies.
- **CMP-004.5.6.5** A chain-of-custody record SHALL be opened at acquisition of each forensic item and SHALL record: item identifier and description; hash value; date, time and location of acquisition; acquirer; every transfer, with releasing and receiving person, date, time, purpose and hash verification; storage location; and final disposition.
- **CMP-004.5.6.6** Physical forensic items SHALL be sealed in tamper-evident packaging with the seal number recorded in the chain-of-custody record, and stored in a locked evidence store with access limited to named personnel and logged, under SEC-016.
- **CMP-004.5.6.7** A break in the Chain of Custody, or a hash mismatch, SHALL be reported to the GC and the CISO within 1 business day and recorded on the chain-of-custody record.
- **CMP-004.5.6.8** Clock synchronization for systems producing Evidence and logs SHALL meet SEC-012 section 5.4, so that timestamps are reliable.

### 5.7 Evidence repository

- **CMP-004.5.7.1** The Head of GRC SHALL designate one Evidence repository (which may be a GRC tool with linked storage) as the authoritative store for control Evidence. Forensic Evidence MAY be held in a separate restricted store under the SOC Manager, linked by reference. HR case files and whistleblower case files MAY be held in their case-management systems, provided those systems meet sections 5.6 and 5.7.
- **CMP-004.5.7.2** The repository SHALL be classified at the highest Classification Level of the Evidence it holds, and at least Confidential.
- **CMP-004.5.7.3** Access SHALL be role-based and follow Least Privilege: Control Owners write to their Controls only; GRC personnel and Internal Audit have read access to all control Evidence; no user other than named repository administrators can delete; External Auditors receive time-limited read access to a defined scope. Access SHALL be authenticated using MFA per SEC-004 and reviewed per SEC-003.
- **CMP-004.5.7.4** Evidence SHALL be encrypted at rest and in transit per SEC-006.
- **CMP-004.5.7.5** The repository SHALL be backed up under SEC-018 and assigned a Recovery Tier under RSK-004 of no lower than Tier 2.
- **CMP-004.5.7.6** The repository SHALL apply retention labels per record class and SHALL support Legal Hold flags that block deletion.
- **CMP-004.5.7.7** `[GDPR]` Evidence containing Personal Data of EU/EEA Data Subjects SHALL be stored in locations permitted under CMP-005 Chapter V requirements.
- **CMP-004.5.7.8** The Head of GRC SHALL be able to produce any Evidence item requested by an auditor, QSA or regulator within 2 business days of the request.
- **CMP-004.5.7.9** Where a repository is migrated or replaced, the Head of GRC SHALL verify that all Evidence, metadata, hashes, retention labels and Legal Hold flags transfer completely, by hash comparison, before the source is decommissioned.

### 5.8 Physical records

- **CMP-004.5.8.1** Paper records within scope SHOULD be digitized into the Evidence repository and the paper disposed of under SEC-017, unless an original is legally required.
- **CMP-004.5.8.2** Retained paper records classified Confidential or Restricted SHALL be stored in locked containers in areas controlled under SEC-016, with a register of box contents, record class and destruction date.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| Head of GRC | Owns this Policy and the retention schedule; designates and administers the Evidence repository; reviews the schedule every 12 months; produces Evidence to auditors and regulators; monitors disposal compliance. |
| GC | Concurs in this Policy and schedule changes; sets jurisdiction-specific periods; issues, manages and releases Legal Holds; maintains the Legal Hold Register; approves extended retention. |
| ISSC | Approves this Policy. |
| CISO | Ensures Evidence integrity controls; receives chain-of-custody break reports. |
| CPO / DPO | Ensure Personal Data periods align with the ROPA; approve anonymization techniques; own rows R-08, R-18, R-19. |
| Record Owners (per schedule) | Retain, protect and dispose of records in their class; run manual disposals where automation is not possible. |
| Control Owners | Collect, label and store Evidence within 10 business days of Control operation. |
| System Owners | Implement automated retention and deletion; suspend deletion on Legal Hold within 2 business days. |
| SOC Manager | Retains security logs and incident records; maintains the forensic Evidence store and Chain of Custody. |
| CIO | Retains Backups per row R-10; preserves departing custodians' data under hold; owns disposal records. |
| CHRO | Retains training, screening and disciplinary records; notifies the GC of departing custodians under hold. |
| Head of Facilities | Retains CCTV and visitor logs; secures physical evidence stores and paper archives. |
| Internal Audit Director | Owns audit records; tests compliance with this Policy under CMP-002. |
| All Workforce Members | Store records in approved systems; do not delete held records; report potential litigation to the GC within 1 business day. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| CMP-004.7.1 | Policy documents and prior versions | 7 years after superseded |
| CMP-004.7.2 | Control evidence, audit workpapers, access reviews | 7 years |
| CMP-004.7.3 | Security logs | 12 months minimum, of which the most recent 90 days immediately available; `[HIPAA]` logs from ePHI systems 6 years |
| CMP-004.7.4 | Incident records and Post-Incident Reviews | 7 years after closure |
| CMP-004.7.5 | Risk register entries, risk acceptances, exceptions | 7 years after closure or expiry |
| CMP-004.7.6 | Training records and policy acknowledgements | Employment or engagement + 7 years |
| CMP-004.7.7 | Third-party assessments and contracts | Contract term + 7 years |
| CMP-004.7.8 | Data subject request records | 3 years after closure |
| CMP-004.7.9 | Whistleblower reports | 7 years after closure |
| CMP-004.7.10 | Backups | Daily 35 days · monthly 13 months · `[SOX]` year-end backups of financially significant systems 7 years |
| CMP-004.7.11 | CCTV recordings / visitor logs | 90 days / 12 months |
| CMP-004.7.12 | Personal data | Per the purpose in the ROPA; deleted or anonymized within 30 days after the purpose ends, unless under legal hold |
| CMP-004.7.13 | `[PCI]` Cardholder data | Only as long as the documented business need; purge process run at least every 3 months; sensitive authentication data never stored after authorization |
| CMP-004.7.14 | Compliance program records (R-14) | 7 years after superseded or closed |
| CMP-004.7.15 | Assurance reports (R-15) | 7 years from report date |
| CMP-004.7.16 | ISSC minutes and decisions (R-16) | 7 years |
| CMP-004.7.17 | Board of Directors and Audit Committee minutes (R-17) | Permanent |
| CMP-004.7.18 | Privacy accountability records (R-18) | Life of the processing activity + 7 years |
| CMP-004.7.19 | Consent and preference records (R-19) | Life of the consent or preference + 3 years |
| CMP-004.7.20 | HR disciplinary case records (R-20) | Employment or engagement + 7 years; `[HIPAA]` sanctions at least 6 years |
| CMP-004.7.21 | Asset, media and disposal records (R-21); identity and access records (R-23); BC/DR records (R-24) | 7 years |
| CMP-004.7.22 | Key management records (R-22) | 7 years after key destruction |
| CMP-004.7.23 | Legal Hold records (R-25) | 7 years after release |
| CMP-004.7.24 | Transitory records (R-27) | Max 90 days |
| CMP-004.7.25 | `[HIPAA]` floor for §164.316 / §164.530(j) documentation | 6 years from creation or last effective date, whichever is later |
| CMP-004.7.26 | Disposal after retention ends (other than R-12, R-13) | Within 30 days |
| CMP-004.7.27 | Manual disposal run where automation not possible | At least every 3 months |
| CMP-004.7.28 | DSR identity verification documents | Deleted within 30 days of DSR closure |
| CMP-004.7.29 | Legal Hold notice issued | Within 1 business day of the hold decision |
| CMP-004.7.30 | Deletion suspended by System Owners | Within 2 business days of notice |
| CMP-004.7.31 | Custodian acknowledgement | Within 5 business days |
| CMP-004.7.32 | Legal Hold reminders | Every 6 months and on change of scope |
| CMP-004.7.33 | Evidence stored after Control operation | Within 10 business days |
| CMP-004.7.34 | Evidence integrity | Hash at ingestion (SEC-006 algorithm); WORM or object-lock for R-02, R-03, R-04, R-15 |
| CMP-004.7.35 | Chain-of-custody break or hash mismatch reported | Within 1 business day to GC and CISO |
| CMP-004.7.36 | Evidence production to auditor, QSA or regulator | Within 2 business days of request |
| CMP-004.7.37 | Evidence repository Recovery Tier | Tier 2 or higher (RSK-004) |
| CMP-004.7.38 | Retention schedule review | Every 12 months and within 30 days of a relevant legal change |
| CMP-004.7.39 | Former Workforce Member mailbox and files | Preserved 90 days after Separation, then business records moved and the remainder deleted (CMP-004.5.2.9) |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Information Systems holding in-scope records with automated retention configured | 100% of systems that support it | Quarterly | Head of GRC |
| Record classes with a disposal run (automated or manual) in the last 3 months | 100% | Quarterly | Head of GRC |
| Records found past retention + 30 days (sample of 25 records per system per year) | 0 | Every 12 months | Head of GRC |
| `[PCI]` Quarterly CHD purge completed | 100% of quarters | Quarterly | Head of Security Engineering |
| Security log availability: 90 days online, 12 months total (sampled systems) | 100% | Quarterly | SOC Manager |
| Control Evidence stored within 10 business days of operation | ≥ 95% | Monthly | Head of GRC |
| Auditor requests fulfilled within 2 business days | ≥ 95% | Per audit | Head of GRC |
| Legal Hold custodian acknowledgements within 5 business days | 100% | Per hold | GC |
| System deletion suspended within 2 business days of a hold | 100% | Per hold | GC |
| Hash verification failures or chain-of-custody breaks | 0 | Quarterly | CISO |
| Evidence items lacking required metadata (sample) | < 2% | Quarterly | Head of GRC |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following SHALL NOT receive an Exception: Legal Hold requirements (section 5.4);
the prohibition on altering, back-dating or destroying Evidence (CMP-004.5.5.5,
CMP-004.5.2.7); `[PCI]` the prohibition on storing Sensitive Authentication Data after
authorization (row R-13); `[HIPAA]` the 6-year documentation floor (CMP-004.5.2.2); and any
retention minimum imposed by law. Exceptions that would extend retention of Personal Data
beyond row R-12 SHALL be reviewed by the CPO and the GC.

## 10. Enforcement

Non-compliance is handled under CMP-007.

Destruction, alteration or concealment of Evidence or of records subject to a Legal Hold or
audit is a Category 4 violation under CMP-007 and may also constitute a criminal offense
(including `[SOX]` §802). Third-Party failure to return or destroy records is handled under
the contractual remedies in RSK-003.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| CMP-004.5.1 – 5.2 | 7.5.3; A.5.31, A.5.33, A.5.34 | GV.OC-03, PR.DS-01 | SI-12, AU-11, PM-21 | 3.1, 3.4 | C1.1, C1.2, CC2.1 | APO14, BAI08 | PCI DSS 3.2.1, 3.3.1, 10.5.1; HIPAA §164.316(b)(2)(i), §164.530(j); GDPR Art. 5(1)(e), 30; Cal. Civ. Code §1798.100(a)(3); SOX §802 |
| CMP-004.5.3 | A.5.33, A.7.14, A.8.10 | PR.DS-01, PR.PS-03 | MP-6, SI-12 | 3.5 | C1.2 | APO14, DSS06 | PCI DSS 3.2.1, 9.4.7; HIPAA §164.310(d)(2)(i); GDPR Art. 5(1)(e), 17 |
| CMP-004.5.4 | A.5.31, A.5.33 | GV.OC-03 | SI-12 | 3.4 | CC2.1 | APO14 | SOX §802; GDPR Art. 17(3)(e) |
| CMP-004.5.5 – 5.7 | 7.5.3, 9.1; A.5.28, A.5.33, A.8.15, A.8.17 | PR.DS-01, PR.PS-04, RS.AN-03 | AU-9, AU-10, AU-11, IR-4, CA-7 | 8.10 | CC4.1, CC7.3 | MEA01, MEA03, DSS05 | PCI DSS 10.3.3, 10.5.1; HIPAA §164.312(b), §164.312(c)(1) |
| CMP-004.5.8 | A.7.10, A.5.33 | PR.DS-01 | MP-4, PE-3 | — | C1.1 | DSS05 | HIPAA §164.310(d)(1) |

## 12. Related documents

ISP-000, GOV-002, GOV-003, GOV-006, RSK-003, RSK-004, CMP-001, CMP-002, CMP-003, CMP-005,
CMP-006, CMP-007, CMP-008, CMP-009, CMP-010, SEC-001, SEC-002, SEC-003, SEC-004, SEC-005,
SEC-006, SEC-011, SEC-012, SEC-013, SEC-016, SEC-017, SEC-018, SEC-019, RES-002, RES-003,
RES-004, RES-005, PPL-001, PPL-002, TPL-001 to TPL-010, REF-001

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Head of GRC | | | |
| Concurrence: General Counsel (GC) | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
