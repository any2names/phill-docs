# TPL-004 — Vendor Security Questionnaire

## 1. Document control

| Field | Value |
|---|---|
| Document ID | TPL-004 |
| Title | Vendor Security Questionnaire |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | T — Template |
| Classification | Internal (template); completed questionnaire: Confidential |
| Owner | Head of GRC |
| Approver | Chief Information Security Officer (CISO) |
| Effective date | [DECISION REQUIRED: Date of CISO approval] |
| Next review date | Effective date + 12 months |
| Parent document | RSK-003 Third-Party & Supply Chain Risk Management Policy |
| Related documents | RSK-002, RSK-004, RSK-006, CMP-004, CMP-005, TPL-001 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Head of GRC | Initial release |

## 3. Purpose

This questionnaire collects the information the Organization needs to perform due diligence
on a Third Party under RSK-003. Questions are tiered so that the depth of the questionnaire
matches the vendor tier, and regulation-specific modules are added only where they apply.
Responses are scored so that findings can be rated under RSK-002 and recorded in the Risk
Register.

## 4. Instructions

| Item | Instruction |
|---|---|
| Who completes it | The Third Party completes sections 5.1–5.15 for the modules that apply. The Organization's Business Sponsor completes the intake details in section 5.1. The Head of GRC (or delegate) completes the scoring in section 5.16. |
| Which questions apply | Each question is marked **C** (Core), **S** (Standard) or **F** (Full). Vendor Tier 3: answer **C** questions. Vendor Tier 2: answer **C** and **S**. Vendor Tier 1: answer **C**, **S** and **F**. Vendor Tier 4: not required (RSK-003). Regulation modules (sections 5.12–5.15) apply where the Head of GRC marks them applicable in section 5.1, regardless of tier. |
| Use of existing reports | Where the Third Party provides a current SOC 2 Type II report or ISO/IEC 27001 certificate with Statement of Applicability meeting RSK-003, the Head of GRC MAY mark questions covered by the report as "Covered by report" and reference the report section. |
| Evidence | Questions marked † require Evidence (document, report extract, screenshot). Answers without required Evidence are scored as "No". |
| When | At onboarding, at each reassessment at the frequency for the vendor tier in RSK-003, and on event-driven reassessment. |
| Response time | The Third Party SHOULD return the completed questionnaire within 15 business days of receipt. |
| Storage and retention | The Head of GRC stores the completed questionnaire, Evidence and scoring in the GRC repository, linked to the third-party inventory entry. Retain for the period set in CMP-004. |
| Classification | Completed questionnaires and Evidence are Confidential under SEC-002 and are shared only with the Organization's assessment team. |

**Answer key:** Yes = fully implemented for all in-scope services · Partial = implemented for some services or with gaps (explain) · No = not implemented · N/A = not applicable (explain).

## 5. Form

### 5.1 Intake and general information

| # | Field | Value |
|---|---|---|
| 1.1 | Third Party legal name, registered address, parent company | |
| 1.2 | Services provided to the Organization | |
| 1.3 | Vendor tier (RSK-003), confirmed by Head of GRC | ☐ Tier 1 Critical ☐ Tier 2 High ☐ Tier 3 Moderate |
| 1.4 | Highest Classification Level of Organization data accessed (SEC-002) | ☐ Public ☐ Internal ☐ Confidential ☐ Restricted |
| 1.5 | Recovery Tier of supported Organization service (RSK-004) | ☐ Tier 0 ☐ Tier 1 ☐ Tier 2 ☐ Tier 3 ☐ N/A |
| 1.6 | Countries where Organization data is stored, processed or accessed (including support) | |
| 1.7 | Applicable modules | ☐ 5.12 `[PCI]` ☐ 5.13 `[HIPAA]` ☐ 5.14 `[GDPR]` / `[CPRA]` ☐ 5.15 AI Systems (RSK-006) ☐ `[SOX]` (SOC 1 Type II report requested) |
| 1.8 | Independent assurance reports available (type, period, scope) † | |
| 1.9 | Security contact (name, role, email, 24×7 phone) | |
| 1.10 | Respondent name, role and date | |

### 5.2 Governance and risk management

| # | Tier | Question | Answer | Comments / Evidence ref |
|---|---|---|---|---|
| 2.1 | C | Do you have an information security policy approved by management and reviewed at least every 12 months? † | | |
| 2.2 | C | Is a named individual accountable for information security? | | |
| 2.3 | S | Do you perform a risk assessment at least every 12 months using a documented method? | | |
| 2.4 | S | Do all personnel receive security awareness training at hire and at least every 12 months? | | |
| 2.5 | S | Are personnel with access to customer data subject to background screening, where lawful? | | |
| 2.6 | S | Do personnel sign confidentiality agreements before access? | | |
| 2.7 | F | Is your security program certified or attested against a recognized framework (e.g. ISO/IEC 27001, SOC 2)? † | | |
| 2.8 | F | Do you have an internal audit or independent assessment function that tests security Controls? | | |
| 2.9 | F | Do you maintain cyber insurance? State coverage limit. | | |

### 5.3 Access control

| # | Tier | Question | Answer | Comments / Evidence ref |
|---|---|---|---|---|
| 3.1 | C | Is MFA enforced for all access to systems holding Organization data? | | |
| 3.2 | C | Is access granted on Least Privilege and Need to Know? | | |
| 3.3 | C | Is access revoked within 24 hours of personnel separation? | | |
| 3.4 | S | Are user and privileged access reviews performed? State the frequency of each. † | | |
| 3.5 | S | Is Phishing-resistant MFA required for privileged access? | | |
| 3.6 | S | Do you support SSO integration with the Organization's Identity Provider (e.g. SAML, OIDC)? | | |
| 3.7 | F | Is privileged access granted just-in-time and session-recorded? | | |
| 3.8 | F | Are shared and Service Account credentials stored in a secrets vault and rotated? | | |

### 5.4 Encryption and data protection

| # | Tier | Question | Answer | Comments / Evidence ref |
|---|---|---|---|---|
| 4.1 | C | Is Organization data encrypted in transit using protocols meeting the minimums in SEC-006 (provided with this questionnaire)? State protocol versions. | | |
| 4.2 | C | Is Organization data encrypted at rest using algorithms and key lengths meeting SEC-006? State algorithm and key length. | | |
| 4.3 | S | Are encryption keys managed in a Key Management Service or HSM with defined rotation? | | |
| 4.4 | S | Is Organization data logically segregated from other customers' data? Describe the method. | | |
| 4.5 | F | Do you support customer-managed encryption keys? | | |
| 4.6 | F | Is Data Loss Prevention applied to prevent exfiltration of customer data? | | |
| 4.7 | S | Will Organization data be returned and securely destroyed within the period required by RSK-003 after contract end, with a Certificate of Destruction? | | |

### 5.5 Secure development (SDLC)

| # | Tier | Question | Answer | Comments / Evidence ref |
|---|---|---|---|---|
| 5.1 | C | Do you follow a documented secure development lifecycle? | | |
| 5.2 | S | Is code peer-reviewed and scanned (SAST, dependency/SCA) before release? | | |
| 5.3 | S | Is threat modeling performed for new features and architecture changes? | | |
| 5.4 | S | Are production and non-production environments separated, with no production customer data in non-production? | | |
| 5.5 | F | Can you provide an SBOM for software delivered to the Organization, on request? † | | |
| 5.6 | F | Are releases signed, and is build-pipeline integrity protected (e.g. aligned to SLSA or NIST SP 800-218)? | | |
| 5.7 | F | Can you provide a secure software development attestation? † | | |

### 5.6 Vulnerability management

| # | Tier | Question | Answer | Comments / Evidence ref |
|---|---|---|---|---|
| 6.1 | C | Are systems holding Organization data scanned for Vulnerabilities? State internal and external scan frequency. | | |
| 6.2 | C | State your remediation timeframes for Critical and High Vulnerabilities. | | |
| 6.3 | S | Is an independent Penetration Test performed at least every 12 months? Provide the executive summary. † | | |
| 6.4 | S | Do you operate a Vulnerability Disclosure Program? | | |
| 6.5 | F | Do you prioritize Vulnerabilities in the CISA KEV catalog? State remediation timeframe. | | |
| 6.6 | F | Is EDR deployed on all servers and Endpoints that access Organization data? | | |

### 5.7 Logging, monitoring and incident response

| # | Tier | Question | Answer | Comments / Evidence ref |
|---|---|---|---|---|
| 7.1 | C | Do you have a documented incident response plan tested at least every 12 months? † | | |
| 7.2 | C | Will you notify the Organization of a Security Incident affecting its data within the period required by RSK-003 for your tier? | | |
| 7.3 | S | Are security logs centrally collected and monitored 24×7? State the retention period. | | |
| 7.4 | S | Can you provide the Organization with audit logs of access to its data on request? | | |
| 7.5 | F | Have you had a Security Incident or Personal Data Breach in the last 36 months affecting customer data? Describe. | | |
| 7.6 | F | Will you participate in the Organization's incident response exercises? | | |

### 5.8 Business continuity and disaster recovery

| # | Tier | Question | Answer | Comments / Evidence ref |
|---|---|---|---|---|
| 8.1 | C | Do you have a business continuity plan and a disaster recovery plan? | | |
| 8.2 | S | State the RTO and RPO for the services provided to the Organization. | | |
| 8.3 | S | Are BC/DR plans tested at least every 12 months? Provide the latest test summary. † | | |
| 8.4 | S | Are backups encrypted, stored in a separate location, and protected from modification (immutable or offline)? | | |
| 8.5 | F | Do you operate the service from more than one geographically separate site or region? | | |
| 8.6 | F | Do you have contingency arrangements for your own critical suppliers? | | |

### 5.9 Privacy

| # | Tier | Question | Answer | Comments / Evidence ref |
|---|---|---|---|---|
| 9.1 | C | Will you process Personal Data of the Organization? List categories of data and Data Subjects. | | |
| 9.2 | C | Will you use Organization data only to provide the contracted services? | | |
| 9.3 | S | Do you have a designated privacy officer or DPO? | | |
| 9.4 | S | Can you assist the Organization in responding to Data Subject Requests within the deadlines set in CMP-010? | | |
| 9.5 | F | Do you sell or share Personal Data, or use it for cross-context behavioral advertising? | | |

### 5.10 Subprocessors and fourth parties

| # | Tier | Question | Answer | Comments / Evidence ref |
|---|---|---|---|---|
| 10.1 | C | List all subcontractors, Subprocessors and Cloud Service providers that will access or host Organization data, with location. † | | |
| 10.2 | S | Do you flow down security and privacy obligations equivalent to your contract with the Organization to each Subprocessor? | | |
| 10.3 | S | Will you give notice of new Subprocessors within the period required by RSK-003, with a right to object? | | |
| 10.4 | F | How do you assess and monitor your Subprocessors' security? | | |

### 5.11 Physical and personnel security

| # | Tier | Question | Answer | Comments / Evidence ref |
|---|---|---|---|---|
| 11.1 | S | Are facilities hosting Organization data protected by badge access, visitor logging and CCTV? | | |
| 11.2 | F | Are data center providers independently attested (e.g. SOC 2 Type II, ISO/IEC 27001)? † | | |

### 5.12 `[PCI]` Payment card module

| # | Tier | Question | Answer | Comments / Evidence ref |
|---|---|---|---|---|
| 12.1 | All | Provide your current PCI DSS v4.0.1 Attestation of Compliance (AOC) covering the services provided. † | | |
| 12.2 | All | Provide a responsibility matrix identifying which PCI DSS requirements you manage, which the Organization manages, and which are shared. † | | |
| 12.3 | All | Will you acknowledge in writing your responsibility for the security of account data you possess, store, process or transmit for the Organization, or to the extent you could affect the security of the CDE? | | |
| 12.4 | All | Do you store SAD after authorization? (Required answer: No) | | |

### 5.13 `[HIPAA]` Health information module

| # | Tier | Question | Answer | Comments / Evidence ref |
|---|---|---|---|---|
| 13.1 | All | Will you create, receive, maintain or transmit PHI for the Organization? | | |
| 13.2 | All | Will you sign the Organization's BAA before any PHI is disclosed? | | |
| 13.3 | All | Have you performed a HIPAA Security Rule risk analysis in the last 12 months? Provide a summary. † | | |
| 13.4 | All | Do you have a designated HIPAA Security Official? | | |
| 13.5 | All | Will you obtain BAAs from your own subcontractors that handle PHI? | | |

### 5.14 `[GDPR]` `[CPRA]` Personal data module

| # | Tier | Question | Answer | Comments / Evidence ref |
|---|---|---|---|---|
| 14.1 | All | Will you sign a Data Processing Agreement meeting GDPR Art. 28(3)? | | |
| 14.2 | All | Will Personal Data be transferred outside the EU/EEA? State the transfer mechanism (e.g. Adequacy Decision, Standard Contractual Clauses, EU-US Data Privacy Framework certification). | | |
| 14.3 | All | Do you maintain a record of processing activities as a Processor (GDPR Art. 30(2))? | | |
| 14.4 | All | Will you notify the Organization of a Personal Data Breach without undue delay and within the period required by RSK-003? | | |
| 14.5 | All | `[CPRA]` Will you agree to service provider or contractor terms under Cal. Civ. Code §1798.100(d) and §1798.140, including no selling or sharing of Personal Data? | | |

### 5.15 AI Systems module (RSK-006)

| # | Tier | Question | Answer | Comments / Evidence ref |
|---|---|---|---|---|
| 15.1 | All | Does the service use AI Systems, including Generative AI, to process Organization data? Describe the use and the models used. | | |
| 15.2 | All | Will Organization inputs or outputs be used to train or improve any model? (Required answer: No, unless the Organization consents in writing) | | |
| 15.3 | All | State the retention period for prompts, inputs and outputs. | | |
| 15.4 | All | Provide model or system documentation (e.g. model card) describing intended use, limitations and evaluation results. † | | |
| 15.5 | All | Do you test for prompt injection, data leakage and other adversarial attacks? Describe. | | |
| 15.6 | All | Do you test for bias and fairness where outputs affect individuals? Describe metrics. | | |
| 15.7 | All | Will you notify the Organization of material model changes within the notice period required by RSK-006? | | |
| 15.8 | All | List foundation model providers and other AI Subprocessors. | | |
| 15.9 | All | State your role and conformity status under the EU AI Act, where applicable. | | |

### 5.16 Scoring (completed by the Organization)

**Question scoring:** Yes = 2 · Partial = 1 · No = 0 · N/A (accepted) = excluded · "Covered by report" = scored from the report.

| Section | Applicable questions | Points available | Points scored | % | Findings raised |
|---|---|---|---|---|---|
| 5.2 Governance | | | | | |
| 5.3 Access control | | | | | |
| 5.4 Encryption | | | | | |
| 5.5 SDLC | | | | | |
| 5.6 Vulnerability management | | | | | |
| 5.7 Incident response | | | | | |
| 5.8 BC/DR | | | | | |
| 5.9 Privacy | | | | | |
| 5.10 Subprocessors | | | | | |
| 5.11 Physical | | | | | |
| 5.12–5.15 Modules | | | | | |
| **Total** | | | | | |

**Overall rating guidance** (subject to findings, which govern the decision):

| Overall % | Rating |
|---|---|
| ≥ 90% | Strong |
| 75% – < 90% | Satisfactory |
| 60% – < 75% | Needs improvement — remediation commitments required |
| < 60% | Weak — escalate to CISO before engagement |

**Findings:** Each "No" or "Partial" on a C question, and each "Partial" or "No" on an S or F question that leaves a Risk, SHALL be recorded as a finding and scored under RSK-002. A "No" on question 12.3, 12.4, 13.2, 14.1 or 15.2, where the module applies, is an automatic finding that blocks engagement until resolved.

| Finding # | Question ref | Description | Likelihood (1–5) | Impact (1–5) | Score | Level | Remediation required by (RSK-003) | Risk ID (TPL-001) |
|---|---|---|---|---|---|---|---|---|
| 1 | | | | | | | | |
| 2 | | | | | | | | |
| 3 | | | | | | | | |

**Assessment outcome:**

| Field | Value |
|---|---|
| Residual third-party Risk level (RSK-002) | ☐ Low ☐ Medium ☐ High ☐ Critical |
| Recommendation | ☐ Approve ☐ Approve with remediation commitments ☐ Approve subject to Risk Acceptance (TPL-002) ☐ Reject |
| Next reassessment due (RSK-003) | |

## 6. Approval signatures

### 6.1 Third Party attestation

I confirm that the responses in this questionnaire are complete and accurate to the best of my knowledge, and that I am authorized to provide them on behalf of the Third Party.

| Role | Name | Signature | Date |
|---|---|---|---|
| Third Party authorized representative | | | |

### 6.2 Organization review

| Role | Name | Signature | Date |
|---|---|---|---|
| Assessor (Head of GRC or delegate) | | | |
| Business Sponsor (Risk Owner) | | | |
| CISO (vendor Tier 1, or where outcome is Weak) | | | |

### 6.3 Template approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Head of GRC | | | |
| Approver: CISO | | | |
