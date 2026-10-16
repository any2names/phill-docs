# RSK-001 — Risk Management Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | RSK-001 |
| Title | Risk Management Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Head of GRC |
| Approver | Information Security Steering Committee (ISSC); Risk Appetite (section 5.3) ratified by the Audit Committee |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | RSK-002, RSK-003, RSK-004, RSK-005, RSK-006, CMP-001, CMP-003, CMP-004, GOV-001, GOV-003, TPL-001, TPL-002 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Head of GRC | Initial release |

## 3. Purpose

This Policy establishes the Organization's framework for identifying, analyzing, evaluating,
treating, monitoring and communicating Risk to its Information Assets, operations, legal
obligations and stakeholders. It sets the Organization's Risk Appetite and Risk Tolerance,
defines the permitted Risk Treatment options, and fixes the authority and maximum validity
of every Risk Acceptance. The method is aligned to ISO 31000:2018 (principles, framework
and process) and NIST SP 800-30 Rev. 1 (risk framing, assessment, response and monitoring).
The scoring method, criteria and treatment deadlines that implement this Policy are set in
RSK-002.

## 4. Scope

- **People:** all Workforce Members, and every Risk Owner, Control Owner, Asset Owner, Data Owner and System Owner.
- **Systems and data:** every Information Asset and Information System in the scope of the Information Security Program defined in ISP-000, at every Classification Level, whether on premises, in a Cloud Service or operated by a Third Party.
- **Locations:** all Organization sites, remote work locations and regions in which the Organization operates.
- **Third parties:** Risk arising from Third Parties is assessed under this Policy using the third-party method in RSK-003.
- **Risk categories:** the categories in section 5.3. Enterprise risks outside these categories (for example market or credit risk) are out of scope except where they share a Control or an Information Asset with an in-scope Risk.

## 5. Policy statements

### 5.1 Risk management framework and principles

- **RSK-001.5.1.1** The Organization SHALL operate a single risk management process, applied consistently to every Risk category in section 5.3, consisting of the ISO 31000 activities: scope, context and criteria; Risk identification; Risk analysis; Risk evaluation; Risk Treatment; monitoring and review; recording and reporting; communication and consultation.
- **RSK-001.5.1.2** The process SHALL use the NIST SP 800-30 Rev. 1 risk model: each Risk SHALL be expressed in terms of a Threat (source and event), the Vulnerability or predisposing condition it exploits, the likelihood of occurrence and the resulting impact.
- **RSK-001.5.1.3** All Risks SHALL be scored, rated and assigned treatment deadlines using the method in RSK-002. No other scoring method SHALL be used for Risks recorded in the Risk Register.
- **RSK-001.5.1.4** The Head of GRC SHALL maintain the Risk Register using TPL-001 as the single authoritative record of in-scope Risks. Local risk logs (for example project risk logs) SHALL transfer every Risk rated Medium or above to the Risk Register within 10 business days of rating.
- **RSK-001.5.1.5** Risk management SHALL be integrated into the following decisions, each of which SHALL record a reference to the Risk Register entry or to a risk assessment under RSK-002: approval of new Information Systems handling Confidential or Restricted data; Normal and Emergency Changes with a Change Risk Rating of High under SEC-013.5.3.1; onboarding of vendor Tier 1 and Tier 2 Third Parties under RSK-003; approval of AI Systems under RSK-006; Exceptions under CMP-003; and mergers, acquisitions and divestitures.
- **RSK-001.5.1.6** The Head of GRC SHALL review the risk management process against ISO 31000 and NIST SP 800-30 at least every 12 months and SHALL report the result, with any improvement actions, to the ISSC.

### 5.2 Risk context and identification

- **RSK-001.5.2.1** The Head of GRC SHALL document the internal and external context of the risk process at least every 12 months, covering business objectives, the Obligations Register (CMP-001), the threat landscape report produced under RSK-005, the Business Impact Analysis (RSK-004) and stakeholder expectations.
- **RSK-001.5.2.2** Risks SHALL be identified from at least the following sources: the enterprise risk assessment and triggered assessments (RSK-002); Vulnerability management results (SEC-011); Security Incidents and Post-Incident Reviews (RES-002); internal and external audit findings (CMP-002); third-party assessments (RSK-003); Threat Models and threat intelligence (RSK-005); BIA results (RSK-004); AI System assessments (RSK-006); Exceptions (CMP-003); and reports from Workforce Members.
- **RSK-001.5.2.3** Any Workforce Member who identifies a potential Risk SHALL report it to the Head of GRC through the channel published under GOV-002. The Head of GRC SHALL acknowledge each report within 5 business days.
- **RSK-001.5.2.4** Each Risk SHALL be recorded with a single Risk Owner at the level of authority able to fund and direct its treatment. The Head of GRC SHALL assign a Risk Owner within 5 business days of a Risk being recorded; where ownership is disputed, the CISO SHALL decide.
- **RSK-001.5.2.5** Each Risk SHALL be assigned to exactly one primary Risk category from section 5.3 and MAY be tagged with secondary categories.

### 5.3 Risk Appetite and Risk Tolerance

- **RSK-001.5.3.1** [DECISION REQUIRED: Risk Appetite posture for the Organization (SUITE-REGISTER decision #1). Recommended default: Conservative.] The Organization's Risk Appetite is **Conservative**: the Organization SHALL NOT retain any Residual Risk above Medium outside an approved Risk Acceptance.
- **RSK-001.5.3.2** Risk Appetite and Risk Tolerance for each Risk category SHALL be as stated in the table below. The column "Maximum Residual Risk without acceptance" sets the highest Residual Risk level that may be retained under an approved treatment plan without a Risk Acceptance; the column "Maximum acceptable Residual Risk" sets the highest level that may be retained at all, and only with a Risk Acceptance under section 5.5.

| # | Risk category | Appetite statement | Appetite level | Maximum Residual Risk without acceptance | Maximum acceptable Residual Risk |
|---|---|---|---|---|---|
| C1 | Information security (Confidentiality, Integrity, Availability of Information Assets) | The Organization accepts minimal security Risk and invests to keep Residual Risk within tolerance before pursuing new capability. | Minimal | Medium | High |
| C2 | Privacy & data protection | The Organization does not accept Risk of unlawful processing of Personal Data or of a Personal Data Breach. | Averse | Low | Medium |
| C3 | Regulatory & compliance | The Organization does not accept Risk of knowing non-compliance with a law, regulation or binding contract recorded in the Obligations Register. | Averse | Low | Medium |
| C4 | Financial reporting `[SOX]` | The Organization does not accept Risk of a Material Weakness in internal control over financial reporting. | Averse | Low | Medium |
| C5 | Operational resilience | The Organization accepts minimal Risk that a Recovery Tier 0 or Recovery Tier 1 service cannot be restored within its RTO (RSK-004). | Minimal | Medium | High |
| C6 | Third-party & supply chain | The Organization accepts minimal Risk from Third Parties and requires Third Parties to meet the Organization's own control standards. | Minimal | Medium | High |
| C7 | Technology, AI & Emerging Technology | The Organization accepts cautious Risk to adopt new technology, including AI Systems, where Controls in RSK-006 are in place before production use. | Cautious | Medium | High |
| C8 | Strategic & reputational | The Organization accepts cautious Risk in pursuit of strategic objectives, provided C1–C7 tolerances are not exceeded. | Cautious | Medium | High |
| C9 | People & safety | The Organization does not accept Risk of physical harm to any person arising from its Information Systems or facilities. | Averse | Low | Medium |

- **RSK-001.5.3.3** A Residual Risk rated Critical SHALL NOT be accepted in categories C2, C3, C4 and C9. Such a Risk SHALL be avoided or mitigated, and the CISO SHALL report it to the CEO and the Audit Committee within 10 business days of rating.
- **RSK-001.5.3.4** A Residual Risk rated Critical in categories C1, C5, C6, C7 and C8 MAY be accepted only by the authority in section 5.5, for no longer than the Critical validity in section 5.5, and only while an approved treatment plan is in progress.
- **RSK-001.5.3.5** Where a Risk carries secondary categories, the most restrictive tolerance among its primary and secondary categories SHALL apply.
- **RSK-001.5.3.6** The KRIs that measure each tolerance in this section SHALL be defined, collected and reported under GOV-003. When a KRI breaches its threshold, the Head of GRC SHALL open or re-rate the corresponding Risk Register entry within 5 business days.
- **RSK-001.5.3.7** The Head of GRC SHALL review this section at least every 12 months and after any merger, acquisition, entry into a new regulated market or Sev-1 incident. Changes SHALL be approved by the ISSC and ratified by the Audit Committee before taking effect.

### 5.4 Risk Treatment

- **RSK-001.5.4.1** Every Risk whose Residual Risk exceeds the "Maximum Residual Risk without acceptance" for its category SHALL have a documented Risk Treatment decision using one or more of the following options:

| Option | ISO 31000 / NIST SP 800-30 response | Requirements |
|---|---|---|
| Mitigate | Modify likelihood or impact / Mitigate | Treatment plan with Controls, Control Owner, milestones and target Residual Risk, completed within the treatment deadline in RSK-002. |
| Transfer | Share the Risk / Share or transfer | Contract or insurance coverage reviewed by the GC; transfer does not remove the Organization's accountability under law. Remaining Residual Risk SHALL still be recorded and rated. |
| Avoid | Remove the Risk source / Avoid | Decision to stop, not start, or redesign the activity, approved by the Risk Owner and recorded with the date the activity ceased. |
| Accept | Retain the Risk by informed decision / Accept | Risk Acceptance under section 5.5 using TPL-002. |

- **RSK-001.5.4.2** The Risk Owner SHALL select the treatment option and submit the treatment plan to the Head of GRC within the treatment-plan deadline in RSK-002 for the Risk's level.
- **RSK-001.5.4.3** Each treatment plan SHALL state: the Controls to be implemented or improved; the accountable Control Owner for each; milestones with dates; the target Residual Risk score; and the evidence that will demonstrate completion.
- **RSK-001.5.4.4** Treatment plans that require Changes SHALL be executed under SEC-013. Treatment plans that address a Vulnerability SHALL also meet the remediation SLA in SEC-011; where the two deadlines differ, the earlier SHALL apply.
- **RSK-001.5.4.5** On completion of a treatment plan, the Head of GRC SHALL re-score the Residual Risk using RSK-002 and SHALL obtain Evidence of Control operation before closing the treatment.
- **RSK-001.5.4.6** A treatment plan that misses a milestone by more than 30 days SHALL be escalated by the Head of GRC to the next acceptance authority level in section 5.5.

### 5.5 Risk Acceptance

- **RSK-001.5.5.1** Risk Acceptance SHALL be requested by the Risk Owner on TPL-002 and SHALL be approved by the authority for the Residual Risk level, as follows:

| Residual Risk level (RSK-002) | Acceptance authority |
|---|---|
| Low | Risk Owner |
| Medium | CISO |
| High | ISSC |
| Critical | CEO, with the Audit Committee notified within 10 business days |

- **RSK-001.5.5.2** A Risk Acceptance SHALL be valid for a maximum of 12 months. A Risk Acceptance for a Critical Residual Risk SHALL be valid for a maximum of 90 days. The expiry date SHALL be recorded on TPL-002 and in the Risk Register.
- **RSK-001.5.5.3** Except for Low Residual Risk, for which the Risk Owner is the authority, an approver SHALL NOT approve acceptance of a Risk that they own, or a Risk arising from an activity they directly manage; in that case the next authority level in section 5.5.1 SHALL approve.
- **RSK-001.5.5.4** A Risk Acceptance SHALL NOT exceed the "Maximum acceptable Residual Risk" for the Risk's category in section 5.3.
- **RSK-001.5.5.5** A Risk Acceptance SHALL NOT be used to authorize non-compliance with a requirement of law, regulation or a binding contract, including PCI DSS. Deviations from such requirements SHALL follow CMP-003, using a Compensating Control where the regulation permits one.
- **RSK-001.5.5.6** Every Risk Acceptance SHALL record the business justification, the Residual Risk score, the Controls relied on to limit the Risk, the conditions that would void the acceptance, and the expiry date.
- **RSK-001.5.5.7** A Risk Acceptance SHALL become void before expiry if: the Residual Risk score increases; a condition recorded under RSK-001.5.5.6 occurs; a Security Incident rated Sev-1 or Sev-2 under RES-002 is caused by the accepted Risk; or the Risk Owner leaves the role. The Head of GRC SHALL notify the approver within 5 business days of the voiding event.
- **RSK-001.5.5.8** The Head of GRC SHALL notify the Risk Owner 30 days before each Risk Acceptance expires. At expiry, the Risk SHALL be treated or re-accepted through a new TPL-002 submission; an expired acceptance SHALL NOT be extended without a new approval.
- **RSK-001.5.5.9** A Risk SHALL NOT be accepted more than twice in succession at the same level without the next authority level in section 5.5.1 approving the second renewal.
- **RSK-001.5.5.10** Exceptions approved under CMP-003 that leave a Residual Risk SHALL be recorded in the Risk Register and linked to the Exception record.

### 5.6 Monitoring, review and escalation

- **RSK-001.5.6.1** The ISSC SHALL review the Risk Register quarterly, including all Risks rated High or Critical, all treatment plans past a milestone, all Risk Acceptances due to expire within the next quarter, and all KRI breaches reported under GOV-003.
- **RSK-001.5.6.2** Risk Owners SHALL review the status, score and treatment progress of each Risk they own at the following minimum frequency: Critical monthly; High monthly; Medium quarterly; Low every 12 months. The Head of GRC SHALL record each review date in the Risk Register.
- **RSK-001.5.6.3** A Risk newly rated Critical SHALL be reported by the Head of GRC to the CISO within 1 business day of rating and to the ISSC within 5 business days. A Risk newly rated High SHALL be reported to the CISO within 5 business days.
- **RSK-001.5.6.4** The CISO SHALL report the Organization's risk profile, including all Critical and High Risks, open Risk Acceptances, and Risks exceeding tolerance in section 5.3, to the Audit Committee at the cadence set in GOV-003.
- **RSK-001.5.6.5** The Head of GRC SHALL close a Risk only when the Risk Owner confirms that the Risk source no longer exists or the Residual Risk is within tolerance, and SHALL record the closure reason and date.
- **RSK-001.5.6.6** Risk Register entries, Risk Acceptances and treatment Evidence SHALL be retained for the period set in CMP-004.

### 5.7 Communication, consultation and competence

- **RSK-001.5.7.1** The Head of GRC SHALL consult the GC on every Risk in category C3, the CPO on every Risk in category C2, the CFO on every Risk in category C4, and the Business Continuity Manager on every Risk in category C5 before treatment is selected.
- **RSK-001.5.7.2** Risk Owners SHALL be informed of their assigned Risks, scores, deadlines and acceptance expiries through the Risk Register within 5 business days of each change.
- **RSK-001.5.7.3** Each Risk Owner and each person performing risk assessments SHALL complete training on this Policy and RSK-002 before first performing the role and every 12 months thereafter, delivered under PPL-002.5.4.4.
- **RSK-001.5.7.4** The Risk Register SHALL be classified Confidential under SEC-002. Access SHALL be limited to the ISSC, the Head of GRC and delegates, Internal Audit, and each Risk Owner for their own Risks.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| Board of Directors | Sets the Organization's overall risk posture; receives the annual program report under GOV-003. |
| Audit Committee | Ratifies Risk Appetite and Risk Tolerance (RSK-001.5.3.7); receives notification of Critical Risk Acceptances and non-acceptable Critical Risks (5.3.3, 5.5.1). |
| CEO | Approves Risk Acceptance for Critical Residual Risk (5.5.1). |
| ISSC | Approves this Policy; reviews the Risk Register quarterly (5.6.1); approves Risk Acceptance for High Residual Risk; approves changes to Risk Appetite before Audit Committee ratification. |
| CISO | Approves Risk Acceptance for Medium Residual Risk; resolves Risk ownership disputes (5.2.4); reports the risk profile to the Audit Committee (5.6.4). |
| Head of GRC | Owns this Policy; maintains the Risk Register; assigns Risk Owners; tracks treatment plans and acceptance expiries; escalates per 5.4.6 and 5.6.3. |
| Risk Owner | Accepts accountability for assigned Risks; selects treatment; submits treatment plans and TPL-002 requests; reviews Risks at the frequency in 5.6.2; approves Risk Acceptance for Low Residual Risk. |
| Control Owner | Implements and evidences Controls named in treatment plans. |
| GC, CPO, CFO, Business Continuity Manager | Consulted on Risks in categories C3, C2, C4 and C5 respectively (5.7.1). |
| Internal Audit Director | Provides independent assurance over this Policy's operation under CMP-002. |
| Workforce Members | Report potential Risks (5.2.3). |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| RSK-001.7.1 | Risk Appetite | Conservative (adopter decision #1): no residual risk above Medium outside an approved acceptance |
| RSK-001.7.2 | Risk acceptance authority | Low: Risk Owner · Medium: CISO · High: ISSC · Critical: CEO, with Audit Committee notified within 10 business days |
| RSK-001.7.3 | Risk Acceptance validity | Max 12 months; Critical max 90 days |
| RSK-001.7.4 | Risk Register review | ISSC reviews quarterly |
| RSK-001.7.5 | Critical Residual Risk acceptance prohibited | Categories C2 Privacy, C3 Regulatory, C4 Financial reporting, C9 People & safety |
| RSK-001.7.6 | Risk Owner review frequency | Critical and High monthly · Medium quarterly · Low every 12 months |
| RSK-001.7.7 | Escalation of newly rated Risks | Critical: CISO within 1 business day, ISSC within 5 business days · High: CISO within 5 business days |
| RSK-001.7.8 | Risk Owner assignment | Within 5 business days of recording |
| RSK-001.7.9 | Transfer of Medium+ Risks from local logs | Within 10 business days of rating |
| RSK-001.7.10 | Acceptance expiry notice | 30 days before expiry |
| RSK-001.7.11 | Consecutive acceptances at same level | Maximum 2; second renewal approved by next authority level |
| RSK-001.7.12 | Treatment milestone slippage escalation | More than 30 days late |
| RSK-001.7.13 | Scoring method, levels and treatment-plan deadlines | As set in RSK-002 |
| RSK-001.7.14 | Retention of Risk records | As set in CMP-004 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Residual Risks above category tolerance without a valid Risk Acceptance | 0 | Monthly | Head of GRC |
| Risk Acceptances past expiry date | 0 | Monthly | Head of GRC |
| Treatment plans submitted within the RSK-002 deadline | ≥ 95% | Quarterly | Head of GRC |
| Treatment plan milestones met on schedule | ≥ 90% | Quarterly | Head of GRC |
| Risks with a named Risk Owner within 5 business days | 100% | Quarterly | Head of GRC |
| Risk Owner reviews completed at required frequency | ≥ 95% | Quarterly | Head of GRC |
| ISSC quarterly Risk Register review held and minuted | 4 per year | Annually | CISO |
| Critical Risk escalations within 1 business day | 100% | Quarterly | Head of GRC |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following requirements SHALL NOT be subject to Exception: RSK-001.5.3.3 (prohibition on accepting Critical Residual Risk in categories C2, C3, C4 and C9), RSK-001.5.5.1 (acceptance authority), RSK-001.5.5.2 (acceptance validity) and RSK-001.5.5.5 (no acceptance of legal non-compliance).

## 10. Enforcement

Non-compliance is handled under CMP-007.

Approval of a Risk Acceptance outside the authority in section 5.5, or retention of a Residual Risk above tolerance without an approved Risk Acceptance, SHALL be reported by the Head of GRC to the ISSC at its next meeting and SHALL be treated as a Control failure for the purposes of CMP-002.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| RSK-001.5.1 | 6.1.1, 6.1.2, 8.2 | GV.RM-01, GV.RM-06 | PM-9, RA-1 | — | CC3.1, CC3.2 | EDM03, APO12 | `[HIPAA]` §164.308(a)(1)(ii)(A)–(B); `[PCI]` 12.3.1 |
| RSK-001.5.2 | 4.1, 4.2, 6.1.2 | GV.OC-01, ID.RA-03, ID.RA-04 | RA-3, PM-28 | — | CC3.2, CC3.3 | APO12.01 | `[GDPR]` Art. 24, 32 |
| RSK-001.5.3 | 6.1.1, 6.1.2(a) | GV.RM-02, GV.RM-03 | PM-9, PM-28 | — | CC3.1 | EDM03.01, APO12.06 | `[SOX]` §404 |
| RSK-001.5.4 | 6.1.3, 8.3 | GV.RM-04, ID.RA-06 | RA-7, PM-4 | — | CC3.2, CC5.1 | APO12.06 | `[HIPAA]` §164.308(a)(1)(ii)(B) |
| RSK-001.5.5 | 6.1.3(f) | GV.RM-04, ID.RA-07 | RA-7, PM-9 | — | CC3.2 | APO12.06 | `[PCI]` 12.3.1 |
| RSK-001.5.6 | 8.2, 9.1, 9.3 | GV.OV-01, GV.OV-03, ID.IM-01 | PM-9, CA-7 | — | CC4.1, CC4.2 | MEA01, APO12.04 | `[SOX]` §404 |
| RSK-001.5.7 | 7.2, 7.3, 7.4 | GV.RR-02, PR.AT-01 | AT-3, PM-13 | 14.1 | CC2.2, CC2.3 | APO12.04 | — |

## 12. Related documents

ISP-000, GOV-001, GOV-002, GOV-003, GOV-006, RSK-002, RSK-003, RSK-004, RSK-005, RSK-006, CMP-001, CMP-002, CMP-003, CMP-004, CMP-007, SEC-002, SEC-011, SEC-013, RES-002, PPL-002, TPL-001, TPL-002, REF-001, REF-002

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Head of GRC | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
| Ratification of section 5.3: Audit Committee Chair | | | |
