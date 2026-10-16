# CMP-002 — Internal Audit & Control Testing Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | CMP-002 |
| Title | Internal Audit & Control Testing Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Internal Audit Director |
| Approver | Audit Committee † (governance independence) |
| Effective date | [DECISION REQUIRED: Date of Audit Committee approval] |
| Next review date | Effective date + 12 months, and on the event-triggered reviews defined in GOV-002 |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-001, GOV-002, GOV-003, RSK-001, RSK-002, CMP-001, CMP-003, CMP-004, CMP-007, CMP-008, CMP-009, SEC-011, SEC-019, REF-001, REF-002 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Internal Audit Director | Initial release |

## 3. Purpose

This Policy establishes the independence, mandate and planning of Internal Audit for the
Information Security Program, and the Organization's requirements for testing Controls,
selecting samples, classifying and remediating deficiencies, and coordinating with external
auditors, service auditors and Qualified Security Assessors. It ensures that control
assurance is independent, risk-based, repeatable and sufficient to support management's
assertions, including the SOC 2 Type II examination, `[SOX]` §§302 and 404 assessments
and `[PCI]` PCI DSS validation.

## 4. Scope

- **People:** the Internal Audit function and any co-sourced or outsourced provider acting for it; the Head of GRC and GRC staff performing second-line control testing; Control Owners; and all Workforce Members who provide Evidence or are interviewed during testing.
- **Systems:** all Information Systems, Cloud Services and Controls within the Information Security Program defined in ISP-000 and mapped in REF-001, including Financially Significant Systems `[SOX]`, the CDE `[PCI]` and systems holding ePHI `[HIPAA]`.
- **Data:** all Evidence, audit workpapers, samples, issue records and reports produced under this Policy.
- **Locations:** all Organization sites and remote working locations within ISP-000 scope.
- **Third Parties:** co-sourced audit providers, External Auditors, service auditors, QSAs, ASVs and other assessors; and Third Parties whose Controls the Organization relies on (assessed under RSK-003).

## 5. Policy statements

### 5.1 Internal Audit mandate and independence

- **CMP-002.5.1.1** The Audit Committee SHALL approve an Internal Audit Charter that sets out Internal Audit's purpose, authority, responsibility and scope, and SHALL re-approve it every 12 months.
- **CMP-002.5.1.2** The Internal Audit Director SHALL report functionally to the Audit Committee and administratively to the CEO. [DECISION REQUIRED: Administrative reporting line of the Internal Audit Director. Recommended default: CEO]
- **CMP-002.5.1.3** The Audit Committee SHALL approve the appointment, removal, performance evaluation and remuneration of the Internal Audit Director, and the Internal Audit budget.
- **CMP-002.5.1.4** Internal Audit SHALL have unrestricted access to all records, Information Systems, facilities and Workforce Members relevant to an engagement, subject only to Legal Privilege as determined by the GC. Any restriction of access SHALL be reported by the Internal Audit Director to the Audit Committee chair within 2 business days.
- **CMP-002.5.1.5** Internal Audit SHALL NOT design, implement, operate or own any Control it may audit, and SHALL NOT approve Exceptions, Risk Acceptances or Changes. Internal Audit MAY advise on control design where the advice is documented and the Audit Committee is informed in the next quarterly report.
- **CMP-002.5.1.6** An internal auditor SHALL NOT audit an activity for which they held operational responsibility within the previous 12 months.
- **CMP-002.5.1.7** Each internal auditor and co-sourced provider staff member SHALL sign a declaration of independence and conflicts of interest before their first engagement and every 12 months thereafter. A declared conflict SHALL result in reassignment.
- **CMP-002.5.1.8** The Internal Audit Director SHALL meet the Audit Committee in private session, without management present, at least every 12 months, and at any other time either party requests.
- **CMP-002.5.1.9** Internal Audit SHALL conform with the Institute of Internal Auditors' Global Internal Audit Standards. The Internal Audit Director SHALL perform an internal quality assessment every 12 months, and SHALL obtain an external quality assessment by a qualified independent assessor at least every 5 years, reporting results to the Audit Committee.
- **CMP-002.5.1.10** Internal auditors performing information security engagements SHALL hold, or be supervised by a person holding, a recognized audit or security qualification (e.g. CISA, CISSP, CIA), and SHALL complete at least 40 hours of continuing professional education every 12 months.

### 5.2 Annual risk-based audit plan

- **CMP-002.5.2.1** The Internal Audit Director SHALL prepare an annual risk-based audit plan and submit it to the Audit Committee for approval no later than 30 days before the start of each fiscal year.
- **CMP-002.5.2.2** The audit plan SHALL be based on documented inputs, including as a minimum: the Risk Register (RSK-001), the Obligations Register and Compliance Calendar (CMP-001), prior internal and external audit results, open issues under CMP-002.5.8, Security Incidents of Severity Sev-1 or Sev-2 since the last plan, significant Changes and new Critical Vendors, and input from the ISSC, CISO, CFO and GC.
- **CMP-002.5.2.3** The audit plan SHALL rank auditable areas by Residual Risk under RSK-002 and SHALL set audit frequency so that:
  - every auditable area with a Critical or High Residual Risk is audited at least every 12 months;
  - every auditable area with a Medium Residual Risk is audited at least every 24 months;
  - every suite Policy domain (GOV, RSK, CMP, SEC, RES, PPL) is audited at least every 36 months.
- **CMP-002.5.2.4** The audit plan SHALL state for each engagement: objective, scope, planned quarter, estimated hours, and required skills; and SHALL state the total resources required and any resource shortfall.
- **CMP-002.5.2.5** `[HIPAA]` The audit plan SHALL include an audit of Security Rule compliance against CMP-008 at least every 24 months.
- **CMP-002.5.2.6** `[SOX]` The audit plan SHALL include the testing of ITGC Key Controls over Financially Significant Systems needed to support management's annual SOX §404 assessment, in coordination with CMP-009 and the External Auditor.
- **CMP-002.5.2.7** Changes to the approved plan that add, remove or defer an engagement SHALL be approved by the Audit Committee. The Internal Audit Director MAY add an unplanned engagement in response to an emerging risk and SHALL report it to the Audit Committee at its next meeting.
- **CMP-002.5.2.8** The audit plan SHALL include an audit of the operation of CMP-006 and of sanction consistency under CMP-007 at least every 24 months.

### 5.3 Lines of assurance

- **CMP-002.5.3.1** Control Owners (first line) SHALL operate their Controls and SHALL complete a control self-assessment of each Key Control they own at least every 6 months, recording the result and supporting Evidence under CMP-004.
- **CMP-002.5.3.2** The Head of GRC (second line) SHALL test the operating effectiveness of every Key Control in SOC 2 Type II examination scope at least every 6 months, and every other Control mapped in REF-001 at least every 12 months, using the methods and sample sizes in this Policy.
- **CMP-002.5.3.3** Internal Audit (third line) SHALL provide independent assurance through the engagements in the annual audit plan, and MAY rely on second-line testing only after re-performing a sample of it under CMP-002.5.6.10.
- **CMP-002.5.3.4** The Head of GRC SHOULD implement automated continuous control monitoring for Controls whose operation is recorded in system data (e.g. MFA enforcement, Access Review completion, scan coverage, Backup success). Automated monitoring SHALL NOT replace the testing in CMP-002.5.3.2 until the monitoring logic itself has been tested under CMP-002.5.5.6.

### 5.4 Engagement conduct

- **CMP-002.5.4.1** Each engagement SHALL have a documented planning memorandum stating objective, scope, period under review, criteria (suite requirement IDs and REF-001 mappings), approach and staffing, approved by the Internal Audit Director before fieldwork.
- **CMP-002.5.4.2** Internal Audit SHALL notify the accountable executive and Control Owners in writing at least 10 business days before fieldwork begins, except for unannounced engagements authorized by the Audit Committee chair.
- **CMP-002.5.4.3** Control Owners SHALL provide requested Evidence within 5 business days of request. A request outstanding beyond 10 business days SHALL be escalated to the accountable executive and recorded as a scope limitation if not resolved.
- **CMP-002.5.4.4** Internal Audit SHALL issue a draft report within 15 business days of the end of fieldwork. Management SHALL provide written responses, including remediation owner and target date for each finding, within 10 business days of the draft report.
- **CMP-002.5.4.5** Internal Audit SHALL issue the final report within 30 days of the end of fieldwork to the accountable executive, the CISO, the Head of GRC, and the Audit Committee. Reports rating any finding as a Significant Deficiency or Material Weakness SHALL also be sent to the CEO and CFO.
- **CMP-002.5.4.6** Each report SHALL contain an overall rating (Effective · Needs Improvement · Ineffective), each finding with condition, criteria, cause, effect and classification under CMP-002.5.7, and management's response.

### 5.5 Control testing methods

- **CMP-002.5.5.1** Testing SHALL cover both design effectiveness and operating effectiveness. Design effectiveness SHALL be evaluated by a walkthrough of one instance of the Control from initiation to completion before operating-effectiveness testing.
- **CMP-002.5.5.2** Testers SHALL use one or more of the following methods, documented for each test step:

  | Method | Description | Evidential strength |
  |---|---|---|
  | Inquiry | Questioning the Control Owner or performer about how the Control operates | Lowest; SHALL NOT be used alone to conclude a Control is operating effectively |
  | Observation | Watching the Control being performed at the time it operates | Moderate; applies only to the point in time observed |
  | Inspection | Examining records, configurations, system outputs, approvals or tickets that evidence the Control's operation | High |
  | Re-performance | Independently executing the Control, or recalculating its result, and comparing outcomes | Highest |

- **CMP-002.5.5.3** Operating-effectiveness testing of each Key Control SHALL include inspection or re-performance. Inquiry SHALL be corroborated by at least one other method for every Control.
- **CMP-002.5.5.4** Testing SHALL cover the full period of reliance. Samples SHALL be drawn from the whole period, and where interim testing is performed, roll-forward testing SHALL cover any remaining period longer than 3 months.
- **CMP-002.5.5.5** Where a test relies on information produced by the Organization (e.g. a user listing, a ticket report, a system-generated population), the tester SHALL validate its completeness and accuracy by inspecting the query or report parameters and reconciling it to the source system, and SHALL record this validation.
- **CMP-002.5.5.6** An automated Control MAY be tested with one instance per configuration (test of one) where the ITGCs over the system (change management under SEC-013 and access under SEC-003) have been tested as effective for the same period. Without effective ITGCs, the automated Control SHALL be tested using the sample size for its frequency.
- **CMP-002.5.5.7** Testing SHALL be documented in workpapers that record: Control ID, test objective, method, population and source, sample selection method and items, results per item, deviations, conclusion, tester name and date, and reviewer name and date.
- **CMP-002.5.5.8** Every workpaper SHALL be reviewed and signed off by a person other than the tester within 10 business days of completion. Workpapers SHALL be stored and retained under CMP-004.
- **CMP-002.5.5.9** Testers SHALL NOT test a Control they operate, or a Control whose Evidence they produced.

### 5.6 Sampling

- **CMP-002.5.6.1** Sample sizes SHALL be no smaller than those in the table below. The "Elevated" column applies to Key Controls, Controls in `[PCI]` or `[HIPAA]` scope, and Controls mitigating a Risk rated High or Critical under RSK-002.

  | Control frequency | Approx. population per 12 months | Minimum sample — Standard | Minimum sample — Elevated |
  |---|---|---|---|
  | Annual | 1 | 1 | 1 |
  | Semi-annual | 2 | 1 | 2 |
  | Quarterly | 4 | 2 | 2 |
  | Monthly | 12 | 2 | 3 |
  | Weekly | 52 | 5 | 10 |
  | Daily | 250–365 | 20 | 30 |
  | Multiple times per day | > 365 | 25 | 40 |
  | Automated (with effective ITGCs) | n/a | 1 per configuration | 1 per configuration |
  | Event-driven (e.g. new hires, Changes, Separations) | Count of events in period | Per the row whose population is closest to the event count; all items where population ≤ 5 | Per the row whose population is closest to the event count; all items where population ≤ 5 |

- **CMP-002.5.6.2** Where the testing period is shorter than 12 months, sample sizes SHALL be reduced in proportion to the period but SHALL NOT fall below 2 for any Control with a population of 2 or more.
- **CMP-002.5.6.3** Samples SHALL be selected randomly (using a documented random-number method or tool) or systematically with a random start. Haphazard or judgmental selection SHALL NOT be used for Key Controls; it MAY be used to supplement a random sample, for example to target high-risk items.
- **CMP-002.5.6.4** For Controls with multiple locations, systems or instances, the sample SHALL include items from each instance, or each instance SHALL be tested as a separate population.
- **CMP-002.5.6.5** No deviations are tolerated in the minimum sample. Where one deviation is found in a sample of 10 or more, the tester MAY extend the sample by the original sample size; if no further deviation is found, the Control MAY be concluded effective with the deviation recorded as an observation. Any deviation in a sample smaller than 10, or a second deviation in an extended sample, SHALL result in the Control being concluded not effective.
- **CMP-002.5.6.6** Each deviation SHALL be investigated to determine its Root Cause and whether it is isolated or systemic before classification under CMP-002.5.7.
- **CMP-002.5.6.7** Where an External Auditor, service auditor or QSA requires larger samples, their sample sizes SHALL apply to that engagement.
- **CMP-002.5.6.8** A remediated Control SHALL operate for the following minimum period before it is re-tested for closure: Multiple times per day or Daily — 30 days; Weekly — 5 weeks; Monthly — 2 months; Quarterly — 1 quarter; Semi-annual or Annual — 1 instance.
- **CMP-002.5.6.9** Re-tests for closure SHALL use the sample sizes in CMP-002.5.6.1 applied to the post-remediation period, with a minimum of the Standard sample size or the entire post-remediation population, whichever is smaller.
- **CMP-002.5.6.10** Where Internal Audit intends to rely on second-line testing, it SHALL re-perform at least 10% of the second-line test steps (minimum 1 Control per domain) and SHALL NOT rely on the testing if any re-performed conclusion differs.
- **CMP-002.5.6.11** `[SOX]` For Key Controls over Financially Significant Systems, minimum sample sizes and minimum operation before retest are set in CMP-009.5.10.3 and CMP-009.5.12.2, and apply instead of CMP-002.5.6.1, CMP-002.5.6.8 and CMP-002.5.6.9.

### 5.7 Deficiency classification

- **CMP-002.5.7.1** Every finding SHALL be classified using the criteria below. The classification SHALL consider both the likelihood that the Control failure results in a misstatement, Security Incident, Personal Data Breach or regulatory non-compliance, and the potential magnitude, scored under RSK-002.

  | Classification | Criteria | Indicative RSK-002 Residual Risk |
  |---|---|---|
  | Observation | No Control failure; an opportunity to improve efficiency or design, or an isolated deviation in an extended sample under CMP-002.5.6.5 | Low |
  | Deficiency | A Control Deficiency (GOV-006) that does not meet the criteria for a higher classification | Low or Medium |
  | Significant Deficiency | A Significant Deficiency (GOV-006); for non-financial Controls, also any deficiency in a Key Control, or any deficiency that leaves a High Residual Risk, a reportable SOC 2 exception, or a PCI DSS requirement "not in place" | High |
  | Material Weakness `[SOX]` | A Material Weakness (GOV-006), assessed using the likelihood and magnitude criteria in PCAOB AS 2201 | Critical |
  | Critical Deficiency (non-SOX) | A deficiency that leaves a Critical Residual Risk, or that would cause an applicable obligation in the Obligations Register to be assessed Non-compliant with regulatory consequence | Critical |

- **CMP-002.5.7.2** `[SOX]` Evaluation, classification and aggregation of ITGC deficiencies affecting Financially Significant Systems SHALL follow CMP-009 section 5.11.
- **CMP-002.5.7.3** `[SOX]` Escalation of Significant Deficiencies and Material Weaknesses in ITGCs over Financially Significant Systems to the Audit Committee, and their consideration for SOX §302 and §404 disclosure, SHALL follow CMP-009.5.11.4 and CMP-009.5.11.5.
- **CMP-002.5.7.4** Significant Deficiencies (other than `[SOX]` ITGC deficiencies under CMP-002.5.7.3) and Critical Deficiencies SHALL be reported by the Internal Audit Director to the Audit Committee chair within 5 business days of classification, and to the ISSC at its next meeting.
- **CMP-002.5.7.5** A finding SHALL NOT be downgraded after the final report is issued except on new Evidence, documented by the Internal Audit Director and reported to the Audit Committee.
- **CMP-002.5.7.6** Findings that are technical Vulnerabilities SHALL be remediated within the remediation SLA in SEC-011 where that SLA is shorter than the timeline in CMP-002.5.8.

### 5.8 Issue management and remediation

- **CMP-002.5.8.1** The Head of GRC SHALL record every finding from Internal Audit, second-line testing, control self-assessment, external audits, SOC 2 examinations, QSA assessments, regulator examinations and investigations under CMP-006 in a single Issue Register, with: issue ID, source, Control ID, classification, description, Root Cause, remediation owner (an accountable executive or functional lead), action plan, target date, status, and validation result.
- **CMP-002.5.8.2** Remediation owners SHALL submit a remediation action plan and SHALL complete remediation within the timelines below, measured from the date of the final report or classification:

  | Classification | Action plan due | Remediation due |
  |---|---|---|
  | Critical Deficiency | 10 business days | 60 days |
  | Significant Deficiency | 15 business days | 90 days |
  | Deficiency | 20 business days | 180 days |
  | Observation | 30 days (response) | 12 months or the next audit of the area, whichever is earlier |

- **CMP-002.5.8.3** Each action plan SHALL address Root Cause, not only the instances found, and SHALL state the Evidence that will demonstrate remediation.
- **CMP-002.5.8.4** A remediation target date MAY be extended once, by no more than the original remediation period, with approval of the CISO for Deficiencies and Observations, and of the ISSC for Significant Deficiencies. Extension of a Critical Deficiency target date SHALL be approved by the Audit Committee. `[SOX]` Remediation plans, approval and retesting of ITGC deficiencies over Financially Significant Systems SHALL follow CMP-009.5.12 instead of CMP-002.5.8.2 and this item.
- **CMP-002.5.8.5** Where remediation cannot be completed within the extended date, the remediation owner SHALL obtain an Exception under CMP-003 or a Risk Acceptance under RSK-001 before the extended date passes.
- **CMP-002.5.8.6** An issue SHALL be closed only after the issuing function (Internal Audit for its findings; the Head of GRC for all others) has validated remediation by re-testing under CMP-002.5.6.8 – 5.6.9. Self-declared closure by the remediation owner SHALL NOT be accepted.
- **CMP-002.5.8.7** The Head of GRC SHALL report overdue issues to the ISSC monthly. Issues more than 30 days overdue SHALL be escalated to the accountable executive and reported by the Internal Audit Director to the Audit Committee at its next quarterly meeting.
- **CMP-002.5.8.8** The Internal Audit Director SHALL report to the Audit Committee quarterly: plan progress, engagement results, open issues by classification and age, overdue issues, extensions granted, and any scope limitation.
- **CMP-002.5.8.9** The Internal Audit Director SHALL provide the Audit Committee, every 12 months, with an overall conclusion on the effectiveness of the Information Security Program's Controls, based on the year's engagements.

### 5.9 Coordination with External Auditors, service auditors and QSAs

- **CMP-002.5.9.1** The Head of GRC SHALL be the single coordination point for the SOC 2 Type II examination, `[PCI]` QSA assessments and other information security assessments; the CFO SHALL be the coordination point for the external financial statement auditor, with the Head of GRC coordinating ITGC requests. External assessment scheduling and scope are governed by CMP-001.
- **CMP-002.5.9.2** The Internal Audit Director SHALL share the annual audit plan and relevant reports with the external financial statement auditor and service auditor, and SHALL agree with them, before fieldwork, the extent of any reliance on Internal Audit work (PCAOB AS 2605; AICPA AU-C 610 and AT-C 205 as applicable).
- **CMP-002.5.9.3** Engagement of the external financial statement auditor for any non-audit service SHALL be pre-approved by the Audit Committee. The external financial statement auditor SHALL NOT perform Internal Audit services.
- **CMP-002.5.9.4** External Auditor and assessor Evidence requests SHALL be tracked in a request list (provided-by-client list) with request date, owner, due date and delivery date. Control Owners SHALL respond within 5 business days unless the engagement letter sets a shorter period.
- **CMP-002.5.9.5** Evidence provided to external parties SHALL be delivered through the Evidence repository or a secure transfer method using the protocols approved in SEC-006 section 5.2, SHALL be the minimum required for the request, and SHALL have Personal Data, CHD and PHI masked unless the request requires it and the CPO approves.
- **CMP-002.5.9.6** `[PCI]` The QSA SHALL be engaged for the ROC under CMP-001. The Head of GRC SHALL provide the QSA with the CDE scope documentation from SEC-019, the targeted risk analyses and any customized-approach controls matrix from REF-001, and the results of second-line PCI DSS testing. Requirements assessed "not in place" SHALL be recorded as Significant Deficiencies and remediated before the AOC is signed, or reported to the acquirer as required.
- **CMP-002.5.9.7** Findings from External Auditors, service auditors, QSAs and regulators SHALL be entered in the Issue Register within 10 business days of receipt and managed under CMP-002.5.8.
- **CMP-002.5.9.8** External Auditors and assessors SHALL be granted read-only, time-bound access to Information Systems where direct access is required, provisioned under SEC-003 and removed at the end of fieldwork.

### 5.10 Records

- **CMP-002.5.10.1** Audit plans, planning memoranda, workpapers, sample selections, reports, management responses, the Issue Register and remediation validation Evidence SHALL be retained under the retention schedule in CMP-004.
- **CMP-002.5.10.2** Workpapers SHALL be locked against change on report issuance; any later amendment SHALL be recorded with date, author and reason.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| Audit Committee | Approves this Policy, the Internal Audit Charter and the annual audit plan; oversees Internal Audit independence and the Internal Audit Director; receives quarterly reports and Significant Deficiency / Material Weakness escalations; approves Material Weakness extensions; pre-approves non-audit services by the External Auditor. |
| Internal Audit Director | Owns this Policy; prepares and executes the audit plan; maintains independence and quality; issues reports; validates remediation of Internal Audit findings; reports to the Audit Committee. |
| CEO | Administrative Line Manager of the Internal Audit Director; `[SOX]` considers Material Weaknesses for §302 / §404 disclosure. |
| CFO | `[SOX]` Determines ITGC deficiency classification with Internal Audit and the Head of GRC; reports Material Weaknesses to the Audit Committee; coordinates with the external financial statement auditor. |
| CISO | Approves extensions for Deficiencies and Observations; accountable executive for security Control findings; receives all reports. |
| ISSC | Receives overdue issue reports; approves Significant Deficiency extensions. |
| GC | Determines Legal Privilege restrictions on access; advises on disclosure. |
| CPO | Approves disclosure of Personal Data to External Auditors where masking is not possible. |
| Head of GRC | Performs second-line control testing; maintains the Issue Register; coordinates external assessments and request lists; validates closure of non-Internal Audit issues. |
| Control Owners | Operate Controls; complete self-assessments; provide Evidence within the response times; own remediation of findings on their Controls. |
| Remediation owners | Submit action plans and complete remediation within the timelines in CMP-002.5.8.2. |
| External Auditors, service auditors, QSAs | Perform independent assessments under their engagement letters and professional standards. |

Role names and accountabilities are established in GOV-001 and consolidated in REF-002.

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| CMP-002.7.1 | Internal Audit reporting line | Functional: Audit Committee; administrative: CEO (default) |
| CMP-002.7.2 | Internal Audit Charter re-approval | Every 12 months |
| CMP-002.7.3 | Audit Committee private session with Internal Audit Director | At least every 12 months |
| CMP-002.7.4 | Auditor cooling-off from operational responsibility | 12 months |
| CMP-002.7.5 | Internal / external quality assessment | Every 12 months / at least every 5 years |
| CMP-002.7.6 | Auditor continuing professional education | 40 hours every 12 months |
| CMP-002.7.7 | Annual audit plan submitted for approval | ≥ 30 days before fiscal year start |
| CMP-002.7.8 | Audit coverage | Critical / High Residual Risk areas every 12 months; Medium every 24 months; every Policy domain every 36 months; `[HIPAA]` Security Rule every 24 months; CMP-006 and CMP-007 every 24 months |
| CMP-002.7.9 | First-line control self-assessment of Key Controls | Every 6 months |
| CMP-002.7.10 | Second-line testing | SOC 2 Key Controls every 6 months; other REF-001 Controls every 12 months |
| CMP-002.7.11 | Fieldwork notice | ≥ 10 business days |
| CMP-002.7.12 | Evidence response (internal and external requests) | 5 business days; escalation at 10 business days |
| CMP-002.7.13 | Draft report / management response / final report | 15 business days after fieldwork / 10 business days after draft / 30 days after fieldwork |
| CMP-002.7.14 | Workpaper review | Within 10 business days of completion, by a person other than the tester |
| CMP-002.7.15 | Sample sizes | Per table in CMP-002.5.6.1; `[SOX]` ITGCs per CMP-009.5.10.3 |
| CMP-002.7.16 | Roll-forward testing required | Where remaining period > 3 months |
| CMP-002.7.17 | Deviation tolerance | 0 in minimum sample; one extension permitted for samples ≥ 10 |
| CMP-002.7.18 | Minimum operation before closure re-test | Daily+ 30 days · Weekly 5 weeks · Monthly 2 months · Quarterly 1 quarter · Semi-annual/Annual 1 instance; `[SOX]` ITGCs per CMP-009.5.12.2 |
| CMP-002.7.19 | Escalation of Significant Deficiency or Critical Deficiency to Audit Committee | Within 5 business days of classification; `[SOX]` ITGC deficiencies per CMP-009.5.11.4 |
| CMP-002.7.20 | Remediation timelines | Critical Deficiency 60 days · Significant Deficiency 90 days · Deficiency 180 days · Observation 12 months (action plans per CMP-002.5.8.2); `[SOX]` ITGC deficiencies per CMP-009.5.12 |
| CMP-002.7.21 | Remediation of Vulnerability findings | SLA in SEC-011 where shorter |
| CMP-002.7.22 | Remediation extensions | One extension, ≤ original period; approval per CMP-002.5.8.4 |
| CMP-002.7.23 | External findings entered in Issue Register | Within 10 business days of receipt |
| CMP-002.7.24 | Retention of audit workpapers and Evidence | Per CMP-004 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Annual audit plan engagements completed in planned quarter | ≥ 90%; 100% by fiscal year end | Quarterly | Internal Audit Director |
| Final reports issued within 30 days of fieldwork end | 100% | Quarterly | Internal Audit Director |
| Second-line tests completed on schedule | 100% | Quarterly | Head of GRC |
| Key Controls concluded effective | ≥ 95% | Quarterly | Head of GRC |
| Workpapers reviewed within 10 business days | 100% | Quarterly | Internal Audit Director |
| Open issues past remediation due date | 0 Material Weakness / Critical / Significant Deficiency; ≤ 5% of Deficiencies | Monthly | Head of GRC |
| Issues re-opened after closure validation | 0 | Quarterly | Internal Audit Director |
| Average age of open issues by classification | Within remediation timeline | Quarterly | Head of GRC |
| External Evidence requests delivered by due date | ≥ 95% | Per engagement | Head of GRC |
| `[SOX]` Material Weaknesses at fiscal year end | 0 | Annual | CFO |
| `[PCI]` Requirements "not in place" at AOC signature | 0 | Every 12 months | CISO |
| Independence declarations current | 100% | Every 12 months | Internal Audit Director |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following requirements SHALL NOT receive an Exception: Internal Audit's functional
reporting line to the Audit Committee (CMP-002.5.1.2); the prohibition on Internal Audit
operating Controls it audits (CMP-002.5.1.5); the prohibition on testers testing their own
Controls (CMP-002.5.5.9); and escalation of Significant Deficiencies, Critical Deficiencies
and Material Weaknesses to the Audit Committee (CMP-002.5.7.3 – 5.7.4). Exceptions to
other requirements of this document SHALL also be reported to the Audit Committee at its
next meeting.

## 10. Enforcement

Non-compliance is handled under CMP-007.

Obstruction of an audit, restriction of auditor access without GC privilege determination,
or provision of falsified or altered Evidence SHALL be reported by the Internal Audit
Director to the Audit Committee chair within 2 business days and handled under CMP-007.
Concerns about accounting or auditing matters MAY also be raised under CMP-006.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| CMP-002.5.1 | 5.1, 5.3, 9.2.1; A.5.35 | GV.OV-01, GV.RR-01 | CA-2, PM-1 | — | CC1.2, CC1.5 | MEA04, EDM05 | SOX §301; PCI DSS 12.4 |
| CMP-002.5.2 | 9.2.2; A.5.35 | GV.OV-01, GV.RM-01 | CA-2, PM-14 | — | CC4.1 | MEA02, MEA04 | 45 CFR §164.308(a)(8); SOX §404 |
| CMP-002.5.3 | 9.1, 9.2; A.5.36 | GV.OV-02, ID.IM-02 | CA-2, CA-7 | — | CC4.1 | MEA01, MEA02 | PCI DSS 12.4.2; GDPR Art. 32(1)(d) |
| CMP-002.5.4 – 5.6 | 9.1, 9.2.2; A.5.35, A.5.36 | ID.IM-02 | CA-2, CA-7 | — | CC4.1 | MEA02, MEA04 | SOX §404; PCI DSS 12.4.2.1 |
| CMP-002.5.7 – 5.8 | 10.1, 10.2 | GV.OV-03, ID.IM-01 | CA-5, PM-4 | — | CC4.2, CC5.1 | MEA02, BAI06 | SOX §§302, 404; 45 CFR §164.308(a)(1)(ii)(B) |
| CMP-002.5.9 | 9.2; A.5.35 | GV.OV-01, GV.SC-01 | CA-2, CA-7 | — | CC2.3, CC4.1 | MEA04 | SOX §§301, 404; PCI DSS 12.4 |
| CMP-002.5.10 | 7.5.3; A.5.33 | GV.PO-01 | AU-11 | — | CC4.1 | MEA04 | SOX §404 |

## 12. Related documents

ISP-000, GOV-001, GOV-002, GOV-003, RSK-001, RSK-002, RSK-003, CMP-001, CMP-003, CMP-004,
CMP-006, CMP-007, CMP-008, CMP-009, SEC-003, SEC-006, SEC-011, SEC-013, SEC-019, REF-001,
REF-002

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Internal Audit Director | | | |
| Approver: Audit Committee Chair, on behalf of the Audit Committee | | | |
