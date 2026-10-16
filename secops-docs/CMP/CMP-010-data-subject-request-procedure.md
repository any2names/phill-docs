# CMP-010 — Data Subject Request Procedure

## 1. Document control

| Field | Value |
|---|---|
| Document ID | CMP-010 |
| Title | Data Subject Request Procedure |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 3 — Procedure |
| Classification | Internal |
| Owner | Data Protection Officer (DPO) |
| Approver | Chief Privacy Officer (CPO) |
| Effective date | [DECISION REQUIRED: Date of CPO approval] |
| Next review date | Effective date + 12 months, and on the event-triggered reviews in GOV-002.7.4 |
| Parent document | CMP-005 Data Privacy & Protection Policy |
| Related documents | CMP-001, CMP-003, CMP-004, CMP-005, CMP-007, RSK-003, SEC-002, SEC-003, SEC-006, SEC-018, RES-002, TPL-010, REF-001 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | DPO | Initial release |

## 3. Purpose

This Procedure sets out how the Organization receives, verifies, fulfils, refuses, records and
reports Data Subject Requests (DSRs), so that every request is answered completely, securely and
within the legal deadlines of the GDPR (Articles 12 to 22) and the CCPA as amended by the CPRA
(Cal. Civ. Code §1798.100 et seq. and Cal. Code Regs. tit. 11, §7000 et seq.).

## 4. Scope

**This entire document is a conditional module. It applies only where the Organization
processes Personal Data of EU/EEA residents `[GDPR]` or of California consumers `[CPRA]`**, as
recorded in the Obligations Register (CMP-001). Steps tagged `[GDPR]` apply only to GDPR
requests; steps tagged `[CPRA]` apply only to CPRA requests; untagged steps apply to both.

| Dimension | In scope |
|---|---|
| People | All Workforce Members (any of whom may receive a DSR); Workforce Members designated by the DPO to handle DSRs; Data Owners and System Owners who search, correct or delete data |
| Systems | Every Information System and Cloud Service that holds Personal Data, as recorded in the ROPA (TPL-010) and the Asset Inventory (SEC-001), including Backups, archives, logs and end-user storage |
| Data | All Personal Data for which the Organization is a Controller (or a "business" under the CPRA); and Personal Data it processes as a Processor (or "service provider" / "contractor"), for which section 5.11 applies |
| Locations | All locations and jurisdictions in which the Organization processes in-scope Personal Data |
| Third parties | Processors and Subprocessors acting for the Organization, and third parties to whom the Organization has sold or shared Personal Data `[CPRA]` |

Requests under other laws (e.g. other US state privacy laws, UK GDPR) SHALL be handled using
this Procedure with the deadlines of the applicable law as recorded in the Obligations Register;
where that law's deadline is shorter, the shorter deadline applies.

## 5. Procedure

### 5.1 Intake channels

- **CMP-010.5.1.1** The DPO SHALL maintain the following intake channels and publish them in the Organization's Privacy Notice:
  1. a web form on the Organization's website;
  2. a dedicated privacy email address;
  3. `[CPRA]` a toll-free telephone number, unless the Organization operates exclusively online and has a direct relationship with the consumer, in which case the email address satisfies this requirement (Cal. Civ. Code §1798.130(a)(1)); and
  4. `[CPRA]` a "Do Not Sell or Share My Personal Information" link and, where Sensitive Personal Information is used for purposes beyond those permitted in Cal. Code Regs. tit. 11, §7027(m), a "Limit the Use of My Sensitive Personal Information" link (or a single alternative opt-out link), and processing of Opt-out Preference Signals such as Global Privacy Control.
- **CMP-010.5.1.2** Where the Organization has an authenticated customer account, a DSR MAY also be submitted through the account. The Organization SHALL NOT require a Data Subject to create an account to submit a DSR.
- **CMP-010.5.1.3** A DSR SHALL be treated as valid in any form and through any channel, including post, social media and a conversation with a Workforce Member, if it can be understood as a request to exercise a right. No specific wording is required.
- **CMP-010.5.1.4** Any Workforce Member who receives a DSR outside the channels in CMP-010.5.1.1 SHALL forward it, unaltered and with the date and time of receipt, to the privacy email address within 1 business day, and SHALL NOT respond substantively.
- **CMP-010.5.1.5** The DPO SHALL test each intake channel every 3 months by submitting a test request and confirming it is logged within the time in CMP-010.5.2.1.

### 5.2 Logging and triage

- **CMP-010.5.2.1** Workforce Members designated by the DPO SHALL log every DSR in the DSR log within 1 business day of receipt by the Organization (not of receipt by the privacy team), recording the fields in CMP-010.5.14.2.
- **CMP-010.5.2.2** At logging, Workforce Members designated by the DPO SHALL determine:
  1. the right or rights being exercised (sections 5.7 and 5.8);
  2. the applicable law or laws (GDPR, CPRA or other), based on the requester's stated residence and the processing involved; where more than one applies, the stricter deadline and the broader right SHALL be applied;
  3. whether the Organization is Controller (or business) or Processor (or service provider) for the data concerned (Processor requests follow section 5.11);
  4. the verification tier (section 5.4); and
  5. the due date (section 5.3).
- **CMP-010.5.2.3** `[CPRA]` Workforce Members designated by the DPO SHALL send a written acknowledgement within the time in CMP-010.5.3.1, stating that the request was received, how verification will be performed, and when a response can be expected.
- **CMP-010.5.2.4** `[GDPR]` Workforce Members designated by the DPO SHOULD send the same acknowledgement for GDPR requests within 10 business days.
- **CMP-010.5.2.5** Where a request is unclear, Workforce Members designated by the DPO SHALL ask the requester to clarify within 5 business days of receipt. The clarification request SHALL NOT be used to delay the response, and the deadline SHALL continue to run.

### 5.3 Deadlines

- **CMP-010.5.3.1** The following response deadlines SHALL apply, measured from the date of receipt by the Organization:

| Law | Acknowledge | Respond | Extension |
|---|---|---|---|
| `[GDPR]` | — (CMP-010.5.2.4) | 1 month | Extendable by 2 months (section 5.9) |
| `[CPRA]` | Within 10 business days | Within 45 days | Extendable by 45 days (section 5.9) |
| `[CPRA]` Opt-out of sale or sharing; limit use of Sensitive Personal Information | — | As soon as feasibly possible, and no later than 15 business days (Cal. Code Regs. tit. 11, §7026(f), §7027(g)) | None |

- **CMP-010.5.3.2** `[GDPR]` "1 month" SHALL be calculated from the day of receipt to the corresponding calendar date in the next month; where there is no corresponding date, the deadline is the last day of that month. Where the deadline falls on a weekend or public holiday, the response SHALL be sent no later than the preceding business day.
- **CMP-010.5.3.3** The DSR log SHALL calculate the due date at logging and flag each open request 10 days and 3 days before its due date to the DPO.
- **CMP-010.5.3.4** `[GDPR]` [ASSUMPTION: Where the Organization requests additional information to confirm identity under GDPR Art. 12(6), the deadline runs from receipt of that information, consistent with EDPB Guidelines 01/2022. The GC SHALL confirm this against the practice of the lead Supervisory Authority.] `[CPRA]` The CPRA deadline is not suspended while verification is pending.

### 5.4 Identity verification by risk

- **CMP-010.5.4.1** Workforce Members designated by the DPO SHALL verify the identity of the requester using the tier in the table below, matching information provided by the requester against information the Organization already holds. The team SHALL NOT request more information than the tier requires.

| Tier | Applies to | Verification method |
|---|---|---|
| V0 — No verification | `[CPRA]` opt-out of sale or sharing; `[CPRA]` limit use of Sensitive Personal Information; `[GDPR]` objection to direct marketing (Art. 21(2)); withdrawal of consent | None. Only the information needed to locate the records (e.g. email address, cookie or device identifier) SHALL be requested. Opt-out Preference Signals are honored for the browser or device and any known associated consumer profile |
| V1 — Standard | Confirmation of processing and categories of Personal Data; `[CPRA]` request to know categories; rectification or correction of non-Restricted data; restriction; objection on legitimate-interest grounds | Request submitted through an authenticated account session; or a match of at least 2 data points held by the Organization (`[CPRA]` "reasonable degree of certainty", Cal. Code Regs. tit. 11, §7062(b)) |
| V2 — High | Copy of Personal Data (access); `[CPRA]` request to know specific pieces; portability; erasure or deletion; correction of Restricted data; any request concerning Sensitive Personal Information | Authenticated account session with step-up MFA (SEC-004); or a match of at least 3 data points held by the Organization plus, `[CPRA]`, a declaration signed under penalty of perjury (`[CPRA]` "reasonably high degree of certainty", §7062(c)) |

- **CMP-010.5.4.2** A copy of a government identifier SHALL be requested only where no tier method in CMP-010.5.4.1 can be completed. Verification information collected for a DSR SHALL be used only for verification, transmitted and stored as Restricted data under SEC-002, and deleted within the time in CMP-004.5.2.3. Only the verification outcome SHALL be kept in the DSR log.
- **CMP-010.5.4.3** Workforce Members designated by the DPO SHALL send any request for verification information within 5 business days of logging.
- **CMP-010.5.4.4** Where the requester does not provide the verification information within 30 days of the request, or verification fails, Workforce Members designated by the DPO SHALL close the request as unverified and send the notice in CMP-010.5.12.4.
- **CMP-010.5.4.5** `[CPRA]` Where a request to delete cannot be verified, the Organization SHALL inform the consumer and, where it sells or shares Personal Information, SHALL ask whether the consumer wishes to opt out of sale or sharing. Where a request to know specific pieces cannot be verified, the Organization SHALL evaluate it as a request to know categories.
- **CMP-010.5.4.6** `[GDPR]` Where the Organization cannot identify the Data Subject, it SHALL inform the requester and explain what additional information would enable identification (Art. 11(2), Art. 12(2)).
- **CMP-010.5.4.7** Suspected fraudulent requests (e.g. a mismatch between the verified identity and the delivery address, or repeated failed verification) SHALL be escalated to the DPO within 1 business day and, where a Security Incident is suspected, reported under RES-002.

### 5.5 Authorized Agents

- **CMP-010.5.5.1** A request MAY be submitted by an Authorized Agent: `[CPRA]` a natural person or a business entity acting for the consumer under Cal. Code Regs. tit. 11, §7063; `[GDPR]` a person holding a written mandate from the Data Subject; or a parent or legal guardian of a minor or a person holding a power of attorney.
- **CMP-010.5.5.2** Workforce Members designated by the DPO SHALL require from the agent written permission signed by the Data Subject, specifying the rights to be exercised. For V2 requests, the team SHALL also either verify the Data Subject's own identity directly at V2, or obtain direct confirmation from the Data Subject that the agent has permission.
- **CMP-010.5.5.3** `[CPRA]` Where the agent holds a power of attorney under California Probate Code §§4121 to 4130, the steps in CMP-010.5.5.2 SHALL NOT be required beyond verifying the power of attorney and the agent's identity.
- **CMP-010.5.5.4** `[CPRA]` For opt-out and limit requests (Tier V0), the Organization MAY require only the signed permission.
- **CMP-010.5.5.5** Where the agent's authority cannot be established within 30 days of the request for it, the request SHALL be closed under CMP-010.5.4.4, and the Data Subject SHALL be told how to submit the request directly.
- **CMP-010.5.5.6** Personal Data in a response to an agent request SHALL be delivered to the Data Subject directly, unless the signed permission expressly authorizes delivery to the agent.

### 5.6 Locating Personal Data

- **CMP-010.5.6.1** For each verified request, Workforce Members designated by the DPO SHALL identify the systems to be searched from the ROPA (TPL-010) and the Asset Inventory, and SHALL send a search task to the System Owner of each system within 3 business days of verification.
- **CMP-010.5.6.2** Each System Owner SHALL complete the search, correction, restriction or deletion task and return the result, with Evidence (e.g. query output, ticket, screenshot), within 10 business days of the task being issued.
- **CMP-010.5.6.3** Searches SHALL cover structured and unstructured stores, including email, collaboration tools, file shares, ticketing systems, logs that are searchable by identifier, and the systems of Processors (section 5.10).
- **CMP-010.5.6.4** The DPO SHALL escalate any overdue search task to the System Owner's executive within 1 business day after it becomes overdue.

### 5.7 Handling each right: GDPR `[GDPR]`

- **CMP-010.5.7.1** `[GDPR]` **Access (Art. 15).**
  1. Confirm whether Personal Data concerning the Data Subject is processed.
  2. Compile a copy of the Personal Data from all searches.
  3. Add the supplementary information required by Art. 15(1)–(2): purposes; categories of Personal Data; recipients or categories of recipients, including in third countries; the retention period or criteria (from TPL-010 and CMP-004); the rights to rectification, erasure, restriction and objection; the right to complain to a Supervisory Authority; the source of data not collected from the Data Subject; the existence of automated decision-making, with meaningful information about the logic involved; and the safeguards for transfers to third countries.
  4. Redact Personal Data of other individuals, trade secrets and legally privileged material, recording each redaction and its basis (Art. 15(4)).
  5. Submit the response to the DPO (or delegate) for quality review before release.
  6. Deliver under section 5.13 in a commonly used electronic form where the request was made electronically. The first copy is free of charge.
- **CMP-010.5.7.2** `[GDPR]` **Rectification (Art. 16).**
  1. Confirm the inaccuracy or incompleteness with the Data Owner, using evidence supplied by the Data Subject where needed.
  2. Correct or complete the data in every system holding it.
  3. Notify each recipient of the correction under section 5.10, unless this proves impossible or involves disproportionate effort, and tell the Data Subject about those recipients on request (Art. 19).
  4. Where the Organization disputes the accuracy, restrict the data under CMP-010.5.7.4 while the dispute is resolved, if the Data Subject requests it.
- **CMP-010.5.7.3** `[GDPR]` **Erasure (Art. 17).**
  1. Confirm that one of the grounds in Art. 17(1) applies.
  2. Check for exemptions under Art. 17(3) (e.g. a legal obligation to retain, or the establishment, exercise or defence of legal claims) and for any Legal Hold (CMP-004.5.4.7). Data covered by an exemption SHALL be retained only to the extent of the exemption and restricted from other use.
  3. Erase the data from production systems and end-user storage.
  4. For Backups, put the data beyond use: it SHALL NOT be restored to production use, and SHALL be erased when the Backup expires under CMP-004. If a Backup is restored, the erasure SHALL be re-applied before the restored system is used (SEC-018).
  5. Instruct Processors under section 5.10 and notify recipients under Art. 19.
  6. Where the Organization made the data public, take "reasonable steps", including technical measures, to inform other Controllers processing it of the erasure request (Art. 17(2)). The DPO SHALL document the steps taken.
- **CMP-010.5.7.4** `[GDPR]` **Restriction (Art. 18).**
  1. Confirm that one of the grounds in Art. 18(1) applies.
  2. Mark the data as restricted in each system so that, apart from storage, it is processed only with the Data Subject's consent, for legal claims, to protect another person's rights, or for important public interest.
  3. Notify recipients under Art. 19.
  4. Inform the Data Subject before the restriction is lifted.
- **CMP-010.5.7.5** `[GDPR]` **Portability (Art. 20).**
  1. Confirm the processing is based on consent or contract and carried out by automated means.
  2. Provide the Personal Data the Data Subject provided (including observed data) in a structured, commonly used, machine-readable format (e.g. CSV or JSON).
  3. Where requested and technically feasible, transmit it directly to another Controller over an encrypted channel meeting SEC-006.
- **CMP-010.5.7.6** `[GDPR]` **Objection (Art. 21).**
  1. Objection to direct marketing (including related profiling): stop the processing for direct marketing within 2 business days of receipt. No balancing test applies.
  2. Objection to processing based on legitimate interests or public interest: stop the processing unless the DPO documents compelling legitimate grounds that override the Data Subject's interests, rights and freedoms, or the processing is needed for legal claims. The processing SHALL be suspended while the DPO assesses the objection, where the Data Subject requests restriction under Art. 18(1)(d).
- **CMP-010.5.7.7** `[GDPR]` **Automated individual decision-making (Art. 22).** Where a Data Subject contests a decision based solely on automated processing that produces legal or similarly significant effects, the Data Owner SHALL arrange human review of the decision by a Workforce Member with authority to change it, and the Data Subject SHALL be given the opportunity to express their point of view. The outcome SHALL be communicated within the deadline in CMP-010.5.3.1.
- **CMP-010.5.7.8** `[GDPR]` **Withdrawal of consent (Art. 7(3)).** Processing based on the withdrawn consent SHALL stop within the time in CMP-005.5.5.4.

### 5.8 Handling each right: CPRA `[CPRA]`

- **CMP-010.5.8.1** `[CPRA]` **Right to know / access (§§1798.100, 1798.110, 1798.115).**
  1. Determine whether categories, specific pieces, or both, are requested; if unclear, provide both, subject to verification tier.
  2. Provide: categories of Personal Information collected; categories of sources; business or commercial purposes for collecting, selling or sharing; categories of third parties to which it is disclosed; categories sold or shared and to whom; categories disclosed for a business purpose and to whom; and the specific pieces, where requested and verified at V2.
  3. Cover Personal Information collected in the 12 months before the request and, where requested, information collected on or after 1 January 2022, unless this proves impossible or would involve disproportionate effort, which the DPO SHALL document.
  4. Do not disclose Social Security numbers, driver's license or other government identification numbers, financial account numbers, health insurance or medical identification numbers, account passwords, security questions and answers, or unique biometric data. State instead that the Organization collects that type of information (Cal. Code Regs. tit. 11, §7024(d)).
  5. Deliver in a portable and, to the extent technically feasible, readily usable format under section 5.13.
  6. The Organization is not required to respond to more than two requests to know from the same consumer in a 12-month period (§1798.130(b)); a third request SHALL be refused under CMP-010.5.12.4.
- **CMP-010.5.8.2** `[CPRA]` **Right to delete (§1798.105).**
  1. Check the exceptions in §1798.105(d) (e.g. completing the transaction, security and integrity, debugging, legal obligation, internal uses compatible with the context) and any Legal Hold (CMP-004.5.4.7).
  2. Delete by permanently erasing, de-identifying or aggregating the Personal Information in production systems.
  3. For archives and Backups, delete when the archive or Backup is next accessed or used, and restrict use until then.
  4. Notify service providers and contractors to delete under section 5.10.
  5. Notify all third parties to which the Organization sold or shared the Personal Information to delete it, unless this proves impossible or involves disproportionate effort, which the DPO SHALL document.
  6. Tell the consumer whether the request was complied with and, where data is retained under an exception, which exception applies.
  7. Maintain a record of the request so that deleted data is not re-collected or re-associated, retained under section 5.14.
- **CMP-010.5.8.3** `[CPRA]` **Right to correct (§1798.106).**
  1. Consider the totality of the circumstances, including the nature of the information, how it was obtained, and documentation provided by the consumer, to decide whether the information is more likely than not inaccurate.
  2. Correct the information in every system holding it, and instruct service providers and contractors under section 5.10.
  3. Where the Organization declines, explain the basis and tell the consumer they can submit a written statement of up to 250 words, which the Organization SHALL attach to the disputed information and make available with it.
  4. The Organization MAY delete the information instead of correcting it if deletion does not adversely affect the consumer, or the consumer consents.
- **CMP-010.5.8.4** `[CPRA]` **Opt-out of sale or sharing (§1798.120).**
  1. Stop selling and sharing the consumer's Personal Information within the deadline in CMP-010.5.3.1.
  2. Notify each third party to which the Organization sold or shared the consumer's Personal Information after the consumer submitted the request and before the Organization complied, and direct them to comply and forward the request to any further recipient.
  3. Treat an Opt-out Preference Signal (e.g. Global Privacy Control) as a valid opt-out for the browser or device and any associated known profile, without requiring further information.
  4. Wait at least 12 months before asking the consumer to opt back in (§1798.135(c)(4)).
- **CMP-010.5.8.5** `[CPRA]` **Limit use and disclosure of Sensitive Personal Information (§1798.121).** Stop using and disclosing Sensitive Personal Information for purposes other than those permitted in Cal. Code Regs. tit. 11, §7027(m), within the deadline in CMP-010.5.3.1, and notify service providers, contractors and third parties under CMP-010.5.8.4 step 2.
- **CMP-010.5.8.6** `[CPRA]` **Non-discrimination (§1798.125).** The Organization SHALL NOT deny goods or services, charge different prices, provide a different quality of service, or retaliate against a Workforce Member, applicant or contractor, because they exercised a right. Any financial incentive linked to Personal Information SHALL be offered only under a notice of financial incentive approved by the CPO.

### 5.9 Extensions and extension notices

- **CMP-010.5.9.1** An extension MAY be used only when the DPO approves it and records the reason in the DSR log before the original deadline.
- **CMP-010.5.9.2** `[GDPR]` An extension of up to 2 further months MAY be applied only where it is necessary because of the complexity or number of the requests (Art. 12(3)). The Data Subject SHALL be informed of the extension, with the reasons for the delay, within 1 month of receipt.
- **CMP-010.5.9.3** `[CPRA]` An extension of up to 45 additional days MAY be applied where "reasonably necessary" (§1798.130(a)(2)), taking into account the complexity and number of the consumer's requests. The consumer SHALL be notified of the extension, with the reason, within the first 45-day period.
- **CMP-010.5.9.4** `[CPRA]` No extension SHALL be applied to an opt-out or limit request.
- **CMP-010.5.9.5** The extension notice SHALL state the new due date and SHALL include any part of the response already available.

### 5.10 Processor, Subprocessor and recipient flow-down

- **CMP-010.5.10.1** Where a verified request requires action by a Processor or Subprocessor (rectification, erasure, restriction, correction, deletion, or retrieval of data for access or portability), Workforce Members designated by the DPO SHALL send written instructions to each relevant Processor within 5 business days of verification, using the contact in the Data Processing Agreement maintained under RSK-003.
- **CMP-010.5.10.2** The instruction SHALL require the Processor to act, to flow the instruction down to its Subprocessors, and to confirm completion in writing within 10 business days, or the shorter period in the Data Processing Agreement. Contractual terms obliging Processors to assist are set in CMP-005 and RSK-003.
- **CMP-010.5.10.3** The DPO SHALL escalate a Processor that has not confirmed within the required period to the Head of Procurement within 1 business day, and SHALL record any resulting delay to the Data Subject response in the DSR log.
- **CMP-010.5.10.4** `[GDPR]` Notifications to recipients under Art. 19, and `[CPRA]` to third parties under CMP-010.5.8.2 and CMP-010.5.8.4, SHALL be sent within 5 business days of the action being completed in the Organization's own systems.

### 5.11 When the Organization is a Processor

- **CMP-010.5.11.1** Where the Organization receives a DSR concerning Personal Data it processes as a Processor (or service provider or contractor), Workforce Members designated by the DPO SHALL forward the request to the relevant Controller (or business) within 2 business days of receipt, and SHALL NOT respond substantively to the Data Subject unless the Controller instructs it to.
- **CMP-010.5.11.2** Workforce Members designated by the DPO MAY tell the requester that the request has been passed to the Controller, without disclosing whether Personal Data is held.
- **CMP-010.5.11.3** The Organization SHALL carry out Controller instructions relating to a DSR within the period in the Data Processing Agreement or, where none is set, within 10 business days, and SHALL flow the instruction down to its own Subprocessors under section 5.10.

### 5.12 Exemptions, refusals and fees

- **CMP-010.5.12.1** Every full or partial refusal SHALL be approved by the DPO; refusals relying on a legal exemption, Legal Hold or litigation SHALL also be approved by the GC.
- **CMP-010.5.12.2** Grounds for refusal or partial refusal SHALL be limited to:
  1. failed or incomplete verification (section 5.4);
  2. `[GDPR]` the request is "manifestly unfounded or excessive", in particular because of its repetitive character (Art. 12(5)); `[CPRA]` the request is "manifestly unfounded or excessive" (§1798.145(h)(3)), with the burden of proof on the Organization;
  3. `[GDPR]` exemptions in Art. 15(4), Art. 17(3), Art. 21(1) (compelling legitimate grounds) and restrictions in Union or Member State law under Art. 23;
  4. `[CPRA]` the exceptions in §1798.105(d) for deletion, the exemptions in §1798.145 (including legal obligations, legal claims and evidentiary privilege), and information exempt under §1798.146 (medical information and PHI governed by HIPAA) or §1798.145(e) (data subject to the Gramm-Leach-Bliley Act);
  5. `[CPRA]` a third or later request to know within 12 months (CMP-010.5.8.1 step 6); and
  6. disclosure would adversely affect the rights and freedoms of others, which SHALL be addressed by redaction wherever possible rather than full refusal.
- **CMP-010.5.12.3** DSRs SHALL be handled free of charge. A fee MAY be charged only for a request that is "manifestly unfounded or excessive", or `[GDPR]` for further copies under Art. 15(3), and only where the DPO approves the fee and documents that it reflects administrative cost.
- **CMP-010.5.12.4** A refusal notice SHALL be sent within the deadline in CMP-010.5.3.1 and SHALL state: which parts of the request are refused; the reason and legal basis; the parts that are fulfilled; `[GDPR]` the right to lodge a complaint with a Supervisory Authority and to seek a judicial remedy (Art. 12(4)); and `[CPRA]` where a deletion request is denied, whether the Organization sells or shares the data and how to opt out.

### 5.13 Response delivery and closure

- **CMP-010.5.13.1** Responses containing Personal Data SHALL be delivered through a secure portal or as an encrypted file, with the decryption key sent by a separate channel, meeting SEC-006. Responses SHALL NOT be sent to an address or account that was not verified under section 5.4.
- **CMP-010.5.13.2** Responses SHALL be written in clear and plain language, in the language of the request where the Organization operates in that language.
- **CMP-010.5.13.3** Workforce Members designated by the DPO SHALL close the request in the DSR log only after the response is sent and all Processor confirmations are received or escalated under CMP-010.5.10.3.

### 5.14 Logging and records

- **CMP-010.5.14.1** The DPO SHALL maintain a DSR log in a system with access restricted under SEC-003 to Workforce Members designated by the DPO, the DPO, the CPO and the GC.
- **CMP-010.5.14.2** The DSR log SHALL record for each request: unique ID; date and time of receipt and channel; applicable law; right or rights requested; requester type (Data Subject or agent); verification tier, method and outcome (not the verification documents); Controller or Processor role; due date and any extension, with reason and notice date; systems searched and Processors instructed, with confirmation dates; actions taken; outcome (fulfilled, partially fulfilled, refused, unverified, withdrawn) and refusal grounds; response date and delivery method; handler; and DPO review.
- **CMP-010.5.14.3** DSR log entries and response records SHALL be retained for the period in CMP-004 row R-08 for data subject request records. `[CPRA]` That period SHALL be no shorter than the 24 months required by Cal. Code Regs. tit. 11, §7101.

### 5.15 CPRA metrics disclosure `[CPRA]`

- **CMP-010.5.15.1** `[CPRA]` The CPO SHALL determine by 31 January of each year whether, in the previous calendar year, the Organization knew or should have known that it, alone or in combination, bought, received for commercial purposes, sold or shared the Personal Information of 10,000,000 or more consumers (Cal. Code Regs. tit. 11, §7102(a)), and SHALL record the determination.
- **CMP-010.5.15.2** `[CPRA]` Where the threshold is met, the DPO SHALL compile, for the previous calendar year (the 12 months from 1 January to 31 December), the number of requests to know, delete, correct, opt out of sale or sharing, and limit use of Sensitive Personal Information that the Organization received, complied with in whole or in part, and denied, and the median or mean number of days within which it substantively responded to each type.
- **CMP-010.5.15.3** `[CPRA]` The CPO SHALL approve the metrics and publish them in, or through a link in, the Organization's privacy policy by 1 July of each calendar year.
- **CMP-010.5.15.4** `[CPRA]` Where the threshold is met, the Organization SHALL also establish, document and comply with a training policy so that all individuals responsible for handling consumer requests are informed of the CPRA requirements (Cal. Code Regs. tit. 11, §7102(b)). This training is delivered under PPL-002.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| DPO | Owns this Procedure; maintains intake channels and the DSR log; approves extensions, refusals and fees; performs quality review of access responses; escalates overdue tasks; compiles CPRA metrics |
| CPO | Approves this Procedure; determines CPRA metrics applicability; approves and publishes metrics; approves financial incentive notices |
| GC | Approves refusals relying on legal exemptions, Legal Hold or litigation; confirms deadline-calculation assumptions |
| Workforce Members designated by the DPO | Logs, triages, verifies and coordinates requests; sends acknowledgements, instructions and responses |
| System Owners | Complete search, correction, restriction and deletion tasks within 10 business days and provide Evidence |
| Data Owners | Confirm accuracy disputes; arrange human review for Art. 22 requests |
| Head of Procurement | Receives escalations of non-responsive Processors and enforces contractual assistance terms |
| CISO | Ensures secure response delivery and the security of the DSR log; receives suspected fraudulent-request escalations through RES-002 |
| Workforce Members | Forward any DSR received to the privacy email address within 1 business day |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| CMP-010.7.1 | `[GDPR]` Response deadline | GDPR: 1 month, extendable by 2 months (from receipt) |
| CMP-010.7.2 | `[CPRA]` Acknowledgement deadline | CPRA: acknowledge within 10 business days (of receipt) |
| CMP-010.7.3 | `[CPRA]` Response deadline | CPRA: respond within 45 days, extendable by 45 days (from receipt) |
| CMP-010.7.4 | `[CPRA]` Opt-out of sale or sharing; limit use of Sensitive Personal Information | No later than 15 business days |
| CMP-010.7.5 | Forwarding of misdirected DSRs | Within 1 business day |
| CMP-010.7.6 | Logging | Within 1 business day of receipt by the Organization |
| CMP-010.7.7 | Clarification request | Within 5 business days of receipt |
| CMP-010.7.8 | Verification information request | Within 5 business days of logging |
| CMP-010.7.9 | Close as unverified | No verification information within 30 days of request |
| CMP-010.7.10 | Deletion of verification documents | Per CMP-004.5.2.3 |
| CMP-010.7.11 | Search tasks issued to System Owners | Within 3 business days of verification |
| CMP-010.7.12 | System Owner task completion | Within 10 business days of issue |
| CMP-010.7.13 | Processor instruction | Within 5 business days of verification |
| CMP-010.7.14 | Processor confirmation | Within 10 business days, or shorter contractual period |
| CMP-010.7.15 | Recipient / third-party notification | Within 5 business days of completing own-system action |
| CMP-010.7.16 | Forwarding to Controller when the Organization is Processor | Within 2 business days |
| CMP-010.7.17 | Stop direct marketing on objection; stop processing on consent withdrawal | Objection: within 2 business days; consent withdrawal: per CMP-005.5.5.4 |
| CMP-010.7.18 | Intake channel testing | Every 3 months |
| CMP-010.7.19 | DSR record retention | As set in CMP-004 |
| CMP-010.7.20 | `[CPRA]` Metrics publication | By 1 July each year, for the previous calendar year, where the §7102 threshold is met |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| DSRs responded to within the legal deadline (including approved extensions) | 100% | Monthly | DPO |
| `[CPRA]` Acknowledgements sent within 10 business days | 100% | Monthly | DPO |
| `[CPRA]` Opt-out and limit requests actioned within 15 business days | 100% | Monthly | DPO |
| DSRs logged within 1 business day of receipt | ≥ 98% | Monthly | DPO |
| Requests extended, as a share of total | ≤ 10% | Quarterly | DPO |
| System Owner tasks completed within 10 business days | ≥ 95% | Monthly | DPO |
| Processor confirmations received within the required period | ≥ 95% | Quarterly | DPO |
| Responses delivered to an unverified recipient | 0 | Monthly | DPO |
| Supervisory Authority or regulator complaints upheld relating to DSR handling | 0 | Quarterly | CPO |
| Intake channel tests passed | 100% | Quarterly | DPO |

DSR metrics are reported to the ISSC monthly as part of the operational metrics under GOV-003.

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

No Exception MAY be granted against a statutory deadline, a statutory verification limit, the
prohibition on discrimination, or the content of a refusal notice. These are legal requirements,
not internal standards.

## 10. Enforcement

Non-compliance is handled under CMP-007.

Failure to forward a DSR, deliberate delay, or disclosure of Personal Data to an unverified
requester SHALL be reported to the DPO and, where Personal Data was disclosed, handled as a
Security Incident under RES-002 and assessed for notification under RES-003.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| CMP-010.5.1 – 5.3 | A.5.31, A.5.34 | GV.OC-03 | PT-5, PM-26 | 3.1 | P1.1, P5.1 | APO13, MEA03 | `[GDPR]` Art. 12; `[CPRA]` §1798.130, §1798.135; Cal. Code Regs. tit. 11, §§7025–7027 |
| CMP-010.5.4 – 5.5 | A.5.16, A.5.34 | PR.AA-02 | IA-12, PM-26 | — | P5.1 | DSS05 | `[GDPR]` Art. 11, 12(6); `[CPRA]` Cal. Code Regs. tit. 11, §§7060–7063 |
| CMP-010.5.6 – 5.8 | A.5.12, A.5.34 | ID.AM-07 | PM-5, PT-2, SI-18 | 3.2 | P5.1, P5.2, P4.3 | APO14 | `[GDPR]` Art. 7(3), 15–22; `[CPRA]` §§1798.100–1798.125 |
| CMP-010.5.9 | A.5.34 | GV.OC-03 | PM-26 | — | P5.1 | MEA03 | `[GDPR]` Art. 12(3); `[CPRA]` §1798.130(a)(2) |
| CMP-010.5.10 – 5.11 | A.5.19, A.5.20, A.5.34 | GV.SC-05 | SA-9, PM-26 | 15.4 | P6.1, CC9.2 | APO10 | `[GDPR]` Art. 19, 28(3)(e); `[CPRA]` §1798.105(c) |
| CMP-010.5.12 | A.5.34 | GV.OC-03 | PM-26 | — | P5.1 | MEA03 | `[GDPR]` Art. 12(4)–(5), 17(3), 23; `[CPRA]` §§1798.105(d), 1798.145, 1798.146 |
| CMP-010.5.13 | A.5.14, A.8.24 | PR.DS-02 | SC-8 | 3.10 | C1.1, P6.1 | DSS05 | `[GDPR]` Art. 12(1), 32 |
| CMP-010.5.14 – 5.15 | 7.5; A.5.33 | GV.OV-01 | AU-11, PM-26 | — | P8.1 | MEA01 | `[GDPR]` Art. 5(2); `[CPRA]` Cal. Code Regs. tit. 11, §§7101–7102 |

## 12. Related documents

CMP-001, CMP-003, CMP-004, CMP-005, CMP-007, GOV-003, RSK-003, SEC-001, SEC-002, SEC-003,
SEC-004, SEC-006, SEC-018, RES-002, RES-003, PPL-002, TPL-010, REF-001, REF-002

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Data Protection Officer (DPO) | | | |
| Approver: Chief Privacy Officer (CPO) | | | |
