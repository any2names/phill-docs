# CMP-007 — Enforcement & Disciplinary Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | CMP-007 |
| Title | Enforcement & Disciplinary Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Human Resources Officer (CHRO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-002, GOV-004, CMP-003, CMP-004, CMP-006, RSK-003, RES-001, RES-002, PPL-001, PPL-002 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CHRO | Initial release |

## 3. Purpose

This document establishes how the Organization enforces every document in the Information
Security & GRC Policy Suite. It sets the categories of violation, a proportional sanctions
matrix, the process and due-process protections that apply before a sanction is imposed,
the contractual remedies used against Third Parties, and the documentation required. It
is the sanction policy required by `[HIPAA]` 45 CFR §164.308(a)(1)(ii)(C) and
§164.530(e), and it supports the SOC 2 requirement that the Organization holds individuals
accountable for their internal control responsibilities.

Every other suite document refers to this document for enforcement and does not set its
own sanctions.

## 4. Scope

- **People:** all Workforce Members, at every level of seniority, including executives and
  members of governance bodies to the extent their terms of engagement permit; and
  Third Parties and their personnel bound by contract to comply with suite documents.
- **Conduct:** any violation of a SHALL or SHALL NOT requirement of a suite document, of an
  approved Exception's conditions (CMP-003), of a law or regulation recorded in the
  obligations register (CMP-001), or of a contractual information security or privacy
  obligation, whether by action or omission.
- **Systems and data:** all Information Assets and all data, in any form, owned by or
  entrusted to the Organization.
- **Locations:** all locations. Where local employment law, a collective agreement or a
  works council agreement requires a different process, that requirement prevails and the
  CHRO SHALL record the local variant (CMP-007.5.4.10).
- **Not in scope:** performance management unrelated to suite documents, and general
  workplace conduct, which are handled under PPL-001 and other HR policies.

## 5. Policy statements

### 5.1 Principles

- **CMP-007.5.1.1** Sanctions SHALL be applied consistently: the same violation category, aggravating and mitigating factors and occurrence count SHALL lead to a sanction within the same range of the matrix in section 5.3, irrespective of the individual's seniority, function or performance.
- **CMP-007.5.1.2** Sanctions SHALL be proportional to the violation category determined under section 5.2 and adjusted only by the factors in section 5.3.3.
- **CMP-007.5.1.3** No sanction other than an interim measure under CMP-007.5.4.4 SHALL be imposed before the due-process steps in section 5.4 are complete.
- **CMP-007.5.1.4** The Organization SHALL distinguish between human error in a well-designed process and conduct that is negligent, reckless or willful. Where root-cause analysis under RES-002 or CMP-002 attributes a violation to a Control or process design failure, the responsible Control Owner SHALL remediate the design, and the individual SHALL NOT be sanctioned above Category 1 for that violation.
- **CMP-007.5.1.5** A person who self-reports a violation within 1 business day of becoming aware of it, and who cooperates fully, SHALL receive a reduction of at least one sanction level under section 5.3.3, except for Category 4 violations involving intent to harm or personal gain.
- **CMP-007.5.1.6** No Workforce Member SHALL be sanctioned for a good-faith report, for participating in an investigation, or for refusing to carry out an instruction that would violate a suite document or the law (CMP-006).
- **CMP-007.5.1.7** A manager who directs, knowingly permits or fails to act on a reported violation by a direct or indirect report SHALL be subject to sanction as if the manager had committed the violation.

### 5.2 Violation categories

- **CMP-007.5.2.1** The CHRO, on the recommendation of the investigating function, SHALL assign each substantiated violation one of the following categories:

| Category | Description | Examples |
|---|---|---|
| 1 — Minor | Inadvertent violation with no or negligible impact; no Internal, Confidential or Restricted data exposed outside authorized recipients; no Security Incident above Sev-4. | Late completion of mandatory training under PPL-002; repeated failure of phishing simulations; leaving an unlocked Endpoint unattended in an Organization facility; misclassification of a document without disclosure. |
| 2 — Moderate | Negligent violation, or a minor violation causing limited impact: exposure of Internal or Confidential data, a Sev-3 Security Incident, or circumvention of a Control without intent to cause harm. | Sharing Confidential data with an unauthorized internal recipient; using unapproved Shadow IT for Confidential data; failing to report a Security Event within the time set in RES-001; installing unapproved software in violation of GOV-004. |
| 3 — Serious | Reckless or knowing violation, or a negligent violation causing significant impact: exposure of Restricted data, a Sev-2 Security Incident, a reportable Personal Data Breach, or a violation of a `[PCI]`, `[HIPAA]`, `[SOX]`, `[GDPR]` or `[CPRA]` requirement. | Sharing credentials or a Secret; disabling EDR or logging on an Endpoint; accessing Restricted data without a business need; making an Emergency Change without following SEC-013; failing to follow a Legal Hold. |
| 4 — Severe | Willful, malicious or criminal violation; violation for personal gain; or any violation causing a Sev-1 Security Incident or a Material Cybersecurity Incident `[SOX]`. Also any of the conduct listed in CMP-007.5.2.2. | Theft or sale of data; deliberate sabotage; installing Malware; unauthorized access to another person's account; falsification of Evidence or audit records; deliberate bypass of SoD in a Financially Significant System. |

- **CMP-007.5.2.2** The following SHALL always be classified Category 4: retaliation against a reporter or witness (CMP-006); attempting to identify an anonymous reporter (CMP-006); destruction, alteration or concealment of Evidence or records subject to a Legal Hold or audit (CMP-004); obstruction of an investigation or audit, including misleading an internal or External Auditor or a QSA; knowingly making a false report that causes harm to another person; and `[HIPAA]` knowing access to or disclosure of PHI for personal gain or malicious harm.
- **CMP-007.5.2.3** Where a single act involves several violations, the CHRO SHALL assign the category of the most serious violation.
- **CMP-007.5.2.4** Severity of the resulting Security Incident SHALL be taken from the Severity Level assigned under RES-002; Classification Level of exposed data SHALL be taken from SEC-002. The CHRO SHALL NOT reclassify either for the purpose of sanctioning.

### 5.3 Sanctions matrix

- **CMP-007.5.3.1** Sanctions SHALL be selected from the following levels:

| Level | Sanction |
|---|---|
| S1 | Documented coaching by the manager and completion of targeted remedial training within 30 days |
| S2 | Written warning, remedial training within 30 days, and a review of the individual's access entitlements by the System Owner within 10 business days |
| S3 | Final written warning; removal or restriction of privileged or Restricted-data access for at least 90 days; ineligibility for bonus or promotion in the current review cycle [DECISION REQUIRED: Whether financial consequences are part of S3. Recommended default: Yes, where lawful in the jurisdiction] |
| S4 | Termination of employment or engagement; permanent revocation of access under SEC-003; referral to law enforcement or regulators where the GC so decides; recovery of losses where lawful |

- **CMP-007.5.3.2** The baseline sanction SHALL be determined by violation category and the number of prior substantiated violations of any category within the look-back period:

| Category | First occurrence | Second occurrence | Third or subsequent occurrence | Look-back period |
|---|---|---|---|---|
| 1 — Minor | S1 | S2 | S3 | 12 months |
| 2 — Moderate | S2 | S3 | S4 | 24 months |
| 3 — Serious | S3 | S4 | S4 | 36 months |
| 4 — Severe | S4 | — | — | Not applicable |

- **CMP-007.5.3.3** The decision maker MAY move the sanction up or down by one level from the baseline only on the basis of the following documented factors:
  - **Aggravating:** intent or personal gain; concealment; the individual holds a Privileged Account, CDE access or a security, audit or compliance role; prior written instruction on the same requirement; harm to Data Subjects, patients or cardholders; the violation affected a Financially Significant System `[SOX]`.
  - **Mitigating:** self-reporting (CMP-007.5.1.5 requires at least one level); full cooperation; immediate action to contain harm; ambiguous or conflicting instructions from the Organization; the individual had not yet received training required by PPL-002 for the relevant requirement.
- **CMP-007.5.3.4** A Category 4 violation SHALL NOT be reduced below S3, and a Category 4 violation listed in CMP-007.5.2.2 SHALL NOT be reduced below S4 except with the written approval of the GC and the CHRO stating the reason.
- **CMP-007.5.3.5** Any sanction that departs from the matrix other than under CMP-007.5.3.3 SHALL be approved in writing by both the CHRO and the CISO, with the reason recorded; the CHRO SHALL report each such departure to the ISSC in the next quarterly report.
- **CMP-007.5.3.6** For Workforce Members engaged through a staffing agency or as independent contractors, levels S2 and S3 SHALL be applied as written notice to the engaging Third Party, and S4 as removal from the Organization's engagement under section 5.5.
- **CMP-007.5.3.7** Sanctions SHALL NOT include any measure prohibited by applicable law, including fines deducted from wages where unlawful.

### 5.4 Process and due process

- **CMP-007.5.4.1** Suspected violations SHALL be referred to the CHRO by: the CISO or SOC Manager from a Security Incident (RES-002); the GC from an investigation under CMP-006; the Internal Audit Director or Head of GRC from audit or control testing (CMP-002); the CPO or DPO from privacy reviews (CMP-005); `[HIPAA]` the HIPAA Privacy Officer or HIPAA Security Officer; or any manager. The CHRO SHALL log each referral within 2 business days of receipt.
- **CMP-007.5.4.2** The CHRO SHALL assign an investigator who is independent of the individual's reporting line and the subject matter. Where the facts have already been established by an investigation under CMP-006, by a Post-Incident Review under RES-002, or by an audit under CMP-002, the CHRO MAY rely on that investigation's findings.
- **CMP-007.5.4.3** Fact-finding SHOULD be completed within 30 days of referral. Extensions SHALL be approved by the CHRO with a recorded reason.
- **CMP-007.5.4.4** Pending investigation, the CISO MAY order immediate suspension or restriction of an individual's access to Information Systems where continued access poses a risk to Information Assets, and the CHRO MAY place the individual on paid administrative leave. Interim measures are not sanctions, SHALL be documented with the reason, and SHALL be reviewed by the CHRO every 10 business days.
- **CMP-007.5.4.5** Before any sanction of S2 or above, the individual SHALL receive written notice of: the requirement allegedly violated; a summary of the facts and Evidence relied on; the proposed violation category; and the right to respond.
- **CMP-007.5.4.6** The individual SHALL have at least 5 business days from notice to respond in writing or at a meeting, and MAY be accompanied by a colleague or, where provided by law or collective agreement, a representative.
- **CMP-007.5.4.7** The decision maker SHALL issue a written decision within 10 business days of the response (or of the response deadline), stating the category, the baseline sanction, any aggravating or mitigating factors applied, the final sanction and the right of appeal. Decision makers are:

| Sanction level | Decision maker | Required consultation |
|---|---|---|
| S1 | Individual's manager | HR business partner |
| S2 | Individual's manager and HR business partner | CISO's delegate for security violations; CPO's delegate for privacy violations |
| S3 | CHRO or delegate (director level or above) | CISO; CPO for privacy violations; GC |
| S4 | CHRO | GC; CISO; for executives, the CEO; for the CEO or an ISSC member, the Audit Committee Chair |

- **CMP-007.5.4.8** The individual MAY appeal a decision of S2 or above in writing within 10 business days of receiving it. The appeal SHALL be decided within 15 business days by a person senior to and independent of the original decision maker, nominated by the CHRO (or by the GC where the CHRO made the original decision). The appeal decision is final within the Organization.
- **CMP-007.5.4.9** Interviews and investigations SHALL respect the confidentiality requirements of CMP-006 section 5.5 and the privacy requirements of CMP-005. Monitoring data used as Evidence SHALL have been collected under GOV-004 and SEC-012.
- **CMP-007.5.4.10** Where the law of a jurisdiction, a collective agreement or a works council agreement requires additional steps, notice periods or consultations, the CHRO SHALL document the local variant in an annex approved by the GC, and SHALL apply it in that jurisdiction.
- **CMP-007.5.4.11** Where the facts indicate a possible criminal offense, the GC SHALL decide within 5 business days of referral whether to involve law enforcement, and the CHRO SHALL coordinate the disciplinary timeline with the GC so the investigation is not prejudiced.
- **CMP-007.5.4.12** Where an S4 sanction results in Separation, access revocation and asset return SHALL follow SEC-003 and PPL-001.

### 5.5 Third Parties

- **CMP-007.5.5.1** The Head of Procurement SHALL ensure that every contract with a Third Party that accesses Organization Information Assets or processes Personal Data includes: an obligation to comply with the suite documents identified in the contract; the Organization's right to require removal of named Third-Party personnel; the right to suspend access; audit rights; a cure period; termination for cause; and indemnification or liability for breach, as required by RSK-003.
- **CMP-007.5.5.2** On a substantiated Third-Party violation, the Head of Procurement, with the Head of GRC and the GC, SHALL apply the following remedies by category:

| Category | Minimum remedy | Additional remedies available |
|---|---|---|
| 1 — Minor | Written notice to the Third Party's account manager; corrective action requested within 30 days | Additional training of the Third Party's personnel |
| 2 — Moderate | Formal notice of breach with a corrective action plan due within 10 business days and completion within 30 days | Out-of-cycle reassessment under RSK-003; on-site or remote audit |
| 3 — Serious | Formal notice of breach; suspension of the responsible personnel's access within 1 business day; corrective action plan due within 5 business days; out-of-cycle reassessment under RSK-003 | Removal of personnel; suspension of service; withholding of payment where the contract allows; contractual penalties |
| 4 — Severe | Immediate suspension of all Third-Party access to Restricted data pending review; GC decision on termination for cause within 10 business days | Termination; claims for damages and indemnity; referral to law enforcement; notification to regulators |

- **CMP-007.5.5.3** The CISO SHALL be able to suspend a Third Party's access to Information Systems immediately, without waiting for contractual process, where continued access poses a risk to Information Assets.
- **CMP-007.5.5.4** Each Third-Party violation and remedy SHALL be recorded in the Third Party's record under RSK-003 and considered in its next risk assessment and tiering.
- **CMP-007.5.5.5** Where a Third Party is a Processor or Business Associate, the CPO (and `[HIPAA]` the HIPAA Privacy Officer) SHALL decide whether the violation requires action under CMP-005, the BAA or RES-003, and `[HIPAA]` whether termination is required under 45 CFR §164.504(e)(1)(ii).

### 5.6 `[HIPAA]` Sanction policy

- **CMP-007.5.6.1** `[HIPAA]` This document is the Organization's sanction policy under 45 CFR §164.308(a)(1)(ii)(C) for Workforce Members who fail to comply with the Organization's security policies and procedures, and under 45 CFR §164.530(e)(1) for privacy policies and procedures.
- **CMP-007.5.6.2** `[HIPAA]` Every violation involving PHI or ePHI SHALL be categorized at Category 2 or higher unless the HIPAA Privacy Officer documents that no PHI was used or disclosed in violation of the Privacy Rule.
- **CMP-007.5.6.3** `[HIPAA]` The HIPAA Privacy Officer (for PHI) and the HIPAA Security Officer (for ePHI) SHALL be consulted on the category and sanction for every violation involving PHI, and SHALL receive a copy of each decision.
- **CMP-007.5.6.4** `[HIPAA]` Sanctions SHALL NOT be applied to a Workforce Member for a disclosure protected by 45 CFR §164.502(j) (whistleblowers and workforce crime victims) or for activities protected by 45 CFR §164.530(g)(2) (CMP-006).
- **CMP-007.5.6.5** `[HIPAA]` Documentation of each sanction applied SHALL be retained under CMP-004 row R-20. Sanction statistics are reviewed under CMP-008.5.4.3.

### 5.7 Documentation and records

- **CMP-007.5.7.1** For every referral, the CHRO SHALL maintain a case record containing: the referral and source; the requirement violated; investigation findings; the category; the baseline sanction; aggravating and mitigating factors; the notice issued and the individual's response; the decision and decision maker; any appeal and outcome; any interim measures; and the date each sanction was completed.
- **CMP-007.5.7.2** Case records SHALL be classified Restricted under SEC-002, stored in the HR case-management system with access limited to the CHRO, named HR personnel and the GC, and retained and deleted under CMP-004 row R-20. Records under Legal Hold SHALL NOT be deleted.
- **CMP-007.5.7.3** The CHRO SHALL notify the System Owner and the CISO within 1 business day of any sanction that requires an access change, and the access change SHALL be completed within the time in SEC-003.7.5, or SEC-003.7.3 where access is revoked.
- **CMP-007.5.7.4** The CHRO SHALL report to the ISSC quarterly, in anonymized form: referrals received, cases closed, violations by category and suite document, sanctions by level, departures from the matrix, appeals and their outcomes, and Third-Party remedies.
- **CMP-007.5.7.5** The Head of GRC SHALL use the quarterly report to identify suite documents with recurring violations and SHALL refer each such document to its Document Owner for review under GOV-002 and to the CISO for targeted training under PPL-002.
- **CMP-007.5.7.6** Sanctions consistency SHALL be audited by Internal Audit at least every 24 months under CMP-002.5.2.8, by sampling closed cases against the matrix in section 5.3.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CHRO | Owns this document; receives referrals; assigns investigators; decides S3 and S4 sanctions; administers due process and appeals; maintains case records; reports quarterly to the ISSC. |
| ISSC | Approves this document; reviews quarterly enforcement reporting and departures from the matrix. |
| CISO | Refers security violations; orders interim access suspension; is consulted on S3 and S4 sanctions; co-approves departures from the matrix. |
| GC | Advises on legal risk, local variants and law enforcement referral; is consulted on S3 and S4; decides appeals where the CHRO made the original decision; decides Third-Party termination for cause. |
| CPO / DPO | Refer privacy violations; are consulted on sanctions for privacy violations; decide Processor-related actions. |
| HIPAA Privacy Officer / HIPAA Security Officer | `[HIPAA]` Consulted on every PHI-related violation; receive copies of decisions. |
| Head of Procurement | Ensures contract clauses; applies Third-Party remedies. |
| Head of GRC | Links violations to Control and document reviews; records Third-Party violations under RSK-003. |
| Internal Audit Director | Audits sanction consistency every 24 months. |
| Audit Committee Chair | Is consulted on sanctions involving the CEO or an ISSC member. |
| Managers | Decide S1 and S2 sanctions with HR; refer violations; apply sanctions consistently. |
| System Owners | Implement access changes resulting from sanctions. |
| Workforce Members | Comply with suite documents; cooperate with investigations; may respond to and appeal decisions. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| CMP-007.7.1 | Violation categories | Four: 1 Minor · 2 Moderate · 3 Serious · 4 Severe |
| CMP-007.7.2 | Sanction levels | Four: S1 coaching and training · S2 written warning · S3 final written warning and access restriction · S4 termination |
| CMP-007.7.3 | Look-back periods for repeat violations | Category 1: 12 months · Category 2: 24 months · Category 3: 36 months |
| CMP-007.7.4 | Permitted adjustment from baseline | ± 1 level, on documented factors only |
| CMP-007.7.5 | Self-reporting window for mitigation | Within 1 business day of awareness; at least one-level reduction |
| CMP-007.7.6 | Referral logged by CHRO | Within 2 business days |
| CMP-007.7.7 | Fact-finding target | 30 days from referral |
| CMP-007.7.8 | Interim measure review | Every 10 business days |
| CMP-007.7.9 | Individual's response period | At least 5 business days from notice |
| CMP-007.7.10 | Written decision | Within 10 business days of response or deadline |
| CMP-007.7.11 | Appeal filing / appeal decision | Within 10 business days / within 15 business days |
| CMP-007.7.12 | Remedial training on S1 or S2 | Completed within 30 days |
| CMP-007.7.13 | Access restriction on S3 | At least 90 days |
| CMP-007.7.14 | Notice of sanction-driven access change to System Owner and CISO | Within 1 business day; change completed per SEC-003.7.5 (SEC-003.7.3 for revocation) |
| CMP-007.7.15 | Third-Party Category 3: suspension of responsible personnel's access | Within 1 business day |
| CMP-007.7.16 | Third-Party Category 4: termination decision | Within 10 business days |
| CMP-007.7.17 | Law enforcement referral decision | Within 5 business days of referral |
| CMP-007.7.18 | Enforcement reporting to ISSC | Quarterly |
| CMP-007.7.19 | Sanction consistency audit | Every 24 months |
| CMP-007.7.20 | Retention of case records | Per CMP-004 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Referrals logged within 2 business days | 100% | Quarterly | CHRO |
| Cases with fact-finding completed within 30 days | ≥ 85% | Quarterly | CHRO |
| Decisions issued within 10 business days of response | ≥ 95% | Quarterly | CHRO |
| Sanctions within the matrix range (no unapproved departure) | 100% | Quarterly | CHRO |
| Appeals overturning the original decision | Tracked; ≥ 25% triggers a process review by the CHRO | Quarterly | CHRO |
| Sanction-driven access changes completed per SEC-003 | 100% | Quarterly | CISO |
| Repeat violators (second occurrence within look-back) | Downward trend over 4 quarters | Quarterly | CHRO |
| Third-Party corrective action plans completed on time | ≥ 90% | Quarterly | Head of Procurement |
| `[HIPAA]` PHI-related decisions copied to HIPAA Privacy/Security Officer | 100% | Quarterly | CHRO |
| Sanction consistency audit findings closed within CMP-002 timelines | 100% | Each audit | CHRO |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

Departures from the sanctions matrix in an individual case are not Exceptions; they are
governed by CMP-007.5.3.5. The following requirements SHALL NOT receive an Exception: the
due-process steps in CMP-007.5.4.5 – 5.4.8; the prohibition on sanctioning protected
reporting (CMP-007.5.1.6 and CMP-007.5.6.4); and `[HIPAA]` the existence and application of
the sanction policy in section 5.6.

## 10. Enforcement

Non-compliance is handled under CMP-007.

Failure by a manager or decision maker to apply this document, including inconsistent or
undocumented sanctions, is itself a violation categorized under section 5.2 and decided by
the CHRO, or by the GC where the CHRO is the subject.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| CMP-007.5.1 – 5.3 | 5.1, 7.3; A.6.4 | GV.RR-04, GV.PO-01 | PS-8, PL-4 | — | CC1.1, CC1.5 | APO07 | 45 CFR §164.308(a)(1)(ii)(C); 45 CFR §164.530(e); PCI DSS 12.1 |
| CMP-007.5.4 | A.6.4, A.6.5, A.5.28 | GV.RR-04 | PS-4, PS-8, AC-2 | 5.3, 6.2 | CC1.5, CC6.2 | APO07 | GDPR Art. 88 (employment context); local employment law |
| CMP-007.5.5 | A.5.19, A.5.20, A.5.22 | GV.SC-05, GV.SC-07 | SR-6, PS-7, SA-9 | 15.4, 15.7 | CC9.2 | APO10 | GDPR Art. 28; 45 CFR §164.504(e)(1)(ii); PCI DSS 12.8 |
| CMP-007.5.6 | A.6.4 | GV.RR-04 | PS-8 | — | CC1.5 | APO07, MEA03 | 45 CFR §§164.308(a)(1)(ii)(C), 164.502(j), 164.530(e), 164.530(g) |
| CMP-007.5.7 | 7.5, 9.1, 10.2 | GV.OV-01, ID.IM-01 | PS-8, PM-1 | — | CC1.5, CC4.1 | APO07, MEA01 | 45 CFR §164.530(e)(2) |

## 12. Related documents

ISP-000, GOV-002, GOV-004, GOV-006, CMP-001, CMP-002, CMP-003, CMP-004, CMP-005, CMP-006,
CMP-008, RSK-003, SEC-002, SEC-003, SEC-012, SEC-013, RES-001, RES-002, RES-003, PPL-001,
PPL-002, REF-002

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Chief Human Resources Officer (CHRO) | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
