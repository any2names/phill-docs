# GOV-001 — Security Governance & Organization Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | GOV-001 |
| Title | Security Governance & Organization Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Information Security Officer (CISO) |
| Approver | Chief Executive Officer (CEO) † (this document creates the ISSC) |
| Effective date | [DECISION REQUIRED: Date of CEO approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | ISP-000, GOV-002, GOV-003, GOV-006, RSK-001, CMP-002, CMP-005, CMP-008, CMP-009, REF-002 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CISO | Initial release |

## 3. Purpose

This Policy establishes the organizational structure of the Information Security Program
created by ISP-000. It charters the Information Security Steering Committee (ISSC), sets the
CISO's reporting line, defines the accountabilities of every canonical role used in the policy
suite, designates the statutory officers required by HIPAA and GDPR, and sets the Segregation
of Duties rules that apply across the Organization.

## 4. Scope

- **People:** every individual who holds a role named in section 5.4, every Workforce Member, and every Third Party acting under the Organization's direction.
- **Systems and data:** every Information System and process where a duty in the conflicting-duties matrix (section 5.7) is performed.
- **Locations:** all Organization sites and regions in the scope of ISP-000.
- **Third parties:** Third Parties that perform a role or duty named in this Policy on the Organization's behalf (for example an outsourced DPO or managed SOC), bound through contract under RSK-003.

## 5. Policy statements

### 5.1 Governance structure

- **GOV-001.5.1.1** The Organization's information security governance structure SHALL consist of, in order of authority: the Board of Directors, the Audit Committee, the CEO, the ISSC and the CISO, supported by the executives, statutory officers and functional leads defined in section 5.4.
- **GOV-001.5.1.2** Every role in section 5.4 that applies to the Organization SHALL be assigned to a named individual. The Head of GRC SHALL maintain a Role-assignment Register recording the role, the named holder, the named deputy, the date of appointment and any role combination approved under section 5.8.
- **GOV-001.5.1.3** The Role-assignment Register SHALL be updated within 10 business days of any change of holder and SHALL be reviewed by the ISSC every 12 months.
- **GOV-001.5.1.4** Every executive and functional-lead role in section 5.4 SHALL have a named deputy who can exercise its accountabilities in this suite during an absence longer than 5 business days. The deputy SHALL NOT be a person whose duties conflict under section 5.7.
- **GOV-001.5.1.5** Every Asset Owner, Data Owner and System Owner SHALL be recorded in the Asset Inventory under SEC-001.

### 5.2 CISO appointment and reporting line

- **GOV-001.5.2.1** [DECISION REQUIRED: CISO reporting line (adopter decision #6). Recommended default: reports to the CEO, for independence from IT operations.] The CISO SHALL report to the CEO.
- **GOV-001.5.2.2** The CISO SHALL report to the Audit Committee at least quarterly and to the Board of Directors at least annually. Report content is set in GOV-003.
- **GOV-001.5.2.3** The CISO SHALL NOT report to the CIO, the CTO or any other role accountable for operating the Information Systems the CISO oversees.
- **GOV-001.5.2.4** The CEO SHALL appoint and remove the CISO. The CEO SHALL notify the Chair of the Audit Committee of any appointment or removal of the CISO within 10 business days, stating the reason for a removal.
- **GOV-001.5.2.5** The CISO SHALL hold, or obtain within 12 months of appointment, at least one recognized information security management certification. [DECISION REQUIRED: Accepted certifications. Recommended default: CISSP, CISM or an equivalent approved by the CEO.]

### 5.3 Information Security Steering Committee (ISSC) charter

- **GOV-001.5.3.1** The CEO establishes the ISSC by approval of this Policy. The ISSC directs the Information Security Program, approves Tier 1 Policies, and exercises the risk and exception authorities assigned to it in RSK-001 and CMP-003.
- **GOV-001.5.3.2** The ISSC SHALL have the following composition:

| Position | Role |
|---|---|
| Chair | CISO |
| Voting members | CIO, CTO, CPO, GC, CFO, CHRO, Head of GRC |
| Non-voting members | Internal Audit Director, DPO, HIPAA Security Officer |
| Secretary (non-member) | A Workforce Member in the GRC function, appointed by the Head of GRC |

- **GOV-001.5.3.3** [DECISION REQUIRED: ISSC Vice-Chair. Recommended default: the GC.] The GC SHALL serve as Vice-Chair. The Vice-Chair presides whenever the Chair is absent or recused under GOV-001.5.3.9.
- **GOV-001.5.3.4** Quorum SHALL be a majority of voting members, including the Chair or the Chair's delegate. A meeting without quorum MAY discuss but SHALL NOT decide.
- **GOV-001.5.3.5** The ISSC SHALL meet at least quarterly. The Chair SHALL convene an extraordinary meeting within 5 business days of the declaration of a Sev-1 Security Incident (RES-002).
- **GOV-001.5.3.6** Decisions SHALL be taken by a simple majority of voting members present. The Chair holds a casting vote only, used to break a tie.
- **GOV-001.5.3.7** A voting member MAY appoint a delegate who reports directly to them. A delegate SHALL hold the member's vote. A member SHALL NOT be represented by a delegate at more than 2 consecutive meetings.
- **GOV-001.5.3.8** Between meetings, the Chair MAY put a decision to written resolution. A written resolution passes when a majority of all voting members approve it in writing within 10 business days of circulation, and SHALL be recorded in the minutes of the next meeting.
- **GOV-001.5.3.9** A member SHALL NOT vote on, and SHALL NOT preside over, a decision on a document they own, an Exception they requested, or a Risk Acceptance for a Risk they own. Recused members SHALL be excluded from the quorum count for that item.
- **GOV-001.5.3.10** The ISSC SHALL, at a minimum: approve Tier 1 Policies under GOV-002; review the Risk Register quarterly under RSK-001; decide High-level Risk Acceptances and Exceptions under RSK-001 and CMP-003; review the operational metrics required by GOV-003; approve the roadmap in REF-003; conduct the annual management review required by ISP-000; and review the Role-assignment Register every 12 months.
- **GOV-001.5.3.11** The Secretary SHALL circulate the agenda and papers at least 5 business days before a scheduled meeting and draft minutes within 10 business days after it. Minutes SHALL record attendance, quorum, recusals, decisions, votes and actions with owners and due dates, and SHALL be approved at the next meeting.
- **GOV-001.5.3.12** ISSC minutes and papers SHALL be classified at least Confidential under SEC-002 and retained under CMP-004.
- **GOV-001.5.3.13** The ISSC SHALL review this charter (section 5.3) every 12 months and recommend changes to the CEO.

### 5.4 Role definitions and accountabilities

- **GOV-001.5.4.1** Each role in the tables below SHALL carry the accountabilities stated for it. Activity-level assignments across all suite documents are consolidated in REF-002; where REF-002 and this section conflict, this section prevails and the Head of GRC SHALL correct REF-002 within 10 business days.

#### 5.4.2 Governance bodies

| Role | Accountabilities |
|---|---|
| Board of Directors | Ultimate accountability for information security risk; approves ISP-000; receives the annual program report (GOV-003). |
| Audit Committee | Oversight of the program on behalf of the Board of Directors; ratifies Risk Appetite (RSK-001); approves CMP-002 and CMP-006; directs the Internal Audit Director; receives the CISO's quarterly report and KRI dashboard; receives notice of Critical Risk Acceptances. |
| CEO | Accountable for operating the program; approves this Policy; appoints the CISO; accepts Critical Risks (RSK-001); approves role combinations (section 5.8); designates the statutory officers (section 5.5). |
| ISSC | Directs the program between Audit Committee meetings; approves Tier 1 Policies; decides High-level Risk Acceptances and Exceptions; conducts management review (section 5.3). |

#### 5.4.3 Executives

| Role | Accountabilities |
|---|---|
| CFO | Accountable for internal control over financial reporting; approves CMP-009 `[SOX]`; owns the business case for program budget within the financial plan; Risk Owner for financial-process Risks. |
| CIO | Accountable for the secure operation of corporate Information Systems; owns SEC-001, SEC-008, SEC-013, SEC-014, SEC-017, SEC-018 and RES-005; implements security requirements in IT operations. |
| CTO | Accountable for the security of products, engineering platforms and production Cloud Services; owns SEC-009 and SEC-010. |
| CISO | Leads the program under ISP-000; chairs the ISSC; approves Tier 2 Standards; accepts Medium Risks (RSK-001); owns the documents assigned in the README; reports to the Audit Committee and Board of Directors (section 5.2). |
| CPO | Accountable for the privacy program; owns CMP-005 and RES-003; approves CMP-010, TPL-005 and TPL-010 `[GDPR]` `[CPRA]`. |
| GC | Accountable for legal advice on information security and privacy obligations; owns CMP-006; issues Legal Holds; concurs on CMP-004 and RES-003; determines Legal Privilege in investigations. |
| CHRO | Accountable for workforce lifecycle security; owns PPL-001 and CMP-007; triggers joiner, mover and leaver events relied on by SEC-003. |

#### 5.4.4 Statutory designations

| Role | Accountabilities |
|---|---|
| Data Protection Officer (DPO) `[GDPR]` | Performs the tasks in GDPR Art. 39 under the independence safeguards in section 5.5; owns CMP-010, TPL-005 and TPL-010; acts as contact point for supervisory authorities and Data Subjects. |
| HIPAA Security Officer `[HIPAA]` | The security official required by 45 CFR §164.308(a)(2); owns CMP-008; accountable for the development and implementation of HIPAA Security Rule policies and procedures. |
| HIPAA Privacy Officer `[HIPAA]` | The privacy official required by 45 CFR §164.530(a)(1); accountable for HIPAA Privacy Rule policies, complaints and individual rights relating to PHI; coordinates with the HIPAA Security Officer on ePHI matters. |

#### 5.4.5 Functional leads

| Role | Accountabilities |
|---|---|
| Head of GRC | Maintains the policy suite (GOV-002), GOV-006, REF-001 and REF-002; runs the risk (RSK-001, RSK-002), third-party (RSK-003), compliance (CMP-001), exception (CMP-003) and evidence (CMP-004) processes; maintains the Role-assignment Register. |
| Head of Security Engineering | Designs and operates technical security controls; owns SEC-004, SEC-005, SEC-006, SEC-007, SEC-011, SEC-019 and TPL-008. |
| SOC Manager | Operates security monitoring and incident handling; owns SEC-012, RSK-005, RES-002, TPL-006 and TPL-007. |
| Internal Audit Director | Provides independent assurance over the program; owns CMP-002; reports functionally to the Audit Committee and administratively to the CEO or CFO; holds no operational responsibility for any Control. |
| Business Continuity Manager | Runs business continuity and the BIA; owns RSK-004 and RES-004; approves RES-005. |
| Head of Facilities | Accountable for physical and environmental security of Organization sites; owns SEC-016. |
| Head of Procurement | Ensures every Third Party engagement passes the security due diligence and contract requirements of RSK-003 before signature; maintains the supplier master record. |

#### 5.4.6 Generic roles

| Role | Accountabilities |
|---|---|
| Asset Owner | Accountable for an Information Asset's classification, authorized use, protection and lifecycle; approves access; acts as Risk Owner for Risks to the asset unless the Risk Register names another. |
| Data Owner | Accountable for a defined data set's classification (SEC-002), permitted uses, access approvals and retention (CMP-004). |
| System Owner | Accountable for an Information System's operation, security configuration, Change (SEC-013), Vulnerability remediation (SEC-011) and Access Reviews (SEC-003). |
| Data Custodian | Operates the technical Controls protecting an Information Asset as directed by the Asset Owner or Data Owner; holds no authority to approve access to it. |
| Workforce Member | Complies with GOV-004 and every suite document that applies to their role; completes training (PPL-002) and attestations (GOV-002); reports Security Incidents (RES-001) and concerns (CMP-006). |
| Third Party | Complies with the security obligations in its contract under RSK-003, including suite documents incorporated by reference. |

- **GOV-001.5.4.7** Every Workforce Member job description for a role in sections 5.4.2–5.4.5 SHALL list that role's accountabilities. The CHRO SHALL confirm this at appointment.
- **GOV-001.5.4.8** Information security responsibilities SHALL be included in the objectives of every executive and functional lead in section 5.4.3 and 5.4.5, and assessed in their annual performance review.

### 5.5 Statutory officer designations

- **GOV-001.5.5.1** `[HIPAA]` [DECISION REQUIRED: HIPAA Security Officer designation (adopter decision #5). Recommended default: the CISO; approval of CMP-008 then moves to the ISSC.] The CEO SHALL designate the CISO as HIPAA Security Officer in writing. The designation SHALL be recorded in the Role-assignment Register and retained under CMP-004.
- **GOV-001.5.5.2** `[HIPAA]` The CEO SHALL designate a HIPAA Privacy Officer in writing. [DECISION REQUIRED: HIPAA Privacy Officer designation. Recommended default: the CPO.] The CPO SHALL be designated HIPAA Privacy Officer.
- **GOV-001.5.5.3** `[HIPAA]` The HIPAA Security Officer and HIPAA Privacy Officer MAY be the same individual; the combination SHALL be recorded in the Role-assignment Register. Where they are different individuals, they SHALL meet at least quarterly to coordinate on ePHI matters.
- **GOV-001.5.5.4** `[GDPR]` [DECISION REQUIRED: DPO appointment (adopter decision #8). Recommended default: appoint a DPO where GDPR Art. 37(1) applies, for example large-scale processing of special-category data or large-scale systematic monitoring.] The CEO SHALL appoint a DPO where GDPR Art. 37(1) applies, and SHALL record in the Role-assignment Register the assessment of Art. 37(1) applicability, reviewed every 12 months by the GC.
- **GOV-001.5.5.5** `[GDPR]` The DPO MAY be a Workforce Member or a Third Party under a service contract (GDPR Art. 37(6)). The DPO SHALL be appointed on the basis of professional qualities and expert knowledge of data protection law and practice (Art. 37(5)).
- **GOV-001.5.5.6** `[GDPR]` The CPO SHALL publish the DPO's contact details and communicate them to each competent Supervisory Authority within 30 days of appointment or change (Art. 37(7)).
- **GOV-001.5.5.7** `[PCI]` Service provider: the CISO SHALL be the executive accountable for the protection of CHD and for the PCI DSS compliance program (PCI DSS 12.4.1). The designation SHALL be recorded in the Role-assignment Register; the program charter and its content are set in SEC-019.5.10.7.

### 5.6 DPO independence `[GDPR]`

- **GOV-001.5.6.1** `[GDPR]` The DPO SHALL report directly to the CEO, as the highest management level, and SHALL have a right of direct access to the Audit Committee (Art. 38(3)). The DPO SHALL report to the Audit Committee at least every 12 months.
- **GOV-001.5.6.2** `[GDPR]` The DPO SHALL NOT receive instructions regarding the exercise of the tasks in Art. 39 (Art. 38(3)). No Workforce Member SHALL direct the DPO's conclusions or advice.
- **GOV-001.5.6.3** `[GDPR]` The DPO SHALL NOT be dismissed or penalized for performing the DPO's tasks (Art. 38(3)). Any proposal to dismiss, demote or change the terms of the DPO SHALL be notified to the Chair of the Audit Committee before it takes effect.
- **GOV-001.5.6.4** `[GDPR]` The DPO SHALL NOT hold any position in which the DPO determines the purposes and means of processing Personal Data (Art. 38(6)). The DPO SHALL NOT be the CEO, CFO, CIO, CTO, CISO, CPO, GC, CHRO, Head of Security Engineering, or a head of a marketing, sales or product function.
- **GOV-001.5.6.5** `[GDPR]` The DPO SHALL be involved in all issues relating to the protection of Personal Data (Art. 38(1)). At a minimum, the DPO SHALL be consulted before approval of every DPIA (TPL-005), before every ISSC decision affecting Personal Data, and within 24 hours of the escalation of a suspected Personal Data Breach under RES-003.
- **GOV-001.5.6.6** `[GDPR]` The CEO SHALL provide the DPO with the resources, access to Personal Data and processing operations, and training necessary to maintain expert knowledge (Art. 38(2)). The DPO SHALL submit an annual resource statement to the CEO, and the CEO SHALL record the response.
- **GOV-001.5.6.7** `[GDPR]` The DPO SHALL be bound by secrecy or confidentiality concerning the performance of the DPO's tasks (Art. 38(5)). Data Subjects MAY contact the DPO directly (Art. 38(4)).
- **GOV-001.5.6.8** `[GDPR]` Where the DPO's advice is not followed, the decision-maker SHALL record the reasons in writing and the record SHALL be retained under CMP-004.

### 5.7 Segregation of Duties

- **GOV-001.5.7.1** No individual SHALL perform both duties of any pair listed in the conflicting-duties matrix below for the same Information Asset, transaction, document or Risk, except under an approved compensating control listed in the matrix.
- **GOV-001.5.7.2** Conflicting-duties matrix:

| ID | Duty A | Duty B | Rule | Permitted compensating control |
|---|---|---|---|---|
| SOD-01 | Own a suite document | Approve the same document | Prohibited (owner ≠ approver) | None; approval passes to the next level under GOV-002 |
| SOD-02 | Request access for oneself | Approve that access | Prohibited | None |
| SOD-03 | Administer accounts on a system | Review access on that system (SEC-003) | Prohibited | Independent second reviewer signs the Access Review |
| SOD-04 | Hold Privileged Account on a system | Review privileged activity logs for that system (SEC-012) | Prohibited | Logs reviewed by the SOC; administrator has no write access to logs |
| SOD-05 | Develop or author a Change | Approve the same Change (SEC-013) | Prohibited | Peer review by another qualified Workforce Member, recorded in the change record |
| SOD-06 | Develop code | Deploy it to production without independent review (SEC-010) | Prohibited | Automated pipeline with enforced peer review; direct production write access removed |
| SOD-07 | Operate a Control | Test that Control for assurance (CMP-002) | Prohibited | None for Key Controls; for other Controls, re-performance by the Head of GRC |
| SOD-08 | Request an Exception | Approve the same Exception (CMP-003) | Prohibited | None; approval passes to the next authority |
| SOD-09 | Own a Risk | Accept the same Risk above Low (RSK-001) | Prohibited | None; acceptance passes to the next authority |
| SOD-10 | Hold one component of a split cryptographic key | Hold another component of the same key (SEC-006) | Prohibited | None |
| SOD-11 | Select or manage a Third Party | Perform its security assessment (RSK-003) | Prohibited | Assessment reviewed and signed by the Head of GRC |
| SOD-12 | `[SOX]` Create or change vendor or payee master data | Approve payments to that vendor or payee | Prohibited | None in Financially Significant Systems |
| SOD-13 | `[SOX]` Post journal entries | Approve the same journal entries | Prohibited | None in Financially Significant Systems |
| SOD-14 | Investigate a Security Incident | Be the subject of, or have a personal interest in, the same incident (RES-002) | Prohibited | Reassignment by the SOC Manager or CISO |
| SOD-15 | Perform any operational, Control-owning or management role | Hold the Internal Audit Director role or perform internal audit (CMP-002) | Prohibited | None |
| SOD-16 | `[GDPR]` Determine purposes and means of processing | Act as DPO | Prohibited (section 5.6) | None |
| SOD-17 | Perform a Backup or restore | Sign off the restore test result (SEC-018) | Prohibited | Test result verified by the System Owner |
| SOD-18 | Grant or administer security tool configuration (e.g. SIEM, EDR) | Disable or suppress alerts from that tool without second approval | Prohibited | Suppression rules require SOC Manager approval in the tool |

- **GOV-001.5.7.3** Each System Owner SHALL identify the SoD conflicts that apply within their Information System and SHALL enforce them through system roles where the system supports it. `[SOX]` For Financially Significant Systems, SoD rule sets SHALL be documented under CMP-009.
- **GOV-001.5.7.4** Where a conflicting combination is detected during an Access Review (SEC-003), the System Owner SHALL remove one of the conflicting entitlements or obtain an Exception under CMP-003 within the access-change timeframe in SEC-003.
- **GOV-001.5.7.5** A compensating control SHALL be used only where it is listed in the matrix, or where an Exception has been approved under CMP-003, and its operation SHALL be evidenced under CMP-004.

### 5.8 Role combinations for smaller adopters

- **GOV-001.5.8.1** An individual MAY hold more than one role in section 5.4 only where the combination is listed as Permitted in the table below, or is approved by the CEO as an Exception under CMP-003 with Audit Committee notification. Every combination SHALL be recorded in the Role-assignment Register.
- **GOV-001.5.8.2** Where a combination makes one individual both Document Owner and approver of a document, approval SHALL pass to the ISSC; where the ISSC is already the approver, the individual SHALL recuse under GOV-001.5.3.9.
- **GOV-001.5.8.3** Combination table:

| Combination | Status | Conditions |
|---|---|---|
| CISO + HIPAA Security Officer | Permitted (recommended default) | CMP-008 approval moves to the ISSC |
| CPO + HIPAA Privacy Officer | Permitted (recommended default) | — |
| CIO + CTO | Permitted | Documents owned by both roles remain approved by the ISSC |
| Head of GRC + Business Continuity Manager | Permitted | — |
| Head of Security Engineering + SOC Manager | Permitted | SOD-04 compensating control required; SEC-012 and RES-002 approval unaffected |
| CPO + GC | Permitted | RES-003 concurrence given by a GC deputy |
| Head of Facilities + Head of Procurement | Permitted | — |
| CHRO + any role other than CISO, DPO or Internal Audit Director | Permitted | CMP-007 decisions about the CHRO's own function referred to the GC |
| CISO + Head of GRC | Prohibited | Removes independent challenge of risk and compliance; breaches SOD-01 for TPL-series and RSK-002 |
| CISO + CIO, CTO or Head of Security Engineering | Prohibited | Breaches GOV-001.5.2.3 and SOD-07 |
| CISO + SOC Manager | Permitted only below 250 Workforce Members | RES-002, TPL-006 and TPL-007 approval passes to the ISSC; SOD-04 compensating control required |
| Internal Audit Director + any other role | Prohibited | SOD-15; internal audit MAY be outsourced to a Third Party under CMP-002 |
| DPO + any role in GOV-001.5.6.4 | Prohibited | SOD-16 |
| CFO + Head of GRC | Prohibited | Breaches SOD-01 for CMP-009 `[SOX]` |

- **GOV-001.5.8.4** The ISSC SHALL review every role combination every 12 months and when the Organization's Workforce grows by more than 25% from the date the combination was approved.

### 5.9 Competence and resourcing

- **GOV-001.5.9.1** The CISO SHALL maintain a security function staffing plan, reviewed by the ISSC every 12 months, that identifies the roles required to operate the controls in the suite and any vacancies.
- **GOV-001.5.9.2** A vacancy in any role in section 5.4.3–5.4.5 lasting more than 90 days SHALL be reported by the CISO to the Audit Committee in the next quarterly report, with the interim arrangement.
- **GOV-001.5.9.3** Holders of roles in sections 5.4.3–5.4.5 SHALL complete the role-based training defined in PPL-002.

### 5.10 Contact with authorities and special interest groups

- **GOV-001.5.10.1** The GC SHALL maintain a register of contacts with regulators, supervisory authorities, law enforcement and payment brands, reviewed every 12 months. Only the GC, the CPO, the DPO or a person they authorize in writing SHALL communicate with these authorities on information security or privacy matters.
- **GOV-001.5.10.2** The CISO SHALL maintain membership of at least one information-sharing and analysis organization or professional security community relevant to the Organization's sector, and SHALL designate who participates.

### 5.11 Security in project management

- **GOV-001.5.11.1** Every project that introduces or materially changes an Information System, a Third Party processing Confidential or Restricted data, or a processing activity involving Personal Data SHALL include an information security risk assessment under RSK-002 before the project passes its design approval gate.
- **GOV-001.5.11.2** The project sponsor SHALL record the assessment outcome and the CISO's sign-off (or the sign-off of the CISO's delegate) in the project record.

## 6. Roles & responsibilities

| Role | Responsibility under this Policy |
|---|---|
| CEO | Approves this Policy; appoints the CISO and statutory officers; approves role combinations by Exception |
| CISO | Owns this Policy; chairs the ISSC; maintains the staffing plan; signs off project risk assessments |
| ISSC | Operates under the charter in section 5.3; reviews role assignments and combinations |
| GC | Vice-Chair of the ISSC; reviews DPO applicability; maintains the authorities contact register |
| Head of GRC | Maintains the Role-assignment Register and REF-002 |
| CHRO | Confirms role accountabilities in job descriptions and performance objectives |
| System Owners | Identify and enforce SoD conflicts in their Information Systems |
| DPO | Exercises GDPR Art. 39 tasks independently; reports to the CEO and Audit Committee |
| Internal Audit Director | Tests SoD controls under CMP-002 |

### 6.1 Summary RACI for program-level activities

R = Responsible, A = Accountable, C = Consulted, I = Informed. The master RACI for all
suite activities is REF-002.

| Activity | Board | Audit Comm. | CEO | ISSC | CISO | Head of GRC | CIO / CTO | CPO / DPO | GC | CHRO | Internal Audit Dir. |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Approve ISP-000 | A | R | C | C | R | C | I | I | C | I | I |
| Ratify Risk Appetite (RSK-001) | I | A | R | R | R | R | I | I | C | I | I |
| Approve Tier 1 Policies (GOV-002) | — | I | I | A | C | R | C | C | C | C | I |
| Approve Tier 2 Standards (see note 2) | — | — | — | I | A | R | C | C | I | — | I |
| Maintain the policy suite | — | — | — | I | A | R | C | C | C | C | I |
| Enterprise risk assessment (RSK-002) | — | I | I | C | A | R | C | C | C | C | I |
| Accept Critical Risk (RSK-001) | — | I | A | C | R | R | C | C | C | — | I |
| Approve Exceptions (CMP-003), Critical residual risk | — | I | A | C | C | R | C | C | C | — | — |
| Approve Exceptions (CMP-003), High residual risk | — | I | — | A | C | R | C | C | C | — | — |
| Approve Exceptions (CMP-003), Medium residual risk | — | I | — | C | A | R | C | C | C | — | — |
| Approve Exceptions (CMP-003), Low residual risk (see note 3) | — | — | — | — | C | R | C | — | — | — | — |
| Sev-1 Security Incident response (RES-002) (see note 1) | I | I | I | I | A | C | C / I | C | C | C | — |
| Breach notification decision (RES-003) | I | I | C | I | C | — | C | A | R | — | — |
| Security awareness and training (PPL-002) | — | — | I | C | A/R | C | C | C | — | C | — |
| Internal audit of the program (CMP-002) | — | A | I | I | C | C | C | C | — | — | R |
| Metrics and Board reporting (GOV-003) | I | I | I | C | A | R | C | C | — | — | I |
| Obligations Register (CMP-001) | — | I | — | I | C | A | — | C | R | — | I |
| Third-party risk management (RSK-003) | — | — | — | I | A | R | C | C | C | — | I |
| SOX ITGC scope and assertion `[SOX]` (CMP-009) | — | I | C | I | C | R | C | — | C | — | C |

The CFO is Accountable for SOX ITGC scope and assertion under CMP-009 and is omitted from
the columns above for width; REF-002 shows the full assignment.

Notes:

1. Sev-1 response: the SOC Manager and the Incident Commander are Responsible under RES-002 and are omitted from the columns above for width. In the CIO / CTO column, the CIO is Consulted and the CTO is Informed.
2. Tier 2 Standards are approved by the CISO except CMP-009, which is approved by the CFO (SOX §404), and CMP-008, which is approved by the ISSC where the CISO is the HIPAA Security Officer (README ‡).
3. Low residual risk Exceptions are approved (A) by the Risk Owner under CMP-003.5.4.3 and RSK-001; the Risk Owner is omitted from the columns above for width.

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| GOV-001.7.1 | ISSC composition | Chair: CISO. Voting: CIO, CTO, CPO, GC, CFO, CHRO, Head of GRC. Non-voting: Internal Audit Director, DPO, HIPAA Security Officer |
| GOV-001.7.2 | ISSC quorum | Quorum = majority of voting members incl. Chair or delegate |
| GOV-001.7.3 | ISSC cadence | Meets at least quarterly; extraordinary meeting within 5 business days of a Sev-1 incident |
| GOV-001.7.4 | CISO reporting line | Reports to the CEO; reports to the Audit Committee at least quarterly; reports to the Board of Directors at least annually |
| GOV-001.7.5 | ISSC papers circulated before meeting | At least 5 business days |
| GOV-001.7.6 | ISSC draft minutes circulated | Within 10 business days |
| GOV-001.7.7 | Written resolution response window | 10 business days |
| GOV-001.7.8 | Maximum consecutive meetings by delegate | 2 |
| GOV-001.7.9 | Role-assignment Register update after change of holder | Within 10 business days |
| GOV-001.7.10 | Notice to Audit Committee Chair of CISO appointment or removal | Within 10 business days |
| GOV-001.7.11 | CISO certification | Held or obtained within 12 months of appointment |
| GOV-001.7.12 | `[GDPR]` DPO contact details published and notified to Supervisory Authority | Within 30 days of appointment or change |
| GOV-001.7.13 | `[GDPR]` DPO consulted on suspected Personal Data Breach | Within 24 hours of escalation under RES-003 |
| GOV-001.7.14 | Role-combination review | Every 12 months, and on Workforce growth > 25% |
| GOV-001.7.15 | Key security role vacancy reported to Audit Committee | Vacancy > 90 days |
| GOV-001.7.16 | Deputy coverage | Absence > 5 business days |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| ISSC meetings held against required cadence, with quorum | 100% | Quarterly | CISO |
| Roles in section 5.4 with a named holder and deputy in the register | 100% | Quarterly | Head of GRC |
| SoD conflicts found in Access Reviews and not resolved within the SEC-003 timeframe | 0 | Quarterly | Head of GRC |
| Role combinations in force without a register entry or approval | 0 | Every 12 months | Head of GRC |
| ISSC actions overdue by more than 30 days | 0 | Quarterly | CISO |
| `[GDPR]` DPIAs approved without recorded DPO consultation | 0 | Quarterly | DPO |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003. No Exception MAY be
granted to SOD-01, SOD-02, SOD-08, SOD-09, SOD-15 or SOD-16, to GOV-001.5.2.3, or to the DPO
independence requirements in section 5.6. Exceptions to section 5.8 are approved by the CEO
with notification to the Audit Committee.

## 10. Enforcement

Non-compliance is handled under CMP-007. Retaliation against the DPO, the CISO or the Internal
Audit Director for the performance of their duties SHALL be reported to the Audit Committee
and handled under CMP-006.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| GOV-001.5.1 – 5.2 | 5.1, 5.3; A.5.2, A.5.4 | GV.RR-01, GV.RR-02 | PM-2, PM-29 | — | CC1.2, CC1.3 | EDM01, APO01 | `[PCI]` 12.1.3, 12.1.4; `[SOX]` §404 |
| GOV-001.5.3 | 5.1, 9.3 | GV.RR-01, GV.OV-01 | PM-1 | — | CC1.2, CC2.2 | EDM01, APO01 | — |
| GOV-001.5.4 | 5.3; A.5.2 | GV.RR-02 | PM-2, PS-9 | — | CC1.3, CC1.5 | APO01, APO07 | `[PCI]` 12.1.3 |
| GOV-001.5.5 | 5.3; A.5.2, A.5.34 | GV.RR-02 | PM-2 | — | CC1.3 | APO01 | `[HIPAA]` §164.308(a)(2), §164.530(a)(1); `[GDPR]` Art. 37 |
| GOV-001.5.6 | A.5.34 | GV.RR-02 | PT-1 | — | CC1.3 | APO01 | `[GDPR]` Art. 38, 39 |
| GOV-001.5.7 | A.5.3 | GV.RR-02 | AC-5, AC-6 | 6.8 | CC5.1, CC6.3 | DSS05, DSS06 | `[PCI]` 6.5.4, 7.2; `[SOX]` §404 |
| GOV-001.5.8 | 5.3; A.5.3 | GV.RR-02 | AC-5 | — | CC1.3 | APO01 | — |
| GOV-001.5.9 | 7.1, 7.2 | GV.RR-03 | PM-3, PM-13 | — | CC1.4 | APO07 | — |
| GOV-001.5.10 | A.5.5, A.5.6 | GV.OC-02, ID.RA-02 | IR-6, PM-15 | — | CC2.3 | APO08 | — |
| GOV-001.5.11 | A.5.8 | GV.RM-03 | SA-3, PL-2 | — | CC3.4 | BAI01 | — |

## 12. Related documents

ISP-000, GOV-002, GOV-003, GOV-006, RSK-001, RSK-002, RSK-003, CMP-002, CMP-003, CMP-004,
CMP-005, CMP-006, CMP-007, CMP-008, CMP-009, SEC-001, SEC-003, SEC-010, SEC-012, SEC-013,
SEC-018, RES-002, RES-003, PPL-002, REF-002

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CISO | | | |
| Approver: CEO | | | |
