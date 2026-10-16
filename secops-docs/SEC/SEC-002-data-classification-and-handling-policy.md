# SEC-002 — Data Classification & Handling Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | SEC-002 |
| Title | Data Classification & Handling Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Information Security Officer (CISO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-004, GOV-006, RSK-006, CMP-004, CMP-005, SEC-001, SEC-003, SEC-006, SEC-008, SEC-012, SEC-014, SEC-017, SEC-019 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CISO | Initial release |

## 3. Purpose

This Policy establishes the Organization's four Classification Levels and the minimum handling
requirements that apply to information at each level throughout its lifecycle: creation,
labelling, storage, transmission, sharing, printing, use with Generative AI, retention and
disposal. It also sets the Organization's Data Loss Prevention requirements. Consistent
classification allows every other control in the suite to be scaled to the harm that
unauthorized disclosure, alteration or loss of the information would cause.

## 4. Scope

| Dimension | In scope |
|---|---|
| People | All Workforce Members and Third Parties who create, access, process, store, transmit or dispose of Organization information |
| Systems | All Information Systems, Cloud Services, SaaS applications, Endpoints, Mobile Devices (including BYOD under SEC-008), AI Systems and Media that hold Organization information |
| Data | All information created, received or maintained by or for the Organization, in any format (electronic, paper, verbal, audio, video, images), including Personal Data, PHI, CHD, Secrets, source code, and data held by Third Parties on the Organization's behalf |
| Locations | All Organization premises, remote work locations, travel, Cloud Service regions, and Third-Party facilities |
| Third parties | Third Parties that receive, store, process or transmit Organization information; their obligations are imposed through contract under RSK-003 |

## 5. Policy statements

### 5.1 Classification Levels

- **SEC-002.5.1.1** All Organization information SHALL be assigned one of four Classification Levels: **Public · Internal · Confidential · Restricted** (Restricted includes PHI, cardholder data, authentication secrets, special-category and sensitive personal information, government identifiers).
- **SEC-002.5.1.2** The Classification Level SHALL be assigned by the Data Owner using the criteria in section 5.2. Where a data set meets the criteria of more than one level, the highest applicable level SHALL apply.
- **SEC-002.5.1.3** Information that has not been classified SHALL be handled as Internal, except that any information containing Personal Data SHALL be handled as at least Confidential, and any information meeting a Restricted criterion in section 5.2 SHALL be handled as Restricted, regardless of label.
- **SEC-002.5.1.4** Information received from a Third Party under a confidentiality obligation SHALL be classified at least Confidential, or at the level the contract requires if higher.
- **SEC-002.5.1.5** A compilation, extract, report, derived data set, model output or Backup SHALL carry the highest Classification Level of the information it contains, unless the Data Owner reclassifies it under section 5.6.
- **SEC-002.5.1.6** The Classification Level of each data store and Information System SHALL be recorded in the Asset Inventory under SEC-001 as the highest Classification Level of the data it stores, processes or transmits.

### 5.2 Classification criteria and examples

| Level | Criteria (any one is sufficient) | Examples |
|---|---|---|
| **Public** | Approved for release to the public by the Data Owner and, for external communications, by the communications function; disclosure causes no harm | Published marketing material, press releases, public website content, published product documentation, published job postings, public regulatory filings after release |
| **Internal** | Intended for Workforce Members and authorized Third Parties for Organization business; unauthorized disclosure would cause limited harm (impact score 1–2 under RSK-002) | Internal policies and procedures (unless marked higher), organization charts, internal announcements, non-sensitive project plans, intranet content, meeting notes without Confidential content |
| **Confidential** | Unauthorized disclosure could cause material harm to the Organization, its customers or Workforce Members (impact score 3–4 under RSK-002); or it contains Personal Data that is not Restricted; or it is subject to a contractual confidentiality obligation; or it is non-public financial information | Customer lists and contracts, non-public financial results before release, pricing models, business strategy, source code, system architecture and network diagrams, vulnerability and Penetration Test reports, audit reports, Asset Inventory, employee contact and HR records not containing Restricted elements, security logs, Risk Register |
| **Restricted** | Unauthorized disclosure could cause severe harm or regulatory penalty (impact score 5 under RSK-002); or it is a category named in SEC-002.5.1.1 | `[HIPAA]` PHI and ePHI · `[PCI]` CHD and SAD · Secrets (passwords, private keys, API keys, tokens, connection strings) · `[GDPR]` `[CPRA]` Sensitive Personal Information (health, biometric, genetic, racial or ethnic origin, religious beliefs, sexual orientation, precise geolocation, union membership, account log-in credentials) · government identifiers (social security numbers, passport, driver's license and national identity numbers, tax identifiers) · financial account numbers with access codes · `[SOX]` material non-public financial information before disclosure · encryption key material · Break-glass Account credentials · Legal Hold material designated by the GC |

- **SEC-002.5.2.1** The CISO SHALL maintain a classification guide, published with this Policy, listing additional examples by business function. The guide SHALL NOT lower any classification set by this section.
- **SEC-002.5.2.2** The CPO SHALL confirm the classification of each category of Personal Data recorded in the ROPA (`[GDPR]` TPL-010) and in CMP-005.
- **SEC-002.5.2.3** `[SOX]` The CFO SHALL designate which financial information is material non-public information and the date from which it becomes Public.

### 5.3 Data Owner duties

- **SEC-002.5.3.1** Each data set SHALL have a Data Owner recorded in the Asset Inventory (SEC-001). The Data Owner SHALL classify the data set before it is first stored in a production Information System.
- **SEC-002.5.3.2** The Data Owner SHALL review the classification of each data set they own at the frequency in SEC-002.7.6 and on any event in SEC-002.5.6.2.
- **SEC-002.5.3.3** The Data Owner SHALL approve access to Confidential and Restricted data under SEC-003, applying Least Privilege and Need to Know.
- **SEC-002.5.3.4** Workforce Members who create information SHALL apply the Classification Level at creation, using the classification guide, where the information is not already within a classified data set.

### 5.4 Handling matrix

- **SEC-002.5.4.1** Information SHALL be handled in accordance with the matrix below for its Classification Level. Each cell is a minimum; a Data Owner MAY impose stricter handling.
- **SEC-002.5.4.2** Cryptographic algorithms, key lengths and protocols referred to as "encrypted" in the matrix SHALL meet the minimums in SEC-006.
- **SEC-002.5.4.3** A system or tool SHALL be treated as approved in the matrix only if it is registered in the Asset Inventory (SEC-001) with a recorded highest Classification Level equal to or higher than the information concerned.

| Activity | Public | Internal | Confidential | Restricted |
|---|---|---|---|---|
| **Labelling** | No label required | No label required; unlabelled information is Internal (SEC-002.5.1.3) | SHALL be labelled "Confidential" in document header or footer, file metadata or sensitivity label, and email subject or sensitivity label; physical Media and paper SHALL be marked on the cover or first page | SHALL be labelled "Restricted" in header and footer of every page, file metadata or sensitivity label, and email subject; physical Media SHALL carry an external label; systems holding Restricted data SHALL display the label in the application where technically supported |
| **Storage — electronic** | Any approved system | Approved Organization systems only; SHALL NOT be stored on personal accounts or personal cloud storage | Approved systems only; access limited by Need to Know under SEC-003; encrypted at rest; SHALL NOT be stored on unencrypted removable Media; on BYOD only within a managed container under SEC-008 | Only systems approved for Restricted data in the Asset Inventory; encrypted at rest; access logged under SEC-012; SHALL NOT be stored on BYOD, personal accounts or removable Media except encrypted removable Media approved in writing by the Data Owner and CISO for a documented purpose; `[PCI]` PAN rendered unreadable wherever stored, per SEC-019 (PCI DSS 3.5.1); `[PCI]` SAD SHALL NOT be stored after authorization |
| **Storage — physical** | No requirement | Not left unattended in public areas | Stored in locked drawer, cabinet or room when unattended; clear-desk applies (SEC-016) | Stored in locked container in an access-controlled area; removal from Organization premises requires Data Owner approval and a log entry |
| **Transmission** | No requirement | Over Organization-managed networks or encrypted channels | Encrypted in transit over any network outside a single Organization-controlled network segment; email to external recipients encrypted in transit (SEC-014) | Encrypted in transit on all networks, including internal networks; file transfer only through approved secure transfer services; `[PCI]` PAN SHALL NOT be sent by end-user messaging technologies unless encrypted (PCI DSS 4.2.2); verbal disclosure only to authenticated recipients with Need to Know |
| **Sharing externally** | Permitted once approved for release under SEC-002.5.2 | Permitted to Third Parties for an Organization business purpose under contract or non-disclosure agreement | Data Owner approval; Third Party bound by contract with confidentiality terms and assessed under RSK-003; shared only via approved platforms with per-recipient access and link expiry at or below SEC-002.7.3; `[GDPR]` `[CPRA]` Personal Data only with a processing agreement under CMP-005 | Data Owner approval and CISO approval (CPO approval where Personal Data); Minimum Necessary data; Third Party assessed under RSK-003 with contract including security terms and, where applicable, `[HIPAA]` BAA or `[GDPR]` Art. 28 terms; encrypted; each disclosure recorded in a disclosure log retained per CMP-004; public or anonymous links prohibited |
| **Printing and copying** | No requirement | Collect output promptly | Printed only on Organization-managed printers; collected immediately; secure print release where available | Printed only when no electronic alternative meets the business need; secure print release (badge or PIN) required; copies numbered where the Data Owner requires; SHALL NOT be printed at home or on Third-Party or public printers |
| **Use with Generative AI tools** | Permitted with any Generative AI tool, subject to GOV-004 | Only Generative AI tools approved under RSK-006 and registered in the Asset Inventory; consumer or free-tier tools prohibited | Only Generative AI tools approved under RSK-006 for Confidential data, with contractual terms that prohibit the provider from training models on Organization inputs or outputs and that limit provider retention; Organization SSO enforced | Prohibited, except in a Generative AI tool or AI System approved under RSK-006 specifically for Restricted data, with the approval of the Data Owner and CISO (and the CPO for Personal Data); `[HIPAA]` BAA in place for PHI; `[PCI]` CHD and SAD SHALL NOT be entered into any Generative AI tool; Secrets SHALL NOT be entered into any Generative AI tool |
| **Verbal and meetings** | No requirement | No requirement | Not discussed in public places; virtual meetings use Organization-approved platforms | Discussed only with authenticated participants with Need to Know; meeting recordings and AI transcription prohibited unless the Data Owner approves and the recording is stored as Restricted |
| **Retention** | Per CMP-004 | Per CMP-004 | Per CMP-004 | Per CMP-004; `[PCI]` CHD retention and purge per CMP-004 |
| **Disposal** | No requirement | Per SEC-017 | Per SEC-017 | Per SEC-017 |
| **Non-production use** | Permitted | Permitted | SHALL NOT be used in development or test environments unless masked, tokenized or synthetic, or the environment meets production controls and the Data Owner approves | SHALL NOT be used in development or test environments; masked, tokenized or synthetic data SHALL be used; `[PCI]` live PAN prohibited in pre-production (PCI DSS 6.5.5) |
| **Loss or suspected disclosure** | No reporting required | Report to the SOC Manager per RES-001 | Report to the SOC Manager per RES-001 immediately on discovery | Report to the SOC Manager per RES-001 immediately on discovery; Personal Data loss handled under RES-003 |

### 5.5 Data Loss Prevention

- **SEC-002.5.5.1** The CISO SHALL operate Data Loss Prevention (DLP) controls covering, at minimum, the channels and coverage targets in SEC-002.7.4: corporate email, web and Cloud Service uploads from managed Endpoints, removable Media and printing on managed Endpoints, sanctioned SaaS collaboration platforms, and approved Generative AI tools.
- **SEC-002.5.5.2** DLP detection rules SHALL, at minimum, identify: `[PCI]` PAN (pattern and Luhn validation); government identifiers; `[HIPAA]` PHI identifiers combined with health terms; Secrets (private key headers, cloud access keys, tokens, connection strings); documents bearing Confidential or Restricted labels; and source code from Organization repositories.
- **SEC-002.5.5.3** DLP rules SHALL block, not only alert on, transmission of Restricted information to: personal email domains, unapproved Cloud Services and SaaS, unapproved Generative AI tools, and unencrypted removable Media. Confidential information sent to these destinations SHALL at minimum generate an alert and a user notification requiring a business justification.
- **SEC-002.5.5.4** A Workforce Member MAY override a DLP block for Confidential (not Restricted) information only by entering a business justification; overrides SHALL be logged and reviewed by the SOC Manager at the frequency in SEC-002.7.5.
- **SEC-002.5.5.5** DLP alerts SHALL be sent to the SIEM and triaged by the SOC under the alert triage SLAs in SEC-012. Confirmed unauthorized disclosure of Confidential or Restricted information SHALL be handled as a Security Incident under RES-001.
- **SEC-002.5.5.6** The Head of Security Engineering SHALL review DLP rule effectiveness, false-positive rates and coverage at the frequency in SEC-002.7.5, and SHALL test each blocking rule for Restricted data with test data at least every 6 months.
- **SEC-002.5.5.7** DLP inspection of Workforce Member communications SHALL be limited to the Organization's systems and accounts, described to Workforce Members in GOV-004, and `[GDPR]` assessed by a DPIA under CMP-005 where Personal Data of EU/EEA Workforce Members is processed.
- **SEC-002.5.5.8** The CISO SHALL maintain data discovery scanning of data stores in the Asset Inventory at the frequency in SEC-002.7.7 to detect Restricted data stored outside systems approved for Restricted data. Findings SHALL be remediated by the Data Owner within the time in SEC-002.7.8.
- **SEC-002.5.5.9** `[PCI]` Data discovery SHALL include a scan for cleartext PAN outside the defined CDE at least every 12 months and after Significant Change to the CDE (PCI DSS 12.5.2 scoping, 12.10.7 response to unexpected PAN).

### 5.6 Reclassification

- **SEC-002.5.6.1** Only the Data Owner MAY reclassify information. Lowering a Classification Level of Restricted information SHALL also require CISO approval, and of Personal Data, CPO approval.
- **SEC-002.5.6.2** The Data Owner SHALL review classification when: (a) information is approved for public release; (b) data sets are aggregated, joined or enriched in a way that increases sensitivity; (c) Personal Data is de-identified, pseudonymized, anonymized or re-identified; (d) the purpose or use of the data changes; (e) a legal, regulatory or contractual obligation changes; or (f) a time-bound sensitivity lapses (for example, `[SOX]` financial results after public disclosure).
- **SEC-002.5.6.3** Aggregation of Confidential Personal Data into a data set containing records of more than the threshold in SEC-002.7.9 Data Subjects SHALL be classified Restricted. [DECISION REQUIRED: Record-count threshold above which aggregated Confidential Personal Data becomes Restricted. Recommended default: 10,000 Data Subjects]
- **SEC-002.5.6.4** Data that has been anonymized so that Data Subjects are no longer identifiable MAY be reclassified below Confidential only after the CPO confirms in writing that the anonymization technique meets CMP-005. Pseudonymized Personal Data SHALL remain at least Confidential.
- **SEC-002.5.6.5** Each reclassification SHALL be recorded with the data set, old and new level, reason, approver and date, and the Asset Inventory updated under SEC-001.
- **SEC-002.5.6.6** On reclassification upward, the Data Owner SHALL ensure that within the time in SEC-002.7.10 the data is moved to systems approved for the new level, labels are updated, and access is re-reviewed under SEC-003.
- **SEC-002.5.6.7** Workforce Members who believe information is misclassified SHALL notify the Data Owner and handle the information at the higher of the two levels until the Data Owner decides.

### 5.7 Third Parties

- **SEC-002.5.7.1** Contracts with Third Parties that receive Confidential or Restricted information SHALL require handling equivalent to this Policy for the Classification Level concerned, notification of loss within the period required by RES-003 and RSK-003, and return or certified deletion at contract end consistent with SEC-017.
- **SEC-002.5.7.2** Third Parties SHALL NOT receive Restricted information until the Third-Party assessment under RSK-003 is complete and approved.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CISO | Owns this Policy; maintains the classification guide; operates DLP and data discovery; approves Restricted external sharing, Restricted downgrades and use of Restricted data with approved Generative AI tools. |
| ISSC | Approves this Policy. |
| CPO | Confirms classification of Personal Data categories; approves sharing and reclassification of Personal Data; confirms anonymization. |
| DPO | `[GDPR]` Advises on DPIAs for DLP monitoring and on Personal Data classification. |
| CFO | `[SOX]` Designates material non-public financial information and its release date. |
| GC | Designates Legal Hold material; advises on contractual confidentiality obligations. |
| Head of Security Engineering | Implements DLP and labelling technology; reviews DLP rule effectiveness and tests blocking rules. |
| SOC Manager | Triages DLP alerts; reviews overrides; escalates Security Incidents. |
| CIO | Records Classification Levels in the Asset Inventory (SEC-001); configures printing and storage controls. |
| Data Owner | Classifies and reclassifies data; approves access and external sharing; remediates data discovery findings; reviews classification. |
| Data Custodian | Applies technical controls required by the handling matrix. |
| Workforce Member | Labels and handles information per the matrix; reports loss or misclassification. |
| Third Party | Handles Organization information per contract terms aligned with this Policy. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| SEC-002.7.1 | Classification Levels | Public · Internal · Confidential · Restricted (Restricted includes PHI, cardholder data, authentication secrets, special-category and sensitive personal information, government identifiers) |
| SEC-002.7.2 | Default handling of unclassified information | Internal; Personal Data at least Confidential; Restricted criteria always Restricted |
| SEC-002.7.3 | Maximum lifetime of an external sharing link for Confidential information | 30 days |
| SEC-002.7.4 | DLP coverage | 100% of managed Endpoints, corporate email, sanctioned SaaS collaboration platforms and approved Generative AI tools |
| SEC-002.7.5 | DLP override review; DLP rule effectiveness review | Overrides: weekly · Rule effectiveness and coverage: quarterly · Blocking-rule testing: every 6 months |
| SEC-002.7.6 | Data Owner classification review | Every 12 months |
| SEC-002.7.7 | Data discovery scanning of data stores | Quarterly; `[PCI]` cleartext PAN discovery at least every 12 months and after Significant Change |
| SEC-002.7.8 | Remediation of Restricted data found outside approved systems | Within 10 business days of the finding |
| SEC-002.7.9 | Aggregation threshold for Restricted classification of Personal Data | 10,000 Data Subjects (adopter decision) |
| SEC-002.7.10 | Completion of handling changes after upward reclassification | Within 30 days |
| SEC-002.7.11 | Encryption at rest and in transit | Per SEC-006 |
| SEC-002.7.12 | Retention; disposal | Per CMP-004; per SEC-017 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Data stores in Asset Inventory with a recorded Classification Level and Data Owner | 100% | Monthly | CIO |
| Managed Endpoints with active DLP agent | 100% | Monthly | Head of Security Engineering |
| Restricted data found outside approved systems, remediated within 10 business days | 100% | Quarterly | CISO |
| DLP alerts triaged within SEC-012 SLA | ≥ 95% | Monthly | SOC Manager |
| DLP overrides reviewed weekly | 100% | Monthly | SOC Manager |
| Blocking-rule tests passed | 100% | Every 6 months | Head of Security Engineering |
| Data Owner classification reviews completed on schedule | ≥ 95% | Quarterly | CISO |
| Confirmed unauthorized disclosures of Restricted data | 0 | Monthly | CISO |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following SHALL NOT receive an Exception: storage of `[PCI]` SAD after authorization;
entry of `[PCI]` CHD or Secrets into any Generative AI tool; use of Restricted data in
development or test environments without masking, tokenization or synthetic substitution
where `[PCI]` PAN is involved.

## 10. Enforcement

Non-compliance is handled under CMP-007.

Intentional disclosure of Restricted information to an unauthorized party, or deliberate
circumvention of DLP controls, SHALL be referred to the CHRO and GC under CMP-007.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| SEC-002.5.1 – 5.3 Classification | A.5.12, A.5.9 | ID.AM-05, ID.AM-07 | RA-2, PM-5 | 3.1, 3.2, 3.7 | C1.1, CC3.2 | APO14, BAI08 | `[GDPR]` Art. 5(1)(f), 9, 30; `[CPRA]` §1798.140(ae); `[HIPAA]` §164.308(a)(1)(ii)(A) |
| SEC-002.5.4 Handling matrix | A.5.10, A.5.13, A.5.14, A.7.7, A.7.10, A.8.11 | PR.DS-01, PR.DS-02, PR.DS-10 | MP-3, MP-4, MP-5, SC-8, SC-28, AC-21 | 3.3, 3.6, 3.9, 3.10, 3.11 | CC6.1, CC6.7, C1.1 | DSS05, DSS06 | `[PCI]` 3.2.1, 3.3.1, 3.5.1, 4.2.2, 6.5.5, 9.4; `[HIPAA]` §164.312(a)(2)(iv), (e)(1); `[GDPR]` Art. 28, 32 |
| SEC-002.5.4 Generative AI row | A.5.10, A.5.12 | PR.DS-01, GV.SC-07 | AC-21, SA-9 | 3.3 | C1.1, CC9.2 | APO14 | `[GDPR]` Art. 28, 35 |
| SEC-002.5.5 Data Loss Prevention | A.8.12 | PR.DS-01, PR.DS-02, DE.CM-01 | SC-7, AC-4, SI-4 | 3.13, 3.14 | CC6.7, C1.1 | DSS05 | `[PCI]` 12.5.2, 12.10.7; `[HIPAA]` §164.312(b) |
| SEC-002.5.6 Reclassification | A.5.12 | ID.AM-07 | RA-2 | 3.7 | C1.1 | APO14 | `[GDPR]` Art. 4(5), 89 |
| SEC-002.5.7 Third Parties | A.5.14, A.5.20 | GV.SC-05 | SA-9, PS-7 | 15.4 | C1.1, CC9.2 | APO10 | `[HIPAA]` §164.308(b)(1); `[GDPR]` Art. 28 |

## 12. Related documents

ISP-000, GOV-004, GOV-006, RSK-002, RSK-003, RSK-006, CMP-003, CMP-004, CMP-005, CMP-007,
SEC-001, SEC-003, SEC-006, SEC-008, SEC-012, SEC-014, SEC-016, SEC-017, SEC-019, RES-001,
RES-003, TPL-005, TPL-010

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CISO | | | |
| Approver: ISSC Vice-Chair, on behalf of the ISSC (CISO recused as Document Owner under GOV-001.5.3.9) | | | |
