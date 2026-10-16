# GOV-004 — Acceptable Use Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | GOV-004 |
| Title | Acceptable Use Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Information Security Officer (CISO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-002, GOV-006, RSK-006, CMP-005, CMP-006, CMP-007, SEC-002, SEC-004, SEC-008, SEC-014, SEC-015, RES-001, PPL-001, PPL-002, TPL-009 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CISO | Initial release. Absorbs the confidentiality and conflict-of-interest content of retired GOV-005 (Code of Conduct, Information Security Addendum); identifier GOV-005 is retired and not reused. |

## 3. Purpose

This Policy sets the rules of behavior that every Workforce Member and Third Party user SHALL
follow when using the Organization's Information Assets. It defines acceptable and prohibited
use, the limits of personal use, the use of Generative AI tools, social media and intellectual
property, the confidentiality and conflict-of-interest obligations relating to information
security, and the notice that the Organization monitors the use of its Information Systems.

## 4. Scope

- **People:** every Workforce Member, and every individual working for a Third Party who is given an account on, or access to, an Organization Information System.
- **Systems:** every Information System, Endpoint, Mobile Device, network, Cloud Service, communication tool and account provided, managed or paid for by the Organization, and every personally owned device used under SEC-008 while it is used for Organization business.
- **Data:** all information owned by or entrusted to the Organization, at every Classification Level under SEC-002.
- **Locations:** Organization premises, remote work locations and travel (SEC-015).
- **Third parties:** Third Parties whose personnel use Organization Information Assets, bound by contract under RSK-003.

## 5. Policy statements

### 5.1 General principles

- **GOV-004.5.1.1** Information Assets are provided for the Organization's business purposes. Users SHALL use them only for authorized business purposes and for the personal use permitted in section 5.5.
- **GOV-004.5.1.2** Users SHALL access only the information and Information Systems they are authorized to access, on the basis of Need to Know and Least Privilege, even where a system technically permits wider access.
- **GOV-004.5.1.3** Users SHALL handle information according to its Classification Level and the handling rules in SEC-002.
- **GOV-004.5.1.4** Users SHALL comply with every suite document that applies to their role, and SHALL attest to this Policy under GOV-002 using TPL-009 or its electronic equivalent.
- **GOV-004.5.1.5** Where a User is unsure whether an action is permitted by this Policy, the User SHALL ask their manager or the security team before taking the action.

### 5.2 Accounts and credentials

- **GOV-004.5.2.1** Users SHALL NOT share their passwords, MFA factors, tokens, certificates or other Secrets with any person, including managers, colleagues and IT support staff.
- **GOV-004.5.2.2** Users SHALL NOT use another person's account, or allow another person to use theirs.
- **GOV-004.5.2.3** Users SHALL create and protect credentials in accordance with SEC-004 and SHALL store Organization passwords only in an Organization-approved password manager.
- **GOV-004.5.2.4** Users SHALL NOT reuse a password used for an Organization account on any non-Organization service.
- **GOV-004.5.2.5** Users SHALL NOT use their Organization email address to register for non-business services, except professional services approved by their manager (for example professional association memberships).
- **GOV-004.5.2.6** Users who suspect that a credential has been disclosed or compromised SHALL change it and report it within the time limit in RES-001.5.2.1.
- **GOV-004.5.2.7** Users with Privileged Accounts SHALL use them only for the administrative tasks that require them and SHALL use a separate standard account for email, web browsing and other non-administrative work (SEC-005).

### 5.3 Endpoints, devices and workplace

- **GOV-004.5.3.1** Users SHALL access Organization Information Systems only from Organization-managed Endpoints, or from personally owned devices enrolled under SEC-008.
- **GOV-004.5.3.2** Users SHALL lock their screen whenever they leave an Endpoint unattended. Automatic lock settings are set in SEC-004 and SHALL NOT be altered by Users.
- **GOV-004.5.3.3** Users SHALL NOT disable, uninstall, bypass or reconfigure security software or settings on an Endpoint, including EDR, disk Encryption, firewall, patching agents and device management.
- **GOV-004.5.3.4** Users SHALL install only software on the Approved End-user Technology List, or software installed through the Organization's managed software catalogue. The CIO SHALL maintain the Approved End-user Technology List, covering software, hardware, Cloud Services and removable Media, and SHALL publish it to all Users.
- **GOV-004.5.3.5** Users SHALL NOT connect personal or unapproved hardware (including network devices, wireless access points and removable Media) to Organization networks or Endpoints, except as permitted by SEC-008.
- **GOV-004.5.3.6** At the end of each working day and whenever their workspace is left unattended for more than 30 minutes, Users SHALL secure Confidential and Restricted information in paper form or on removable Media in a locked drawer or cabinet and SHALL remove it from printers and shared spaces (clear desk).
- **GOV-004.5.3.7** Users SHALL report the loss or theft of any Endpoint, Mobile Device, Media or access badge within the time limit in RES-001.5.2.1.
- **GOV-004.5.3.8** Users working remotely or travelling SHALL comply with SEC-015.

### 5.4 Prohibited use

- **GOV-004.5.4.1** Users SHALL NOT use Organization Information Assets to:
  1. Circumvent, disable or test any security Control, or perform scanning, Penetration Testing, password cracking or traffic interception, unless authorized in writing under SEC-011.
  2. Access, copy, alter or delete information without authorization, or exceed authorized access.
  3. Introduce Malware, or knowingly open files or links reported as malicious.
  4. Create, store, transmit or access material that is unlawful, harassing, discriminatory, defamatory, sexually explicit, or that promotes violence, as defined in the Organization's human resources conduct rules.
  5. Infringe copyright, trademark, patent, trade secret or licensing terms (section 5.10).
  6. Operate an outside business, perform paid work for another party, or conduct political campaigning.
  7. Mine cryptocurrency or consume computing resources for non-business purposes.
  8. Send unsolicited bulk messages, chain messages or messages that misrepresent the sender's identity.
  9. Install or use remote access, anonymization, proxy or tunneling tools (for example Tor or personal VPN services) that are not on the Approved End-user Technology List.
  10. Transfer Organization information to personal email accounts, personal cloud storage, personal devices not enrolled under SEC-008, or any Cloud Service not approved under SEC-001 and RSK-003 (Shadow IT).
  11. Configure automatic forwarding of Organization email to an external address.
  12. Record meetings or calls without notifying all participants, or where recording is prohibited by law.
  13. Collect, copy or export Organization information in anticipation of Separation.
  14. Gamble, or access sites categorized as gambling, adult content or illegal file sharing.
  15. Engage in any activity that violates applicable law or regulation.
- **GOV-004.5.4.2** `[PCI]` Users SHALL NOT copy, move, store or transmit Cardholder Data outside the CDE, SHALL NOT send unprotected PANs through end-user messaging technologies (for example email, chat or SMS), and SHALL NOT store Sensitive Authentication Data in any form.
- **GOV-004.5.4.3** `[HIPAA]` Users SHALL access, use and disclose PHI only as permitted for their job function under CMP-008, and SHALL NOT access PHI of any individual, including themselves, family members, colleagues or public figures, without a job-related need.
- **GOV-004.5.4.4** The SOC Manager MAY authorize named security personnel in writing to perform activities in GOV-004.5.4.1 items 1, 3 and 9 for security testing, investigation or research. The authorization SHALL state scope and duration and SHALL be retained under CMP-004.

### 5.5 Personal use

- **GOV-004.5.5.1** Users MAY make incidental personal use of Organization email, internet access, telephones and Endpoints, provided that the use:
  1. does not breach section 5.4 or any other suite document;
  2. does not interfere with the User's duties or with the work of others;
  3. does not incur additional cost to the Organization beyond fixed-cost services already provided;
  4. does not involve storing personal files on Organization Information Systems beyond 1 GB per User, or storing personal files in shared repositories; and
  5. does not involve installing software or browser extensions for personal purposes.
- **GOV-004.5.5.2** Users SHALL NOT use Organization accounts, devices or networks to process the Personal Data of others for personal purposes.
- **GOV-004.5.5.3** Personal information that a User chooses to store on Organization Information Systems is subject to monitoring under section 5.13 and MAY be deleted at Separation. Users SHALL remove personal files before their Separation date.
- **GOV-004.5.5.4** A manager MAY restrict personal use for a role or team where business needs require it, by written notice to the affected Users.

### 5.6 Email, messaging and collaboration

- **GOV-004.5.6.1** Users SHALL conduct Organization business only through Organization-provided email, messaging and collaboration tools on the Approved End-user Technology List. Technical controls for these tools are set in SEC-014.
- **GOV-004.5.6.2** Users SHALL verify any request received by email, message or telephone to change payment details, transfer funds, disclose credentials or bypass a Control, by contacting the requester through a separately known channel before acting.
- **GOV-004.5.6.3** Users SHALL report suspected phishing messages using the reporting function provided under SEC-014.5.2.4 and SHALL NOT forward them to colleagues.
- **GOV-004.5.6.4** Users SHALL share Confidential and Restricted information with external recipients only through methods permitted for that Classification Level in SEC-002.

### 5.7 Data storage and Shadow IT

- **GOV-004.5.7.1** Users SHALL store Organization information only in Organization-approved repositories listed on the Approved End-user Technology List, and SHALL NOT keep the only copy of business information on a local Endpoint drive.
- **GOV-004.5.7.2** Users SHALL NOT sign up for, or use, any Cloud Service, browser extension, plug-in or integration for Organization business unless it is approved under SEC-001 and RSK-003, regardless of whether it is free of charge.
- **GOV-004.5.7.3** Users SHALL NOT grant third-party applications OAuth or API access to Organization accounts or data unless the application is on the Approved End-user Technology List.

### 5.8 Generative AI tools

- **GOV-004.5.8.1** Users SHALL use Generative AI tools for Organization business only where the tool is approved under RSK-006, and only within the Classification Levels and use cases recorded for that tool in the approved AI tools list (RSK-006.5.4.1).
- **GOV-004.5.8.2** Users SHALL NOT enter Confidential or Restricted information, Personal Data, Secrets or source code into any Generative AI tool unless RSK-006 approves that tool for that type of information.
- **GOV-004.5.8.3** Users SHALL NOT use personal accounts on Generative AI services for Organization work, even where the same service is approved under an Organization account.
- **GOV-004.5.8.4** Users SHALL review Generative AI output for accuracy, bias and suitability before relying on it, sharing it outside their team or publishing it, and remain accountable for any output they use.
- **GOV-004.5.8.5** Users SHALL NOT use Generative AI output to make or support a decision producing legal or similarly significant effects on an individual (for example hiring, termination, credit or access to services) unless that use case is approved under RSK-006.
- **GOV-004.5.8.6** Code produced with Generative AI assistance SHALL be subject to the same review and testing requirements as other code under SEC-010 (SEC-010.5.3.5).
- **GOV-004.5.8.7** Users SHALL label content as AI-generated where RSK-006.5.6.6 or applicable law requires disclosure.
- **GOV-004.5.8.8** Users SHALL report any entry of information into a non-approved Generative AI tool, or any AI output that discloses Organization or third-party information, under RES-001.

### 5.9 Social media and public communications

- **GOV-004.5.9.1** Users SHALL NOT disclose Confidential or Restricted information on social media, forums, code-sharing sites, public repositories or any other public platform.
- **GOV-004.5.9.2** Users SHALL NOT speak, post or publish on behalf of the Organization unless authorized in writing by the CEO or the CEO's delegate for external communications.
- **GOV-004.5.9.3** Users who identify themselves as Workforce Members on social media SHALL make clear that their views are their own when discussing topics related to the Organization's business.
- **GOV-004.5.9.4** Users SHALL NOT post images or video showing Endpoint screens, whiteboards, access badges, restricted areas of Organization facilities, or Organization network or security architecture.
- **GOV-004.5.9.5** Users SHOULD NOT publish details of the Organization's specific security technologies, configurations or internal processes in professional profiles or public talks without approval of the CISO.
- **GOV-004.5.9.6** Users SHALL NOT disclose Vulnerabilities in Organization Information Systems publicly. Vulnerabilities SHALL be reported under RES-001 or, for external reporters, through the VDP under SEC-011.
- **GOV-004.5.9.7** Users SHALL report suspected social engineering approaches received through social media (for example fake recruiter contacts requesting internal information) under RES-001.

### 5.10 Intellectual property and software licensing

- **GOV-004.5.10.1** Information, software, inventions and other work product created by Workforce Members in the course of their work for the Organization are the property of the Organization, as set out in the terms of employment or engagement under PPL-001.
- **GOV-004.5.10.2** Users SHALL NOT copy, install or distribute software, fonts, media, datasets or other material in breach of its license or copyright.
- **GOV-004.5.10.3** Users SHALL use open-source components in Organization software only in accordance with the license compliance requirements in SEC-010.5.9.5.
- **GOV-004.5.10.4** Users SHALL NOT bring to the Organization, or use in their work, confidential information or trade secrets belonging to a former employer or other third party without that party's authorization.
- **GOV-004.5.10.5** Users SHALL protect third-party confidential information received under a non-disclosure agreement in accordance with that agreement and SEC-002.
- **GOV-004.5.10.6** Users SHALL NOT publish, contribute or upload Organization source code, models or data to any public repository, open-source project or dataset without written approval of the CTO.

### 5.11 Confidentiality obligations

- **GOV-004.5.11.1** Every Workforce Member SHALL keep confidential all Organization information classified Internal, Confidential or Restricted, and all information entrusted to the Organization by customers, Third Parties and individuals, and SHALL use it only to perform their duties.
- **GOV-004.5.11.2** Every Workforce Member SHALL sign a confidentiality or non-disclosure undertaking before access to Organization information is granted, as part of the terms of employment or engagement under PPL-001. Acceptance of this Policy under TPL-009 SHALL constitute that undertaking where no separate agreement is signed.
- **GOV-004.5.11.3** [DECISION REQUIRED: Duration of post-Separation confidentiality. Recommended default: indefinite for Restricted information and trade secrets; 5 years after Separation for other Confidential and Internal information, or longer where a contract or law requires.] Confidentiality obligations SHALL continue after Separation: indefinitely for Restricted information and trade secrets, and for 5 years after Separation for other Confidential and Internal information, or longer where a contract or law requires.
- **GOV-004.5.11.4** `[GDPR]` Workforce Members SHALL process Personal Data only on the documented instructions of the Organization (GDPR Art. 29), and their confidentiality undertaking SHALL cover Personal Data (Art. 28(3)(b)).
- **GOV-004.5.11.5** `[HIPAA]` Workforce Members with access to PHI SHALL protect its confidentiality in accordance with CMP-008 and the HIPAA Privacy Officer's policies.
- **GOV-004.5.11.6** Workforce Members SHALL NOT discuss Confidential or Restricted information in public places, on public transport, or in any setting where it can be overheard or viewed by unauthorized persons.
- **GOV-004.5.11.7** Nothing in this Policy prohibits a Workforce Member from reporting a possible violation of law to a government agency or regulator, or from making disclosures protected under CMP-006 or applicable whistleblower law.

### 5.12 Conflicts of interest relating to information security

- **GOV-004.5.12.1** Workforce Members SHALL disclose to their manager and the GC, within 10 business days of the conflict arising, any of the following:
  1. A personal financial interest, directorship, advisory role or employment in a Third Party that provides security products or services to the Organization, or that is being evaluated to do so.
  2. A close personal relationship with a person whose access, Exception, Risk Acceptance or Change the Workforce Member approves or reviews.
  3. Outside work in information security, including consulting, Penetration Testing, bug bounty participation or security research, that relates to the Organization, its customers, its competitors or its Third Parties.
  4. Any other interest that could influence, or appear to influence, a security assessment, access decision, incident investigation or audit performed by the Workforce Member.
- **GOV-004.5.12.2** Every Workforce Member in a role named in GOV-001 sections 5.4.2–5.4.5, every Workforce Member in the security, GRC, IT and internal audit functions, and every member of the CAB SHALL complete an annual conflict-of-interest declaration as part of the attestation in GOV-002, using TPL-009.
- **GOV-004.5.12.3** A Workforce Member with a disclosed or undisclosed conflict SHALL NOT participate in the related assessment, selection, approval, review or investigation. The GC, with the CISO, SHALL decide within 10 business days of disclosure what restriction or mitigation applies and SHALL record the decision.
- **GOV-004.5.12.4** Workforce Members SHALL NOT accept gifts, hospitality, payments or favors from a Third Party whose security assessment, selection, access approval or contract they are performing or influencing.
- **GOV-004.5.12.5** Workforce Members SHALL NOT participate in any external bug bounty or vulnerability research program targeting the Organization's Information Systems.
- **GOV-004.5.12.6** Workforce Members SHALL NOT use access granted for their duties to obtain information for personal benefit, for trading in securities, or for the benefit of a third party.
- **GOV-004.5.12.7** The GC SHALL maintain the conflict-of-interest register and retain declarations under CMP-004.

### 5.13 Monitoring notice

- **GOV-004.5.13.1** The Organization monitors and records the use of its Information Systems, networks, Endpoints, accounts and communication tools, including email, messaging, web access, file activity, authentication and system logs, for security, compliance, operational and legal purposes. Logging and monitoring controls are set in SEC-012.
- **GOV-004.5.13.2** To the extent permitted by applicable law, Users SHALL have no expectation of privacy in any information they create, store, send or receive on Organization Information Systems, including personal information stored under section 5.5.
- **GOV-004.5.13.3** Monitoring of an identified individual's communications or file content, beyond automated security monitoring, SHALL be authorized in writing in advance by the GC and the CHRO, with the CISO informed, and SHALL be limited to the stated purpose and period.
- **GOV-004.5.13.4** `[GDPR]` Monitoring of Workforce Members in the EU/EEA SHALL be necessary and proportionate to its stated purpose, SHALL be described in the Workforce Privacy Notice issued under CMP-005, SHALL be subject to a DPIA (TPL-005) where required, and SHALL be preceded by information to or consultation with employee representative bodies where local law requires.
- **GOV-004.5.13.5** Communications protected by Legal Privilege, and communications between a User and the DPO, an employee representative or a whistleblower channel under CMP-006, SHALL NOT be reviewed for content except as permitted by law and authorized by the GC.
- **GOV-004.5.13.6** Every Information System that permits interactive logon SHALL display a notice, before logon, that the system is for authorized use only and that use is monitored. The Head of Security Engineering SHALL maintain the standard notice text.

### 5.14 Reporting obligations

- **GOV-004.5.14.1** Users SHALL report suspected Security Incidents, Personal Data Breaches, lost or stolen devices, suspected phishing and suspected violations of this Policy through the security reporting channel in RES-001.5.2.2.
- **GOV-004.5.14.2** Users MAY raise information security concerns confidentially or anonymously under CMP-006.
- **GOV-004.5.14.3** Users SHALL NOT investigate a suspected Security Incident themselves beyond preserving the situation and reporting it, unless they are assigned to do so under RES-002.

### 5.15 Return of assets and access at Separation

- **GOV-004.5.15.1** On Separation, Users SHALL return all Organization Information Assets, devices, Media, badges and tokens, and SHALL delete Organization information from personally owned devices, as required by PPL-001 and SEC-008.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CISO | Owns this Policy; approves exceptions to public disclosure of security details (GOV-004.5.9.5); decides conflict mitigations with the GC |
| ISSC | Approves this Policy |
| CIO | Maintains and publishes the Approved End-user Technology List |
| CTO | Approves contributions of Organization code, models or data to public repositories |
| GC | Receives conflict-of-interest disclosures; maintains the conflict register; authorizes individual monitoring with the CHRO |
| CHRO | Co-authorizes individual monitoring; acts on breaches under CMP-007 |
| CPO / DPO | Issues the Workforce Privacy Notice covering monitoring (CMP-005); advises on monitoring DPIAs |
| SOC Manager | Authorizes security testing activities under GOV-004.5.4.4 |
| Head of Security Engineering | Maintains the logon notice text |
| Managers | Answer User questions on permitted use; receive conflict disclosures; MAY restrict personal use |
| Workforce Members and Third Party users | Comply with this Policy; attest under GOV-002; report incidents and conflicts |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| GOV-004.7.1 | Attestation to this Policy | At the times set in GOV-002 |
| GOV-004.7.2 | Screen lock when leaving an Endpoint unattended | Every time; automatic lock per SEC-004 |
| GOV-004.7.3 | Clear desk | End of each working day and when unattended > 30 minutes |
| GOV-004.7.4 | Personal file storage on Organization systems | ≤ 1 GB per User; none in shared repositories |
| GOV-004.7.5 | Conflict-of-interest disclosure | Within 10 business days of the conflict arising |
| GOV-004.7.6 | Conflict mitigation decision by GC and CISO | Within 10 business days of disclosure |
| GOV-004.7.7 | Annual conflict-of-interest declaration (roles in GOV-004.5.12.2) | Every 12 months with GOV-002 attestation |
| GOV-004.7.8 | Post-Separation confidentiality | Indefinite for Restricted information and trade secrets; 5 years for other Confidential and Internal information |
| GOV-004.7.9 | Reporting of lost devices, suspected credential compromise and suspected incidents | Within the time limit in RES-001.5.2.1 |
| GOV-004.7.10 | Generative AI tools and permitted data | Only as approved under RSK-006 |
| GOV-004.7.11 | Gifts from Third Parties under security assessment or selection by the recipient | None accepted |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Workforce Members with current attestation to this Policy (GOV-003 KPI-14) | ≥ 98% | Monthly | Head of GRC |
| Required annual conflict-of-interest declarations completed | 100% | Every 12 months | GC |
| Unapproved Cloud Services detected in use (Shadow IT discovery) | Decreasing quarter on quarter; 0 handling Restricted data | Quarterly | CIO |
| Data Loss Prevention alerts confirmed as AUP violations | Decreasing quarter on quarter | Quarterly | SOC Manager |
| Detected use of non-approved Generative AI services with Organization data | 0 | Monthly | CISO |
| Information Systems with interactive logon displaying the monitoring notice | 100% | Every 12 months | Head of Security Engineering |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003. No Exception MAY be
granted to GOV-004.5.2.1 (credential sharing), GOV-004.5.4.2 `[PCI]`, GOV-004.5.11.7
(protected disclosures) or GOV-004.5.12.3 (participation while conflicted). Authorizations
under GOV-004.5.4.4 are not Exceptions.

## 10. Enforcement

Non-compliance is handled under CMP-007. The Organization MAY suspend a User's access
immediately, pending investigation, where a violation of this Policy poses a risk to Information
Assets. Violations by Third Party personnel are also handled under the Third Party's contract
(RSK-003).

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| GOV-004.5.1 – 5.4 | A.5.10, A.5.15, A.8.1 | PR.AA-05, PR.AT-01 | PL-4, AC-8 | 2.5, 2.7, 4.3 | CC1.1, CC2.2 | DSS05.04 | `[PCI]` 12.2.1, 4.2.2; `[HIPAA]` §164.308(a)(3)(ii)(A) |
| GOV-004.5.3 | A.7.7, A.8.1, A.8.19 | PR.PS-02, PR.PS-05 | PL-4, CM-11 | 2.3, 4.3 | CC6.8 | DSS05.03 | `[HIPAA]` §164.310(b) |
| GOV-004.5.5 – 5.7 | A.5.10, A.5.14, A.5.23 | ID.AM-02 | PL-4 | 2.1, 3.3 | CC6.7 | DSS05.04 | — |
| GOV-004.5.8 | A.5.10 | GV.PO-01 | PL-4 | — | CC2.2 | APO13 | `[GDPR]` Art. 22 |
| GOV-004.5.9 | A.5.10, A.5.14 | PR.AT-01 | PL-4(1) | — | CC2.2 | DSS05.04 | — |
| GOV-004.5.10 | A.5.32 | GV.OC-03 | CM-10 | — | CC2.2 | MEA03 | — |
| GOV-004.5.11 | A.6.2, A.6.6 | PR.AT-01 | PS-6 | — | C1.1, CC1.1 | APO07 | `[GDPR]` Art. 28(3)(b), 29; `[HIPAA]` §164.308(a)(3) |
| GOV-004.5.12 | A.5.3, A.6.2 | GV.RR-04 | PS-6 | — | CC1.1 | APO07 | `[SOX]` §406 |
| GOV-004.5.13 | A.8.15, A.8.16 | DE.CM-03 | AC-8, AU-1 | 8.1 | CC7.2 | DSS05.07 | `[GDPR]` Art. 5, 6, 13, 35, 88 |
| GOV-004.5.14 | A.6.8 | RS.MA-01 | IR-6 | 14.6 | CC2.3 | DSS02 | — |
| GOV-004.5.15 | A.5.11, A.6.5 | PR.AA-05 | PS-4 | 6.2 | CC6.2, CC6.5 | APO07.06 | `[HIPAA]` §164.308(a)(3)(ii)(C) |

## 12. Related documents

GOV-001, GOV-002, GOV-006, RSK-003, RSK-006, CMP-004, CMP-005, CMP-006, CMP-007, CMP-008,
SEC-001, SEC-002, SEC-004, SEC-005, SEC-008, SEC-010, SEC-011, SEC-012, SEC-014, SEC-015,
SEC-019, RES-001, RES-002, PPL-001, PPL-002, TPL-005, TPL-009

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CISO | | | |
| Approver: ISSC Vice-Chair, on behalf of the ISSC (CISO recused as Document Owner under GOV-001.5.3.9) | | | |
