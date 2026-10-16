# ISP-000 — Information Security Program Charter

## 1. Document control

| Field | Value |
|---|---|
| Document ID | ISP-000 |
| Title | Information Security Program Charter |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 0 — Charter |
| Classification | Internal |
| Owner | Chief Information Security Officer (CISO) |
| Approver | Board of Directors (via Audit Committee) |
| Effective date | [DECISION REQUIRED: Date of Board of Directors approval] |
| Next review date | Effective date + 12 months |
| Parent document | None (top of the document hierarchy) |
| Related documents | GOV-001, GOV-002, GOV-003, GOV-006, RSK-001, CMP-001, CMP-002, REF-001, REF-002, REF-003 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CISO | Initial release |

## 3. Purpose

This Charter establishes the Organization's Information Security Program. It records the
mandate given by the Board of Directors, the objectives of the program, its scope, the
authority granted to the CISO, the Organization's high-level Risk Appetite, the structure of
the policy suite, and the way the Board of Directors oversees the program.

## 4. Scope

- **People:** every Workforce Member, and every Third Party that accesses, processes or supports the Organization's Information Assets.
- **Systems and data:** every Information Asset owned, leased, operated or used by or on behalf of the Organization, in any form and at any location, including Cloud Services and Information Systems operated by Third Parties.
- **Entities and locations:** the Organization, including its subsidiaries and controlled affiliates, at every site and in every region in which it operates. [DECISION REQUIRED: Legal entities excluded from the program. Recommended default: none excluded.]
- **Regulated data:** the conditional modules listed in the suite README apply where the Organization is subject to the matching obligation, as recorded in the Obligations Register (CMP-001).
- **Assurance scope:** the SOC 2 Type II examination covers the Trust Services Criteria listed in ISP-000.5.3.3.

## 5. Policy statements

### 5.1 Mandate

- **ISP-000.5.1.1** The Board of Directors establishes the Information Security Program and directs management to operate it in accordance with this Charter and the documents of the policy suite.
- **ISP-000.5.1.2** The Board of Directors retains ultimate accountability for the Organization's information security risk. It delegates oversight of the program to the Audit Committee, which SHALL report on that oversight to the Board of Directors at least every 12 months.
- **ISP-000.5.1.3** The CEO is accountable to the Board of Directors for the operation of the program and SHALL delegate its day-to-day leadership to the CISO.
- **ISP-000.5.1.4** The CEO SHALL establish the Information Security Steering Committee (ISSC) through GOV-001. The ISSC is the management body that approves Tier 1 Policies and directs the program between Board of Directors and Audit Committee meetings.
- **ISP-000.5.1.5** Every Workforce Member SHALL comply with the documents of the policy suite that apply to them. Every Third Party SHALL comply with them to the extent required by contract under RSK-003.

### 5.2 Objectives

- **ISP-000.5.2.1** The program SHALL pursue the following objectives. Each objective is measured by the metrics named in GOV-003, and the CISO SHALL report progress against them in the annual program report required by GOV-003.

| # | Objective | Measured by (GOV-003) |
|---|---|---|
| O1 | Protect the Confidentiality, Integrity and Availability of Information Assets in proportion to their Classification Level (SEC-002) | Vulnerability, access and incident KPIs |
| O2 | Keep Residual Risk within the Risk Appetite set in RSK-001 | Risk KRIs |
| O3 | Meet every legal, regulatory and contractual information security and privacy obligation recorded in the Obligations Register (CMP-001) | Compliance KPIs; regulatory findings |
| O4 | Obtain and maintain a SOC 2 Type II examination report with no qualified opinion | Audit and control-testing KPIs |
| O5 | Restore critical processes and Information Systems within their Recovery Tier targets (RSK-004) | Resilience KPIs |
| O6 | Make every Workforce Member aware of their security responsibilities (PPL-002) | Training and phishing KPIs |

- **ISP-000.5.2.2** The ISSC SHALL review the objectives every 12 months and SHALL propose changes to the Audit Committee as part of the annual review of this Charter.

### 5.3 Scope of the program

- **ISP-000.5.3.1** The program SHALL cover governance, risk management, compliance, security controls, resilience, people security, third-party security and privacy, organized into the document series ISP, GOV, RSK, CMP, SEC, RES, PPL, TPL and REF.
- **ISP-000.5.3.2** The program SHALL be aligned with ISO/IEC 27001:2022, NIST CSF 2.0, NIST SP 800-53 Rev. 5, CIS Controls v8.1, the SOC 2 Trust Services Criteria and COBIT 2019. The Head of GRC SHALL maintain the mapping of suite requirements to these frameworks in REF-001.
- **ISP-000.5.3.3** [DECISION REQUIRED: SOC 2 Trust Services Criteria in scope. Recommended default: Security, Availability and Confidentiality; Privacy optional because CMP-005 covers GDPR and CPRA directly.] The SOC 2 Type II examination SHALL cover the Security, Availability and Confidentiality criteria.
- **ISP-000.5.3.4** Any exclusion of a legal entity, business unit, location or Information System from the program SHALL be approved by the Audit Committee and recorded in this Charter.

### 5.4 Authority of the CISO

- **ISP-000.5.4.1** The CISO is authorized to lead, direct and coordinate the program across the Organization. The CISO's reporting line is set in GOV-001.
- **ISP-000.5.4.2** The CISO SHALL have access to every Information System, record, facility and Workforce Member needed to assess or investigate information security risk, subject only to Legal Hold and to Legal Privilege as determined by the GC.
- **ISP-000.5.4.3** The CISO is authorized to direct the immediate isolation of an Information System, suspension of an account, or disconnection of a Third Party connection where the CISO judges that it poses an active threat of a Sev-1 or Sev-2 Security Incident. The CISO SHALL report each such action to the CEO and the affected Asset Owner within 24 hours.
- **ISP-000.5.4.4** The CISO is authorized to halt a Change or deployment that would introduce a Critical Risk (RSK-002) pending an ISSC decision. The ISSC SHALL decide within 5 business days of the halt.
- **ISP-000.5.4.5** The CISO is authorized to approve Tier 2 Standards and to approve Tier 3 documents and Templates as set out in the approval rule in GOV-002.
- **ISP-000.5.4.6** The CISO SHALL have the right of direct, unfiltered access to the Chair of the Audit Committee and SHALL use it whenever the CISO judges that a matter is being withheld from, or misrepresented to, the Audit Committee.
- **ISP-000.5.4.7** The CISO SHALL submit the program's annual budget and resource requirements to the CEO. Any shortfall the CISO judges to create Residual Risk above the Risk Appetite SHALL be reported to the Audit Committee.

### 5.5 Risk appetite

- **ISP-000.5.5.1** [DECISION REQUIRED: Risk Appetite stance (adopter decision #1). Recommended default: Conservative.] The Organization's Risk Appetite for information security risk is Conservative: the Organization does not knowingly retain Residual Risk above the threshold set in RSK-001 except through a Risk Acceptance granted under RSK-001.
- **ISP-000.5.5.2** The quantitative Risk Appetite, Risk Tolerances and acceptance authorities are set in RSK-001 and ratified by the Audit Committee. This Charter SHALL NOT be read to override them.
- **ISP-000.5.5.3** The Organization has no appetite for knowing non-compliance with a legal or regulatory obligation. A Risk Acceptance or Exception SHALL NOT be used to permit it.

### 5.6 Document hierarchy

- **ISP-000.5.6.1** The policy suite SHALL be organized in the following tiers. The approval rule for each tier, and its exceptions, are set in GOV-002.

| Tier | Type | Content |
|---|---|---|
| 0 | Charter | This document: what and why; Board of Directors mandate |
| 1 | Policies | What is required, one document per topic |
| 2 | Standards | Measurable technical and operational requirements supporting a Policy |
| 3 | Procedures and Plans | How requirements are carried out |
| T | Templates | Forms that record required outputs |
| Ref | Master references | Glossary, control mapping, RACI and roadmap |

- **ISP-000.5.6.2** Where two suite documents conflict, the document in the higher tier SHALL prevail. Where a suite document conflicts with applicable law, the law SHALL prevail. The Document Owner who identifies a conflict SHALL report it to the Head of GRC for resolution under GOV-002.
- **ISP-000.5.6.3** Defined terms are held only in GOV-006, and roles and accountabilities only in GOV-001 and REF-002.

### 5.7 Board oversight

- **ISP-000.5.7.1** The Audit Committee SHALL receive the CISO's reports at the cadence set in GOV-001, with the content and KRI dashboard set in GOV-003.
- **ISP-000.5.7.2** The Board of Directors SHALL receive the annual program report defined in GOV-003, including progress against the objectives in ISP-000.5.2.1 and the roadmap in REF-003.
- **ISP-000.5.7.3** The Audit Committee SHALL ratify the Risk Appetite under RSK-001 and SHALL receive notice of Critical Risk Acceptances as required by RSK-001.
- **ISP-000.5.7.4** The Audit Committee SHALL oversee independent assurance over the program through the internal audit plan under CMP-002 and SHALL receive every SOC 2 Type II examination report.
- **ISP-000.5.7.5** `[SOX]` The Audit Committee SHALL be informed of any Security Incident under assessment for materiality under RES-003, in time for disclosure decisions.
- **ISP-000.5.7.6** At least one member of the Board of Directors or the Audit Committee SHALL complete information security and cyber-risk oversight training every 12 months under PPL-002.

### 5.8 Review and continual improvement

- **ISP-000.5.8.1** The CISO SHALL review this Charter every 12 months and on any event-triggered review under GOV-002, and SHALL submit it to the Audit Committee for recommendation to the Board of Directors.
- **ISP-000.5.8.2** The ISSC SHALL conduct a management review of the program every 12 months covering the inputs required by ISO/IEC 27001:2022 clause 9.3, and SHALL record decisions and actions in its minutes.

## 6. Roles & responsibilities

| Role | Responsibility under this Charter |
|---|---|
| Board of Directors | Approves this Charter; holds ultimate accountability; receives the annual program report |
| Audit Committee | Oversees the program; recommends this Charter for approval; ratifies Risk Appetite; oversees independent assurance |
| CEO | Accountable for program operation; establishes the ISSC (GOV-001); allocates resources |
| ISSC | Directs the program; approves Policies; conducts the annual management review |
| CISO | Owns this Charter; leads the program; exercises the authority in ISP-000.5.4 |
| Head of GRC | Maintains the policy suite (GOV-002) and the control mapping (REF-001) |
| Internal Audit Director | Provides independent assurance under CMP-002 |

Accountabilities for every role are defined in GOV-001 and consolidated in REF-002.

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| ISP-000.7.1 | Review of this Charter | Every 12 months, and on event-triggered review under GOV-002 |
| ISP-000.7.2 | CISO reporting to CEO, Audit Committee and Board of Directors | Cadence in GOV-001 |
| ISP-000.7.3 | Report to CEO and Asset Owner after an emergency action under ISP-000.5.4.3 | Within 24 hours |
| ISP-000.7.4 | ISSC decision after a halt under ISP-000.5.4.4 | Within 5 business days |
| ISP-000.7.5 | Audit Committee report on oversight to the Board of Directors | At least every 12 months |
| ISP-000.7.6 | ISSC management review | Every 12 months |
| ISP-000.7.7 | Risk Appetite | Set in RSK-001 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Charter reviewed and approved within 12 months of the previous approval | Yes | Annually | CISO |
| Audit Committee meetings with a CISO report, against the GOV-001 cadence | 100% | Quarterly | CISO |
| Program objectives O1–O6 at green status (GOV-003 thresholds) | ≥ 5 of 6 | Annually | CISO |
| Emergency actions under ISP-000.5.4.3 reported within 24 hours | 100% | Quarterly | CISO |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003. No Exception MAY be
granted to ISP-000.5.1, ISP-000.5.5.3 or ISP-000.5.7; changes to these require approval of a
revised Charter by the Board of Directors.

## 10. Enforcement

Non-compliance is handled under CMP-007. Obstruction of the CISO's authority under
ISP-000.5.4 SHALL be reported by the CISO to the CEO and, where it involves the CEO, to the
Chair of the Audit Committee.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| ISP-000.5.1 | 4.4, 5.1, 5.3 | GV.OC-01, GV.RR-01 | PM-1, PM-2 | — | CC1.2, CC1.3 | EDM01, APO01 | `[HIPAA]` §164.308(a)(2); `[PCI]` 12.1.1, 12.4.1; `[SOX]` §404 |
| ISP-000.5.2 | 6.2 | GV.OC-01, GV.OV-01 | PM-6 | — | CC3.1 | APO13, MEA01 | `[GDPR]` Art. 24, 32 |
| ISP-000.5.3 | 4.1–4.3 | GV.OC-03, GV.PO-01 | PM-1 | — | CC2.2 | APO01 | — |
| ISP-000.5.4 | 5.3; A.5.2 | GV.RR-02 | PM-2 | — | CC1.3 | APO01 | `[PCI]` 12.1.3 |
| ISP-000.5.5 | 6.1.1 | GV.RM-02 | PM-9 | — | CC3.1, CC3.2 | EDM03, APO12 | — |
| ISP-000.5.6 | 5.2, 7.5; A.5.1 | GV.PO-01 | PL-1, PM-1 | — | CC5.3 | APO01 | `[PCI]` 12.1.1; `[HIPAA]` §164.316 |
| ISP-000.5.7 | 5.1, 9.3 | GV.OV-01, GV.RR-01 | PM-1 | — | CC1.2, CC4.2 | EDM01, EDM05, MEA01 | `[SOX]` §302, §404 |
| ISP-000.5.8 | 9.3, 10.1 | GV.OV-02, ID.IM-01 | PM-1 | — | CC4.1 | MEA01 | `[PCI]` 12.1.2 |

## 12. Related documents

GOV-001, GOV-002, GOV-003, GOV-006, RSK-001, RSK-002, RSK-003, RSK-004, CMP-001, CMP-002,
CMP-003, CMP-005, CMP-007, SEC-002, RES-003, PPL-002, REF-001, REF-002, REF-003

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CISO | | | |
| Recommended by: Chair of the Audit Committee | | | |
| Approver: Chair of the Board of Directors, on behalf of the Board of Directors | | | |
