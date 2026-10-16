# RSK-002 — Risk Assessment Standard

## 1. Document control

| Field | Value |
|---|---|
| Document ID | RSK-002 |
| Title | Risk Assessment Standard |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 2 — Standard |
| Classification | Internal |
| Owner | Head of GRC |
| Approver | Chief Information Security Officer (CISO) |
| Effective date | [DECISION REQUIRED: Date of CISO approval] |
| Next review date | Effective date + 12 months |
| Parent document | RSK-001 Risk Management Policy |
| Related documents | RSK-003, RSK-004, RSK-005, RSK-006, SEC-011, SEC-013, SEC-019, RES-002, CMP-001, TPL-001, TPL-002 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Head of GRC | Initial release |

## 3. Purpose

This Standard sets the measurable method by which the Organization assesses Risk under
RSK-001: the 5×5 likelihood and impact scales and their criteria, the risk level bands, the
frequency and triggers for risk assessment, the deadlines for Risk Treatment plans, and
`[PCI]` the targeted risk analyses required by PCI DSS v4.0.1 Requirements 12.3.1 and 12.3.2.
It ensures that any two assessors scoring the same Risk reach the same result.

## 4. Scope

- **People:** the Head of GRC, Risk Owners, assessors, Control Owners, and any Workforce Member or Third Party performing a risk assessment for the Organization.
- **Systems and data:** all Information Assets and Information Systems within ISP-000 scope, at every Classification Level.
- **Assessment types:** the enterprise risk assessment; triggered assessments; system and project assessments; third-party assessments (whose tiering and due diligence are in RSK-003, but whose resulting Risks are scored here); threat-model findings (RSK-005); AI System assessments (RSK-006); and `[PCI]` targeted risk analyses.
- **Locations and third parties:** all locations and all Third Parties in scope of RSK-001.

## 5. Requirements

### 5.1 Assessment method

- **RSK-002.5.1.1** Each risk assessment SHALL follow these steps in order: (1) define the scope and the Information Assets involved, with their Classification Level (SEC-002) and Recovery Tier (RSK-004); (2) identify Threat sources and Threat events, using the threat landscape and Threat Models produced under RSK-005; (3) identify Vulnerabilities and predisposing conditions; (4) identify existing Controls; (5) score Inherent Risk; (6) rate Control effectiveness; (7) score Residual Risk; (8) evaluate the Residual Risk against the Risk Tolerance in RSK-001; (9) record the result in the Risk Register using TPL-001.
- **RSK-002.5.1.2** Risk SHALL be scored as **likelihood × impact** on a 5×5 matrix, giving a score from 1 to 25.
- **RSK-002.5.1.3** Inherent Risk SHALL be scored assuming no Controls specific to the Risk are operating. Residual Risk SHALL be scored taking into account only Controls that are implemented and for which Evidence of operation exists.
- **RSK-002.5.1.4** The impact score SHALL be the highest score reached on any single impact dimension in section 5.3. Impact scores SHALL NOT be averaged across dimensions.
- **RSK-002.5.1.5** Where a Risk has more than one credible scenario, each scenario SHALL be scored and the Risk SHALL take the highest resulting score.
- **RSK-002.5.1.6** Each scored Risk SHALL record the rationale for the likelihood and impact selected, referencing the criteria in sections 5.2 and 5.3 and the data relied on (for example incident history, Vulnerability scan results, threat intelligence, audit findings).
- **RSK-002.5.1.7** Every Inherent and Residual Risk score SHALL be reviewed by a second person independent of the assessor before it is recorded as final. For Risks rated High or Critical, the reviewer SHALL be the Head of GRC or the CISO.
- **RSK-002.5.1.8** Where quantitative data is available, the assessor MAY additionally express Risk as annualized loss expectancy in currency. The qualitative 5×5 score SHALL remain the basis for risk level, treatment deadline and acceptance authority.

### 5.2 Likelihood criteria

- **RSK-002.5.2.1** Likelihood SHALL be scored using the following criteria. The assessor SHALL select the highest level for which any one criterion is met.

| Score | Level | Probability over the next 12 months | Frequency indicator | Threat and Vulnerability indicators |
|---|---|---|---|---|
| 1 | Rare | < 5% | Has not occurred at the Organization or its sector peers in the last 10 years | Requires a nation-state-level capability, or exploitation of a Vulnerability for which no public exploit or technique is known |
| 2 | Unlikely | 5% – < 20% | Occurred in the sector in the last 10 years, not at the Organization | Requires specialist skill and insider knowledge; multiple layered Controls must fail |
| 3 | Possible | 20% – < 50% | Occurred at the Organization in the last 10 years, or in the sector in the last 3 years | Public exploit or technique exists; at least one Control layer must fail |
| 4 | Likely | 50% – < 80% | Occurred at the Organization in the last 3 years | Actively exploited in the wild (for example listed in the CISA KEV catalog) or a single Control failure is sufficient |
| 5 | Almost certain | ≥ 80% | Occurs at the Organization at least once a year, or is occurring now | Exploitation is automated or commoditized, and the Information Asset is exposed with no effective Control |

### 5.3 Impact criteria

- **RSK-002.5.3.1** Impact SHALL be scored on each of the following five dimensions. The impact score is the highest dimension score (RSK-002.5.1.4).
- **RSK-002.5.3.2** [DECISION REQUIRED: Financial impact thresholds. Recommended default: the percentages of annual consolidated revenue shown below; the Organization MAY replace them with absolute currency amounts approved by the CFO.] Financial thresholds SHALL be computed from the most recent audited annual consolidated revenue and updated by the Head of GRC within 30 days of publication of the annual financial statements.

| Score | Level | Financial | Regulatory & legal | Operational | Reputational | Safety & privacy |
|---|---|---|---|---|---|---|
| 1 | Insignificant | Loss < 0.1% of annual revenue | No breach of an obligation in the Obligations Register | Disruption of a Recovery Tier 2 or Recovery Tier 3 service within its RTO; no Recovery Tier 0 or Recovery Tier 1 impact | No external awareness | No Personal Data affected; no injury |
| 2 | Minor | 0.1% – < 0.5% of annual revenue | Minor non-compliance, self-identified and correctable without regulator or customer notification | Recovery Tier 2 or Recovery Tier 3 service unavailable beyond its RTO; or a Recovery Tier 0 or Recovery Tier 1 service degraded but within RTO | Isolated customer complaints; no media coverage | Fewer than 100 individuals' Personal Data classified Internal or Confidential exposed; no Restricted data; no injury |
| 3 | Moderate | 0.5% – < 1% of annual revenue | Breach requiring notification to a regulator, payment brand or customer under contract; audit qualification of a single control | A Recovery Tier 1 service unavailable beyond its RTO, or a Recovery Tier 0 service at its RTO | Local or trade media coverage; one key customer formally escalates | 100 – 999 individuals' Personal Data exposed, or any Restricted data of fewer than 100 individuals; minor injury requiring first aid |
| 4 | Major | 1% – < 5% of annual revenue | Regulatory investigation, enforcement notice or fine; qualified SOC 2 Type II opinion; `[SOX]` Significant Deficiency; `[PCI]` loss of compliant status | A Recovery Tier 0 service unavailable beyond its RTO; or multiple Recovery Tier 1 services unavailable beyond RTO | National media coverage; loss of a key customer or partner | 1,000 – 99,999 individuals' Personal Data exposed, or Restricted data of 100 – 9,999 individuals; injury requiring medical treatment |
| 5 | Severe | ≥ 5% of annual revenue | Loss of a license or right to operate; criminal liability; consent decree; `[SOX]` Material Weakness; `[PCI]` termination of card acceptance | Recovery Tier 0 services unavailable beyond their maximum tolerable period of disruption (RSK-004) | Sustained international media coverage; loss of multiple key customers; executive departure | ≥ 100,000 individuals' Personal Data exposed, or Restricted data of ≥ 10,000 individuals, or Sensitive Personal Information processed unlawfully at scale; serious injury or loss of life |

- **RSK-002.5.3.3** Personal Data counts in section 5.3.2 SHALL count unique individuals. Where the count cannot be determined, the assessor SHALL use the total number of records in the affected data set.
- **RSK-002.5.3.4** `[GDPR]` `[CPRA]` `[HIPAA]` Where a Risk involves Personal Data, the CPO or DPO SHALL confirm the Safety & privacy dimension score before the assessment is finalized.

### 5.4 Risk level bands and the matrix

- **RSK-002.5.4.1** Risk levels SHALL be assigned from the score as follows: **Low 1–4 · Medium 5–9 · High 10–16 · Critical 17–25.**
- **RSK-002.5.4.2** The resulting matrix is:

| Likelihood ↓ / Impact → | 1 Insignificant | 2 Minor | 3 Moderate | 4 Major | 5 Severe |
|---|---|---|---|---|---|
| **5 Almost certain** | 5 Medium | 10 High | 15 High | 20 Critical | 25 Critical |
| **4 Likely** | 4 Low | 8 Medium | 12 High | 16 High | 20 Critical |
| **3 Possible** | 3 Low | 6 Medium | 9 Medium | 12 High | 15 High |
| **2 Unlikely** | 2 Low | 4 Low | 6 Medium | 8 Medium | 10 High |
| **1 Rare** | 1 Low | 2 Low | 3 Low | 4 Low | 5 Medium |

- **RSK-002.5.4.3** The risk level SHALL determine the treatment-plan deadline (section 5.7), the acceptance authority and validity (RSK-001), the Risk Owner review frequency (RSK-001) and the Exception approval authority (CMP-003).

### 5.5 Control effectiveness

- **RSK-002.5.5.1** Each Control relied on to reduce Inherent Risk to Residual Risk SHALL be rated using the following scale, and the rating SHALL be supported by Evidence no older than 12 months:

| Rating | Criteria | Maximum reduction allowed |
|---|---|---|
| Effective | Designed to address the Risk, operating, and tested with no exceptions in the last 12 months (by CMP-002 testing, SOC 2 Type II examination, or a documented Control Owner test) | Likelihood or impact reduced by up to 2 levels per Control, total reduction up to 3 levels per axis |
| Partially effective | Designed and operating, but untested, or tested with exceptions that are being remediated | Likelihood or impact reduced by up to 1 level per Control, total reduction up to 2 levels per axis |
| Ineffective or not implemented | Not designed for the Risk, not operating, or tested with unremediated exceptions | No reduction |

- **RSK-002.5.5.2** Preventive Controls SHALL reduce likelihood; detective and corrective Controls (including Backup and DR under SEC-018 and RES-005) SHALL reduce impact. A single Control SHALL NOT reduce both axes.
- **RSK-002.5.5.3** Transfer through insurance or contract SHALL reduce only the Financial impact dimension and SHALL NOT reduce the Regulatory & legal, Reputational or Safety & privacy dimensions.

### 5.6 Assessment frequency and triggers

- **RSK-002.5.6.1** The Head of GRC SHALL perform an enterprise risk assessment covering every Risk category in RSK-001 at least every 12 months.
- **RSK-002.5.6.2** In addition, a triggered risk assessment SHALL be performed on each of the following events: Significant Change (see RSK-002.5.6.3); onboarding of a new vendor Tier 1 Third Party under RSK-003; a Sev-1 or Sev-2 Security Incident under RES-002; a new or changed legal obligation recorded in the Obligations Register (CMP-001); a merger or acquisition.
- **RSK-002.5.6.3** For the purpose of RSK-002.5.6.2, Significant Change (GOV-006) SHALL include at minimum: a new Information System or Cloud Service that will store, process or transmit Restricted data; a change to a Recovery Tier 0 or Recovery Tier 1 system's architecture, hosting location or Identity Provider; a new internet-facing service; `[PCI]` any change to CDE scope or segmentation as defined in SEC-019; `[SOX]` a change to a Financially Significant System as defined in CMP-009; entry into a new country or regulated market; and any Change with a Change Risk Rating of High under SEC-013.5.3.1.
- **RSK-002.5.6.4** A triggered assessment SHALL be completed within 30 days of the trigger, except that an assessment triggered by a Sev-1 or Sev-2 Security Incident SHALL be completed within 10 business days of the Post-Incident Review required by RES-002, and an assessment for a Significant Change SHALL be completed before the change is deployed to production.
- **RSK-002.5.6.5** System-level risk assessments SHALL be repeated for each Recovery Tier 0 and Recovery Tier 1 system and each system holding Restricted data at least every 12 months, and for all other in-scope systems at least every 24 months.
- **RSK-002.5.6.6** `[HIPAA]` The enterprise risk assessment SHALL include an accurate and thorough assessment of the potential risks and Vulnerabilities to the Confidentiality, Integrity and Availability of all ePHI the Organization creates, receives, maintains or transmits, covering every Information System and location holding ePHI.
- **RSK-002.5.6.7** The enterprise risk assessment report SHALL be approved by the CISO and presented to the ISSC within 30 days of completion.

### 5.7 Treatment deadlines

- **RSK-002.5.7.1** The Risk Owner SHALL have an approved treatment plan, or a submitted TPL-002 Risk Acceptance, in place within the following deadlines from the date the Risk is rated: **Critical 30 days · High 60 days · Medium 90 days · Low by the next annual enterprise risk assessment.**
- **RSK-002.5.7.2** For a Risk rated Critical, the Risk Owner SHALL implement interim measures to reduce likelihood or impact within 5 business days of rating, and SHALL record them in the Risk Register.
- **RSK-002.5.7.3** Treatment plans for Risks rated Critical or High SHALL target a Residual Risk at or below the "Maximum Residual Risk without acceptance" for the Risk category in RSK-001.
- **RSK-002.5.7.4** Deadlines SHALL run from the date the score is recorded as final under RSK-002.5.1.7; review SHALL be completed within 5 business days of the assessor's draft score.

### 5.8 `[PCI]` Targeted Risk Analysis

- **RSK-002.5.8.1** `[PCI]` A Targeted Risk Analysis (TRA) under PCI DSS Requirement 12.3.1 SHALL be performed for each PCI DSS requirement that permits the Organization to set the frequency of a control, including at minimum, where applicable to the Organization's CDE: 5.2.3.1 (evaluation of system components not at risk from malware), 5.3.2.1 (malware scan frequency), 7.2.5.1 (review of application and system account access), 8.6.3 (change frequency of application and system account passwords), 9.5.1.2.1 (inspection frequency of point-of-interaction devices), 10.4.2.1 (log review frequency for other system components), 11.3.1.1 (handling of non-high and non-critical vulnerabilities), 11.6.1 (frequency of change- and tamper-detection on Payment Pages) and 12.10.4.1 (frequency of incident response personnel training).
- **RSK-002.5.8.2** `[PCI]` Each 12.3.1 TRA SHALL document: the assets being protected; the Threats the requirement is protecting against; the factors that contribute to the likelihood and impact of a Threat being realized; and the resulting analysis that determines, and justifies, how frequently the control is performed to minimize the likelihood of the Threat being realized.
- **RSK-002.5.8.3** `[PCI]` Each 12.3.1 TRA SHALL be reviewed at least once every 12 months to determine whether the results remain valid or whether a new TRA is needed, and SHALL be re-performed on any change to CDE scope or segmentation under SEC-019.
- **RSK-002.5.8.4** `[PCI]` Where the Organization meets a PCI DSS requirement using the customized approach, a TRA under Requirement 12.3.2 SHALL be performed for each such requirement and SHALL include all elements specified in PCI DSS Appendix D, covering the customized control's design, the Threats addressed, the assessed likelihood and impact, and the justification that the control meets the requirement's stated objective.
- **RSK-002.5.8.5** `[PCI]` Each 12.3.2 TRA SHALL be approved by the CISO as the senior manager accountable for PCI DSS compliance, and SHALL be performed at least once every 12 months.
- **RSK-002.5.8.6** `[PCI]` TRAs SHALL use the likelihood and impact criteria in sections 5.2 and 5.3 so that results are comparable with the Risk Register. The frequency selected by a 12.3.1 TRA SHALL NOT be less frequent than any frequency set by another suite document for the same Control.
- **RSK-002.5.8.7** `[PCI]` The Head of GRC SHALL maintain an index of all current TRAs, their owners, approval dates and next review dates, linked to the Risk Register.
- **RSK-002.5.8.8** `[PCI]` Risks identified by the cipher suite and protocol review (PCI DSS 12.3.3) under SEC-006.5.1.6, and by the CDE technology review (PCI DSS 12.3.4) under SEC-019.5.10.3, SHALL be submitted by the Head of Security Engineering to the Risk Register and scored under this Standard.

### 5.9 Assessment records and quality

- **RSK-002.5.9.1** Every assessment SHALL produce a record containing the scope, date, assessors, reviewer, Information Assets, scenarios, Inherent Risk score, Controls and their effectiveness ratings, Residual Risk score, rationale, and links to Risk Register entries.
- **RSK-002.5.9.2** Assessment records SHALL be retained as Evidence under CMP-004.
- **RSK-002.5.9.3** The Head of GRC SHALL calibrate assessors at least every 12 months by having at least two assessors independently score the same five sample Risks; where independent scores differ by more than one level on either axis, the Head of GRC SHALL record the cause and update guidance.
- **RSK-002.5.9.4** Assessors SHALL NOT assess Risks in processes or systems they own or operate, except where they are paired with an independent reviewer under RSK-002.5.1.7.

### 5.10 Fraud risk

- **RSK-002.5.10.1** Each enterprise risk assessment under RSK-002.5.6.1 SHALL explicitly assess fraud risk, including: incentives and pressures that could motivate fraud; opportunities to commit fraud, such as weak or bypassed Controls and unmonitored privileged access; attitudes and rationalizations that could allow it; and the risk of management override of Controls.
- **RSK-002.5.10.2** `[SOX]` The assessment SHALL include fraud risk to financial reporting, covering fraudulent financial reporting and misappropriation of assets affecting Financially Significant Systems, and SHALL be shared with the CFO for CMP-009 scoping.
- **RSK-002.5.10.3** Fraud scenarios identified SHALL be scored under this Standard and recorded in the Risk Register. Triggered and system-level assessments SHALL consider fraud where the scope includes financial transactions, payments or privileged access.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CISO | Approves this Standard; approves the enterprise risk assessment report (5.6.7); reviews High and Critical scores (5.1.7); `[PCI]` approves 12.3.2 TRAs (5.8.5). |
| Head of GRC | Owns this Standard; runs the enterprise risk assessment; reviews High and Critical scores; maintains the TRA index; calibrates assessors (5.9.3); updates financial thresholds (5.3.2). |
| Risk Owner | Provides scenario and impact information; submits treatment plans or TPL-002 within the deadlines in 5.7; implements interim measures for Critical Risks (5.7.2). |
| Assessor | Performs assessments according to section 5.1; documents rationale (5.1.6). |
| Control Owner | Provides Evidence supporting Control effectiveness ratings (5.5.1). |
| CPO / DPO | Confirm Safety & privacy impact scores for Risks involving Personal Data (5.3.4). |
| CFO | Approves absolute financial thresholds if the Organization replaces the default percentages (5.3.2). |
| Business Continuity Manager | Supplies Recovery Tier and RTO information used in the Operational dimension. |
| Head of Security Engineering | `[PCI]` Registers Risks from the 12.3.3 and 12.3.4 reviews (5.8.8); performs TRAs for technical controls (SEC-019.5.10.1). |
| SOC Manager | Supplies threat intelligence and incident history used for likelihood (via RSK-005). |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| RSK-002.7.1 | Risk scoring | 5×5 likelihood × impact, score 1–25 |
| RSK-002.7.2 | Risk levels | Low 1–4 · Medium 5–9 · High 10–16 · Critical 17–25 |
| RSK-002.7.3 | Enterprise risk assessment | At least every 12 months, plus triggers (significant change, new Tier 1 vendor, Sev-1/Sev-2 incident, new legal obligation, merger or acquisition) |
| RSK-002.7.4 | Risk treatment plan deadline | Critical 30 days · High 60 days · Medium 90 days · Low next annual assessment |
| RSK-002.7.5 | Triggered assessment completion | 30 days from trigger; Sev-1/Sev-2: 10 business days after Post-Incident Review; Significant Change: before production deployment |
| RSK-002.7.6 | System-level reassessment | Recovery Tier 0/1 and Restricted-data systems every 12 months; all others every 24 months |
| RSK-002.7.7 | Interim measures for Critical Risks | Within 5 business days of rating |
| RSK-002.7.8 | Independent review of scores | Before finalization, within 5 business days of draft; Head of GRC or CISO for High and Critical |
| RSK-002.7.9 | Maximum age of Evidence for Control effectiveness | 12 months |
| RSK-002.7.10 | Enterprise assessment report to ISSC | Within 30 days of completion |
| RSK-002.7.11 | Impact aggregation | Highest single dimension; no averaging |
| RSK-002.7.12 | `[PCI]` 12.3.1 TRA review | At least every 12 months and on CDE scope change |
| RSK-002.7.13 | `[PCI]` 12.3.2 TRA | Per customized-approach requirement, approved by CISO, at least every 12 months |
| RSK-002.7.14 | `[PCI]` Cipher suite and technology reviews (12.3.3, 12.3.4) | Per SEC-006.5.1.6 and SEC-019.5.10.3; resulting Risks scored under this Standard |
| RSK-002.7.15 | Assessor calibration | Every 12 months, 5 sample Risks |
| RSK-002.7.16 | Acceptance authority and validity | As set in RSK-001 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Enterprise risk assessment completed within 12 months of the previous one | Yes | Annually | Head of GRC |
| Triggered assessments completed within the deadline in 5.6.4 | ≥ 95% | Quarterly | Head of GRC |
| Risks with a treatment plan or TPL-002 within the 5.7.1 deadline | ≥ 95% (Critical 100%) | Monthly | Head of GRC |
| Scores with documented rationale and independent review | 100% | Quarterly (sample of 10%) | Head of GRC |
| System-level assessments current per 5.6.5 | 100% | Quarterly | Head of GRC |
| `[PCI]` TRAs reviewed within 12 months | 100% | Quarterly | Head of GRC |
| Assessor calibration variance > 1 level | ≤ 10% of scored axes | Annually | Head of GRC |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

No Exception SHALL be granted to the scoring method (5.1.2), the risk level bands (5.4.1), or `[PCI]` the TRA requirements in section 5.8.

## 10. Enforcement

Non-compliance is handled under CMP-007.

A risk score that is found on review to have been understated against the criteria in sections 5.2 and 5.3 SHALL be corrected within 5 business days, and the corrected score SHALL apply from the original rating date for treatment deadlines.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| RSK-002.5.1 | 6.1.2, 8.2 | GV.RM-06, ID.RA-05 | RA-3 | — | CC3.2 | APO12.02 | `[HIPAA]` §164.308(a)(1)(ii)(A); `[GDPR]` Art. 32(2) |
| RSK-002.5.2 – 5.4 | 6.1.2(c)–(d) | ID.RA-04, ID.RA-05 | RA-3 | — | CC3.2 | APO12.02, APO12.03 | — |
| RSK-002.5.5 | 6.1.3, 9.1 | ID.RA-05, ID.IM-01 | RA-3, CA-2 | — | CC3.2, CC4.1 | MEA02 | `[SOX]` §404 |
| RSK-002.5.6 | 8.2 | ID.RA-07, ID.IM-01 | RA-3 | — | CC3.4 | APO12.02 | `[HIPAA]` §164.308(a)(1)(ii)(A); `[PCI]` 12.3.1 |
| RSK-002.5.7 | 6.1.3, 8.3 | ID.RA-06 | RA-7 | 7.2 | CC3.2, CC5.1 | APO12.06 | `[HIPAA]` §164.308(a)(1)(ii)(B) |
| RSK-002.5.8 | 6.1.2 | ID.RA-05 | RA-3 | — | CC3.2 | APO12.02 | `[PCI]` 12.3.1, 12.3.2, 12.3.3, 12.3.4 |
| RSK-002.5.9 | 7.5.3, 8.2 | GV.RM-06 | RA-3 | — | CC3.2 | APO12.03 | — |
| RSK-002.5.10 | 6.1.2 | ID.RA-03, ID.RA-05 | RA-3 | — | CC3.3 | APO12.02 | `[SOX]` §404 |

## 12. Related documents

RSK-001, RSK-003, RSK-004, RSK-005, RSK-006, CMP-001, CMP-002, CMP-003, CMP-004, CMP-007, CMP-009, SEC-002, SEC-006, SEC-011, SEC-013, SEC-018, SEC-019, RES-002, RES-005, TPL-001, TPL-002, REF-001

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Head of GRC | | | |
| Approver: CISO | | | |
