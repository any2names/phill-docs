# GOV-003 — Security Metrics & Reporting Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | GOV-003 |
| Title | Security Metrics & Reporting Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Information Security Officer (CISO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | ISP-000, GOV-001, GOV-002, RSK-001, RSK-002, CMP-002, CMP-004, REF-001, REF-003 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CISO | Initial release |

## 3. Purpose

This Policy defines how the Organization measures the performance of its Information Security
Program and reports on it. It sets the catalogue of Key Performance Indicators (KPIs) and Key
Risk Indicators (KRIs) with green, amber and red thresholds, the cadence at which they are
reported to the ISSC, the Audit Committee and the Board of Directors, the content of those
reports, and the rules that make reported figures accurate and auditable.

## 4. Scope

- **People:** the CISO, the Head of GRC, every metric owner named in section 5.3, and every governance body that receives reports.
- **Systems and data:** every Information System that is a data source for a metric in the catalogue, and the metrics repository and dashboards.
- **Locations:** all Organization sites and regions in the scope of ISP-000.
- **Third parties:** Third Parties that supply metric data under contract (for example a managed SOC or a training platform provider).

## 5. Policy statements

### 5.1 Metric governance

- **GOV-003.5.1.1** The CISO SHALL maintain the metric catalogue in section 5.3. Each metric SHALL have a recorded definition consisting of: identifier, name, formula (numerator and denominator), data source, owner, collection frequency, home document of any SLA it measures, and green, amber and red thresholds.
- **GOV-003.5.1.2** Metric thresholds that measure compliance with an SLA SHALL reference the SLA in its home document and SHALL NOT restate it. When a home document changes an SLA, the metric SHALL measure against the new SLA from the home document's effective date.
- **GOV-003.5.1.3** Adding, removing or changing a threshold of a KRI SHALL require ISSC approval as a material change under GOV-002. KPI threshold changes SHALL be approved by the CISO and reported to the ISSC at its next meeting.
- **GOV-003.5.1.4** Each metric owner SHALL deliver the metric value for the reporting period to the Head of GRC within 5 business days after period end.
- **GOV-003.5.1.5** Where a metric cannot be produced for a period, the metric owner SHALL report it as "not measured" with the reason. A metric reported "not measured" for 2 consecutive periods SHALL be treated as red.

### 5.2 Data quality and Evidence

- **GOV-003.5.2.1** Metric values SHALL be derived from system-generated data wherever the data source permits. Manually compiled values SHALL identify the preparer and a reviewer who is not the preparer.
- **GOV-003.5.2.2** The data extract or query output supporting each reported value SHALL be retained as Evidence under CMP-004.
- **GOV-003.5.2.3** The Head of GRC SHALL re-perform the calculation for at least 3 metrics, selected at random, in each quarterly KRI dashboard before it is issued, and SHALL record the result.
- **GOV-003.5.2.4** The Internal Audit Director MAY include metric accuracy in the internal audit plan under CMP-002. Any material misstatement of a reported metric SHALL be corrected in the next report with an explanation.
- **GOV-003.5.2.5** Population coverage SHALL be stated for every percentage metric (for example "of 1,240 in-scope assets"). Assets or accounts excluded from a population SHALL be listed with the reason.

### 5.3 KPI and KRI catalogue

- **GOV-003.5.3.1** The following KPIs SHALL be measured. G = green, A = amber, R = red.

| ID | KPI | Home of SLA / requirement | Green | Amber | Red | Frequency | Owner |
|---|---|---|---|---|---|---|---|
| KPI-01 | % of Critical vulnerabilities remediated within the SEC-011 SLA | SEC-011 | ≥ 95% | 85% to < 95% | < 85% | Monthly | Head of Security Engineering |
| KPI-02 | % of High vulnerabilities remediated within the SEC-011 SLA | SEC-011 | ≥ 90% | 80% to < 90% | < 80% | Monthly | Head of Security Engineering |
| KPI-03 | % of CISA KEV vulnerabilities on internet-facing assets remediated within the SEC-011 SLA | SEC-011 | 100% | 95% to < 100% | < 95% | Monthly | Head of Security Engineering |
| KPI-04 | % of required vulnerability scans completed at the SEC-011 frequency | SEC-011 | 100% | 95% to < 100% | < 95% | Monthly | Head of Security Engineering |
| KPI-05 | % of separations with access revoked within the SEC-003 timeframe | SEC-003 | ≥ 99% | 95% to < 99% | < 95% | Monthly | CISO |
| KPI-06 | % of role changes with access adjusted within the SEC-003 timeframe | SEC-003 | ≥ 95% | 85% to < 95% | < 85% | Monthly | CISO |
| KPI-07 | % of user Access Reviews completed by the SEC-003 deadline | SEC-003 | 100% | 95% to < 100% | < 95% | Quarterly | Head of Security Engineering |
| KPI-08 | % of privileged Access Reviews completed at the SEC-005 frequency | SEC-005 | 100% | — | < 100% | Quarterly | Head of Security Engineering |
| KPI-09 | % of in-scope Users and applications enforcing MFA as required by SEC-004 | SEC-004 | 100% | 98% to < 100% | < 98% | Monthly | Head of Security Engineering |
| KPI-10 | % of Workforce Members completing annual training within the PPL-002 window | PPL-002 | ≥ 98% | 90% to < 98% | < 90% | Monthly | CISO |
| KPI-11 | % of new hires completing training within the PPL-002 timeframe | PPL-002 | ≥ 98% | 90% to < 98% | < 90% | Monthly | CISO |
| KPI-12 | Phishing simulation click rate (latest campaign under PPL-002) | PPL-002 | ≤ 5% | > 5% to 10% | > 10% | Per campaign | CISO |
| KPI-13 | Phishing simulation report rate (latest campaign) | PPL-002 | ≥ 60% | 40% to < 60% | < 40% | Per campaign | CISO |
| KPI-14 | % of Workforce Members with current policy attestation under GOV-002 | GOV-002 | ≥ 98% | 95% to < 98% | < 95% | Monthly | Head of GRC |
| KPI-15 | % of suite documents reviewed within the GOV-002 review cycle | GOV-002 | 100% | 95% to < 100% | < 95% | Monthly | Head of GRC |
| KPI-16 | % of Critical and High alerts triaged within the SEC-012 SLA | SEC-012 | ≥ 98% | 90% to < 98% | < 90% | Monthly | SOC Manager |
| KPI-17 | % of Sev-1 and Sev-2 incidents meeting the RES-002 response SLAs | RES-002 | 100% | 90% to < 100% | < 90% | Monthly | SOC Manager |
| KPI-18 | % of required Post-Incident Reviews completed within the RES-002 deadline | RES-002 | 100% | 80% to < 100% | < 80% | Quarterly | SOC Manager |
| KPI-19 | % of scheduled restore tests completed and successful at the SEC-018 frequency | SEC-018 | 100% | 90% to < 100% | < 90% | Quarterly | CIO |
| KPI-20 | % of Emergency Changes approved retrospectively within the SEC-013 deadline | SEC-013 | 100% | 95% to < 100% | < 95% | Monthly | CIO |
| KPI-21 | % of Endpoints compliant with SEC-008 (managed, encrypted, EDR active) | SEC-008 | ≥ 98% | 95% to < 98% | < 95% | Monthly | CIO |
| KPI-22 | % of Information Assets discovered on the network that are recorded in the Asset Inventory (SEC-001) | SEC-001 | ≥ 98% | 95% to < 98% | < 95% | Monthly | CIO |
| KPI-23 | % of Tier 1 and Tier 2 vendors reassessed at the RSK-003 frequency | RSK-003 | 100% | 90% to < 100% | < 90% | Quarterly | Head of GRC |
| KPI-24 | % of Risk Treatment plans in place within the RSK-002 deadline | RSK-002 | 100% | 90% to < 100% | < 90% | Quarterly | Head of GRC |
| KPI-25 | % of Exception requests decided within the CMP-003 decision time | CMP-003 | 100% | 90% to < 100% | < 90% | Quarterly | Head of GRC |
| KPI-26 | `[GDPR]` `[CPRA]` % of DSRs answered within the CMP-010 deadlines | CMP-010 | 100% | — | < 100% | Monthly | DPO |
| KPI-27 | % of control tests passed in the period (CMP-002) | CMP-002 | ≥ 95% | 85% to < 95% | < 85% | Quarterly | Head of GRC |
| KPI-28 | % of penetration tests completed at the SEC-011 frequency | SEC-011 | 100% | — | < 100% | Quarterly | Head of Security Engineering |

- **GOV-003.5.3.2** The following KRIs SHALL be measured and SHALL form the KRI dashboard.

| ID | KRI | Home of SLA / requirement | Green | Amber | Red | Frequency | Owner |
|---|---|---|---|---|---|---|---|
| KRI-01 | Residual Risks above the RSK-001 Risk Appetite without an approved Risk Acceptance | RSK-001 | 0 | — | ≥ 1 | Monthly | Head of GRC |
| KRI-02 | Critical and High Risks without a Risk Treatment plan past the RSK-002 deadline | RSK-002 | 0 | 1–2 | ≥ 3 | Monthly | Head of GRC |
| KRI-03 | Risk Acceptances or Exceptions past expiry and not closed or renewed (RSK-001, CMP-003) | RSK-001, CMP-003 | 0 | 1–2 | ≥ 3 | Monthly | Head of GRC |
| KRI-04 | Active Exceptions at Critical residual risk (CMP-003) | CMP-003 | 0 | 1 | ≥ 2 | Monthly | Head of GRC |
| KRI-05 | Critical vulnerabilities open beyond the SEC-011 SLA | SEC-011 | 0 | 1–5 | > 5 | Monthly | Head of Security Engineering |
| KRI-06 | Internet-facing assets with a CISA KEV vulnerability beyond the SEC-011 SLA | SEC-011 | 0 | — | ≥ 1 | Weekly | Head of Security Engineering |
| KRI-07 | Privileged Accounts without Phishing-resistant MFA as required by SEC-004 | SEC-004 | 0 | — | ≥ 1 | Monthly | Head of Security Engineering |
| KRI-08 | Information Systems running software past vendor end-of-support without an approved Exception (SEC-001.5.7.4) | SEC-001 | 0 | — | ≥ 1 | Monthly | CIO |
| KRI-09 | Sev-1 Security Incidents in the quarter (RES-002) | RES-002 | 0 | 1 | ≥ 2 | Quarterly | SOC Manager |
| KRI-10 | Personal Data Breaches requiring notification under RES-003 in the quarter | RES-003 | 0 | — | ≥ 1 | Quarterly | CPO |
| KRI-11 | Workforce Members who failed 3 or more phishing simulations in 12 months, as % of Workforce (PPL-002) | PPL-002 | ≤ 2% | > 2% to 5% | > 5% | Quarterly | CISO |
| KRI-12 | Tier 1 vendors with open High or Critical assessment findings past their agreed remediation date (RSK-003) | RSK-003 | 0 | 1 | ≥ 2 | Quarterly | Head of GRC |
| KRI-13 | Tier 0 and Tier 1 Information Systems without a successful DR test within the RES-004 frequency | RES-004 | 0 | — | ≥ 1 | Quarterly | Business Continuity Manager |
| KRI-14 | Significant Deficiency, Critical Deficiency or Material Weakness findings past their remediation due date in CMP-002.5.8.2 | CMP-002 | 0 | 1–2 | ≥ 3 | Quarterly | Head of GRC |
| KRI-15 | Accounts of separated Workforce Members found active after the SEC-003 revocation timeframe | SEC-003 | 0 | 1–3 | > 3 | Monthly | CISO |
| KRI-16 | Roles in GOV-001 sections 5.4.3–5.4.5 vacant for more than 90 days | GOV-001 | 0 | 1 | ≥ 2 | Quarterly | CISO |
| KRI-17 | `[SOX]` Key Control deficiencies in Financially Significant Systems open at quarter end (CMP-009) | CMP-009 | 0 | 1 deficiency | Any Significant Deficiency or Material Weakness | Quarterly | Head of GRC |
| KRI-18 | `[PCI]` Failed or overdue ASV scans or segmentation tests (SEC-011, SEC-019) | SEC-011 | 0 | — | ≥ 1 | Quarterly | Head of Security Engineering |

- **GOV-003.5.3.3** Every percentage threshold SHALL be evaluated on the full population at period end. Band boundaries are as written: "to <" excludes the upper value. A dash (—) means the metric has no amber band and any value outside green is red.
- **GOV-003.5.3.4** The ISSC MAY add metrics to the catalogue. Every added metric SHALL meet GOV-003.5.1.1 before its first report.
- **GOV-003.5.3.5** KRI-01 SHALL be reported separately for each Risk category in RSK-001 (C1 to C9), measured against that category's tolerance in RSK-001.5.3.2, so that each category tolerance has a KRI as required by RSK-001.5.3.6.

### 5.4 Threshold breaches and escalation

- **GOV-003.5.4.1** When a KPI or KRI is red, the metric owner SHALL submit a remediation plan, with actions, owners and dates, to the CISO within 10 business days of the report in which it first appears.
- **GOV-003.5.4.2** When a KRI is red, the CISO SHALL notify the CEO within 5 business days of the value being confirmed, and the ISSC SHALL review the remediation plan at its next meeting.
- **GOV-003.5.4.3** A KRI that is red for 2 consecutive quarters, or KRI-01, KRI-06 or KRI-10 at red in any quarter, SHALL be reported to the Audit Committee as a separate agenda item at its next meeting.
- **GOV-003.5.4.4** A KPI that is amber for 3 consecutive periods SHALL be treated as red for escalation purposes.
- **GOV-003.5.4.5** Where a red KRI indicates a Risk not already in the Risk Register, the Head of GRC SHALL record the Risk under RSK-001 within 10 business days.

### 5.5 Reporting cadence

- **GOV-003.5.5.1** The CISO SHALL report operational metrics monthly to the ISSC, the KRI dashboard quarterly to the Audit Committee, and an annual program report to the Board of Directors.
- **GOV-003.5.5.2** The monthly ISSC metrics report SHALL be issued within 10 business days after month end. In months without an ISSC meeting it SHALL be circulated in writing.
- **GOV-003.5.5.3** The quarterly KRI dashboard SHALL be issued to the Audit Committee with the meeting papers for the Audit Committee meeting following quarter end.
- **GOV-003.5.5.4** The annual program report SHALL be presented to the Board of Directors within 90 days after the end of the Organization's fiscal year. [DECISION REQUIRED: Timing of the annual Board of Directors report. Recommended default: within 90 days after fiscal year end.]

### 5.6 Report content

- **GOV-003.5.6.1** The monthly ISSC report SHALL contain: every KPI and KRI with current value, status, trend over the prior 3 periods and population; red and 3-period amber items with remediation plan status; new Sev-1 and Sev-2 Security Incidents; Exceptions and Risk Acceptances granted, expired and expiring within 60 days; and overdue ISSC actions.
- **GOV-003.5.6.2** The quarterly Audit Committee KRI dashboard SHALL contain: every KRI with status and 4-quarter trend; the top 10 Residual Risks from the Risk Register with owner, level and treatment status; Critical Risk Acceptances granted in the quarter; Sev-1 Security Incidents and notifiable Personal Data Breaches; status of internal and external audit findings; progress against the REF-003 roadmap; regulatory developments recorded under CMP-001; and key security role vacancies under GOV-001.
- **GOV-003.5.6.3** The annual Board of Directors program report SHALL contain:
  1. Progress against the program objectives in ISP-000, with the status of each measured by this Policy.
  2. The Organization's information security risk profile against the Risk Appetite in RSK-001, with year-on-year comparison.
  3. A summary of Security Incidents by Severity Level, and any Material Cybersecurity Incident `[SOX]` or notifiable breach, with lessons learned.
  4. Results of the SOC 2 Type II examination and of other external assessments (for example `[PCI]` Report on Compliance, penetration tests), and the status of findings.
  5. The internal audit opinion on the program, provided by the Internal Audit Director under CMP-002.
  6. Compliance status against the Obligations Register (CMP-001), including regulatory enquiries or enforcement.
  7. Third-party risk: Critical Vendors and material vendor-related events.
  8. Threat landscape relevant to the Organization (RSK-005).
  9. Program resources, budget and staffing, and any resource shortfall that the CISO judges to raise Residual Risk above appetite.
  10. The roadmap for the next 12 months (REF-003) and decisions requested of the Board of Directors.
- **GOV-003.5.6.4** `[SOX]` The annual report and quarterly dashboards SHALL include the information management needs to support the description of cybersecurity risk management, strategy and governance required in the annual report on Form 10-K (Regulation S-K Item 106). The GC SHALL review that content before issue.
- **GOV-003.5.6.5** Every report SHALL be classified Confidential under SEC-002, and SHALL be retained with its supporting Evidence under CMP-004.
- **GOV-003.5.6.6** Reports to the Audit Committee and the Board of Directors SHALL state any metric that was reported "not measured" and any correction to a previously reported value.

### 5.7 Review of the metric catalogue

- **GOV-003.5.7.1** The CISO SHALL review the catalogue every 12 months to confirm each metric remains relevant, measurable and aligned to the Risk Register, and SHALL present the proposed changes to the ISSC.
- **GOV-003.5.7.2** A metric that has been green for 4 consecutive quarters MAY have its frequency reduced by the CISO, but not below quarterly for KRIs.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CISO | Owns this Policy and the catalogue; produces and presents all reports; escalates red KRIs |
| Head of GRC | Compiles metric values; re-performs sample calculations; records new Risks from red KRIs |
| Metric owners (as named in section 5.3) | Deliver values within 5 business days; submit remediation plans for red metrics |
| ISSC | Approves this Policy and KRI threshold changes; reviews monthly reports and remediation plans |
| Audit Committee | Receives the quarterly KRI dashboard and escalated KRIs |
| Board of Directors | Receives the annual program report |
| Internal Audit Director | Contributes the internal audit opinion; MAY audit metric accuracy |
| GC | Reviews `[SOX]` disclosure-related content |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| GOV-003.7.1 | Metrics reporting cadence | Operational metrics monthly to ISSC; KRI dashboard quarterly to Audit Committee; annual program report to Board of Directors |
| GOV-003.7.2 | Metric values delivered by owners | Within 5 business days after period end |
| GOV-003.7.3 | Monthly ISSC report issued | Within 10 business days after month end |
| GOV-003.7.4 | Annual Board of Directors report | Within 90 days after fiscal year end |
| GOV-003.7.5 | Remediation plan for a red metric | Within 10 business days of the report |
| GOV-003.7.6 | Red KRI notification to CEO | Within 5 business days of confirmation |
| GOV-003.7.7 | Escalation of red KRI to Audit Committee | 2 consecutive red quarters, or KRI-01, KRI-06 or KRI-10 red in any quarter |
| GOV-003.7.8 | Amber treated as red | 3 consecutive periods |
| GOV-003.7.9 | "Not measured" treated as red | 2 consecutive periods |
| GOV-003.7.10 | Re-performance sample per quarterly dashboard | At least 3 metrics |
| GOV-003.7.11 | KPI and KRI thresholds | As in section 5.3 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Reports issued on schedule (ISSC, Audit Committee, Board of Directors) | 100% | Quarterly | CISO |
| Catalogue metrics with a complete definition under GOV-003.5.1.1 | 100% | Every 12 months | CISO |
| Re-performed metrics matching the reported value | 100% | Quarterly | Head of GRC |
| Red metrics with a remediation plan within 10 business days | 100% | Quarterly | CISO |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003. No Exception MAY be
granted to the reporting cadence in GOV-003.5.5.1 or to the escalation rule in GOV-003.5.4.3.

## 10. Enforcement

Non-compliance is handled under CMP-007. Knowingly misstating a metric reported under this
Policy SHALL be treated as a serious breach under CMP-007 and reported to the Audit Committee.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| GOV-003.5.1 – 5.3 | 9.1 | GV.OV-03, ID.IM-01 | PM-6, CA-7 | — | CC4.1 | MEA01.01–MEA01.04 | — |
| GOV-003.5.4 | 9.1, 10.2 | GV.OV-02, GV.RM-01 | PM-6, PM-9 | — | CC4.2 | MEA01.05, APO12 | — |
| GOV-003.5.5 – 5.6 | 5.1, 9.1, 9.3 | GV.OV-01, GV.RR-01 | PM-6 | — | CC1.2, CC2.2 | EDM05, MEA01 | `[SOX]` §302, §404; Reg. S-K Item 106 |
| GOV-003.5.7 | 9.1, 10.1 | ID.IM-01 | PM-6 | — | CC4.1 | MEA01 | — |

## 12. Related documents

ISP-000, GOV-001, GOV-002, RSK-001, RSK-002, RSK-003, RSK-005, CMP-001, CMP-002, CMP-003,
CMP-004, CMP-007, CMP-009, CMP-010, SEC-001, SEC-002, SEC-003, SEC-004, SEC-005, SEC-008,
SEC-011, SEC-012, SEC-013, SEC-018, SEC-019, RES-002, RES-003, RES-004, PPL-002, REF-003

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CISO | | | |
| Approver: ISSC Vice-Chair, on behalf of the ISSC (CISO recused as Document Owner under GOV-001.5.3.9) | | | |
