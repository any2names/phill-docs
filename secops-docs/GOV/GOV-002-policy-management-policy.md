# GOV-002 — Policy Management Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | GOV-002 |
| Title | Policy Management Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Head of GRC |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | ISP-000, GOV-001, GOV-006, CMP-003, CMP-004, CMP-007, PPL-001, PPL-002, TPL-009, REF-001, REF-002 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Head of GRC | Initial release |

## 3. Purpose

This Policy governs the full lifecycle of every document in the Organization's Information
Security & GRC Policy Suite: drafting, numbering, approval, publication, workforce attestation,
review, version control and retirement. It ensures that each requirement has one owner and one
home, that every document is current and approved by the right authority, and that every
Workforce Member has acknowledged the documents that apply to them.

## 4. Scope

- **Documents:** every document in the ISP, GOV, RSK, CMP, SEC, RES, PPL, TPL and REF series, and every subordinate procedure, work instruction or guideline that implements a suite document.
- **People:** every Document Owner and approver; every Workforce Member required to attest under section 5.9; the Head of GRC and GRC function.
- **Systems:** the policy repository, the attestation tracking system and any Information System used to draft, approve or publish suite documents.
- **Locations:** all Organization sites and regions in the scope of ISP-000.
- **Third parties:** Third Parties required by contract (RSK-003) to acknowledge suite documents.

## 5. Policy statements

### 5.1 Document hierarchy and approval rule

- **GOV-002.5.1.1** Every suite document SHALL belong to one tier and SHALL be approved by the authority set for that tier below, unless the suite README lists a different approver for that document.

| Tier | Type | Approver |
|---|---|---|
| 0 | Charter | Board of Directors (via Audit Committee) |
| 1 | Policies | ISSC |
| 2 | Standards | CISO |
| 3 | Procedures and Plans | Owner of the parent document; the CISO if that is the same role as the Document Owner |
| T | Templates | Owner of the parent document; the CISO if that is the same role as the Document Owner |
| Ref | Master references | As listed in the suite README |

- **GOV-002.5.1.2** A document's owner SHALL NOT be its approver. Where a role combination under GOV-001 would make one individual both, approval SHALL pass to the ISSC; where the ISSC is the approver, the individual SHALL recuse under GOV-001.
- **GOV-002.5.1.3** Exceptions to the tier approval rule SHALL be limited to those marked † in the suite README, where a regulation or governance independence requires a specific approver (for example GOV-001, CMP-002, CMP-006 and CMP-009). The Head of GRC SHALL record the justification for each † exception in the suite register.
- **GOV-002.5.1.4** `[HIPAA]` Where the CISO is designated HIPAA Security Officer under GOV-001, the approver of CMP-008 SHALL be the ISSC (‡ in the suite README).
- **GOV-002.5.1.5** Where an approver is a body (Board of Directors, Audit Committee, ISSC), approval SHALL be recorded in that body's minutes or written resolution, and the approval table of the document SHALL be signed by the body's chair or, where the chair is recused, by the presiding member.
- **GOV-002.5.1.6** A requirement in a lower-tier document SHALL NOT weaken a requirement in its parent document. Where a conflict is found, the higher-tier document prevails (ISP-000) and the Head of GRC SHALL open a revision of the lower-tier document within 10 business days.

### 5.2 Numbering and naming

- **GOV-002.5.2.1** Every suite document SHALL have a unique identifier in the form `<PREFIX>-<NNN>`, using the following prefixes:

| Prefix | Series |
|---|---|
| ISP | Information Security Program (Charter) |
| GOV | Governance |
| RSK | Risk |
| CMP | Compliance |
| SEC | Security controls |
| RES | Resilience and response |
| PPL | People |
| TPL | Templates |
| REF | Master references |

- **GOV-002.5.2.2** The Head of GRC SHALL assign new identifiers as the next unused number in the series. Identifiers SHALL NOT be reassigned to a different topic.
- **GOV-002.5.2.3** A retired identifier SHALL NOT be reused for any other document. The Head of GRC SHALL keep retired identifiers in the suite register with their retirement date and successor document, if any.
- **GOV-002.5.2.4** Requirements SHALL be numbered `<DOC-ID>.<section>.<subsection>.<item>` (for example `SEC-003.5.2.1`). Minimum-standard rows SHALL be numbered `<DOC-ID>.7.<n>`. A requirement number SHALL NOT be reused within a document for a different requirement after publication; deleted requirements SHALL be marked "Withdrawn" in the next version.
- **GOV-002.5.2.5** Document files SHALL be named `<DOC-ID>-<kebab-case-title>` and stored in the folder for their series.
- **GOV-002.5.2.6** Subordinate procedures and work instructions that are not suite documents SHALL carry the identifier of their parent suite document followed by a local suffix (for example `SEC-013-WI-01`) and SHALL be registered with the Head of GRC.

### 5.3 Document content and structure

- **GOV-002.5.3.1** Every Policy, Standard, Plan and Procedure SHALL contain, in order: Document control; Version history; Purpose; Scope; Policy statements (Requirements for Standards; Procedure for Plans and Procedures); Roles & responsibilities; Minimum standards; Monitoring, measurement & metrics; Exceptions; Enforcement; Framework & regulatory mapping; Related documents; Approval.
- **GOV-002.5.3.2** Every Template SHALL contain, in order: Document control; Version history; Purpose; Instructions; Form; Approval signatures.
- **GOV-002.5.3.3** Every requirement SHALL name an accountable role from GOV-001 and SHALL be verifiable through Evidence. Requirements SHALL state a value, a frequency or a defined term rather than a subjective qualifier.
- **GOV-002.5.3.4** Documents SHALL use the terms defined in GOV-006 and SHALL NOT define terms locally.
- **GOV-002.5.3.5** Documents SHALL use SHALL, SHALL NOT, SHOULD, SHOULD NOT and MAY only in uppercase and only normatively, as set out in GOV-006.
- **GOV-002.5.3.6** Each requirement and each value SHALL have one home document, recorded in the suite register's value ownership map. Other documents SHALL cite the home document by identifier and SHALL NOT restate the value.
- **GOV-002.5.3.7** Regulation-specific clauses SHALL carry the tags `[PCI]`, `[HIPAA]`, `[SOX]`, `[GDPR]` or `[CPRA]`. Organization-specific choices SHALL be written as `[DECISION REQUIRED: <question>. Recommended default: <value>]`.
- **GOV-002.5.3.8** Every document SHALL be classified Internal under SEC-002 unless its content requires Confidential.

### 5.4 Drafting and consultation

- **GOV-002.5.4.1** The Document Owner SHALL prepare each new document or revision and SHALL consult, at a minimum, every role named as Responsible or Accountable for the document's activities in REF-002.
- **GOV-002.5.4.2** Consultation SHALL allow consultees at least 10 business days to comment. The Document Owner SHALL record each comment and its disposition.
- **GOV-002.5.4.3** The GC SHALL review every document that contains a `[PCI]`, `[HIPAA]`, `[SOX]`, `[GDPR]` or `[CPRA]` clause before it is submitted for approval.
- **GOV-002.5.4.4** `[GDPR]` `[CPRA]` The DPO, or the CPO where no DPO is appointed, SHALL be consulted on every document that governs the processing of Personal Data.
- **GOV-002.5.4.5** Before submission for approval, the Head of GRC SHALL perform a conformance check confirming: the structure in section 5.3; use of GOV-006 terms and canonical role names; no restated values owned by another document; the document control block matches the suite README; and the framework mapping is consistent with REF-001. The Head of GRC SHALL record the result in the submission.
- **GOV-002.5.4.6** A document that fails the conformance check SHALL NOT be submitted for approval until the failures are corrected.

### 5.5 Approval

- **GOV-002.5.5.1** The Document Owner SHALL submit the document to the approver with the consultation record and the conformance check result.
- **GOV-002.5.5.2** The approver SHALL approve, approve with changes, or reject the document. Rejection SHALL state the reasons in writing.
- **GOV-002.5.5.3** The effective date of a document SHALL be the date of approval unless the approver sets a later date. The approver MAY set a transition period of up to 90 days for new requirements, recorded in the document control block.
- **GOV-002.5.5.4** The Head of GRC SHALL retain approval Evidence (minutes, resolutions, signed approval tables) under CMP-004.

### 5.6 Publication and communication

- **GOV-002.5.6.1** The Head of GRC SHALL publish each approved document in the policy repository within 10 business days of approval.
- **GOV-002.5.6.2** The policy repository SHALL be the single authoritative source of suite documents. It SHALL be accessible to every Workforce Member, SHALL permit modification only by the GRC function, and SHALL record who published each version and when.
- **GOV-002.5.6.3** Printed or exported copies of suite documents are uncontrolled. Each published document SHALL state that the repository version is authoritative.
- **GOV-002.5.6.4** On publication of a new document or a material revision, the Head of GRC SHALL notify every Workforce Member in the document's scope within the same 10-business-day publication window, stating the effective date and the main changes.
- **GOV-002.5.6.5** The CISO SHALL incorporate material changes to workforce obligations into the next scheduled training content under PPL-002.
- **GOV-002.5.6.6** Suite documents MAY be shared with customers, auditors, regulators and prospective customers only with the approval of the Head of GRC, and, for documents classified Confidential, only under a confidentiality agreement.

### 5.7 Review

- **GOV-002.5.7.1** The Document Owner SHALL review each document at least every 12 months from its last approval, and on the review triggers in the suite README for that document.
- **GOV-002.5.7.2** The Document Owner SHALL start an event-triggered review within 30 days of any of: a material organizational change; a new or changed legal obligation recorded under CMP-001; a Sev-1 Security Incident whose Post-Incident Review (RES-002) identifies a policy-related Root Cause; or an audit finding against the document.
- **GOV-002.5.7.3** Each review SHALL conclude in one of: no change (reconfirmed by the approver, next review date reset); minor change (section 5.8); material change (re-approval); or retirement (section 5.10). The outcome SHALL be recorded in the version history.
- **GOV-002.5.7.4** The Head of GRC SHALL maintain a review calendar and SHALL notify each Document Owner 60 days before a review is due.
- **GOV-002.5.7.5** A document whose review is more than 30 days overdue SHALL be reported to the ISSC. A document whose review is more than 90 days overdue SHALL be reported to the Audit Committee in the next quarterly report. An overdue document remains in force until revised or retired.
- **GOV-002.5.7.6** GOV-006, REF-001 and REF-002 SHALL additionally be reviewed on publication of every new suite document, and REF-003 quarterly.

### 5.8 Change and version control

- **GOV-002.5.8.1** Material Changes (GOV-006) SHALL be approved by the document's approver and SHALL increment the major version (for example 1.3 to 2.0).
- **GOV-002.5.8.2** Minor Changes (GOV-006) MAY be approved by the Head of GRC, SHALL increment the minor version (for example 1.0 to 1.1), and SHALL be reported to the approver within 10 business days. The Head of GRC SHALL NOT approve a Minor Change to a document the Head of GRC owns; such changes SHALL be approved by the CISO.
- **GOV-002.5.8.3** Every version SHALL be recorded in the version history with the version number, date, author role and change summary.
- **GOV-002.5.8.4** Superseded versions SHALL be removed from the active repository on publication of the new version, archived read-only, and retained under CMP-004.
- **GOV-002.5.8.5** The policy repository SHALL record the complete change history of every document, including author, date and content of each change, and SHALL prevent alteration of approved versions.
- **GOV-002.5.8.6** When a home document changes a value recorded in the suite register's value ownership map, the Head of GRC SHALL update the suite register within the publication window and SHALL notify the owners of every document that cites that value.

### 5.9 Workforce attestation

- **GOV-002.5.9.1** Every Workforce Member SHALL attest that they have read, understood and will comply with the documents in their Attestation Set before system access is granted at hire, and then every 12 months.
- **GOV-002.5.9.2** The Attestation Set for every Workforce Member SHALL include GOV-004. The CISO SHALL define additional Attestation Sets by role, at a minimum for: privileged users (SEC-005); developers (SEC-010); incident responders (RES-002); `[HIPAA]` Workforce Members with access to ePHI (CMP-008); and `[PCI]` Workforce Members with access to the CDE (SEC-019).
- **GOV-002.5.9.3** Attestation SHALL be recorded using TPL-009, or an electronic system that captures the same fields: identity of the Workforce Member, document identifiers and versions, date and time, and the attestation statements in TPL-009.
- **GOV-002.5.9.4** On publication of a material change to a document in an Attestation Set, every Workforce Member in that set SHALL re-attest within 30 days of publication.
- **GOV-002.5.9.5** The CHRO SHALL ensure that no system access is provisioned for a new Workforce Member until the Head of GRC's attestation record confirms completion (PPL-001).
- **GOV-002.5.9.6** A Workforce Member whose annual or change-driven attestation is overdue SHALL be escalated as follows: to their manager at 1 day overdue; to the relevant executive at 15 days overdue; and to the CHRO for action under CMP-007 at 30 days overdue.
- **GOV-002.5.9.7** Every Third Party with access to Organization Information Systems SHALL acknowledge GOV-004, and any other suite document named in its contract, before access is granted, either through a TPL-009 form signed by each individual or through a contractual clause binding all its personnel (RSK-003).
- **GOV-002.5.9.8** Attestation records SHALL be retained under CMP-004.
- **GOV-002.5.9.9** `[PCI]` Workforce Members SHALL acknowledge at least every 12 months that they have read and understood the information security policy and procedures (PCI DSS 12.6.3), through the attestation in GOV-002.5.9.1.

### 5.10 Retirement and supersession

- **GOV-002.5.10.1** A document SHALL be retired only with the approval of its approver, recording the reason and any successor document.
- **GOV-002.5.10.2** On retirement, the Head of GRC SHALL: mark the identifier as retired in the suite register; remove the document from the active repository; archive it read-only; and retain it under CMP-004.
- **GOV-002.5.10.3** The owners of every document that references a retired document SHALL update their references within 30 days of the retirement, as a minor change under GOV-002.5.8.2.
- **GOV-002.5.10.4** Where a retired document's content moves to another document, the receiving document's version history SHALL record the retired identifier (for example, GOV-004 records the absorption of retired GOV-005).

### 5.11 Subordinate documents

- **GOV-002.5.11.1** A function MAY issue procedures, work instructions or guidelines that implement a suite document. Each SHALL identify its parent suite document, SHALL NOT weaken or contradict it, and SHALL be approved by the parent document's owner.
- **GOV-002.5.11.2** Subordinate documents SHALL be reviewed at least every 12 months and SHALL be registered in the policy repository index maintained by the Head of GRC.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| Head of GRC | Owns this Policy; maintains the repository, suite register, review calendar and attestation records; performs conformance checks; approves minor changes |
| Document Owners | Draft, consult on, review and revise their documents; start event-triggered reviews within 30 days |
| Approvers (Board of Directors, Audit Committee, CEO, CFO, ISSC, CISO, other listed approvers) | Approve, approve with changes, reject or retire documents |
| ISSC | Approves this Policy and all Tier 1 Policies; receives overdue review reports |
| CISO | Defines role-based Attestation Sets; approves minor changes to documents owned by the Head of GRC; incorporates changes into training |
| GC | Reviews documents carrying regulation tags before approval |
| CPO / DPO | Consulted on documents governing Personal Data |
| CHRO | Blocks access provisioning until hire attestation is complete; acts on overdue attestations under CMP-007 |
| Workforce Members | Attest within the required timeframes and comply with their Attestation Set |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| GOV-002.7.1 | Document approval rule | As in README "Document hierarchy"; owner ≠ approver |
| GOV-002.7.2 | Workforce policy attestation | Before system access is granted at hire, then every 12 months |
| GOV-002.7.3 | Publication after approval | Within 10 business days |
| GOV-002.7.4 | Event-triggered review | Started within 30 days of: material organizational change, new or changed legal obligation, Sev-1 incident with a policy-related root cause, or audit finding against the document |
| GOV-002.7.5 | Scheduled review | At least every 12 months |
| GOV-002.7.6 | Consultation period | At least 10 business days |
| GOV-002.7.7 | Review reminder to Document Owner | 60 days before due date |
| GOV-002.7.8 | Overdue review escalation | ISSC at > 30 days; Audit Committee at > 90 days |
| GOV-002.7.9 | Re-attestation after material change | Within 30 days of publication |
| GOV-002.7.10 | Overdue attestation escalation | Manager at 1 day; executive at 15 days; CHRO (CMP-007) at 30 days |
| GOV-002.7.11 | Minor change reported to approver | Within 10 business days |
| GOV-002.7.12 | Maximum transition period for new requirements | 90 days |
| GOV-002.7.13 | References to a retired document updated | Within 30 days |
| GOV-002.7.14 | Lower-tier conflict revision opened | Within 10 business days of identification |
| GOV-002.7.15 | Retired identifiers | Never reused |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Suite documents reviewed within 12 months of last approval | 100% | Monthly | Head of GRC |
| Approved documents published within 10 business days | 100% | Monthly | Head of GRC |
| Event-triggered reviews started within 30 days of trigger | 100% | Quarterly | Head of GRC |
| Workforce Members with current attestation | ≥ 98% | Monthly | Head of GRC |
| New hires granted access before attestation | 0 | Monthly | CHRO |
| Documents failing conformance check at first submission | ≤ 10% | Quarterly | Head of GRC |
| Retired identifiers reused | 0 | Each new document | Head of GRC |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003. No Exception MAY be
granted to GOV-002.5.1.2 (owner ≠ approver), GOV-002.5.2.3 (retired identifiers) or
GOV-002.5.9.5 (attestation before access).

## 10. Enforcement

Non-compliance is handled under CMP-007. Publication of a document, or of a change to a
document, that has not been approved under this Policy SHALL be treated as a Security Incident
and reported under RES-001.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| GOV-002.5.1 – 5.5 | 5.2, 7.5.2; A.5.1 | GV.PO-01 | PL-1, PM-1 | — | CC5.3 | APO01.03 | `[PCI]` 12.1.1; `[HIPAA]` §164.316(a) |
| GOV-002.5.6 | 5.2, 7.4, 7.5.3; A.5.1 | GV.PO-01 | PL-1 | — | CC2.2 | APO01.03 | `[PCI]` 12.1.1; `[HIPAA]` §164.316(b)(2)(ii) |
| GOV-002.5.7 | 7.5.2; A.5.1 | GV.PO-02 | PL-1 | — | CC5.3 | APO01.03 | `[PCI]` 12.1.2; `[HIPAA]` §164.316(b)(2)(iii) |
| GOV-002.5.8, 5.10 | 7.5.3 | GV.PO-02 | CM-3, PL-1 | — | CC5.3 | APO01.03 | `[HIPAA]` §164.316(b)(1) |
| GOV-002.5.9 | 7.3; A.5.1, A.6.2 | PR.AT-01 | PL-4, PS-6 | 14.1 | CC1.1, CC2.2 | APO07.06 | `[PCI]` 12.6.3; `[HIPAA]` §164.308(a)(5)(i) |
| GOV-002.5.11 | 7.5.1; A.5.37 | GV.PO-01 | PL-1 | — | CC5.3 | APO01.03 | — |

## 12. Related documents

ISP-000, GOV-001, GOV-004, GOV-006, CMP-001, CMP-003, CMP-004, CMP-007, CMP-008, SEC-002,
SEC-005, SEC-010, SEC-019, RES-001, RES-002, PPL-001, PPL-002, RSK-003, TPL-009, REF-001,
REF-002, REF-003

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Head of GRC | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
