# SEC-014 — Email & Communications Security Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | SEC-014 |
| Title | Email & Communications Security Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Information Officer (CIO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months, and on the event-triggered reviews in GOV-002.7.4 |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-004, SEC-001, SEC-002, SEC-003, SEC-005, SEC-006, SEC-008, SEC-012, SEC-013, RSK-003, RES-002, PPL-002, CMP-004, CMP-005 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CIO | Initial release |

## 3. Purpose

This policy sets the Organization's requirements for securing email, messaging,
collaboration, video conferencing and telephony services. It protects the Organization's
domains from spoofing, reduces the risk of phishing, Malware and business email
compromise, ensures information is transmitted in accordance with its Classification
Level, and limits business communications to approved, recorded channels.

## 4. Scope

- **People:** all Workforce Members and Third Parties who send or receive communications using Organization accounts, domains or approved tools.
- **Systems:** email platforms and gateways; all domains and subdomains registered by or for the Organization; instant messaging, chat and collaboration platforms; video conferencing services; telephony, voicemail, fax and contact-center systems; and any Third Party that sends email on the Organization's behalf (e.g. marketing, ticketing or payroll platforms).
- **Data:** all information transmitted through these channels, including attachments, recordings, transcripts and metadata.
- **Locations:** all locations from which these services are used.
- **Third parties:** Third Parties sending email using Organization domains SHALL meet section 5.1 as a contractual condition under RSK-003.

Acceptable personal use of communication tools is governed by GOV-004. Classification and
handling rules are in SEC-002. Endpoint and Mobile Device controls are in SEC-008.

## 5. Policy statements

### 5.1 Domain authentication: SPF, DKIM and DMARC

- **SEC-014.5.1.1** The CIO SHALL maintain a Domain Register listing every domain and subdomain registered by or for the Organization, its purpose (sending, receiving, parked), its DNS host, its registrar, and the Third Parties authorized to send mail on its behalf. The register SHALL be reconciled with the registrar accounts every 6 months.
- **SEC-014.5.1.2** Each sending domain SHALL publish a Sender Policy Framework (SPF) record that lists only authorized sending sources, ends with a hard-fail mechanism (`-all`), and resolves within the SPF limit of 10 DNS lookups.
- **SEC-014.5.1.3** All outbound email from Organization domains, including email sent by authorized Third Parties, SHALL be signed with DomainKeys Identified Mail (DKIM) using a key aligned to the From domain.
- **SEC-014.5.1.4** DKIM signing keys SHALL meet SEC-006.5.2.6. Where a platform supports only shorter RSA keys, the CIO SHALL request the Exception that SEC-006.5.2.6 requires.
- **SEC-014.5.1.5** DKIM keys SHALL be rotated at the Cryptoperiod in SEC-006.7.3, and immediately on suspected compromise or on termination of a Third Party sender.
- **SEC-014.5.1.6** Each domain SHALL publish a Domain-based Message Authentication, Reporting and Conformance (DMARC) record with aggregate reporting (`rua`) to an address monitored by the Organization.
- **SEC-014.5.1.7** The target DMARC policy for every domain is `p=reject`, with subdomain policy `sp=reject` and enforcement applied to 100% of messages. Domains SHALL progress through the following stages, advancing when aggregate reports show that at least 98% of legitimate mail passes DMARC alignment:

| Stage | Policy | Maximum duration |
|---|---|---|
| 1. Monitoring | `p=none` | 90 days from domain onboarding |
| 2. Partial enforcement | `p=quarantine` | 90 days |
| 3. Full enforcement (target) | `p=reject` | Permanent |

- **SEC-014.5.1.8** Domains that send no email (parked domains) SHALL publish an SPF record of `v=spf1 -all`, a DMARC record of `p=reject`, and a null MX record, immediately on registration.
- **SEC-014.5.1.9** The CIO SHALL review DMARC aggregate reports at least weekly and SHALL investigate unauthorized sending sources. Spoofing of an Organization domain detected in reports SHALL be reported to the SOC under SEC-012.
- **SEC-014.5.1.10** Inbound email SHALL be evaluated against the sender's SPF, DKIM and DMARC. Messages failing a sender's `p=reject` policy SHALL be rejected; messages failing `p=quarantine` SHALL be quarantined.
- **SEC-014.5.1.11** Receiving domains SHALL publish an MTA-STS policy in `enforce` mode and a TLS reporting (TLS-RPT) record, so that inbound mail transport is encrypted to the minimums in SEC-006.
- **SEC-014.5.1.12** DNS records for Organization domains SHALL be changed only through SEC-013, and registrar and DNS-hosting accounts SHALL be protected by MFA per SEC-004 and registrar lock.

### 5.2 Anti-phishing and impersonation protection

- **SEC-014.5.2.1** The email platform SHALL apply anti-phishing controls to all inbound mail, including: sender reputation, display-name and domain impersonation detection for executives and finance roles, lookalike-domain detection, and machine-learning or signature-based phishing classification.
- **SEC-014.5.2.2** The CIO SHALL maintain the list of protected identities for impersonation detection, including, at minimum, the Board of Directors, the CEO, CFO, CIO, CTO, CISO, GC, CHRO, and all Workforce Members authorized to approve payments.
- **SEC-014.5.2.3** The SOC Manager SHALL monitor for newly registered domains resembling Organization domains at least daily and SHALL initiate takedown or blocking for each confirmed malicious lookalike within 2 business days.
- **SEC-014.5.2.4** Every email client and mobile email application SHALL provide a one-click "report phishing" function that submits the full message to the SOC.
- **SEC-014.5.2.5** Reported messages SHALL be triaged as alerts under the triage SLAs in SEC-012. Where a reported message is confirmed malicious, the SOC SHALL remove all copies from mailboxes across the Organization within 60 minutes of confirmation.
- **SEC-014.5.2.6** Requests received by email, chat or telephone to change payment instructions, bank details, payroll destinations or vendor master data, or to make an urgent payment, SHALL be verified by a call-back to a telephone number already on record (not one supplied in the request) before action is taken. The CFO SHALL own this verification Control.
- **SEC-014.5.2.7** Phishing awareness and simulation are delivered under PPL-002.

### 5.3 Attachment and link protection

- **SEC-014.5.3.1** All inbound and internal email attachments SHALL be scanned for Malware before delivery. Attachments of file types capable of executing code (e.g. `.exe`, `.js`, `.vbs`, `.scr`, `.iso`, `.img`, `.hta`, `.lnk`, `.ps1`, macro-enabled Office formats) SHALL be blocked unless the sender is on an allow-list approved by the Head of Security Engineering.
- **SEC-014.5.3.2** Attachments that cannot be scanned, including password-protected archives from external senders, SHALL be quarantined pending SOC review.
- **SEC-014.5.3.3** Attachments that pass static scanning SHOULD be detonated in a sandbox before delivery. Where sandboxing delays delivery, delivery of a sanitized version (e.g. converted to PDF) with the original released after analysis is permitted.
- **SEC-014.5.3.4** URLs in inbound email and messaging SHALL be rewritten or otherwise protected so that the destination is evaluated at the time of click. Destinations classified as malicious SHALL be blocked.
- **SEC-014.5.3.5** The same Malware and link protection SHALL apply to files and links shared through approved collaboration platforms where the platform supports it.
- **SEC-014.5.3.6** Changes to email filtering rules, allow-lists and transport rules SHALL follow SEC-013 and SHALL be logged under SEC-012.

### 5.4 External sender tagging and mail-flow restrictions

- **SEC-014.5.4.1** Email received from outside the Organization SHALL display a visible external-sender tag (e.g. a subject prefix or banner) in all supported clients.
- **SEC-014.5.4.2** Collaboration and chat platforms SHALL visibly identify external participants and external channels.
- **SEC-014.5.4.3** Automatic forwarding of email to external domains SHALL be blocked at the platform level. Exceptions SHALL be approved under CMP-003.
- **SEC-014.5.4.4** Creation of mailbox rules that forward, redirect or delete messages SHALL be logged and monitored by the SOC under SEC-012.
- **SEC-014.5.4.5** Legacy authentication protocols that do not support MFA (e.g. basic authentication for POP, IMAP and SMTP) SHALL be disabled. Application relays SHALL authenticate and SHALL be restricted to approved source addresses.
- **SEC-014.5.4.6** Outbound email SHALL be inspected by Data Loss Prevention rules that detect Restricted data patterns defined by the CISO under SEC-002 (e.g. PAN, government identifiers, health identifiers) and that block or encrypt the message in accordance with section 5.5.

### 5.5 Email encryption by Classification Level

- **SEC-014.5.5.1** The Organization SHALL provide the following technical mechanisms. Whether information of each Classification Level may be sent externally at all is determined by SEC-002; this section sets the mechanism to use where it is permitted.

| Classification Level | Internal email | External email |
|---|---|---|
| Public | Opportunistic TLS | Opportunistic TLS |
| Internal | TLS within the Organization's platform | Opportunistic TLS |
| Confidential | TLS within the Organization's platform | Enforced TLS to recipient domains on the Organization's enforced-TLS list; otherwise message-level encryption or the approved secure file-transfer portal |
| Restricted | Message-level encryption, or a link to the approved repository with access restricted to named recipients | Message-level encryption or the approved secure file-transfer portal only, with access restricted to named recipients |

- **SEC-014.5.5.2** Encryption algorithms, protocol versions and key management SHALL meet SEC-006.
- **SEC-014.5.5.3** `[PCI]` PAN in end-user messaging technologies is governed by SEC-019.5.6.4. Messaging and email DLP SHALL enforce it through SEC-014.5.4.6.
- **SEC-014.5.5.4** `[HIPAA]` ePHI sent by email outside the Organization's platform SHALL use message-level encryption or the approved secure portal, unless an individual has requested unencrypted communication after being informed of the risk, as documented under CMP-008.
- **SEC-014.5.5.5** Passwords or keys used to open encrypted messages or archives SHALL be communicated through a separate channel from the message.

### 5.6 Approved messaging and collaboration tools

- **SEC-014.5.6.1** The CIO SHALL maintain a register of approved communication tools (email, chat, collaboration, video conferencing, telephony, SMS gateways) and the highest Classification Level each is approved to carry. Tools SHALL be approved through SEC-001 and, where provided by a Third Party, assessed under RSK-003.
- **SEC-014.5.6.2** Organization business SHALL be conducted only through approved communication tools using Organization-managed accounts. Personal email accounts and unapproved consumer messaging applications SHALL NOT be used for Organization business. Use of unapproved tools is Shadow IT.
- **SEC-014.5.6.3** Messaging features that automatically delete messages (ephemeral or disappearing messages) SHALL be disabled on approved tools, except where the CIO and GC have approved them for a defined use case, so that records are retained under CMP-004.
- **SEC-014.5.6.4** Where a business communication occurs on an unapproved channel (e.g. a customer contacts a Workforce Member by personal text message), the Workforce Member SHALL move the conversation to an approved tool and SHALL preserve a copy of the substantive content in an approved system within 1 business day.
- **SEC-014.5.6.5** Approved collaboration platforms SHALL be configured so that: external sharing is disabled by default and enabled per workspace or channel by the System Owner; guest accounts expire after 90 days without renewal; and sharing links to Confidential or Restricted content require authentication.
- **SEC-014.5.6.6** Third-party applications, bots and integrations connected to approved communication tools SHALL be approved by the Head of Security Engineering before installation.
- **SEC-014.5.6.7** Generative AI features (e.g. meeting summarization, message drafting) within communication tools SHALL be enabled only where approved under RSK-006 (RSK-006.5.2.5).

### 5.7 Video conferencing

- **SEC-014.5.7.1** Meetings SHALL be hosted only on approved video conferencing tools using Organization accounts.
- **SEC-014.5.7.2** Meetings at which Confidential or Restricted information will be discussed SHALL use a waiting room or lobby, admit only identified participants, and SHALL NOT be published with a public join link.
- **SEC-014.5.7.3** Recording or transcription of a meeting SHALL be announced to all participants at the start, and recording SHALL comply with the consent requirements identified in the Obligations Register (CMP-001) for the participants' jurisdictions.
- **SEC-014.5.7.4** Recordings and transcripts SHALL inherit the highest Classification Level of the information discussed, SHALL be stored only in the approved repository, and SHALL be retained and deleted under CMP-004.
- **SEC-014.5.7.5** Hosts SHALL verify, before sharing a screen, that no unrelated Confidential or Restricted information is visible, and SHALL use application-level rather than full-desktop sharing where available.
- **SEC-014.5.7.6** Participants SHALL use headphones and a location that prevents unauthorized persons from hearing or viewing Confidential or Restricted discussions, in accordance with SEC-015.

### 5.8 Telephony, voicemail and fax

- **SEC-014.5.8.1** Voicemail accounts SHALL be protected by a PIN of at least 6 digits that is not sequential, repeated or equal to the extension number. Default PINs SHALL be changed on first use.
- **SEC-014.5.8.2** Restricted information SHALL NOT be left in a voicemail message.
- **SEC-014.5.8.3** Workforce Members SHALL NOT disclose Confidential or Restricted information, credentials or MFA codes by telephone to a caller whose identity has not been verified by a call-back to a number on record or by an identity-verification procedure approved by the CISO (SEC-004.5.3.5). Service desk password and MFA resets SHALL follow the identity-verification requirements in SEC-004.
- **SEC-014.5.8.4** Telephony administration (call routing, forwarding, call recording settings) SHALL be restricted to Privileged Accounts under SEC-005, and changes SHALL follow SEC-013.
- **SEC-014.5.8.5** Call recording SHALL be enabled only on lines approved by the GC and SHALL announce recording to callers. `[PCI]` Call recordings SHALL NOT capture SAD; contact-center systems that take card payments by phone SHALL pause or suppress recording during card-data capture, or use a payment method that keeps card data out of the recording.
- **SEC-014.5.8.6** Fax SHOULD NOT be used. Where fax is required, Confidential or Restricted transmissions SHALL use a cover sheet with a confidentiality notice, the sender SHALL confirm the recipient number before sending, and inbound fax devices SHALL be located in an area with access limited to authorized Workforce Members or deliver to a secured electronic inbox.

### 5.9 Mailbox and account security

- **SEC-014.5.9.1** Access to email and communication tools SHALL require authentication through the Organization's SSO with MFA per SEC-004.
- **SEC-014.5.9.2** Delegate and shared-mailbox access SHALL be granted and reviewed under SEC-003. Administrative access to communication platforms SHALL be managed under SEC-005.
- **SEC-014.5.9.3** Email and communication platform audit logs SHALL be forwarded to the SIEM as required by SEC-012.
- **SEC-014.5.9.4** Mass email to external recipients SHALL be sent only through approved bulk-sending platforms that meet section 5.1, and SHALL comply with marketing consent requirements in CMP-005.

### 5.10 Retention

- **SEC-014.5.10.1** Email, messages, chat, recordings, transcripts and voicemail SHALL be retained and deleted in accordance with CMP-004. Platform retention settings SHALL be configured by the CIO to implement CMP-004 and SHALL NOT be shortened by Users.
- **SEC-014.5.10.2** Legal Holds issued by the GC SHALL be applied to all affected communication tools within 2 business days of issue.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CIO | Owns this policy; maintains the Domain Register and approved tools register; operates email, collaboration and telephony platforms; manages SPF, DKIM, DMARC and MTA-STS; configures retention. |
| CISO | Defines Restricted data patterns for DLP; approves identity-verification procedures; oversees anti-phishing effectiveness. |
| Head of Security Engineering | Engineers and tunes anti-phishing, attachment, link and DLP controls; approves allow-lists and third-party integrations. |
| SOC Manager | Triages reported phishing; removes malicious messages; monitors lookalike domains, DMARC failures and mailbox-rule abuse. |
| CFO | Owns call-back verification of payment and bank-detail changes. |
| GC | Approves call recording and ephemeral-messaging use cases; issues Legal Holds. |
| CPO / DPO | Advise on recording consent and marketing consent. |
| System Owner | Configures external sharing for the workspaces and channels they own. |
| Workforce Member | Uses approved tools only; reports suspicious messages; applies encryption by Classification Level; verifies payment-change requests. |
| ISSC | Approves this policy. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| SEC-014.7.1 | SPF | `-all` on every sending domain; ≤ 10 DNS lookups |
| SEC-014.7.2 | DKIM | All outbound mail signed; key length per SEC-006.5.2.6; rotation per SEC-006.7.3 |
| SEC-014.7.3 | DMARC target policy | `p=reject`, `sp=reject`, applied to 100% of messages |
| SEC-014.7.4 | DMARC staging | `p=none` ≤ 90 days, then `p=quarantine` ≤ 90 days, then `p=reject`; advance at ≥ 98% legitimate pass rate |
| SEC-014.7.5 | Parked domains | `v=spf1 -all`, DMARC `p=reject`, null MX, on registration |
| SEC-014.7.6 | DMARC report review | Weekly |
| SEC-014.7.7 | Domain Register reconciliation | Every 6 months |
| SEC-014.7.8 | Inbound transport | MTA-STS `enforce` and TLS-RPT on receiving domains |
| SEC-014.7.9 | Lookalike domain monitoring | Daily; takedown or block within 2 business days of confirmation |
| SEC-014.7.10 | Removal of confirmed malicious messages | Within 60 minutes of confirmation |
| SEC-014.7.11 | External auto-forwarding | Blocked |
| SEC-014.7.12 | External sender tagging | All inbound external email |
| SEC-014.7.13 | Collaboration guest accounts | Expire after 90 days without renewal |
| SEC-014.7.14 | Voicemail PIN | ≥ 6 digits, non-trivial |
| SEC-014.7.15 | Legal Hold applied to communication tools | Within 2 business days of issue |
| SEC-014.7.16 | Retention | As set in CMP-004 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Sending domains at DMARC `p=reject` | 100% (after staging) | Monthly | CIO |
| Outbound mail passing DMARC alignment | ≥ 98% | Monthly | CIO |
| Parked domains with null SPF, DMARC reject and null MX | 100% | Quarterly | CIO |
| Confirmed malicious messages removed within 60 minutes | ≥ 95% | Monthly | SOC Manager |
| Phishing messages reaching inboxes per 1,000 mailboxes | Decreasing trend | Monthly | Head of Security Engineering |
| Payment-change requests verified by call-back (sample test) | 100% | Quarterly | CFO |
| Active external auto-forwarding rules | 0 | Monthly | CIO |
| Unapproved communication tools detected | 0 unresolved after 30 days | Quarterly | CIO |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following requirements SHALL NOT receive an Exception: `[PCI]` SEC-019.5.6.4 as applied by SEC-014.5.5.3 (no unprotected PAN by messaging) and SEC-014.5.2.6 (call-back verification of payment changes).

## 10. Enforcement

Non-compliance is handled under CMP-007.

Use of personal accounts or unapproved tools for Organization business, or sending Restricted information without the mechanism required in section 5.5, SHALL be reported to the SOC and assessed as a potential Security Incident under RES-002.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| SEC-014.5.1 | A.5.14, A.8.20, A.8.21 | PR.DS-02, PR.PS-01 | SC-8, SC-20, SI-8 | 9.5 | CC6.7 | DSS05.02 | — |
| SEC-014.5.2 | A.5.14, A.8.7, A.6.3 | DE.CM-09, DE.AE-02 | SI-3, SI-4, SI-8, AT-2 | 9.2, 9.7, 14.2 | CC6.8, CC7.2 | DSS05.01 | PCI DSS 5.4.1 |
| SEC-014.5.3 | A.8.7, A.8.23 | DE.CM-09 | SI-3, SI-8 | 9.3, 9.6, 9.7, 10.1 | CC6.8 | DSS05.01 | PCI DSS 5.2.1, 5.4.1 |
| SEC-014.5.4 | A.5.14, A.8.12 | PR.DS-02 | AC-4, SC-7, SI-4 | 3.13, 9.5 | CC6.7 | DSS05.02 | — |
| SEC-014.5.5 | A.5.14, A.8.24 | PR.DS-02 | SC-8, SC-13 | 3.10 | CC6.7, C1.1 | DSS05.02 | PCI DSS 4.2.2; HIPAA §164.312(e)(1), §164.312(e)(2)(ii); GDPR Art. 32 |
| SEC-014.5.6 | A.5.14, A.5.23, A.5.33 | GV.SC-07, ID.AM-02 | CM-7, SA-9 | 2.3 | CC6.1, CC9.2 | APO10.04, BAI09 | SOX §404 |
| SEC-014.5.7 | A.5.14, A.7.7 | PR.DS-02 | SC-15, AC-20 | — | CC6.7 | DSS05.02 | GDPR Art. 6 |
| SEC-014.5.8 | A.5.14, A.6.3 | PR.AA-01 | IA-2, SC-8 | — | CC6.1 | DSS05.04 | PCI DSS 3.3.1 |
| SEC-014.5.9 | A.5.15, A.8.5 | PR.AA-01, PR.AA-03 | AC-2, IA-2 | 6.3, 6.5 | CC6.1 | DSS05.04 | HIPAA §164.312(d) |
| SEC-014.5.10 | A.5.33 | GV.OC-03 | AU-11, SI-12 | 3.4 | C1.2 | APO14 | HIPAA §164.316(b)(2)(i); SOX §802 |

## 12. Related documents

ISP-000, GOV-004, GOV-006, SEC-001, SEC-002, SEC-003, SEC-004, SEC-005, SEC-006, SEC-008, SEC-012, SEC-013, SEC-015, RSK-003, RSK-006, RES-002, PPL-002, CMP-001, CMP-003, CMP-004, CMP-005, CMP-007, CMP-008, REF-001, REF-002

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CIO | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
