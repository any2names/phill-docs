# REF-001 — Control Mapping Matrix

## 1. Document control

| Field | Value |
|---|---|
| Document ID | REF-001 |
| Title | Control Mapping Matrix |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | Ref — Master reference |
| Classification | Internal |
| Owner | Head of GRC |
| Approver | Chief Information Security Officer (CISO) |
| Effective date | [DECISION REQUIRED: Date of CISO approval] |
| Next review date | Effective date + 12 months, and on approval of any new or revised suite document |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-002, CMP-001, CMP-002, CMP-008, CMP-009, SEC-019, REF-002, REF-003 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Head of GRC | Initial release |

## 3. Purpose

This document is the single consolidated map between the requirements of the Organization's
Information Security & GRC Policy Suite and the external frameworks and regulations the
Organization uses or is subject to. It:

1. maps every policy-statement subsection (section 5.x) of every suite document to ISO/IEC 27001:2022, NIST CSF 2.0, NIST SP 800-53 Rev. 5, CIS Controls v8.1, the SOC 2 Trust Services Criteria, COBIT 2019 and the applicable regulations;
2. designates the Key Controls for the SOC 2 Type II examination;
3. gives reverse-coverage views, from each framework back to the suite, that show coverage and gaps and support the scoping of external assessments; and
4. seeds a future ISO/IEC 27001 Statement of Applicability.

REF-001 contains no requirements of its own beyond how the matrix is maintained (section 5.1).
Each requirement remains in its home document. Where a document's section 11 and this
matrix differ, section 5.1 sets how the difference is resolved.

## 4. Scope

- **Documents:** all 58 suite documents other than the REF series: ISP-000; GOV-001 to GOV-004 and GOV-006; RSK-001 to RSK-006; CMP-001 to CMP-010; SEC-001 to SEC-019; RES-001 to RES-005; PPL-001 and PPL-002; TPL-001 to TPL-010.
- **Frameworks:** the versions fixed in SUITE-REGISTER section A: ISO/IEC 27001:2022 (+Amd 1:2024) clauses 4–10 and Annex A; NIST CSF 2.0; NIST SP 800-53 Rev. 5; CIS Controls v8.1; SOC 2 Trust Services Criteria (2017, revised points of focus 2022); COBIT 2019.
- **Regulations:** `[PCI]` PCI DSS v4.0.1; `[HIPAA]` 45 CFR Part 164 Subparts C and D; `[GDPR]`; `[CPRA]` (Cal. Civ. Code §1798.100 et seq. and Cal. Code Regs. tit. 11); `[SOX]` §§301, 302, 404 and related SEC disclosure rules. Other instruments cited by suite documents (e.g. EU Directive 2019/1937, the EU AI Act, ISO 22301:2019) are shown as "Other".
- **Out of scope:** the ISO/IEC 42001:2023 and NIST AI RMF alignment in RSK-006 section 11.1, which stays in RSK-006. SOC 2 Privacy (P-series) and Processing Integrity (PI-series) criteria are shown where suite documents cite them, but are outside the default examination scope (SUITE-REGISTER decision #2).
- **Users:** the Head of GRC, Control Owners, Document Owners, the Internal Audit Director, and external auditors, QSAs and assessors under CMP-001 and CMP-002.

## 5. Control mapping

### 5.1 Maintenance of this matrix

- **REF-001.5.1.1** Each suite document's section 11 is the primary source for its mappings. The Head of GRC SHALL update this matrix within 10 business days of the approval of any new or revised suite document under GOV-002.
- **REF-001.5.1.2** Before adding a control ID to this matrix, the Head of GRC SHALL verify that it exists in the framework version in section 4. Ranges SHALL be expanded to individual IDs, and lettered list items SHALL be cited by their parent clause. Where an enhancement or sub-ID is uncertain, the parent control SHALL be cited.
- **REF-001.5.1.3** Where this matrix corrects or adds to a document's section 11, the Head of GRC SHALL record the correction in appendix A and SHALL notify the Document Owner. The Document Owner SHALL align section 11 at the next revision of the document under GOV-002. Until then, this matrix prevails for assessment scoping.
- **REF-001.5.1.4** The Head of GRC SHALL designate Key Controls (section 5.4) using these criteria: the Control directly addresses a SOC 2 criterion in examination scope; its failure would allow a material Risk to go undetected; and it operates at a defined frequency that produces Evidence under CMP-004. The CISO SHALL approve the Key Control list before the start of each SOC 2 Type II Observation Period.
- **REF-001.5.1.5** The Key Control list SHALL NOT be changed during an Observation Period except to add Controls. Every addition SHALL be notified to the service auditor within 10 business days.
- **REF-001.5.1.6** The Head of GRC SHALL review the reverse-coverage views (sections 5.5 to 5.10) every 12 months, and after any change of framework version, and SHALL raise every "Not covered" or "Partial" result as a gap in REF-003 or as a Risk under RSK-001.
- **REF-001.5.1.7** Where the Organization pursues ISO/IEC 27001 certification, the Head of GRC SHALL derive the Statement of Applicability from section 5.5. Each Annex A control SHALL be recorded as applicable, with the implementing requirements listed there, or as excluded, with a justification approved by the CISO.
- **REF-001.5.1.8** Where a conditional module does not apply (README "Conditional modules"), the Head of GRC SHALL remove the matching regulation entries and reverse views from this matrix: `[PCI]` section 5.8 and PCI entries; `[HIPAA]` section 5.9 and HIPAA entries; `[SOX]` section 5.10 and SOX entries; `[GDPR]` `[CPRA]` entries.

### 5.2 How to read the matrix

| Column | Content |
|---|---|
| Requirement | `<DOC-ID>.<subsection>` and subsection title. Each row covers every numbered item in that subsection (e.g. row SEC-003.5.12 covers SEC-003.5.12.1 onwards). |
| KC | Key Control ID where the subsection contains a designated Key Control (section 5.4). |
| ISO/IEC 27001:2022 | Clauses 4–10 first, then Annex A controls (A.5.x organizational, A.6.x people, A.7.x physical, A.8.x technological). |
| NIST CSF 2.0 | Subcategories (or a category where the document cited one). |
| NIST SP 800-53 r5 | Base controls; enhancements in parentheses. |
| CIS v8.1 | Safeguards. |
| SOC 2 TSC | Common Criteria (CC), Availability (A1), Confidentiality (C1); Privacy (P) only where cited. |
| COBIT 2019 | Governance and management objectives, or practices where cited. |
| Regulations | Grouped by tag: `[PCI]` PCI DSS v4.0.1 requirement numbers; `[HIPAA]` 45 CFR sections; `[GDPR]` articles; `[CPRA]` Cal. Civ. Code and Cal. Code Regs. tit. 11 sections; `[SOX]` SOX sections and SEC rules; "Other" for other instruments. |

Where a document's section 11 maps a range of subsections in one row (e.g. "5.1 – 5.3"), each
subsection in the range carries that row's mappings. Templates (TPL) contain forms rather than
policy statements. Each template is therefore one row that inherits the mappings of the
requirements it evidences.

### 5.3 Forward matrix: suite requirement to frameworks

#### 5.3.1 Program charter

**ISP-000 Information Security Program Charter**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| ISP-000.5.1 Mandate |  | 4.4, 5.1, 5.3 | GV.OC-01, GV.RR-01 | PM-1, PM-2 | — | CC1.2, CC1.3 | APO01, EDM01 | [PCI] 12.1.1, 12.4.1 · [HIPAA] §164.308(a)(2) · [SOX] §404 |
| ISP-000.5.2 Objectives |  | 6.2 | GV.OC-01, GV.OV-01 | PM-6 | — | CC3.1 | APO13, MEA01 | [GDPR] Art. 24, 32 |
| ISP-000.5.3 Scope of the program |  | 4.1, 4.2, 4.3 | GV.OC-03, GV.PO-01 | PM-1 | — | CC2.2 | APO01 | — |
| ISP-000.5.4 Authority of the CISO |  | 5.3; A.5.2 | GV.RR-02 | PM-2 | — | CC1.3 | APO01 | [PCI] 12.1.3 |
| ISP-000.5.5 Risk appetite |  | 6.1.1 | GV.RM-02 | PM-9 | — | CC3.1, CC3.2 | APO12, EDM03 | — |
| ISP-000.5.6 Document hierarchy |  | 5.2, 7.5; A.5.1 | GV.PO-01 | PL-1, PM-1 | — | CC5.3 | APO01 | [PCI] 12.1.1 · [HIPAA] §164.316 |
| ISP-000.5.7 Board oversight | KC-01 | 5.1, 9.3 | GV.OV-01, GV.RR-01 | PM-1 | — | CC1.2, CC4.2 | EDM01, EDM05, MEA01 | [SOX] §302, §404 |
| ISP-000.5.8 Review and continual improvement |  | 9.3, 10.1 | GV.OV-02, ID.IM-01 | PM-1 | — | CC4.1 | MEA01 | [PCI] 12.1.2 |

#### 5.3.2 Governance

**GOV-001 Security Governance & Organization Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| GOV-001.5.1 Governance structure | KC-02 | 5.1, 5.3; A.5.2, A.5.4 | GV.RR-01, GV.RR-02 | PM-2, PM-29 | — | CC1.2, CC1.3 | APO01, EDM01 | [PCI] 12.1.3, 12.1.4 · [SOX] §404 |
| GOV-001.5.2 CISO appointment and reporting line |  | 5.1, 5.3; A.5.2, A.5.4 | GV.RR-01, GV.RR-02 | PM-2, PM-29 | — | CC1.2, CC1.3 | APO01, EDM01 | [PCI] 12.1.3, 12.1.4 · [SOX] §404 |
| GOV-001.5.3 Information Security Steering Committee (ISSC) charter | KC-03 | 5.1, 9.3 | GV.OV-01, GV.RR-01 | PM-1 | — | CC1.2, CC2.2 | APO01, EDM01 | — |
| GOV-001.5.4 Role definitions and accountabilities |  | 5.3; A.5.2 | GV.RR-02 | PM-2, PS-9 | — | CC1.3, CC1.5 | APO01, APO07 | [PCI] 12.1.3 |
| GOV-001.5.5 Statutory officer designations |  | 5.3; A.5.2, A.5.34 | GV.RR-02 | PM-2 | — | CC1.3 | APO01 | [HIPAA] §164.308(a)(2), §164.530(a)(1) · [GDPR] Art. 37 |
| GOV-001.5.6 DPO independence [GDPR] |  | A.5.34 | GV.RR-02 | PT-1 | — | CC1.3 | APO01 | [GDPR] Art. 38, 39 |
| GOV-001.5.7 Segregation of Duties | KC-04 | A.5.3 | GV.RR-02 | AC-5, AC-6 | 6.8 | CC5.1, CC6.3 | DSS05, DSS06 | [PCI] 6.5.4, 7.2 · [SOX] §404 |
| GOV-001.5.8 Role combinations for smaller adopters |  | 5.3; A.5.3 | GV.RR-02 | AC-5 | — | CC1.3 | APO01 | — |
| GOV-001.5.9 Competence and resourcing |  | 7.1, 7.2 | GV.RR-03 | PM-3, PM-13 | — | CC1.4 | APO07 | — |
| GOV-001.5.10 Contact with authorities and special interest groups |  | A.5.5, A.5.6 | GV.OC-02, ID.RA-02 | IR-6, PM-15 | — | CC2.3 | APO08 | — |
| GOV-001.5.11 Security in project management |  | A.5.8 | GV.RM-03 | PL-2, SA-3 | — | CC3.4 | BAI01 | — |

**GOV-002 Policy Management Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| GOV-002.5.1 Document hierarchy and approval rule |  | 5.2, 7.5.2; A.5.1 | GV.PO-01 | PL-1, PM-1 | — | CC5.3 | APO01.03 | [PCI] 12.1.1 · [HIPAA] §164.316(a) |
| GOV-002.5.2 Numbering and naming |  | 5.2, 7.5.2; A.5.1 | GV.PO-01 | PL-1, PM-1 | — | CC5.3 | APO01.03 | [PCI] 12.1.1 · [HIPAA] §164.316(a) |
| GOV-002.5.3 Document content and structure |  | 5.2, 7.5.2; A.5.1 | GV.PO-01 | PL-1, PM-1 | — | CC5.3 | APO01.03 | [PCI] 12.1.1 · [HIPAA] §164.316(a) |
| GOV-002.5.4 Drafting and consultation |  | 5.2, 7.5.2; A.5.1 | GV.PO-01 | PL-1, PM-1 | — | CC5.3 | APO01.03 | [PCI] 12.1.1 · [HIPAA] §164.316(a) |
| GOV-002.5.5 Approval | KC-05 | 5.2, 7.5.2; A.5.1 | GV.PO-01 | PL-1, PM-1 | — | CC5.3 | APO01.03 | [PCI] 12.1.1 · [HIPAA] §164.316(a) |
| GOV-002.5.6 Publication and communication |  | 5.2, 7.4, 7.5.3; A.5.1 | GV.PO-01 | PL-1 | — | CC2.2 | APO01.03 | [PCI] 12.1.1 · [HIPAA] §164.316(b)(2)(ii) |
| GOV-002.5.7 Review | KC-06 | 7.5.2; A.5.1 | GV.PO-02 | PL-1 | — | CC5.3 | APO01.03 | [PCI] 12.1.2 · [HIPAA] §164.316(b)(2)(iii) |
| GOV-002.5.8 Change and version control |  | 7.5.3 | GV.PO-02 | CM-3, PL-1 | — | CC5.3 | APO01.03 | [HIPAA] §164.316(b)(1) |
| GOV-002.5.9 Workforce attestation | KC-07 | 7.3; A.5.1, A.6.2 | PR.AT-01 | PL-4, PS-6 | 14.1 | CC1.1, CC2.2 | APO07.06 | [PCI] 12.6.3 · [HIPAA] §164.308(a)(5)(i) |
| GOV-002.5.10 Retirement and supersession |  | 7.5.3 | GV.PO-02 | CM-3, PL-1 | — | CC5.3 | APO01.03 | [HIPAA] §164.316(b)(1) |
| GOV-002.5.11 Subordinate documents |  | 7.5.1; A.5.37 | GV.PO-01 | PL-1 | — | CC5.3 | APO01.03 | — |

**GOV-003 Security Metrics & Reporting Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| GOV-003.5.1 Metric governance |  | 9.1 | GV.OV-03, ID.IM-01 | CA-7, PM-6 | — | CC4.1 | MEA01.01, MEA01.02, MEA01.03, MEA01.04 | — |
| GOV-003.5.2 Data quality and Evidence |  | 9.1 | GV.OV-03, ID.IM-01 | CA-7, PM-6 | — | CC4.1 | MEA01.01, MEA01.02, MEA01.03, MEA01.04 | — |
| GOV-003.5.3 KPI and KRI catalogue |  | 9.1 | GV.OV-03, ID.IM-01 | CA-7, PM-6 | — | CC4.1 | MEA01.01, MEA01.02, MEA01.03, MEA01.04 | — |
| GOV-003.5.4 Threshold breaches and escalation |  | 9.1, 10.2 | GV.OV-02, GV.RM-01 | PM-6, PM-9 | — | CC4.2 | APO12, MEA01.05 | — |
| GOV-003.5.5 Reporting cadence | KC-08 | 5.1, 9.1, 9.3 | GV.OV-01, GV.RR-01 | PM-6 | — | CC1.2, CC2.2 | EDM05, MEA01 | [SOX] §302, §404; Reg. S-K Item 106 |
| GOV-003.5.6 Report content |  | 5.1, 9.1, 9.3 | GV.OV-01, GV.RR-01 | PM-6 | — | CC1.2, CC2.2 | EDM05, MEA01 | [SOX] §302, §404; Reg. S-K Item 106 |
| GOV-003.5.7 Review of the metric catalogue |  | 9.1, 10.1 | ID.IM-01 | PM-6 | — | CC4.1 | MEA01 | — |

**GOV-004 Acceptable Use Policy (absorbs GOV-005)**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| GOV-004.5.1 General principles |  | A.5.10, A.5.15, A.8.1 | PR.AA-05, PR.AT-01 | AC-8, PL-4 | 2.5, 2.7, 4.3 | CC1.1, CC2.2 | DSS05.04 | [PCI] 12.2.1, 4.2.2 · [HIPAA] §164.308(a)(3)(ii)(A) |
| GOV-004.5.2 Accounts and credentials |  | A.5.10, A.5.15, A.8.1 | PR.AA-05, PR.AT-01 | AC-8, PL-4 | 2.5, 2.7, 4.3 | CC1.1, CC2.2 | DSS05.04 | [PCI] 12.2.1, 4.2.2 · [HIPAA] §164.308(a)(3)(ii)(A) |
| GOV-004.5.3 Endpoints, devices and workplace |  | A.5.10, A.5.15, A.7.7, A.8.1, A.8.19 | PR.AA-05, PR.AT-01, PR.PS-02, PR.PS-05 | AC-8, CM-11, PL-4 | 2.3, 2.5, 2.7, 4.3 | CC1.1, CC2.2, CC6.8 | DSS05.03, DSS05.04 | [PCI] 12.2.1, 4.2.2 · [HIPAA] §164.308(a)(3)(ii)(A); §164.310(b) |
| GOV-004.5.4 Prohibited use |  | A.5.10, A.5.15, A.8.1 | PR.AA-05, PR.AT-01 | AC-8, PL-4 | 2.5, 2.7, 4.3 | CC1.1, CC2.2 | DSS05.04 | [PCI] 12.2.1, 4.2.2 · [HIPAA] §164.308(a)(3)(ii)(A) |
| GOV-004.5.5 Personal use |  | A.5.10, A.5.14, A.5.23 | ID.AM-02 | PL-4 | 2.1, 3.3 | CC6.7 | DSS05.04 | — |
| GOV-004.5.6 Email, messaging and collaboration |  | A.5.10, A.5.14, A.5.23 | ID.AM-02 | PL-4 | 2.1, 3.3 | CC6.7 | DSS05.04 | — |
| GOV-004.5.7 Data storage and Shadow IT |  | A.5.10, A.5.14, A.5.23 | ID.AM-02 | PL-4 | 2.1, 3.3 | CC6.7 | DSS05.04 | — |
| GOV-004.5.8 Generative AI tools |  | A.5.10 | GV.PO-01 | PL-4 | — | CC2.2 | APO13 | [GDPR] Art. 22 |
| GOV-004.5.9 Social media and public communications |  | A.5.10, A.5.14 | PR.AT-01 | PL-4(1) | — | CC2.2 | DSS05.04 | — |
| GOV-004.5.10 Intellectual property and software licensing |  | A.5.32 | GV.OC-03 | CM-10 | — | CC2.2 | MEA03 | — |
| GOV-004.5.11 Confidentiality obligations |  | A.6.2, A.6.6 | PR.AT-01 | PS-6 | — | C1.1, CC1.1 | APO07 | [HIPAA] §164.308(a)(3) · [GDPR] Art. 28(3)(b), 29 |
| GOV-004.5.12 Conflicts of interest relating to information security |  | A.5.3, A.6.2 | GV.RR-04 | PS-6 | — | CC1.1 | APO07 | [SOX] §406 |
| GOV-004.5.13 Monitoring notice |  | A.8.15, A.8.16 | DE.CM-03 | AC-8, AU-1 | 8.1 | CC7.2 | DSS05.07 | [GDPR] Art. 5, 6, 13, 35, 88 |
| GOV-004.5.14 Reporting obligations |  | A.6.8 | RS.MA-01 | IR-6 | 14.6 | CC2.3 | DSS02 | — |
| GOV-004.5.15 Return of assets and access at Separation |  | A.5.11, A.6.5 | PR.AA-05 | PS-4 | 6.2 | CC6.2, CC6.5 | APO07.06 | [HIPAA] §164.308(a)(3)(ii)(C) |

**GOV-006 Glossary & Definitions**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| GOV-006.5.1 Use of defined terms |  | 5.2, 7.5.1; A.5.1 | GV.PO-01 | PL-1, PM-1 | — | CC2.2, CC5.3 | APO01.02 | — |
| GOV-006.5.2 Normative language |  | 5.2, 7.5.1; A.5.1 | GV.PO-01 | PL-1, PM-1 | — | CC2.2, CC5.3 | APO01.02 | — |
| GOV-006.5.3 Defined terms |  | 7.5.2; A.5.1 | GV.PO-01 | PL-1 | — | CC2.2 | APO01.02 | — |
| GOV-006.5.4 Acronyms |  | 7.5.2; A.5.1 | GV.PO-01 | PL-1 | — | CC2.2 | APO01.02 | — |

#### 5.3.3 Risk

**RSK-001 Risk Management Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| RSK-001.5.1 Risk management framework and principles |  | 6.1.1, 6.1.2, 8.2 | GV.RM-01, GV.RM-06 | PM-9, RA-1 | — | CC3.1, CC3.2 | APO12, EDM03 | [PCI] 12.3.1 · [HIPAA] §164.308(a)(1)(ii)(A)–(B) |
| RSK-001.5.2 Risk context and identification |  | 4.1, 4.2, 6.1.2 | GV.OC-01, ID.RA-03, ID.RA-04 | PM-28, RA-3 | — | CC3.2, CC3.3 | APO12.01 | [GDPR] Art. 24, 32 |
| RSK-001.5.3 Risk Appetite and Risk Tolerance | KC-09 | 6.1.1, 6.1.2 | GV.RM-02, GV.RM-03 | PM-9, PM-28 | — | CC3.1 | APO12.06, EDM03.01 | [SOX] §404 |
| RSK-001.5.4 Risk Treatment |  | 6.1.3, 8.3 | GV.RM-04, ID.RA-06 | PM-4, RA-7 | — | CC3.2, CC5.1 | APO12.06 | [HIPAA] §164.308(a)(1)(ii)(B) |
| RSK-001.5.5 Risk Acceptance | KC-10 | 6.1.3 | GV.RM-04, ID.RA-07 | PM-9, RA-7 | — | CC3.2 | APO12.06 | [PCI] 12.3.1 |
| RSK-001.5.6 Monitoring, review and escalation | KC-11 | 8.2, 9.1, 9.3 | GV.OV-01, GV.OV-03, ID.IM-01 | CA-7, PM-9 | — | CC4.1, CC4.2 | APO12.04, MEA01 | [SOX] §404 |
| RSK-001.5.7 Communication, consultation and competence |  | 7.2, 7.3, 7.4 | GV.RR-02, PR.AT-01 | AT-3, PM-13 | 14.1 | CC2.2, CC2.3 | APO12.04 | — |

**RSK-002 Risk Assessment Standard**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| RSK-002.5.1 Assessment method |  | 6.1.2, 8.2 | GV.RM-06, ID.RA-05 | RA-3 | — | CC3.2 | APO12.02 | [HIPAA] §164.308(a)(1)(ii)(A) · [GDPR] Art. 32(2) |
| RSK-002.5.2 Likelihood criteria |  | 6.1.2 | ID.RA-04, ID.RA-05 | RA-3 | — | CC3.2 | APO12.02, APO12.03 | — |
| RSK-002.5.3 Impact criteria |  | 6.1.2 | ID.RA-04, ID.RA-05 | RA-3 | — | CC3.2 | APO12.02, APO12.03 | — |
| RSK-002.5.4 Risk level bands and the matrix |  | 6.1.2 | ID.RA-04, ID.RA-05 | RA-3 | — | CC3.2 | APO12.02, APO12.03 | — |
| RSK-002.5.5 Control effectiveness |  | 6.1.3, 9.1 | ID.IM-01, ID.RA-05 | CA-2, RA-3 | — | CC3.2, CC4.1 | MEA02 | [SOX] §404 |
| RSK-002.5.6 Assessment frequency and triggers | KC-12 | 8.2 | ID.IM-01, ID.RA-07 | RA-3 | — | CC3.4 | APO12.02 | [PCI] 12.3.1 · [HIPAA] §164.308(a)(1)(ii)(A) |
| RSK-002.5.7 Treatment deadlines |  | 6.1.3, 8.3 | ID.RA-06 | RA-7 | 7.2 | CC3.2, CC5.1 | APO12.06 | [HIPAA] §164.308(a)(1)(ii)(B) |
| RSK-002.5.8 [PCI] Targeted Risk Analysis |  | 6.1.2 | ID.RA-05 | RA-3 | — | CC3.2 | APO12.02 | [PCI] 12.3.1, 12.3.2, 12.3.3, 12.3.4 |
| RSK-002.5.9 Assessment records and quality |  | 7.5.3, 8.2 | GV.RM-06 | RA-3 | — | CC3.2 | APO12.03 | — |
| RSK-002.5.10 Fraud risk | KC-13 | 6.1.2 | ID.RA-03, ID.RA-05 | RA-3 | — | CC3.3 | APO12.02 | [SOX] §404 |

**RSK-003 Third-Party & Supply Chain Risk Management Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| RSK-003.5.1 Governance and inventory |  | A.5.19, A.5.23 | GV.SC-01, GV.SC-04 | PM-30, SR-1, SR-2 | 15.1, 15.2, 15.3 | CC9.2 | APO10.01, APO10.02 | [PCI] 12.8.1 |
| RSK-003.5.2 Tiering |  | A.5.19, A.5.23 | GV.SC-01, GV.SC-04 | PM-30, SR-1, SR-2 | 15.1, 15.2, 15.3 | CC9.2 | APO10.01, APO10.02 | [PCI] 12.8.1 |
| RSK-003.5.3 Due diligence | KC-14 | A.5.19, A.5.21 | GV.SC-06, GV.SC-07, ID.RA-10 | SA-9, SR-6 | 15.5 | CC9.2 | APO10.03 | [PCI] 12.8.3 · [GDPR] Art. 28(1) |
| RSK-003.5.4 Contract requirements | KC-15 | A.5.20 | GV.SC-05 | SA-4, SA-9, SR-3, SR-8 | 15.4 | C1.1, CC9.2 | APO10.03 | [PCI] 12.8.2, 12.8.5 · [HIPAA] §164.308(b)(1), §164.314(a), §164.504(e) · [GDPR] Art. 28(3) · [CPRA] §1798.100(d) |
| RSK-003.5.5 Ongoing monitoring and reassessment | KC-16 | A.5.22 | GV.SC-07, GV.SC-08, GV.SC-09 | CA-7, SA-9, SR-6 | 15.6 | CC4.1, CC9.2 | APO10.05 | [PCI] 12.8.4 · [SOX] §404 |
| RSK-003.5.6 Software and hardware supply chain |  | A.5.21, A.8.30 | GV.SC-09, ID.RA-09 | SA-22, SR-3, SR-4, SR-5, SR-11 | 2.1, 16.4 | CC8.1, CC9.2 | BAI03 | — |
| RSK-003.5.7 Offboarding |  | A.5.19, A.5.22 | GV.SC-10 | PS-7, SA-9, SR-12 | 15.7 | C1.2, CC9.2 | APO10.05 | [GDPR] Art. 28(3)(g) |

**RSK-004 Business Impact Analysis Standard**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| RSK-004.5.1 BIA method |  | 6.1.2; A.5.29, A.5.30 | GV.OC-04, GV.OC-05, ID.RA-04 | CP-2, PM-11, RA-9 | — | A1.2, CC9.1 | DSS04.02 | [HIPAA] §164.308(a)(7)(ii)(E) |
| RSK-004.5.2 Impact over time |  | 6.1.2; A.5.29, A.5.30 | GV.OC-04, GV.OC-05, ID.RA-04 | CP-2, PM-11, RA-9 | — | A1.2, CC9.1 | DSS04.02 | [HIPAA] §164.308(a)(7)(ii)(E) |
| RSK-004.5.3 Recovery Tiers and assignment criteria |  | A.5.30, A.8.14 | ID.AM-05, RC.RP-01 | CP-2, CP-10 | 11.1 | A1.2, A1.3 | DSS04.02, DSS04.03 | [HIPAA] §164.308(a)(7)(ii)(E) · [SOX] §404 |
| RSK-004.5.4 Maximum tolerable period of disruption |  | A.5.30, A.8.14 | ID.AM-05, RC.RP-01 | CP-2, CP-10 | 11.1 | A1.2, A1.3 | DSS04.02, DSS04.03 | [HIPAA] §164.308(a)(7)(ii)(E) · [SOX] §404 |
| RSK-004.5.5 Dependency mapping | KC-17 | A.5.29, A.5.30, A.8.14 | GV.OC-05, GV.SC-04, ID.AM-03 | CP-2, CP-8, RA-9, SA-9 | 15.1 | CC9.1, CC9.2 | APO10, DSS04.02 | — |
| RSK-004.5.6 Minimum resources for recovery |  | 7.5; A.5.30 | GV.OC-04, ID.IM-01 | CP-2 | — | A1.2 | DSS04.01 | [HIPAA] §164.308(a)(7)(i) |
| RSK-004.5.7 Approval, refresh and records | KC-18 | 7.5; A.5.30 | GV.OC-04, ID.IM-01 | CP-2 | — | A1.2 | DSS04.01 | [HIPAA] §164.308(a)(7)(i) |

**RSK-005 Threat Intelligence & Threat Modeling Standard**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| RSK-005.5.1 Intelligence requirements and threat profile |  | A.5.6, A.5.7 | ID.RA-02, ID.RA-03 | PM-16, RA-3 | — | CC3.2 | APO12.01 | — |
| RSK-005.5.2 Intelligence sources |  | A.5.6, A.5.7 | ID.RA-02, ID.RA-03 | PM-16, RA-3 | — | CC3.2 | APO12.01 | — |
| RSK-005.5.3 Processing, analysis and action |  | A.5.7, A.8.8, A.8.16 | DE.AE-02, DE.CM-01, ID.RA-02 | RA-10, SI-4, SI-5 | 7.1, 13.1 | CC7.1, CC7.2 | DSS05.07 | [PCI] 6.3.1 |
| RSK-005.5.4 Handling and sharing |  | A.5.6, A.5.14 | ID.RA-02, RS.CO-03 | PM-15, SI-5 | — | CC2.3 | APO08 | [GDPR] Art. 6(1)(f) |
| RSK-005.5.5 Reporting |  | 9.3; A.5.7 | GV.OV-01, ID.RA-03 | PM-16 | — | CC2.2, CC3.2 | MEA01 | — |
| RSK-005.5.6 Threat modeling |  | A.5.8, A.8.25, A.8.27 | ID.RA-03, ID.RA-05, PR.PS-06 | RA-3, SA-8, SA-11, SA-15 | 16.10, 16.14 | CC3.2, CC8.1 | BAI03.02 | [PCI] 6.2.1 · [GDPR] Art. 25 |
| RSK-005.5.7 MITRE ATT&CK mapping and detection coverage |  | A.8.16 | DE.AE-02, DE.CM-01, ID.IM-02 | CA-8, RA-10, SI-4 | 8.11, 18.1 | CC4.1, CC7.2 | DSS05.07 | — |

**RSK-006 AI & Emerging Technology Risk Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| RSK-006.5.1 Govern: accountability and AI management system |  | 5.1, 5.3, 7.2 | GV.PO-01, GV.RR-02, PR.AT-01 | AT-3, PM-9 | 14.1 | CC1.3, CC2.2 | APO01, EDM03 | Other: EU AI Act Art. 4 |
| RSK-006.5.2 Map: AI System inventory |  | A.5.9 | ID.AM-01, ID.AM-02 | CM-8, PM-5 | 1.1, 2.1 | CC6.1 | BAI09.01 | [GDPR] Art. 30 |
| RSK-006.5.3 Map: risk classification of AI use cases |  | 6.1.2 | ID.RA-04, ID.RA-05 | RA-3, RA-8 | — | CC3.2 | APO12.02 | [GDPR] Art. 35 · Other: EU AI Act Art. 5, 6, 27 |
| RSK-006.5.4 Approved Generative AI tools |  | A.5.10, A.5.12, A.5.14 | PR.AA-05, PR.DS-01, PR.DS-02 | AC-3, AC-4, SC-7 | 3.3, 3.13 | C1.1, CC6.1 | DSS05.02 | [PCI] 3.2.1 · [HIPAA] §164.502(e) · [GDPR] Art. 5(1)(b), 25 |
| RSK-006.5.5 Data input restrictions by Classification Level |  | A.5.10, A.5.12, A.5.14 | PR.AA-05, PR.DS-01, PR.DS-02 | AC-3, AC-4, SC-7 | 3.3, 3.13 | C1.1, CC6.1 | DSS05.02 | [PCI] 3.2.1 · [HIPAA] §164.502(e) · [GDPR] Art. 5(1)(b), 25 |
| RSK-006.5.6 Human oversight |  | A.5.2 | GV.RR-02 | PM-9 | — | CC1.3 | APO01.02 | [GDPR] Art. 22 · [CPRA] §1798.185 · Other: EU AI Act Art. 14, 26, 50 |
| RSK-006.5.7 Model and vendor assessment |  | A.5.19, A.5.20, A.8.25 | GV.SC-06, GV.SC-07 | SA-9, SR-6 | 15.4, 16.1 | CC9.2 | APO10.03 | Other: EU AI Act Art. 25 |
| RSK-006.5.8 Measure and Manage: evaluation, monitoring and incidents |  | A.5.24, A.8.16, A.8.29 | DE.CM-09, ID.RA-01, RS.MA-01 | CA-8, IR-4, SI-4 | 16.13 | CC4.1, CC7.2 | BAI07, MEA01 | Other: EU AI Act Art. 9, 15, 26, 73 |
| RSK-006.5.9 EU AI Act |  | 4.2 | GV.OC-03 | PM-9 | — | CC2.3 | MEA03 | Other: EU AI Act Chapter III |
| RSK-006.5.10 Other Emerging Technology |  | 6.1.2; A.8.24 | ID.RA-05 | RA-3, SC-12 | 3.10 | CC3.4 | APO04 | — |

#### 5.3.4 Compliance and privacy

**CMP-001 Compliance Management Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| CMP-001.5.1 Compliance program governance |  | 4.2, 5.3; A.5.2, A.5.31 | GV.OC-03, GV.RR-02 | PM-1, PM-2 | — | CC1.3, CC2.2 | APO01, MEA03 | [PCI] 12.4.1 · [GDPR] Art. 5(2), 24 |
| CMP-001.5.2 Obligations Register |  | 4.2, 6.1.3; A.5.31, A.5.34 | GV.OC-03 | PL-1, PM-1 | — | CC2.3, CC3.1 | MEA03 | [HIPAA] §160.103 · [GDPR] Art. 3, 24, 27 · [CPRA] §1798.140 |
| CMP-001.5.3 Applicability determination |  | 4.2, 6.1.3; A.5.31, A.5.34 | GV.OC-03 | PL-1, PM-1 | — | CC2.3, CC3.1 | MEA03 | [HIPAA] §160.103 · [GDPR] Art. 3, 24, 27 · [CPRA] §1798.140 |
| CMP-001.5.4 Regulatory change management |  | 4.1, 4.2, 6.3; A.5.31 | GV.OC-03, ID.IM-01 | PM-1 | — | CC3.4 | APO12, MEA03 | — |
| CMP-001.5.5 Compliance Calendar |  | 9.1; A.5.36 | GV.OV-01 | CA-7 | — | CC4.1 | MEA01, MEA03 | [PCI] 12.4.2 |
| CMP-001.5.6 Certification, attestation and assessment management |  | 9.1, 9.2; A.5.35, A.5.36 | GV.OV-01, ID.IM-01 | CA-2, CA-7 | — | CC2.3, CC4.1, CC4.2 | MEA04 | [PCI] 12.3.1, 12.4.1, 12.4.2 · [HIPAA] §164.308(a)(1)(ii)(A)–(B), §164.308(a)(8) · [CPRA] §1798.185 · [SOX] §§302, 404 |
| CMP-001.5.7 Compliance status assessment and monitoring |  | 9.1, 10.2; A.5.36 | GV.OV-01, GV.OV-03 | CA-5, CA-7 | — | CC4.1, CC4.2 | MEA01, MEA03 | [GDPR] Art. 5(2), 24 |
| CMP-001.5.8 Regulator and external inquiries |  | 4.2; A.5.5, A.5.31 | GV.OC-03, GV.SC-01 | PM-1, SA-4 | 15.4 | CC2.3, CC9.2 | APO10, MEA03 | [PCI] 12.8.5 · [GDPR] Art. 31 |
| CMP-001.5.9 Contractual obligations and customer assurance | KC-19 | 4.2; A.5.5, A.5.31 | GV.OC-03, GV.SC-01 | PM-1, SA-4 | 15.4 | CC2.3, CC9.2 | APO10, MEA03 | [PCI] 12.8.5 · [GDPR] Art. 31 |
| CMP-001.5.10 Records |  | 7.5.3; A.5.33 | GV.PO-01 | AU-11 | — | CC2.1 | MEA03 | — |

**CMP-002 Internal Audit & Control Testing Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| CMP-002.5.1 Internal Audit mandate and independence |  | 5.1, 5.3, 9.2.1; A.5.35 | GV.OV-01, GV.RR-01 | CA-2, PM-1 | — | CC1.2, CC1.5 | EDM05, MEA04 | [PCI] 12.4 · [SOX] §301 |
| CMP-002.5.2 Annual risk-based audit plan |  | 9.2.2; A.5.35 | GV.OV-01, GV.RM-01 | CA-2, PM-14 | — | CC4.1 | MEA02, MEA04 | [HIPAA] §164.308(a)(8) · [SOX] §404 |
| CMP-002.5.3 Lines of assurance |  | 9.1, 9.2; A.5.36 | GV.OV-02, ID.IM-02 | CA-2, CA-7 | — | CC4.1 | MEA01, MEA02 | [PCI] 12.4.2 · [GDPR] Art. 32(1)(d) |
| CMP-002.5.4 Engagement conduct |  | 9.1, 9.2.2; A.5.35, A.5.36 | ID.IM-02 | CA-2, CA-7 | — | CC4.1 | MEA02, MEA04 | [PCI] 12.4.2.1 · [SOX] §404 |
| CMP-002.5.5 Control testing methods | KC-20 | 9.1, 9.2.2; A.5.35, A.5.36 | ID.IM-02 | CA-2, CA-7 | — | CC4.1 | MEA02, MEA04 | [PCI] 12.4.2.1 · [SOX] §404 |
| CMP-002.5.6 Sampling |  | 9.1, 9.2.2; A.5.35, A.5.36 | ID.IM-02 | CA-2, CA-7 | — | CC4.1 | MEA02, MEA04 | [PCI] 12.4.2.1 · [SOX] §404 |
| CMP-002.5.7 Deficiency classification |  | 10.1, 10.2 | GV.OV-03, ID.IM-01 | CA-5, PM-4 | — | CC4.2, CC5.1 | BAI06, MEA02 | [HIPAA] §164.308(a)(1)(ii)(B) · [SOX] §§302, 404 |
| CMP-002.5.8 Issue management and remediation | KC-21 | 10.1, 10.2 | GV.OV-03, ID.IM-01 | CA-5, PM-4 | — | CC4.2, CC5.1 | BAI06, MEA02 | [HIPAA] §164.308(a)(1)(ii)(B) · [SOX] §§302, 404 |
| CMP-002.5.9 Coordination with External Auditors, service auditors and QSAs |  | 9.2; A.5.35, A.8.34 | GV.OV-01, GV.SC-01 | CA-2, CA-7 | — | CC2.3, CC4.1 | MEA04 | [PCI] 12.4 · [SOX] §§301, 404 |
| CMP-002.5.10 Records |  | 7.5.3; A.5.33 | GV.PO-01 | AU-11 | — | CC4.1 | MEA04 | [SOX] §404 |

**CMP-003 Policy Exception & Waiver Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| CMP-003.5.1 General principles |  | 5.1, 6.1.3; A.5.1, A.5.31, A.5.36 | GV.PO-01, GV.PO-02, GV.RM-01 | PL-1, PM-9, RA-7 | — | CC1.3, CC5.3 | APO01, APO12 | [PCI] 3.3.1, 12.1.1 · [HIPAA] §164.306(b), §164.316(a) · [GDPR] Art. 5(2), 24 |
| CMP-003.5.2 Requirements that SHALL NOT receive an Exception |  | 5.1, 6.1.3; A.5.1, A.5.31, A.5.36 | GV.PO-01, GV.PO-02, GV.RM-01 | PL-1, PM-9, RA-7 | — | CC1.3, CC5.3 | APO01, APO12 | [PCI] 3.3.1, 12.1.1 · [HIPAA] §164.306(b), §164.316(a) · [GDPR] Art. 5(2), 24 |
| CMP-003.5.3 Request content |  | 6.1.2, 6.1.3; A.5.4 | GV.RM-01, GV.RM-06, ID.RA-05 | PM-9, RA-3, RA-7 | — | CC3.2, CC5.2 | APO12 | [PCI] 12.3.1 · [HIPAA] §164.308(a)(1)(ii)(B) |
| CMP-003.5.4 Assessment and approval | KC-22 | 6.1.2, 6.1.3; A.5.4 | GV.RM-01, GV.RM-06, ID.RA-05 | PM-9, RA-3, RA-7 | — | CC3.2, CC5.2 | APO12 | [PCI] 12.3.1 · [HIPAA] §164.308(a)(1)(ii)(B) |
| CMP-003.5.5 Compensating Controls |  | 6.1.3; A.5.36 | GV.RM-01, ID.RA-06 | CA-2, PM-9 | — | CC4.1, CC5.1 | APO12, MEA02 | [PCI] Appendix B, Appendix C |
| CMP-003.5.6 Duration, renewal and expiry |  | 6.1.3, 8.3 | GV.RM-01, ID.RA-06 | PM-9, RA-7 | — | CC3.2, CC5.2 | APO12 | — |
| CMP-003.5.7 Emergency Exceptions |  | 6.1.3, 8.3 | GV.RM-01, ID.RA-06 | PM-9, RA-7 | — | CC3.2, CC5.2 | APO12 | — |
| CMP-003.5.8 Exception Register |  | 7.5, 9.1, 9.3; A.5.36 | GV.OV-01, GV.OV-03 | CA-5, PM-4, PM-9 | — | CC2.1, CC4.1, CC4.2 | APO12, MEA01, MEA02 | [SOX] §404 |
| CMP-003.5.9 Monitoring and reporting |  | 7.5, 9.1, 9.3; A.5.36 | GV.OV-01, GV.OV-03 | CA-5, PM-4, PM-9 | — | CC2.1, CC4.1, CC4.2 | APO12, MEA01, MEA02 | [SOX] §404 |

**CMP-004 Evidence Management & Records Retention Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| CMP-004.5.1 Retention governance |  | 7.5.3; A.5.31, A.5.33, A.5.34 | GV.OC-03, PR.DS-01 | AU-11, PM-21, SI-12 | 3.1, 3.4 | C1.1, C1.2, CC2.1 | APO14, BAI08 | [PCI] 3.2.1, 3.3.1, 10.5.1 · [HIPAA] §164.316(b)(2)(i), §164.530(j) · [GDPR] Art. 5(1)(e), 30 · [CPRA] §1798.100(a)(3) · [SOX] §802 |
| CMP-004.5.2 Retention schedule |  | 7.5.3; A.5.31, A.5.33, A.5.34 | GV.OC-03, PR.DS-01 | AU-11, PM-21, SI-12 | 3.1, 3.4 | C1.1, C1.2, CC2.1 | APO14, BAI08 | [PCI] 3.2.1, 3.3.1, 10.5.1 · [HIPAA] §164.316(b)(2)(i), §164.530(j) · [GDPR] Art. 5(1)(e), 30 · [CPRA] §1798.100(a)(3) · [SOX] §802 |
| CMP-004.5.3 Secure deletion at end of retention | KC-23 | A.5.33, A.7.14, A.8.10 | PR.DS-01, PR.PS-03 | MP-6, SI-12 | 3.5 | C1.2 | APO14, DSS06 | [PCI] 3.2.1, 9.4.7 · [HIPAA] §164.310(d)(2)(i) · [GDPR] Art. 5(1)(e), 17 |
| CMP-004.5.4 Legal Hold |  | A.5.31, A.5.33 | GV.OC-03 | SI-12 | 3.4 | CC2.1 | APO14 | [GDPR] Art. 17(3)(e) · [SOX] §802 |
| CMP-004.5.5 Evidence collection and quality | KC-24 | 7.5.3, 9.1; A.5.28, A.5.33, A.8.15, A.8.17 | PR.DS-01, PR.PS-04, RS.AN-03 | AU-9, AU-10, AU-11, CA-7, IR-4 | 8.10 | CC4.1, CC7.3 | DSS05, MEA01, MEA03 | [PCI] 10.3.3, 10.5.1 · [HIPAA] §164.312(b), §164.312(c)(1) |
| CMP-004.5.6 Evidence integrity and Chain of Custody |  | 7.5.3, 9.1; A.5.28, A.5.33, A.8.15, A.8.17 | PR.DS-01, PR.PS-04, RS.AN-03 | AU-9, AU-10, AU-11, CA-7, IR-4 | 8.10 | CC4.1, CC7.3 | DSS05, MEA01, MEA03 | [PCI] 10.3.3, 10.5.1 · [HIPAA] §164.312(b), §164.312(c)(1) |
| CMP-004.5.7 Evidence repository |  | 7.5.3, 9.1; A.5.28, A.5.33, A.8.15, A.8.17 | PR.DS-01, PR.PS-04, RS.AN-03 | AU-9, AU-10, AU-11, CA-7, IR-4 | 8.10 | CC4.1, CC7.3 | DSS05, MEA01, MEA03 | [PCI] 10.3.3, 10.5.1 · [HIPAA] §164.312(b), §164.312(c)(1) |
| CMP-004.5.8 Physical records |  | A.5.33, A.7.10 | PR.DS-01 | MP-4, PE-3 | — | C1.1 | DSS05 | [HIPAA] §164.310(d)(1) |

**CMP-005 Data Privacy & Protection Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| CMP-005.5.1 Privacy governance |  | 5.3; A.5.2, A.5.34 | GV.OC-03, GV.RR-02 | PM-19, PT-1 | — | CC1.3, P1.1 | APO01, APO14 | [HIPAA] §164.530(a) · [GDPR] Art. 24, 27, 37–39 |
| CMP-005.5.2 Privacy principles |  | A.5.34 | GV.PO-01 | PT-2, PT-3 | 3.1 | P1.1 | APO14 | [GDPR] Art. 5 · [CPRA] §1798.100 |
| CMP-005.5.3 Lawful basis for processing |  | A.5.31, A.5.34 | GV.OC-03 | PT-2 | — | P3.1 | MEA03 | [HIPAA] §164.502(a) · [GDPR] Art. 6, 9, 10 |
| CMP-005.5.4 Privacy Notices |  | A.5.34 | GV.OC-03 | PT-5 | — | P1.1 | MEA03 | [HIPAA] §164.520 · [GDPR] Art. 12–14 · [CPRA] §1798.100(a), §1798.130 |
| CMP-005.5.5 Consent |  | A.5.34 | GV.OC-03 | PT-4 | — | P2.1 | MEA03 | [GDPR] Art. 7, 8 · [CPRA] §1798.120(c) |
| CMP-005.5.6 Purpose limitation |  | A.5.34 | GV.PO-01 | PT-3 | 3.1 | P4.1 | APO14 | [GDPR] Art. 5(1)(b), 6(4) · [CPRA] §1798.100(c) |
| CMP-005.5.7 Data minimization and de-identification |  | A.5.34, A.8.11, A.8.33 | PR.DS-01 | PT-3, SA-3, SI-12 | 3.1, 16.8 | C1.1, P3.1 | APO14 | [HIPAA] §164.514(b) · [GDPR] Art. 5(1)(c), 25, 32 |
| CMP-005.5.8 Record of Processing Activities |  | A.5.9, A.5.34 | ID.AM-07 | PM-5, PT-3 | 3.2 | P3.1 | APO14 | [GDPR] Art. 30 |
| CMP-005.5.9 Data Protection Impact Assessments |  | 6.1.2; A.5.34 | GV.RM-01, ID.RA-01 | RA-3, RA-8 | — | CC3.2, P3.1 | APO12 | [GDPR] Art. 35, 36 |
| CMP-005.5.10 Privacy by design and by default |  | A.5.8, A.8.10, A.8.25 | PR.PS-01 | AC-6, SA-3, SA-8 | 3.1 | CC8.1, P4.2 | BAI02, BAI03 | [GDPR] Art. 22, 25 |
| CMP-005.5.11 Processor and recipient management |  | A.5.19, A.5.20, A.5.34 | GV.SC-01, GV.SC-05 | SA-9, SR-6 | 15.1, 15.4 | CC9.2, P6.1 | APO10 | [HIPAA] §164.504(e) · [GDPR] Art. 26, 28 · [CPRA] §1798.100(d) |
| CMP-005.5.12 International transfers [GDPR] (Chapter V) |  | A.5.14, A.5.34 | GV.OC-03 | SA-9 | — | P6.1 | MEA03 | [GDPR] Art. 44–49 |
| CMP-005.5.13 [CPRA] Sale, sharing and Sensitive Personal Information |  | A.5.34 | GV.OC-03 | PT-2, PT-4 | — | P2.1, P6.1 | MEA03 | [CPRA] §1798.120, §1798.121, §1798.125, §1798.135; Cal. Code Regs. tit. 11, §7025–7027 |
| CMP-005.5.14 [HIPAA] Minimum Necessary |  | A.5.15, A.5.34 | PR.AA-05 | AC-6, PT-2 | 6.8 | CC6.3 | DSS05 | [HIPAA] §164.502(b), §164.514(d) |
| CMP-005.5.15 Data Subject rights |  | A.5.34 | GV.OC-03 | PM-22, PT-2 | — | P5.1, P5.2 | MEA03 | [GDPR] Art. 12, 15–22 · [CPRA] §1798.105–.130 |
| CMP-005.5.16 Security of Personal Data and Personal Data Breaches |  | A.5.24, A.5.34 | RS.CO-02 | IR-4, IR-6 | 17.1 | CC7.3, P6.3 | DSS02 | [GDPR] Art. 32–34 (see RES-003) |
| CMP-005.5.17 Training and awareness |  | 7.2, 9.2; A.6.3 | ID.IM-01, PR.AT-01 | AT-2, AT-3, CA-2 | 14.1 | CC1.4, CC4.1 | MEA03 | [HIPAA] §164.530(b) · [GDPR] Art. 39(1)(b) |
| CMP-005.5.18 Monitoring and assurance |  | 7.2, 9.2; A.6.3 | ID.IM-01, PR.AT-01 | AT-2, AT-3, CA-2 | 14.1 | CC1.4, CC4.1 | MEA03 | [HIPAA] §164.530(b) · [GDPR] Art. 39(1)(b) |

**CMP-006 Whistleblower & Security Concern Reporting Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| CMP-006.5.1 Duty and right to report |  | 7.4; A.5.31, A.6.8 | GV.OC-03, GV.RR-04 | IR-6, PL-4 | 14.6 | CC1.1, CC2.2, CC2.3 | APO01, MEA03 | [HIPAA] §164.530(d) · [SOX] §301 · Other: EU Directive 2019/1937 Arts. 7–9; SEC Rule 21F-17 |
| CMP-006.5.2 Reporting channels |  | 7.4; A.5.31, A.6.8 | GV.OC-03, GV.RR-04 | IR-6, PL-4 | 14.6 | CC1.1, CC2.2, CC2.3 | APO01, MEA03 | [HIPAA] §164.530(d) · [SOX] §301 · Other: EU Directive 2019/1937 Arts. 7–9; SEC Rule 21F-17 |
| CMP-006.5.3 Receipt, acknowledgement and triage |  | A.5.24, A.5.26, A.5.28, A.6.8 | RS.AN-03, RS.MA-01 | AU-9, IR-4, IR-6 | 17.3 | CC2.2, CC7.3, CC7.4 | DSS02, MEA03 | [GDPR] Art. 5 · Other: EU Directive 2019/1937 Art. 9 |
| CMP-006.5.4 Investigation |  | A.5.24, A.5.26, A.5.28, A.6.8 | RS.AN-03, RS.MA-01 | AU-9, IR-4, IR-6 | 17.3 | CC2.2, CC7.3, CC7.4 | DSS02, MEA03 | [GDPR] Art. 5 · Other: EU Directive 2019/1937 Art. 9 |
| CMP-006.5.5 Confidentiality and anonymity |  | A.5.12, A.5.15, A.5.34 | PR.AA-05, PR.DS-01 | AC-3, AC-6, AU-2 | 3.3, 6.5 | C1.1, CC6.1 | DSS05 | [GDPR] Arts. 5, 30, 35 · Other: EU Directive 2019/1937 Art. 16 |
| CMP-006.5.6 Non-retaliation |  | A.5.31, A.6.4 | GV.RR-04 | PS-8 | — | CC1.1, CC1.5 | APO07 | [HIPAA] §§160.316, 164.530(g)(2) · [SOX] §806 (18 U.S.C. §1514A) · Other: EU Directive 2019/1937 Arts. 19–21 |
| CMP-006.5.7 [SOX] Audit Committee procedures for accounting and auditing complaints |  | 5.1, 9.3 | GV.OV-01, GV.RR-01 | PM-1 | — | CC1.2, CC2.3 | EDM01, MEA02 | [SOX] §301 (Exchange Act §10A(m)(4)–(6)); §§302, 404 |
| CMP-006.5.8 Reporting, oversight and records |  | 7.3, 9.1, 9.3 | GV.OV-01, PR.AT-01 | AT-2, PM-1 | 14.1, 14.6 | CC1.4, CC2.2, CC4.1 | APO07, MEA01 | Other: EU Directive 2019/1937 Art. 18 |
| CMP-006.5.9 Awareness |  | 7.3, 9.1, 9.3 | GV.OV-01, PR.AT-01 | AT-2, PM-1 | 14.1, 14.6 | CC1.4, CC2.2, CC4.1 | APO07, MEA01 | Other: EU Directive 2019/1937 Art. 18 |

**CMP-007 Enforcement & Disciplinary Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| CMP-007.5.1 Principles |  | 5.1, 7.3; A.6.4 | GV.PO-01, GV.RR-04 | PL-4, PS-8 | — | CC1.1, CC1.5 | APO07 | [PCI] 12.1 · [HIPAA] §164.308(a)(1)(ii)(C); §164.530(e) |
| CMP-007.5.2 Violation categories |  | 5.1, 7.3; A.6.4 | GV.PO-01, GV.RR-04 | PL-4, PS-8 | — | CC1.1, CC1.5 | APO07 | [PCI] 12.1 · [HIPAA] §164.308(a)(1)(ii)(C); §164.530(e) |
| CMP-007.5.3 Sanctions matrix |  | 5.1, 7.3; A.6.4 | GV.PO-01, GV.RR-04 | PL-4, PS-8 | — | CC1.1, CC1.5 | APO07 | [PCI] 12.1 · [HIPAA] §164.308(a)(1)(ii)(C); §164.530(e) |
| CMP-007.5.4 Process and due process | KC-25 | A.5.28, A.6.4, A.6.5 | GV.RR-04 | AC-2, PS-4, PS-8 | 5.3, 6.2 | CC1.5, CC6.2 | APO07 | [GDPR] Art. 88 (employment context) · Other: local employment law |
| CMP-007.5.5 Third Parties |  | A.5.19, A.5.20, A.5.22 | GV.SC-05, GV.SC-07 | PS-7, SA-9, SR-6 | 15.4, 15.7 | CC9.2 | APO10 | [PCI] 12.8 · [HIPAA] §164.504(e)(1)(ii) · [GDPR] Art. 28 |
| CMP-007.5.6 [HIPAA] Sanction policy |  | A.6.4 | GV.RR-04 | PS-8 | — | CC1.5 | APO07, MEA03 | [HIPAA] §§164.308(a)(1)(ii)(C), 164.502(j), 164.530(e), 164.530(g) |
| CMP-007.5.7 Documentation and records |  | 7.5, 9.1, 10.2 | GV.OV-01, ID.IM-01 | PM-1, PS-8 | — | CC1.5, CC4.1 | APO07, MEA01 | [HIPAA] §164.530(e)(2) |

**CMP-008 HIPAA Security Rule Implementation Standard**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| CMP-008.5.1 HIPAA status and general requirements (§164.306) |  | 4.2, 4.3; A.5.31 | GV.OC-03 | PL-2, PM-9 | — | CC1.1, CC2.2 | APO01, MEA03 | [HIPAA] §164.306 |
| CMP-008.5.2 HIPAA Security Officer (§164.308(a)(2)) |  | 5.3; A.5.2 | GV.RR-02 | PM-2 | — | CC1.3 | APO01 | [HIPAA] §164.308(a)(2) |
| CMP-008.5.3 ePHI risk analysis (§164.308(a)(1)(ii)(A)) and risk management (§164.308(a)(1)(ii)(B)) |  | 6.1.2, 8.2; A.5.9, A.5.12 | GV.RM-01, ID.RA-01, ID.RA-05 | PM-9, RA-2, RA-3 | 3.2 | CC3.1, CC3.2 | APO12 | [HIPAA] §164.308(a)(1)(ii)(A)–(B) |
| CMP-008.5.4 Sanctions and information system activity review (§164.308(a)(1)(ii)(C)–(D)) |  | 7.3; A.6.4, A.8.15, A.8.16 | DE.AE-02, DE.CM-01 | AU-6, PS-8 | 8.11 | CC1.5, CC7.2 | DSS05 | [HIPAA] §164.308(a)(1)(ii)(C)–(D) |
| CMP-008.5.5 Addressable implementation specification decisions (§164.306(d)(3)) |  | 6.1.3 | GV.RM-01 | PL-2, RA-3 | — | CC3.2, CC5.1 | APO12 | [HIPAA] §164.306(d)(3); §164.316 |
| CMP-008.5.6 Implementation matrix: administrative safeguards (§164.308) |  | A.5.15, A.5.18, A.5.24, A.5.25, A.5.26, A.5.27, A.5.28, A.5.29, A.6.1, A.6.3, A.6.5, A.8.7, A.8.13 | PR.AA-05, PR.AT-01, RC.RP-01, RS.MA-01 | AC-2, AT-2, CP-2, CP-9, IR-4, PS-3, PS-4 | 5.3, 6.1, 6.2, 10.1, 11.2, 14.1, 17.1 | A1.2, A1.3, CC6.2, CC6.3, CC7.4 | DSS04, DSS05, DSS06 | [HIPAA] §164.308 |
| CMP-008.5.7 Implementation matrix: physical safeguards (§164.310) |  | A.7.1, A.7.2, A.7.3, A.7.4, A.7.9, A.7.10, A.7.14, A.8.1 | PR.AA-06, PR.DS-01 | MP-5, MP-6, PE-2, PE-3 | 1.1, 3.5 | CC6.4, CC6.5 | DSS01, DSS05 | [HIPAA] §164.310 |
| CMP-008.5.8 Implementation matrix: technical safeguards (§164.312) |  | A.5.17, A.8.2, A.8.5, A.8.15, A.8.24 | PR.AA-01, PR.DS-01, PR.DS-02, PR.PS-04 | AC-3, AU-2, IA-2, SC-8, SC-13, SC-28, SI-7 | 3.10, 3.11, 6.3, 8.2 | CC6.1, CC6.7, CC7.2 | DSS05 | [HIPAA] §164.312 |
| CMP-008.5.9 Implementation matrix: organizational requirements (§164.314) |  | A.5.19, A.5.20, A.5.21 | GV.SC-05, GV.SC-07 | SA-9, SR-3 | 15.4 | CC9.2 | APO10 | [HIPAA] §164.308(b), §164.314, §164.410 |
| CMP-008.5.10 Implementation matrix: policies, procedures and documentation (§164.316) |  | 7.5; A.5.33 | GV.PO-01 | AU-11, PL-1 | — | CC2.2 | APO01, BAI08 | [HIPAA] §164.316 |
| CMP-008.5.11 Evaluation (§164.308(a)(8)) |  | 9.1, 9.2; A.5.35 | GV.OV-01, ID.IM-01 | CA-2, CA-7 | — | CC4.1, CC4.2 | MEA02, MEA03 | [HIPAA] §164.308(a)(8) |

**CMP-009 SOX IT General Controls Standard**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| CMP-009.5.1 General |  | 4.3, 6.1.3; A.5.9, A.5.31 | GV.OC-03, ID.AM-02 | CM-8, PM-5 | 1.1, 2.1 | CC1.4, CC2.1, CC3.1 | APO01, MEA03 | [SOX] §§302, 404; PCAOB AS 2201 |
| CMP-009.5.2 Scoping Financially Significant Systems |  | 4.3, 6.1.3; A.5.9, A.5.31 | GV.OC-03, ID.AM-02 | CM-8, PM-5 | 1.1, 2.1 | CC1.4, CC2.1, CC3.1 | APO01, MEA03 | [SOX] §§302, 404; PCAOB AS 2201 |
| CMP-009.5.3 ITGC domains |  | 4.3, 6.1.3; A.5.9, A.5.31 | GV.OC-03, ID.AM-02 | CM-8, PM-5 | 1.1, 2.1 | CC1.4, CC2.1, CC3.1 | APO01, MEA03 | [SOX] §§302, 404; PCAOB AS 2201 |
| CMP-009.5.4 Access to programs and data (APD) |  | A.5.3, A.5.15, A.5.16, A.5.18, A.8.2, A.8.5 | PR.AA-01, PR.AA-05 | AC-2, AC-5, AC-6, AU-6, IA-2 | 5.1, 5.3, 6.1, 6.2, 6.8 | CC6.1, CC6.2, CC6.3 | DSS05, DSS06 | [SOX] §404 |
| CMP-009.5.5 Program change (PC) |  | A.8.9, A.8.31, A.8.32 | PR.PS-01 | CM-3, CM-5, CM-6 | 4.1, 16.1 | CC8.1 | BAI06, BAI07 | [SOX] §404 |
| CMP-009.5.6 Program development (PD) |  | A.5.8, A.8.25, A.8.29, A.8.33 | PR.PS-06 | SA-3, SA-8, SA-11 | 16.1 | CC8.1 | BAI03, BAI07 | [SOX] §404 |
| CMP-009.5.7 Computer operations (CO) |  | A.8.6, A.8.13, A.8.15 | DE.CM-09, PR.DS-11 | AU-6, CP-9, CP-10 | 11.2, 11.5 | A1.2, A1.3, CC7.2 | DSS01, DSS04 | [SOX] §404 |
| CMP-009.5.8 Information Produced by the Entity (IPE) and report controls |  | A.5.33, A.8.32 | PR.DS-01 | CM-3, SI-10 | 3.1 | CC2.1, CC8.1 | DSS06 | [SOX] §404; PCAOB AS 1105 |
| CMP-009.5.9 Service organizations and SOC 1 reliance |  | A.5.19, A.5.20, A.5.22 | GV.SC-07 | SA-9, SR-6 | 15.5, 15.6 | CC9.2 | APO10 | [SOX] §404; AICPA SSAE 18 (AT-C 320) |
| CMP-009.5.10 Control testing and quarterly support for §302 certification |  | 9.1, 9.2; A.5.35, A.5.36 | GV.OV-01, ID.IM-01 | CA-2, CA-7 | — | CC4.1 | MEA02 | [SOX] §302; §404(a); Reg. S-K Item 308 |
| CMP-009.5.11 Deficiency evaluation and escalation |  | 10.2 | GV.OV-02, ID.IM-01 | CA-5, PM-4 | — | CC4.2, CC5.1 | MEA02, MEA03 | [SOX] §§302, 404; PCAOB AS 2201 |
| CMP-009.5.12 Remediation |  | 10.2 | GV.OV-02, ID.IM-01 | CA-5, PM-4 | — | CC4.2, CC5.1 | MEA02, MEA03 | [SOX] §§302, 404; PCAOB AS 2201 |

**CMP-010 Data Subject Request Procedure**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| CMP-010.5.1 Intake channels |  | A.5.31, A.5.34 | GV.OC-03 | PM-26, PT-5 | 3.1 | P1.1, P5.1 | APO13, MEA03 | [GDPR] Art. 12 · [CPRA] §1798.130, §1798.135; Cal. Code Regs. tit. 11, §§7025–7027 |
| CMP-010.5.2 Logging and triage |  | A.5.31, A.5.34 | GV.OC-03 | PM-26, PT-5 | 3.1 | P1.1, P5.1 | APO13, MEA03 | [GDPR] Art. 12 · [CPRA] §1798.130, §1798.135; Cal. Code Regs. tit. 11, §§7025–7027 |
| CMP-010.5.3 Deadlines |  | A.5.31, A.5.34 | GV.OC-03 | PM-26, PT-5 | 3.1 | P1.1, P5.1 | APO13, MEA03 | [GDPR] Art. 12 · [CPRA] §1798.130, §1798.135; Cal. Code Regs. tit. 11, §§7025–7027 |
| CMP-010.5.4 Identity verification by risk |  | A.5.16, A.5.34 | PR.AA-02 | IA-12, PM-26 | — | P5.1 | DSS05 | [GDPR] Art. 11, 12(6) · [CPRA] Cal. Code Regs. tit. 11, §§7060–7063 |
| CMP-010.5.5 Authorized Agents |  | A.5.16, A.5.34 | PR.AA-02 | IA-12, PM-26 | — | P5.1 | DSS05 | [GDPR] Art. 11, 12(6) · [CPRA] Cal. Code Regs. tit. 11, §§7060–7063 |
| CMP-010.5.6 Locating Personal Data |  | A.5.12, A.5.34 | ID.AM-07 | PM-5, PT-2, SI-18 | 3.2 | P4.3, P5.1, P5.2 | APO14 | [GDPR] Art. 7(3), 15–22 · [CPRA] §§1798.100–1798.125 |
| CMP-010.5.7 Handling each right: GDPR [GDPR] |  | A.5.12, A.5.34 | ID.AM-07 | PM-5, PT-2, SI-18 | 3.2 | P4.3, P5.1, P5.2 | APO14 | [GDPR] Art. 7(3), 15–22 · [CPRA] §§1798.100–1798.125 |
| CMP-010.5.8 Handling each right: CPRA [CPRA] |  | A.5.12, A.5.34 | ID.AM-07 | PM-5, PT-2, SI-18 | 3.2 | P4.3, P5.1, P5.2 | APO14 | [GDPR] Art. 7(3), 15–22 · [CPRA] §§1798.100–1798.125 |
| CMP-010.5.9 Extensions and extension notices |  | A.5.34 | GV.OC-03 | PM-26 | — | P5.1 | MEA03 | [GDPR] Art. 12(3) · [CPRA] §1798.130(a)(2) |
| CMP-010.5.10 Processor, Subprocessor and recipient flow-down |  | A.5.19, A.5.20, A.5.34 | GV.SC-05 | PM-26, SA-9 | 15.4 | CC9.2, P6.1 | APO10 | [GDPR] Art. 19, 28(3)(e) · [CPRA] §1798.105(c) |
| CMP-010.5.11 When the Organization is a Processor |  | A.5.19, A.5.20, A.5.34 | GV.SC-05 | PM-26, SA-9 | 15.4 | CC9.2, P6.1 | APO10 | [GDPR] Art. 19, 28(3)(e) · [CPRA] §1798.105(c) |
| CMP-010.5.12 Exemptions, refusals and fees |  | A.5.34 | GV.OC-03 | PM-26 | — | P5.1 | MEA03 | [GDPR] Art. 12(4)–(5), 17(3), 23 · [CPRA] §§1798.105(d), 1798.145, 1798.146 |
| CMP-010.5.13 Response delivery and closure |  | A.5.14, A.8.24 | PR.DS-02 | SC-8 | 3.10 | C1.1, P6.1 | DSS05 | [GDPR] Art. 12(1), 32 |
| CMP-010.5.14 Logging and records |  | 7.5; A.5.33 | GV.OV-01 | AU-11, PM-26 | — | P8.1 | MEA01 | [GDPR] Art. 5(2) · [CPRA] Cal. Code Regs. tit. 11, §§7101–7102 |
| CMP-010.5.15 CPRA metrics disclosure [CPRA] |  | 7.5; A.5.33 | GV.OV-01 | AU-11, PM-26 | — | P8.1 | MEA01 | [GDPR] Art. 5(2) · [CPRA] Cal. Code Regs. tit. 11, §§7101–7102 |

#### 5.3.5 Security controls

**SEC-001 Asset Management Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| SEC-001.5.1 Asset Inventory |  | A.5.9, A.5.12 | ID.AM-01, ID.AM-02, ID.AM-04, ID.AM-07 | CM-8, PM-5 | 1.1, 2.1, 3.2, 5.1, 15.1 | CC3.2, CC6.1 | BAI09, BAI10 | [PCI] 6.3.2, 12.5.1 · [HIPAA] §164.310(d)(1) · [SOX] §404 |
| SEC-001.5.2 Inventory scope by asset category |  | A.5.9, A.5.12 | ID.AM-01, ID.AM-02, ID.AM-04, ID.AM-07 | CM-8, PM-5 | 1.1, 2.1, 3.2, 5.1, 15.1 | CC3.2, CC6.1 | BAI09, BAI10 | [PCI] 6.3.2, 12.5.1 · [HIPAA] §164.310(d)(1) · [SOX] §404 |
| SEC-001.5.3 Required inventory attributes |  | A.5.9, A.5.12 | ID.AM-01, ID.AM-02, ID.AM-04, ID.AM-07 | CM-8, PM-5 | 1.1, 2.1, 3.2, 5.1, 15.1 | CC3.2, CC6.1 | BAI09, BAI10 | [PCI] 6.3.2, 12.5.1 · [HIPAA] §164.310(d)(1) · [SOX] §404 |
| SEC-001.5.4 Ownership assignment |  | A.5.9 | GV.RR-02, ID.AM-01 | CM-8, PM-5 | 1.1 | CC1.3, CC6.1 | BAI09 | [HIPAA] §164.310(d)(2)(iii) |
| SEC-001.5.5 Unknown and unauthorized assets |  | A.5.9 | DE.CM-01, ID.AM-01 | CM-8 | 1.2, 1.3, 1.4 | CC6.1, CC7.1 | BAI09 | [PCI] 12.5.1 |
| SEC-001.5.6 Shadow IT |  | A.5.9, A.5.23 | GV.SC-04, ID.AM-02, ID.AM-04 | CM-10, CM-11, SA-9 | 2.3, 15.1 | CC6.8, CC9.2 | APO10, BAI09 | [GDPR] Art. 28, 30 |
| SEC-001.5.7 Asset lifecycle |  | A.5.9, A.5.11, A.7.14 | ID.AM-08 | CM-8, SA-22 | 1.1, 2.2 | CC6.5, CC8.1 | BAI09 | [HIPAA] §164.310(d)(2)(ii) |
| SEC-001.5.8 Software allowlisting |  | A.8.19 | PR.PS-05 | CM-7, CM-10, CM-11 | 2.5, 2.6, 2.7 | CC6.8 | DSS05 | — |
| SEC-001.5.9 Reconciliation and verification | KC-26 | A.5.9 | ID.AM-01, ID.AM-02, ID.AM-08 | CM-8 | 1.1, 2.1 | CC3.2, CC4.1 | BAI09, MEA01 | [PCI] 12.5.1, 12.5.2 · [SOX] §404 |

**SEC-002 Data Classification & Handling Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| SEC-002.5.1 Classification Levels |  | A.5.9, A.5.12 | ID.AM-05, ID.AM-07 | PM-5, RA-2 | 3.1, 3.2, 3.7 | C1.1, CC3.2 | APO14, BAI08 | [HIPAA] §164.308(a)(1)(ii)(A) · [GDPR] Art. 5(1)(f), 9, 30 · [CPRA] §1798.140(ae) |
| SEC-002.5.2 Classification criteria and examples |  | A.5.9, A.5.12 | ID.AM-05, ID.AM-07 | PM-5, RA-2 | 3.1, 3.2, 3.7 | C1.1, CC3.2 | APO14, BAI08 | [HIPAA] §164.308(a)(1)(ii)(A) · [GDPR] Art. 5(1)(f), 9, 30 · [CPRA] §1798.140(ae) |
| SEC-002.5.3 Data Owner duties | KC-27 | A.5.9, A.5.12 | ID.AM-05, ID.AM-07 | PM-5, RA-2 | 3.1, 3.2, 3.7 | C1.1, CC3.2 | APO14, BAI08 | [HIPAA] §164.308(a)(1)(ii)(A) · [GDPR] Art. 5(1)(f), 9, 30 · [CPRA] §1798.140(ae) |
| SEC-002.5.4 Handling matrix |  | A.5.10, A.5.12, A.5.13, A.5.14, A.7.7, A.7.10, A.8.11 | GV.SC-07, PR.DS-01, PR.DS-02, PR.DS-10 | AC-21, MP-3, MP-4, MP-5, SA-9, SC-8, SC-28 | 3.3, 3.6, 3.9, 3.10, 3.11 | C1.1, CC6.1, CC6.7, CC9.2 | APO14, DSS05, DSS06 | [PCI] 3.2.1, 3.3.1, 3.5.1, 4.2.2, 6.5.5, 9.4 · [HIPAA] §164.312(a)(2)(iv), (e)(1) · [GDPR] Art. 28, 32; Art. 28, 35 |
| SEC-002.5.5 Data Loss Prevention |  | A.8.12 | DE.CM-01, PR.DS-01, PR.DS-02 | AC-4, SC-7, SI-4 | 3.13, 3.14 | C1.1, CC6.7 | DSS05 | [PCI] 12.5.2, 12.10.7 · [HIPAA] §164.312(b) |
| SEC-002.5.6 Reclassification |  | A.5.12 | ID.AM-07 | RA-2 | 3.7 | C1.1 | APO14 | [GDPR] Art. 4(5), 89 |
| SEC-002.5.7 Third Parties |  | A.5.14, A.5.20 | GV.SC-05 | PS-7, SA-9 | 15.4 | C1.1, CC9.2 | APO10 | [HIPAA] §164.308(b)(1) · [GDPR] Art. 28 |

**SEC-003 Identity & Access Management Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| SEC-003.5.1 Identity principles |  | A.5.15, A.5.16 | PR.AA-01, PR.AA-05 | AC-1, AC-2, IA-2, IA-4 | 5.1, 6.6, 6.7 | CC6.1, CC6.2 | DSS05.04 | [PCI] 8.2.1 · [HIPAA] §164.312(a)(2)(i) · [SOX] §404 |
| SEC-003.5.2 Joiner |  | A.5.16, A.5.18, A.6.1 | PR.AA-01, PR.AA-02, PR.AA-05 | AC-2, IA-12, PS-3, PS-5 | 6.1 | CC6.2, CC6.3 | APO07, DSS05.04 | [PCI] 7.2.1, 8.2.4 · [HIPAA] §164.308(a)(3)(ii)(B), (a)(4)(ii)(C) |
| SEC-003.5.3 Mover | KC-28 | A.5.16, A.5.18, A.6.1 | PR.AA-01, PR.AA-02, PR.AA-05 | AC-2, IA-12, PS-3, PS-5 | 6.1 | CC6.2, CC6.3 | APO07, DSS05.04 | [PCI] 7.2.1, 8.2.4 · [HIPAA] §164.308(a)(3)(ii)(B), (a)(4)(ii)(C) |
| SEC-003.5.4 Access request and approval | KC-29 | A.5.15, A.5.18, A.8.2, A.8.3 | PR.AA-05 | AC-3, AC-5, AC-6 | 6.1, 6.8 | CC5.2, CC6.1, CC6.3 | DSS05.04 | [PCI] 7.2.1, 7.2.2, 7.2.3, 7.2.6 · [HIPAA] §164.308(a)(4)(ii)(B); §164.502(b) |
| SEC-003.5.5 Role-based access |  | A.5.15, A.5.18, A.8.2, A.8.3 | PR.AA-05 | AC-3, AC-5, AC-6 | 6.1, 6.8 | CC5.2, CC6.1, CC6.3 | DSS05.04 | [PCI] 7.2.1, 7.2.2, 7.2.3, 7.2.6 · [HIPAA] §164.308(a)(4)(ii)(B); §164.502(b) |
| SEC-003.5.6 Least Privilege and Need to Know |  | A.5.15, A.5.18, A.8.2, A.8.3 | PR.AA-05 | AC-3, AC-5, AC-6 | 6.1, 6.8 | CC5.2, CC6.1, CC6.3 | DSS05.04 | [PCI] 7.2.1, 7.2.2, 7.2.3, 7.2.6 · [HIPAA] §164.308(a)(4)(ii)(B); §164.502(b) |
| SEC-003.5.7 Leaver | KC-30 | A.5.18, A.6.5 | PR.AA-01, PR.AA-05 | AC-2, PS-4 | 5.3, 6.2 | CC6.2, CC6.3 | DSS05.04 | [PCI] 8.2.5, 8.2.6 · [HIPAA] §164.308(a)(3)(ii)(C) |
| SEC-003.5.8 Inactive and temporary accounts |  | A.5.18, A.6.5 | PR.AA-01, PR.AA-05 | AC-2, PS-4 | 5.3, 6.2 | CC6.2, CC6.3 | DSS05.04 | [PCI] 8.2.5, 8.2.6 · [HIPAA] §164.308(a)(3)(ii)(C) |
| SEC-003.5.9 Service Account governance |  | A.5.16, A.5.17 | PR.AA-01, PR.AA-03 | AC-2, IA-9 | 5.5 | CC6.1, CC6.2 | DSS05.04 | [PCI] 7.2.5, 7.2.5.1, 8.6.1 |
| SEC-003.5.10 Third-Party access |  | A.5.19, A.5.20 | GV.SC-05, PR.AA-05 | AC-2, AC-17, PS-7 | 6.1, 6.2 | CC6.2, CC9.2 | APO10, DSS05.04 | [PCI] 8.2.3, 8.2.7 · [HIPAA] §164.308(b)(1) |
| SEC-003.5.11 Shared and generic accounts |  | A.5.16 | PR.AA-01 | AC-2, IA-2 | 5.1 | CC6.1 | DSS05.04 | [PCI] 2.2.2, 8.2.2 |
| SEC-003.5.12 Access Reviews | KC-31 | A.5.18 | ID.IM-01, PR.AA-05 | AC-2, AC-6 | 5.1, 5.3 | CC4.1, CC6.2, CC6.3 | DSS05.04, MEA02 | [PCI] 7.2.4 · [HIPAA] §164.308(a)(4)(ii)(C) · [SOX] §404 |
| SEC-003.5.13 Access to identity infrastructure |  | A.5.15, A.8.15 | DE.CM-03, PR.AA-01 | AC-2, AU-2 | 6.6, 8.2 | CC6.1, CC7.2 | DSS05 | [PCI] 10.2.1.5 |

**SEC-004 Password & Authentication Standard**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| SEC-004.5.1 General |  | A.5.17, A.8.5 | PR.AA-01, PR.AA-03 | IA-5 | 5.2 | CC6.1 | DSS05.04 | [PCI] 8.3.5, 8.3.6, 8.3.7, 8.3.9 · [HIPAA] §164.308(a)(5)(ii)(D) |
| SEC-004.5.2 Password construction |  | A.5.17, A.8.5 | PR.AA-01, PR.AA-03 | IA-5 | 5.2 | CC6.1 | DSS05.04 | [PCI] 8.3.5, 8.3.6, 8.3.7, 8.3.9 · [HIPAA] §164.308(a)(5)(ii)(D) |
| SEC-004.5.3 Password change and rotation |  | A.5.17, A.8.5 | PR.AA-01, PR.AA-03 | IA-5 | 5.2 | CC6.1 | DSS05.04 | [PCI] 8.3.5, 8.3.6, 8.3.7, 8.3.9 · [HIPAA] §164.308(a)(5)(ii)(D) |
| SEC-004.5.4 Multi-Factor Authentication | KC-32 | A.8.5 | PR.AA-03 | IA-2 | 6.3, 6.4, 6.5 | CC6.1, CC6.6 | DSS05.04 | [PCI] 8.4.1, 8.4.2, 8.4.3, 8.5.1 · [HIPAA] §164.312(d) |
| SEC-004.5.5 Single Sign-On |  | A.5.16, A.8.5 | PR.AA-01, PR.AA-04 | IA-2, IA-8 | 6.7, 12.5 | CC6.1 | DSS05.04 | — |
| SEC-004.5.6 Breached-password screening |  | A.5.17 | PR.AA-01 | IA-5 | 5.2 | CC6.1 | DSS05.04 | — |
| SEC-004.5.7 Account lockout and throttling |  | A.8.5 | PR.AA-03 | AC-7, AC-11, AC-12, SC-23 | 4.3 | CC6.1 | DSS05.04 | [PCI] 8.2.8, 8.3.4 · [HIPAA] §164.312(a)(2)(iii) |
| SEC-004.5.8 Session management |  | A.8.5 | PR.AA-03 | AC-7, AC-11, AC-12, SC-23 | 4.3 | CC6.1 | DSS05.04 | [PCI] 8.2.8, 8.3.4 · [HIPAA] §164.312(a)(2)(iii) |
| SEC-004.5.9 Credential storage |  | A.5.17, A.8.24 | PR.AA-01, PR.DS-01 | IA-5, SC-28 | 3.11 | CC6.1 | DSS05 | [PCI] 8.3.2 |
| SEC-004.5.10 Secrets in code and configuration |  | A.5.17, A.8.4 | PR.AA-01, PR.PS-06 | IA-5, SA-11 | 16.1 | CC6.1, CC8.1 | BAI03 | [PCI] 8.6.2 |
| SEC-004.5.11 Authentication for APIs and machines |  | A.8.5 | PR.AA-03, PR.AA-04 | IA-3, IA-9, SC-8 | 5.5, 16.1 | CC6.1 | DSS05 | [PCI] 8.3.10, 8.6.3 |
| SEC-004.5.12 Customer-facing applications |  | A.8.5 | PR.AA-03, PR.AA-04 | IA-3, IA-9, SC-8 | 5.5, 16.1 | CC6.1 | DSS05 | [PCI] 8.3.10, 8.6.3 |

**SEC-005 Privileged Access Management Standard**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| SEC-005.5.1 Privileged Account inventory |  | A.5.16, A.8.2 | PR.AA-01, PR.AA-05 | AC-2, AC-6 | 5.4, 6.6 | CC6.1, CC6.3 | DSS05.04 | [PCI] 7.2.1, 7.2.2, 8.2.1 |
| SEC-005.5.2 Separate administrative accounts |  | A.5.16, A.8.2 | PR.AA-01, PR.AA-05 | AC-2, AC-6 | 5.4, 6.6 | CC6.1, CC6.3 | DSS05.04 | [PCI] 7.2.1, 7.2.2, 8.2.1 |
| SEC-005.5.3 PAM vaulting | KC-33 | A.5.17, A.8.2 | PR.AA-01 | AC-2, IA-5 | 5.2, 5.5 | CC6.1 | DSS05.04 | [PCI] 8.3.2, 8.6.2, 8.6.3 |
| SEC-005.5.4 Just-in-Time access |  | A.8.2 | PR.AA-05 | AC-2, AC-6 | 6.8 | CC6.3 | DSS05.04 | [PCI] 7.2.2 |
| SEC-005.5.5 Session management and recording |  | A.8.15, A.8.16 | DE.CM-03, PR.PS-04 | AU-2, AU-12, AU-14 | 8.2, 8.5 | CC7.2 | DSS05.07 | [PCI] 10.2.1.2 · [HIPAA] §164.312(b) · [SOX] §404 |
| SEC-005.5.6 Privileged Access Workstations |  | A.8.1, A.8.2 | PR.AA-05, PR.PS-01 | AC-6, SC-7 | 12.8 | CC6.1, CC6.8 | DSS05.03 | — |
| SEC-005.5.7 Break-glass Accounts |  | A.5.29, A.8.2 | PR.AA-05, RC.RP-01 | AC-2, AC-6, CP-2 | 5.4, 6.5 | A1.2, CC6.1 | DSS04, DSS05 | [HIPAA] §164.312(a)(2)(ii) |
| SEC-005.5.8 Cloud root and owner accounts |  | A.5.29, A.8.2 | PR.AA-05, RC.RP-01 | AC-2, AC-6, CP-2 | 5.4, 6.5 | A1.2, CC6.1 | DSS04, DSS05 | [HIPAA] §164.312(a)(2)(ii) |
| SEC-005.5.9 Privileged Service Accounts |  | A.5.19, A.8.2 | GV.SC-05, PR.AA-05 | AC-6, IA-9, PS-7 | 5.5, 6.5 | CC6.1, CC9.2 | APO10, DSS05 | [PCI] 8.2.7, 8.6.1 |
| SEC-005.5.10 Third-Party privileged access |  | A.5.19, A.8.2 | GV.SC-05, PR.AA-05 | AC-6, IA-9, PS-7 | 5.5, 6.5 | CC6.1, CC9.2 | APO10, DSS05 | [PCI] 8.2.7, 8.6.1 |
| SEC-005.5.11 Privileged access review | KC-34 | A.5.18, A.8.2 | PR.AA-05 | AC-2, AC-6 | 5.4, 6.2 | CC6.2, CC6.3 | DSS05.04 | [PCI] 7.2.4, 7.2.5.1 · [SOX] §404 |
| SEC-005.5.12 Privileged access lifecycle |  | A.5.18, A.8.2 | PR.AA-05 | AC-2, AC-6 | 5.4, 6.2 | CC6.2, CC6.3 | DSS05.04 | [PCI] 7.2.4, 7.2.5.1 · [SOX] §404 |

**SEC-006 Cryptography & Key Management Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| SEC-006.5.1 Use of cryptography |  | A.8.24 | PR.DS-01, PR.DS-02 | SC-8, SC-13, SC-28 | 3.10, 3.11 | CC6.1, CC6.7 | DSS05.02 | [PCI] 3.5.1, 3.5.1.2, 4.2.1, 12.3.3 · [HIPAA] §164.312(a)(2)(iv), (e)(2)(ii) · [GDPR] Art. 32(1)(a) |
| SEC-006.5.2 Approved algorithms and protocols | KC-35 | A.8.24 | PR.DS-01, PR.DS-02 | SC-8, SC-13, SC-28 | 3.10, 3.11 | CC6.1, CC6.7 | DSS05.02 | [PCI] 3.5.1, 3.5.1.2, 4.2.1, 12.3.3 · [HIPAA] §164.312(a)(2)(iv), (e)(2)(ii) · [GDPR] Art. 32(1)(a) |
| SEC-006.5.3 Key management roles and inventory |  | A.8.24 | PR.DS-01 | SC-12, SC-13 | 3.11 | CC6.1 | DSS05.02 | [PCI] 3.6.1, 3.6.1.1, 3.6.1.2, 3.6.1.3, 3.6.1.4, 3.7.1, 3.7.2, 3.7.3, 3.7.8 |
| SEC-006.5.4 Key generation |  | A.8.24 | PR.DS-01 | SC-12, SC-13 | 3.11 | CC6.1 | DSS05.02 | [PCI] 3.6.1, 3.6.1.1, 3.6.1.2, 3.6.1.3, 3.6.1.4, 3.7.1, 3.7.2, 3.7.3, 3.7.8 |
| SEC-006.5.5 Key distribution |  | A.8.24 | PR.DS-01 | SC-12, SC-13 | 3.11 | CC6.1 | DSS05.02 | [PCI] 3.6.1, 3.6.1.1, 3.6.1.2, 3.6.1.3, 3.6.1.4, 3.7.1, 3.7.2, 3.7.3, 3.7.8 |
| SEC-006.5.6 Key storage |  | A.8.24 | PR.DS-01 | SC-12, SC-13 | 3.11 | CC6.1 | DSS05.02 | [PCI] 3.6.1, 3.6.1.1, 3.6.1.2, 3.6.1.3, 3.6.1.4, 3.7.1, 3.7.2, 3.7.3, 3.7.8 |
| SEC-006.5.7 Cryptoperiods and rotation |  | A.8.24 | PR.DS-01 | SC-12 | 3.11 | CC6.1 | DSS05.02 | [PCI] 3.7.4, 3.7.5 |
| SEC-006.5.8 Key revocation and compromise |  | A.8.24 | PR.DS-01 | SC-12 | 3.11 | CC6.1 | DSS05.02 | [PCI] 3.7.4, 3.7.5 |
| SEC-006.5.9 Key destruction |  | A.8.24 | PR.DS-01 | SC-12 | 3.11 | CC6.1 | DSS05.02 | [PCI] 3.7.4, 3.7.5 |
| SEC-006.5.10 Dual control and split knowledge |  | A.5.3, A.8.24 | PR.AA-05 | AC-5, SC-12 | — | CC6.1 | DSS05.02 | [PCI] 3.7.6, 3.7.7, 3.7.9 |
| SEC-006.5.11 Certificate management |  | A.8.24 | PR.AA-03, PR.DS-02 | SC-12, SC-17 | 3.10 | CC6.1, CC6.7 | DSS05.02 | [PCI] 4.2.1, 4.2.1.1 |
| SEC-006.5.12 Crypto-agility |  | A.5.7, A.8.24 | ID.AM-02, ID.IM-01, ID.RA-01 | SA-8, SC-12, SC-13 | 2.1 | CC3.2, CC6.1 | APO13, BAI03 | [PCI] 12.3.3 |
| SEC-006.5.13 Post-Quantum Cryptography |  | A.5.7, A.8.24 | ID.AM-02, ID.IM-01, ID.RA-01 | SA-8, SC-12, SC-13 | 2.1 | CC3.2, CC6.1 | APO13, BAI03 | [PCI] 12.3.3 |
| SEC-006.5.14 Third Parties and Cloud Services |  | A.5.19, A.5.23 | GV.SC-05 | SA-9 | 15.4 | CC9.2 | APO10 | [GDPR] Art. 28, 32 |

**SEC-007 Network Security Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| SEC-007.5.1 Network architecture and zoning |  | A.8.20, A.8.22, A.8.27 | ID.AM-03, PR.IR-01 | AC-4, SC-7 | 12.2, 13.4 | CC6.1, CC6.6 | DSS05.02 | [PCI] 1.2, 1.3, 1.4 · [HIPAA] §164.312(e)(1) |
| SEC-007.5.2 Default-deny traffic control |  | A.8.9, A.8.20, A.8.21 | PR.IR-01, PR.PS-01 | CM-6, CM-7, SC-7 | 4.2, 4.4, 4.5, 13.4 | CC6.6 | DSS05.02 | [PCI] 1.2.1, 1.2.5, 1.3.1, 1.3.2 |
| SEC-007.5.3 Firewall and security-group rule review | KC-36 | A.5.15, A.8.20 | PR.IR-01 | CA-7, SC-7 | 4.2, 12.3 | CC6.6, CC7.1 | DSS05.02 | [PCI] 1.2.7 |
| SEC-007.5.4 Remote access |  | A.6.7, A.8.5 | PR.AA-03, PR.IR-01 | AC-17, IA-2 | 6.4, 12.7 | CC6.1, CC6.6 | DSS05.02, DSS05.04 | [PCI] 8.4.2, 8.4.3, 12.8 · [HIPAA] §164.312(d) |
| SEC-007.5.5 Wireless networks |  | A.8.20 | PR.IR-01 | AC-18 | 12.6 | CC6.6 | DSS05.02 | [PCI] 2.3, 11.2.1 |
| SEC-007.5.6 DNS and egress filtering |  | A.8.20, A.8.23 | DE.CM-01, PR.IR-01 | SC-7, SC-20, SC-21, SC-22 | 9.2, 13.10 | CC6.6, CC6.8 | DSS05.02 | [PCI] 1.3.2, 1.4.2 |
| SEC-007.5.7 Distributed denial-of-service (DDoS) protection |  | A.8.6, A.8.20 | PR.IR-03, PR.IR-04 | SC-5 | 13.10 | A1.1, CC6.6 | DSS05.02 | — |
| SEC-007.5.8 Network documentation | KC-37 | 7.5; A.8.20 | ID.AM-03 | CA-3, PL-2 | 12.4 | CC2.1 | BAI10 | [PCI] 1.2.3, 1.2.4 |
| SEC-007.5.9 Network devices and services |  | A.8.9, A.8.20, A.8.21 | PR.PS-01, PR.PS-02 | AU-12, CM-2, CM-8, SI-2 | 12.1, 12.3, 12.8, 13.9 | CC6.1, CC7.1, CC9.2 | APO10, DSS05.02 | [PCI] 1.2.1, 2.2 |

**SEC-008 Endpoint & Mobile Device Security Policy (incl. BYOD)**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| SEC-008.5.1 Device enrolment and inventory |  | A.5.9, A.8.1 | ID.AM-01, PR.AA-05 | AC-19, CM-8 | 1.1, 4.6 | CC6.1 | BAI09, DSS05.03 | [PCI] 12.5.1 · [HIPAA] §164.310(b) |
| SEC-008.5.2 Configuration and hardening |  | A.8.1, A.8.9, A.8.19 | PR.PS-01, PR.PS-05 | AC-11, CM-6, CM-7, CM-11 | 2.5, 4.1, 4.3, 4.10 | CC6.8, CC7.1 | BAI10, DSS05.03 | [PCI] 2.2 · [HIPAA] §164.310(c), §164.312(a)(2)(iii) |
| SEC-008.5.3 Malware protection and endpoint detection and response (EDR) | KC-38 | A.8.7 | DE.CM-09, PR.PS-01 | SI-3, SI-4 | 10.1, 10.2, 10.7, 13.2 | CC6.8, CC7.2 | DSS05.01 | [PCI] 5.2, 5.3 · [HIPAA] §164.308(a)(5)(ii)(B) |
| SEC-008.5.4 Encryption | KC-39 | A.8.1, A.8.24 | PR.DS-01 | SC-12, SC-28 | 3.6 | CC6.1, CC6.7 | DSS05.03 | [HIPAA] §164.312(a)(2)(iv) · [GDPR] Art. 32 |
| SEC-008.5.5 Operating system support and patching |  | A.8.1, A.8.8 | ID.RA-01, PR.PS-02 | SA-22, SI-2 | 2.2, 7.3, 7.4 | CC7.1 | DSS05.03 | [PCI] 6.3.3 |
| SEC-008.5.6 Local administrator restrictions |  | A.8.2, A.8.18 | PR.AA-05 | AC-2, AC-6 | 5.4 | CC6.1, CC6.3 | DSS05.04 | [PCI] 7.2.1 |
| SEC-008.5.7 Removable media |  | A.7.10, A.8.12 | PR.DS-01 | MP-2, MP-7 | 10.3, 10.4 | CC6.7 | DSS05.06 | [PCI] 5.3.3 · [HIPAA] §164.310(d)(1) |
| SEC-008.5.8 Bring Your Own Device (BYOD) |  | A.6.7, A.8.1 | PR.AA-05, PR.DS-01 | AC-19, AC-20 | 4.12 | CC6.1, CC6.7 | DSS05.03 | [GDPR] Art. 5(1)(c), Art. 32 · [CPRA] §1798.100 |
| SEC-008.5.9 Lost or stolen devices and remote wipe |  | A.5.24, A.6.8, A.8.1 | PR.DS-01, RS.MA-01 | AC-19, IR-6 | 4.11 | CC6.7, CC7.3 | DSS02 | [HIPAA] §164.308(a)(6) · Other: RES-003 obligations |
| SEC-008.5.10 Device lifecycle and return |  | A.5.11, A.7.14 | ID.AM-08 | MP-6, PS-4 | 3.5 | CC6.5 | BAI09 | [HIPAA] §164.310(d)(2) |

**SEC-009 Cloud Security Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| SEC-009.5.1 Shared responsibility |  | A.5.19, A.5.23 | GV.SC-05, GV.SC-07 | SA-9, SR-6 | 15.4 | CC9.2 | APO10 | [PCI] 12.8.5, 12.9 · [HIPAA] §164.314(a) |
| SEC-009.5.2 Approved Cloud Service Providers and onboarding |  | A.5.9, A.5.21, A.5.23 | GV.SC-06, ID.AM-02 | CM-8, SA-4, SA-9 | 2.1, 15.1 | CC3.4, CC9.2 | APO10 | [GDPR] Art. 28 |
| SEC-009.5.3 Landing Zone and account structure |  | A.5.23, A.8.22, A.8.31 | PR.IR-01, PR.PS-01 | AC-4, CM-2, SC-7 | 12.2 | CC6.1, CC6.6 | APO03, BAI10 | [PCI] 1.2, 12.5.2 |
| SEC-009.5.4 Infrastructure as Code and guardrails |  | A.8.9, A.8.32 | PR.PS-01 | CM-2, CM-3, CM-6 | 4.1, 16.7 | CC7.1, CC8.1 | BAI06, BAI10 | [PCI] 2.2, 6.5.1 |
| SEC-009.5.5 Cloud security posture management (CSPM/CNAPP) | KC-40 | A.8.8, A.8.9 | DE.CM-09, ID.RA-01 | CA-7, CM-6, RA-5 | 4.1, 7.5 | CC7.1 | DSS05.07 | [PCI] 11.3 |
| SEC-009.5.6 Identity federation and cloud access |  | A.5.15, A.5.16, A.8.2, A.8.5 | PR.AA-01, PR.AA-03, PR.AA-05 | AC-2, AC-6, IA-2, IA-5 | 5.6, 6.3, 6.5, 6.7 | CC6.1, CC6.2, CC6.3 | DSS05.04 | [PCI] 7.2, 8.4 |
| SEC-009.5.7 Storage exposure controls |  | A.5.10, A.8.3, A.8.24 | PR.DS-01 | AC-3, SC-28 | 3.3, 3.11 | C1.1, CC6.1 | DSS05.02 | [HIPAA] §164.312(a)(2)(iv) · [GDPR] Art. 32 |
| SEC-009.5.8 Cloud logging |  | A.8.15, A.8.16 | DE.CM-01, PR.PS-04 | AU-2, AU-9, AU-12 | 8.2, 8.9 | CC7.2 | DSS05.07 | [PCI] 10.2, 10.3 · [HIPAA] §164.312(b) |
| SEC-009.5.9 Network controls in the cloud |  | A.8.20, A.8.22 | PR.IR-01 | SC-7 | 12.2 | CC6.6 | DSS05.02 | [PCI] 1.3 |
| SEC-009.5.10 Data residency |  | A.5.31, A.5.34 | GV.OC-03 | SA-9 | — | C1.1 | APO10, MEA03 | [GDPR] Art. 44–49 |
| SEC-009.5.11 Kubernetes and container security baseline |  | A.8.9, A.8.19, A.8.22 | PR.PS-01, PR.PS-05 | AC-6, CM-6, CM-7, SI-7 | 4.1, 4.8, 16.7 | CC6.1, CC6.8, CC7.1 | BAI10, DSS05.03 | [PCI] 2.2, 6.3.2 |

**SEC-010 Secure Software Development Lifecycle Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| SEC-010.5.1 Secure development lifecycle |  | A.8.25, A.8.26 | PR.PS-06 | SA-3, SA-8, SA-15 | 16.1, 16.9 | CC8.1 | BAI03 | [PCI] 6.2.1 · [GDPR] Art. 25 |
| SEC-010.5.2 Secure design and threat modeling |  | A.5.8, A.8.27 | ID.RA-04, PR.PS-06 | SA-8, SA-11, SA-17 | 16.10, 16.14 | CC3.2, CC8.1 | BAI03 | [GDPR] Art. 25, Art. 35 |
| SEC-010.5.3 Secure coding standards |  | A.8.28 | PR.PS-06 | SA-11, SI-10 | 16.1, 16.9, 16.11 | CC8.1 | BAI03 | [PCI] 6.2.2, 6.2.4 |
| SEC-010.5.4 Code review | KC-41 | A.8.4, A.8.28, A.8.29 | PR.PS-06 | CM-3, SA-11 | 16.12 | CC8.1 | BAI03, BAI07 | [PCI] 6.2.3, 6.2.3.1 · [SOX] §404 |
| SEC-010.5.5 Automated security testing gates | KC-42 | A.8.8, A.8.29 | ID.RA-01, PR.PS-06 | RA-5, SA-11 | 16.2, 16.12 | CC7.1, CC8.1 | BAI07 | [PCI] 6.2.4, 6.3.1, 11.3 |
| SEC-010.5.6 CI/CD pipeline integrity |  | A.8.4, A.8.31, A.8.32 | PR.PS-01, PR.PS-06 | CM-14, SA-10, SI-7, SR-4, SR-11 | 16.1, 16.7 | CC6.1, CC8.1 | BAI03, BAI06 | [PCI] 6.5.1 |
| SEC-010.5.7 Secrets management |  | A.5.17, A.8.24 | PR.AA-01, PR.DS-01 | IA-5, SC-12, SC-28 | 3.11, 16.1 | CC6.1 | DSS05.04 | [PCI] 8.3.2, 8.6.2 |
| SEC-010.5.8 Software Bill of Materials (SBOM) |  | A.5.21, A.8.25 | GV.SC-04, ID.AM-02 | CM-8, SR-4 | 2.1, 16.4 | CC9.2 | APO10 | [PCI] 6.3.2 |
| SEC-010.5.9 Open-source components and licenses |  | A.5.21, A.5.32, A.8.19 | GV.SC-05, PR.PS-02 | CM-10, SA-22, SR-3 | 2.2, 16.4, 16.5 | CC9.2 | APO10, MEA03 | — |
| SEC-010.5.10 Segregation of environments |  | A.5.3, A.8.31 | PR.IR-01 | AC-5, CM-4, SA-3 | 16.8 | CC6.1, CC8.1 | BAI03, BAI07 | [PCI] 6.5.3, 6.5.4 |
| SEC-010.5.11 Test data |  | A.8.33 | PR.DS-01 | SA-3, SA-11 | 16.8 | C1.1, CC8.1 | BAI07 | [PCI] 6.5.5, 6.5.6 · [GDPR] Art. 5(1)(b), Art. 25 |
| SEC-010.5.12 Public-facing web applications [PCI] |  | A.8.20, A.8.26 | PR.IR-01 | SC-7, SI-7 | 13.10 | CC6.6 | DSS05.02 | [PCI] 6.4.1, 6.4.2, 6.4.3 |
| SEC-010.5.13 Outsourced development |  | A.8.30 | GV.SC-05 | SA-4, SA-11 | 16.1 | CC9.2 | APO10 | — |
| SEC-010.5.14 Program change controls [SOX] |  | A.8.32 | PR.PS-06 | CM-3 | — | CC8.1 | BAI06 | [PCI] 6.5.1 · [SOX] §404 |

**SEC-011 Vulnerability & Patch Management Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| SEC-011.5.1 Program and asset coverage |  | A.5.7, A.5.9, A.8.8 | ID.AM-01, ID.RA-01, ID.RA-02 | CM-8, RA-5, SI-5 | 1.1, 7.1 | CC7.1 | DSS05.07 | [PCI] 6.3.1 · [HIPAA] §164.308(a)(1)(ii)(A) |
| SEC-011.5.2 Scanning | KC-43 | A.8.8, A.8.34 | DE.CM-09, ID.RA-01 | RA-5 | 7.5, 7.6 | CC7.1 | DSS05.07 | [PCI] 11.3.1, 11.3.1.1, 11.3.1.3, 11.3.2, 11.3.2.1 |
| SEC-011.5.3 Severity assignment |  | A.8.8 | ID.RA-05, ID.RA-06 | RA-3, RA-5 | 7.2 | CC3.2, CC7.1 | APO12 | [PCI] 6.3.1 |
| SEC-011.5.4 Remediation | KC-44 | A.8.8 | ID.RA-06, PR.PS-02 | RA-5, SI-2 | 7.2, 7.7 | CC7.1, CC7.4 | BAI06, DSS05.07 | [PCI] 6.3.3 · [HIPAA] §164.308(a)(1)(ii)(B) |
| SEC-011.5.5 Patch management |  | A.8.8, A.8.19, A.8.32 | PR.PS-02, PR.PS-03 | CM-3, SI-2 | 7.3, 7.4 | CC7.1, CC8.1 | BAI06, DSS05.07 | [PCI] 6.3.3 |
| SEC-011.5.6 End-of-support software and hardware |  | A.5.9, A.8.8 | ID.AM-08, PR.PS-02 | SA-22 | 2.2 | CC7.1 | BAI09 | [PCI] 12.3.4 |
| SEC-011.5.7 Penetration testing | KC-45 | A.5.35, A.8.8, A.8.29, A.8.34 | ID.IM-02, ID.RA-01 | CA-8 | 16.13, 18.1, 18.2, 18.3, 18.4, 18.5 | CC4.1, CC7.1 | DSS05.07, MEA02 | [PCI] 11.4.1–11.4.6 · [HIPAA] §164.308(a)(8) |
| SEC-011.5.8 Vulnerability Disclosure Program (VDP) |  | A.5.5, A.6.8, A.8.8 | ID.RA-08 | RA-5, SI-5 | 16.2 | CC2.3, CC7.3 | APO08, DSS05.07 | — |
| SEC-011.5.9 Bug bounty (optional) |  | A.8.8 | ID.RA-08 | RA-5 | 16.2 | CC2.3 | DSS05.07 | — |

**SEC-012 Logging & Monitoring Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| SEC-012.5.1 Logging governance |  | A.8.15, A.8.16 | DE.CM-01, DE.CM-09, PR.PS-04 | AU-1, AU-2, AU-12 | 8.1, 8.2 | CC7.2 | DSS05.07 | [PCI] 10.2.1 · [HIPAA] §164.312(b) |
| SEC-012.5.2 Required Log Sources |  | A.8.15, A.8.16 | DE.CM-01, DE.CM-09, PR.PS-04 | AU-1, AU-2, AU-12 | 8.1, 8.2 | CC7.2 | DSS05.07 | [PCI] 10.2.1 · [HIPAA] §164.312(b) |
| SEC-012.5.3 Required event types and fields |  | A.8.15 | PR.PS-04 | AU-2, AU-3 | 8.5 | CC7.2 | DSS05.07 | [PCI] 10.2.1.1–10.2.1.7, 10.2.2, 3.3.1 · [GDPR] Art. 5(1)(c) |
| SEC-012.5.4 Time synchronization |  | A.8.17 | PR.PS-04 | AU-8 | 8.4 | CC7.2 | DSS05.07 | [PCI] 10.6.1–10.6.3 |
| SEC-012.5.5 Log integrity and protection |  | A.8.15 | PR.DS-01, PR.PS-04 | AU-4, AU-5, AU-9 | 8.3, 8.9 | CC7.2 | DSS05.07 | [PCI] 10.3.1–10.3.4 · [HIPAA] §164.312(b), §164.312(c)(1) |
| SEC-012.5.6 Centralization in a SIEM | KC-46 | A.8.15, A.8.16 | DE.AE-03, DE.AE-07 | AU-6, SI-4 | 8.9, 8.10, 13.1 | CC7.2 | DSS05.07 | [PCI] 10.3.3, 10.5.1 |
| SEC-012.5.7 Detection Use Cases and coverage |  | A.5.7, A.8.16 | DE.AE-02, DE.AE-07, DE.CM-01, DE.CM-03 | AU-6, RA-3, SI-4 | 13.1, 13.3 | CC7.2, CC7.3 | DSS02.01, DSS05.07 | [PCI] 10.4.1.1 |
| SEC-012.5.8 Alert triage and escalation | KC-47 | A.5.25, A.6.8 | DE.AE-02, DE.AE-06, DE.AE-08, RS.MA-01 | IR-4, IR-5, IR-6, SI-4 | 13.1, 17.2 | CC7.3, CC7.4 | DSS02.02, DSS05.07 | [PCI] 10.4.3, 12.10.5 |
| SEC-012.5.9 Log review | KC-48 | A.8.15, A.8.16 | DE.AE-02, DE.CM-03 | AU-6 | 8.11 | CC4.1, CC7.2 | DSS05.07, MEA01 | [PCI] 10.4.1, 10.4.1.1, 10.4.2, 10.4.3 · [HIPAA] §164.308(a)(1)(ii)(D), §164.308(a)(5)(ii)(C) · [SOX] §404 |
| SEC-012.5.10 Log failure alerting |  | A.8.15, A.8.16 | DE.CM-09 | AU-5, SI-4 | 8.2 | CC7.2 | DSS05.07 | [PCI] 10.7.2, 10.7.3 |
| SEC-012.5.11 Monitoring of Third Parties and cloud services |  | A.5.22, A.8.16 | DE.CM-06 | AU-6, SA-9 | 15.6 | CC9.2 | APO10.05 | [HIPAA] §164.314(a) |

**SEC-013 Change & Configuration Management Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| SEC-013.5.1 Change management governance |  | 6.3; A.5.37, A.8.32 | ID.RA-07, PR.PS-01 | CM-3 | 4.1 | CC8.1 | BAI06.01, BAI06.02 | [PCI] 6.5.1 · [SOX] §404 |
| SEC-013.5.2 Change classes |  | 6.3; A.5.37, A.8.32 | ID.RA-07, PR.PS-01 | CM-3 | 4.1 | CC8.1 | BAI06.01, BAI06.02 | [PCI] 6.5.1 · [SOX] §404 |
| SEC-013.5.3 Risk assessment of changes |  | A.8.32 | ID.RA-07 | CM-4, RA-3 | 4.1 | CC3.4, CC8.1 | BAI06.01 | [PCI] 6.5.1 · [GDPR] Art. 35 |
| SEC-013.5.4 Testing |  | A.8.29, A.8.31, A.8.32 | PR.PS-06 | CM-4, SA-11 | 16.1 | CC8.1 | BAI07.05 | [PCI] 6.5.1, 6.5.3 |
| SEC-013.5.5 Approval and the Change Advisory Board | KC-49 | A.8.19, A.8.32 | ID.RA-07, PR.PS-01 | CM-3, CM-5 | 4.1 | CC8.1 | BAI06.01, BAI07.06 | [PCI] 6.5.1 · [SOX] §404 |
| SEC-013.5.6 Implementation and rollback |  | A.8.19, A.8.32 | ID.RA-07, PR.PS-01 | CM-3, CM-5 | 4.1 | CC8.1 | BAI06.01, BAI07.06 | [PCI] 6.5.1 · [SOX] §404 |
| SEC-013.5.7 Post-implementation review |  | 10.2; A.8.32 | ID.IM-03 | CM-3, CM-4 | — | CC8.1 | BAI06.04 | [PCI] 6.5.2 |
| SEC-013.5.8 Configuration Baselines and hardening | KC-50 | A.8.9 | PR.PS-01 | CM-2, CM-6, CM-7 | 4.1, 4.2 | CC7.1 | BAI10.02 | [PCI] 2.2.1–2.2.7 · [HIPAA] §164.308(a)(1)(ii)(B) |
| SEC-013.5.9 Drift detection and unauthorized change | KC-51 | A.8.9, A.8.16 | DE.CM-09, PR.PS-01 | CM-3, CM-6, SI-7 | 4.1 | CC7.1 | BAI10.05, DSS05.07 | [PCI] 11.5.2, 11.6.1 |
| SEC-013.5.10 Configuration items and records |  | A.5.9, A.5.37, A.8.9 | ID.AM-08 | CM-8, CM-9 | 1.1 | CC8.1 | BAI10.03 | [PCI] 1.2.3, 1.2.4 |
| SEC-013.5.11 [SOX] Program change for Financially Significant Systems |  | A.5.3, A.8.32 | GV.OV-01 | AC-5, CM-3, CM-5 | — | CC8.1 | BAI06.01, MEA04 | [SOX] §§302, 404 |
| SEC-013.5.12 Capacity management | KC-52 | A.8.6 | PR.IR-04 | AU-4, CP-2(2) | — | A1.1 | BAI04 | — |

**SEC-014 Email & Communications Security Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| SEC-014.5.1 Domain authentication: SPF, DKIM and DMARC |  | A.5.14, A.8.20, A.8.21 | PR.DS-02, PR.PS-01 | SC-8, SC-20, SI-8 | 9.5 | CC6.7 | DSS05.02 | — |
| SEC-014.5.2 Anti-phishing and impersonation protection |  | A.5.14, A.6.3, A.8.7 | DE.AE-02, DE.CM-09 | AT-2, SI-3, SI-4, SI-8 | 9.2, 9.7, 14.2 | CC6.8, CC7.2 | DSS05.01 | [PCI] 5.4.1 |
| SEC-014.5.3 Attachment and link protection |  | A.8.7, A.8.23 | DE.CM-09 | SI-3, SI-8 | 9.3, 9.6, 9.7, 10.1 | CC6.8 | DSS05.01 | [PCI] 5.2.1, 5.4.1 |
| SEC-014.5.4 External sender tagging and mail-flow restrictions |  | A.5.14, A.8.12 | PR.DS-02 | AC-4, SC-7, SI-4 | 3.13, 9.5 | CC6.7 | DSS05.02 | — |
| SEC-014.5.5 Email encryption by Classification Level |  | A.5.14, A.8.24 | PR.DS-02 | SC-8, SC-13 | 3.10 | C1.1, CC6.7 | DSS05.02 | [PCI] 4.2.2 · [HIPAA] §164.312(e)(1), §164.312(e)(2)(ii) · [GDPR] Art. 32 |
| SEC-014.5.6 Approved messaging and collaboration tools |  | A.5.14, A.5.23, A.5.33 | GV.SC-07, ID.AM-02 | CM-7, SA-9 | 2.3 | CC6.1, CC9.2 | APO10.04, BAI09 | [SOX] §404 |
| SEC-014.5.7 Video conferencing |  | A.5.14, A.7.7 | PR.DS-02 | AC-20, SC-15 | — | CC6.7 | DSS05.02 | [GDPR] Art. 6 |
| SEC-014.5.8 Telephony, voicemail and fax |  | A.5.14, A.6.3 | PR.AA-01 | IA-2, SC-8 | — | CC6.1 | DSS05.04 | [PCI] 3.3.1 |
| SEC-014.5.9 Mailbox and account security |  | A.5.15, A.8.5 | PR.AA-01, PR.AA-03 | AC-2, IA-2 | 6.3, 6.5 | CC6.1 | DSS05.04 | [HIPAA] §164.312(d) |
| SEC-014.5.10 Retention |  | A.5.33 | GV.OC-03 | AU-11, SI-12 | 3.4 | C1.2 | APO14 | [HIPAA] §164.316(b)(2)(i) · [SOX] §802 |

**SEC-015 Remote Work & Travel Security Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| SEC-015.5.1 Eligibility and authorization |  | A.6.7 | PR.AA-05 | AC-17, PE-17 | 12.7 | CC6.1 | DSS05.04 | [PCI] 8.4.2, 12.3.1 |
| SEC-015.5.2 Remote work environment |  | A.6.7, A.7.7, A.7.9 | PR.AA-06, PR.DS-01 | AC-11, PE-17 | 12.7 | CC6.4 | DSS05.05 | [HIPAA] §164.310(b), §164.310(c) |
| SEC-015.5.3 Public places and public Wi-Fi |  | A.6.7, A.7.9, A.8.1 | PR.DS-02 | AC-17, AC-18, AC-19 | 12.7 | CC6.7 | DSS05.02 | — |
| SEC-015.5.4 International travel and High-risk Jurisdictions |  | A.5.31, A.6.7, A.7.9 | GV.OC-03, ID.RA-03 | AC-19, PE-17 | 4.1 | CC3.2, CC6.7 | APO12.01, DSS05.03 | Other: Export-control laws recorded in CMP-001 |
| SEC-015.5.5 Border device inspection |  | A.5.24, A.7.9 | PR.DS-01, RS.MA-01 | AC-19, IR-6 | 17.3 | CC7.3 | DSS02.01 | [HIPAA] §164.308(a)(6) · [GDPR] Art. 33 |
| SEC-015.5.6 Printing at home and away from Organization facilities |  | A.7.7, A.7.14 | PR.DS-01 | MP-4, MP-6 | 3.5 | CC6.5 | DSS05.06 | [HIPAA] §164.310(d)(1) |
| SEC-015.5.7 Physical security of documents and Media outside Organization facilities |  | A.7.9, A.7.10 | PR.DS-01 | MP-4, MP-5 | 3.5 | CC6.4, CC6.7 | DSS05.06 | [PCI] 9.4.2, 9.4.3, 9.4.4 · [HIPAA] §164.310(d)(1) |
| SEC-015.5.8 Reporting loss, theft and suspicious events |  | A.6.8 | RS.MA-01 | IR-6 | 17.3 | CC7.3 | DSS02.01 | — |

**SEC-016 Physical & Environmental Security Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| SEC-016.5.1 Facility Security Zones |  | A.7.1, A.7.3, A.7.6 | PR.AA-06 | PE-1, PE-3 | — | CC6.4 | DSS05.05 | [PCI] 9.1.1, 9.2.1 · [HIPAA] §164.310(a)(1), §164.310(a)(2)(ii) |
| SEC-016.5.2 Badge and physical access control | KC-53 | A.5.18, A.7.2 | PR.AA-06 | PE-2, PE-3, PE-8 | — | CC6.4 | DSS05.05 | [PCI] 9.2.1, 9.2.2, 9.2.3, 9.2.4, 9.3.1, 9.3.1.1 · [HIPAA] §164.310(a)(2)(iii) |
| SEC-016.5.3 Visitor management |  | A.7.2 | PR.AA-06 | PE-3, PE-8 | — | CC6.4 | DSS05.05 | [PCI] 9.3.2, 9.3.3, 9.3.4 |
| SEC-016.5.4 CCTV and monitoring |  | A.7.4 | DE.CM-02 | PE-6 | — | CC6.4, CC7.2 | DSS05.05 | [PCI] 9.2.1.1 · [GDPR] Art. 6, 13 |
| SEC-016.5.5 Data centers, server rooms and network rooms |  | A.7.3, A.7.6, A.7.12 | PR.AA-06, PR.IR-02 | PE-3, PE-4, PE-16 | — | CC6.4 | DSS05.05 | [PCI] 9.2.3, 9.2.4, 9.3.1 |
| SEC-016.5.6 Third-party facilities |  | A.5.22, A.7.1 | GV.SC-07 | PE-3, SA-9 | 15.4 | CC6.4, CC9.2 | APO10.05 | [HIPAA] §164.314(a) |
| SEC-016.5.7 Environmental controls | KC-54 | A.7.5, A.7.11, A.7.13 | DE.CM-02, PR.IR-02 | PE-9, PE-10, PE-11, PE-12, PE-13, PE-14, PE-15, PE-18 | — | A1.2 | DSS01.04, DSS01.05 | [HIPAA] §164.310(a)(2)(i), §164.310(a)(2)(iv) |
| SEC-016.5.8 Delivery and loading areas |  | A.7.2 | PR.AA-06 | PE-16 | — | CC6.4 | DSS05.05 | — |
| SEC-016.5.9 Clear desk and clear screen |  | A.7.7 | PR.DS-01 | AC-11, MP-4 | 4.3 | CC6.4 | DSS05.05 | [HIPAA] §164.310(b), §164.310(c) |
| SEC-016.5.10 Equipment siting and protection |  | A.7.8, A.7.13 | PR.IR-02, PR.PS-03 | MA-2, PE-18 | — | A1.2, CC6.4 | BAI09, DSS01.04 | [PCI] 9.5.1, 9.5.1.1, 9.5.1.2, 9.5.1.2.1, 9.5.1.3 · [HIPAA] §164.310(c) |
| SEC-016.5.11 Physical security of Media within facilities |  | A.7.10 | PR.DS-01 | MP-4 | 3.1 | CC6.4 | DSS05.06 | [PCI] 9.4.1, 9.4.2, 9.4.5, 9.4.5.1 |

**SEC-017 Media Sanitization & Secure Disposal Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| SEC-017.5.1 General |  | A.7.10, A.7.14, A.8.10 | ID.AM-08, PR.DS-01, PR.PS-03 | MP-6 | 3.5 | C1.2, CC6.5 | BAI09, DSS05.06 | [HIPAA] §164.310(d)(2)(i), (ii) · [GDPR] Art. 5(1)(e), 17, 32 |
| SEC-017.5.2 Sanitization method by Classification Level and media type |  | A.7.10, A.7.14, A.8.10 | ID.AM-08, PR.DS-01, PR.PS-03 | MP-6 | 3.5 | C1.2, CC6.5 | BAI09, DSS05.06 | [HIPAA] §164.310(d)(2)(i), (ii) · [GDPR] Art. 5(1)(e), 17, 32 |
| SEC-017.5.3 Custody and storage before sanitization |  | A.7.10, A.7.14 | ID.AM-08 | MP-4, MP-5, MP-6 | 3.5 | C1.2, CC6.5 | BAI09, DSS05.06 | [PCI] 9.4.6 · [HIPAA] §164.310(d)(2)(iii) |
| SEC-017.5.4 Verification |  | A.7.10, A.7.14 | ID.AM-08 | MP-4, MP-5, MP-6 | 3.5 | C1.2, CC6.5 | BAI09, DSS05.06 | [PCI] 9.4.6 · [HIPAA] §164.310(d)(2)(iii) |
| SEC-017.5.5 Records and Certificates of Destruction | KC-55 | A.7.10, A.7.14 | ID.AM-08 | MP-4, MP-5, MP-6 | 3.5 | C1.2, CC6.5 | BAI09, DSS05.06 | [PCI] 9.4.6 · [HIPAA] §164.310(d)(2)(iii) |
| SEC-017.5.6 Cloud Services and logical data deletion |  | A.5.23, A.8.10 | GV.SC-10, PR.DS-01 | MP-6, SA-9, SI-12 | 3.4, 3.5 | C1.2, CC9.2 | APO10, DSS06 | [GDPR] Art. 17, 28(3)(g) · [CPRA] §1798.105 |
| SEC-017.5.7 Third-party disposal vendors |  | A.5.19, A.5.20, A.7.14 | GV.SC-05, GV.SC-07 | SA-9, SR-12 | 15.4 | CC9.2 | APO10 | [HIPAA] §164.308(b)(1) |
| SEC-017.5.8 Payment card data [PCI] |  | A.7.14 | PR.DS-01 | MP-6 | 3.5 | C1.2 | DSS05.06 | [PCI] 3.2.1, 9.4.6, 9.4.7 |
| SEC-017.5.9 Protected health information [HIPAA] |  | A.7.14 | PR.DS-01 | MP-6 | 3.5 | C1.2 | DSS05.06 | [HIPAA] §164.310(d)(2)(i), (ii) |

**SEC-018 Backup Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| SEC-018.5.1 Backup scope and governance |  | A.5.30, A.8.13 | ID.AM-08, PR.DS-11 | CP-2, CP-9 | 11.1 | A1.2 | DSS04.07 | [HIPAA] §164.308(a)(7)(ii)(A) |
| SEC-018.5.2 Backup frequency |  | A.8.13, A.8.14 | PR.DS-11 | CP-9, CP-10 | 11.2 | A1.2 | DSS04.07 | [HIPAA] §164.308(a)(7)(ii)(A) |
| SEC-018.5.3 The 3-2-1-1-0 rule |  | A.8.13 | PR.DS-11 | CP-6, CP-9 | 11.3, 11.4 | A1.2 | DSS04.07 | [PCI] 9.4.1, 9.4.1.1 · [HIPAA] §164.310(d)(2)(iv) |
| SEC-018.5.4 Backup Encryption |  | A.8.13, A.8.24 | PR.DS-01, PR.DS-11 | CP-9, SC-28 | 11.3 | A1.2, CC6.1 | DSS05.02 | [PCI] 3.5.1 · [HIPAA] §164.312(a)(2)(iv) |
| SEC-018.5.5 Access to Backups |  | A.8.2, A.8.13 | PR.AA-05 | AC-6, CP-9 | 5.4, 11.3 | CC6.1, CC6.3 | DSS05.04 | [HIPAA] §164.308(a)(7)(ii)(A) |
| SEC-018.5.6 Restore testing | KC-56 | A.5.30, A.8.13 | PR.DS-11, RC.RP-03 | CP-4, CP-9 | 11.5 | A1.3 | DSS04.04, DSS04.07 | [HIPAA] §164.308(a)(7)(ii)(D) |
| SEC-018.5.7 Monitoring of Backup jobs | KC-57 | A.8.13, A.8.16 | DE.CM-09, PR.DS-11 | CP-9, SI-4 | 11.2 | A1.2, CC7.2 | DSS01.03, DSS04.07 | — |
| SEC-018.5.8 SaaS and Cloud Service data |  | A.5.23, A.8.13 | GV.SC-07, PR.DS-11 | CP-9, SA-9 | 11.1, 15.4 | A1.2, CC9.2 | APO10.04, DSS04.07 | [HIPAA] §164.314(a) |
| SEC-018.5.9 Retention, Legal Hold and disposal |  | A.5.33, A.8.10 | PR.DS-11 | CP-9, MP-6, SI-12 | 3.4, 3.5 | C1.2 | APO14, DSS04.07 | [GDPR] Art. 17 · [CPRA] §1798.105 · [SOX] §404 |

**SEC-019 Cardholder Data Environment Standard**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| SEC-019.5.1 CDE scope definition |  | 4.3; A.5.9, A.5.12 | GV.OC-03, ID.AM-01, ID.AM-07 | CM-8, PM-5, RA-2 | 1.1, 3.2 | CC3.2, CC6.1 | APO03, BAI09 | [PCI] 12.5.1, 12.5.2, 12.5.2.1, 12.5.3 |
| SEC-019.5.2 Scope confirmation (PCI DSS 12.5.2, 12.5.2.1, 12.5.3) |  | 4.3; A.5.9, A.5.12 | GV.OC-03, ID.AM-01, ID.AM-07 | CM-8, PM-5, RA-2 | 1.1, 3.2 | CC3.2, CC6.1 | APO03, BAI09 | [PCI] 12.5.1, 12.5.2, 12.5.2.1, 12.5.3 |
| SEC-019.5.3 Network and data-flow diagrams (PCI DSS 1.2.3, 1.2.4) |  | A.5.9, A.8.20 | ID.AM-03 | AC-4, CM-8, PL-8 | 3.8, 12.4 | CC6.6 | APO03 | [PCI] 1.2.3, 1.2.4 |
| SEC-019.5.4 Segmentation |  | A.8.20, A.8.22 | PR.IR-01 | AC-4, CA-8, SC-7 | 12.2, 13.4, 18.2 | CC6.6 | DSS05 | [PCI] 1.3, 1.4, 11.4.5, 11.4.6 |
| SEC-019.5.5 CDE inventory and cardholder data inventory |  | A.5.9, A.5.12, A.8.12 | DE.CM-09, ID.AM-07 | CM-8, PM-5, SI-4 | 3.1, 3.2 | C1.1, CC6.1 | BAI09 | [PCI] 12.5.1, 12.10.7, 3.2.1 |
| SEC-019.5.6 PAN display and copying (PCI DSS 3.4) |  | A.8.11, A.8.24 | PR.DS-01, PR.DS-02 | AC-3, SC-13, SC-28 | 3.3, 3.10, 3.11 | C1.1, CC6.1, CC6.7 | DSS05 | [PCI] 3.3.2, 3.3.3, 3.4.1, 3.4.2, 3.5.1, 3.5.1.1–3.5.1.3, 4.2.2 |
| SEC-019.5.7 Rendering PAN unreadable (PCI DSS 3.3.2, 3.5) |  | A.8.11, A.8.24 | PR.DS-01, PR.DS-02 | AC-3, SC-13, SC-28 | 3.3, 3.10, 3.11 | C1.1, CC6.1, CC6.7 | DSS05 | [PCI] 3.3.2, 3.3.3, 3.4.1, 3.4.2, 3.5.1, 3.5.1.1–3.5.1.3, 4.2.2 |
| SEC-019.5.8 Payment Page script integrity and tamper detection (PCI DSS 6.4.3, 11.6.1) |  | A.8.26, A.8.28, A.8.32 | DE.CM-09, PR.PS-06 | CM-7, SI-4, SI-7 | 2.7, 16.1 | CC7.1, CC8.1 | BAI06 | [PCI] 6.4.3, 11.6.1 |
| SEC-019.5.9 POI device protection (PCI DSS 9.5.1) |  | A.7.2, A.7.8, A.7.9 | DE.CM-02, PR.AA-06 | MA-5, PE-3, PE-6 | 1.1 | CC6.4 | DSS05 | [PCI] 9.5.1, 9.5.1.1, 9.5.1.2, 9.5.1.2.1, 9.5.1.3 |
| SEC-019.5.10 PCI-specific governance |  | 6.1.2; A.5.19, A.5.20, A.5.21, A.5.22 | GV.SC-07, ID.RA-01 | PM-9, RA-3, SA-9, SR-6 | 15.1, 15.5 | CC3.2, CC9.2 | APO10, APO12 | [PCI] 12.3.1–12.3.4, 12.4.1, 12.4.2, 12.8.1, 12.8.4, 12.8.5, 12.9 |
| SEC-019.5.11 Compliance validation |  | 9.2; A.5.35, A.5.36 | GV.OV-01 | CA-2, CA-7 | 18.1 | CC4.1 | MEA03 | [PCI] v4.0.1 (all requirements) |
| SEC-019.5.12 PCI DSS requirement cross-reference |  | 9.2; A.5.35, A.5.36 | GV.OV-01 | CA-2, CA-7 | 18.1 | CC4.1 | MEA03 | [PCI] v4.0.1 (all requirements) |

#### 5.3.6 Resilience

**RES-001 Incident Response Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| RES-001.5.1 Incident response program |  | A.5.24, A.5.26 | ID.IM-04, RS.MA-01, RS.MA-02 | IR-1, IR-4, IR-8 | 17.1, 17.4 | CC7.3, CC7.4 | DSS02, DSS05 | [PCI] 12.10.1, 12.10.3, 12.10.7 · [HIPAA] §164.308(a)(6) |
| RES-001.5.2 Obligation to report suspected Security Incidents |  | A.5.25, A.6.8 | DE.AE-02, RS.MA-01 | IR-6, IR-7 | 17.2, 17.3 | CC2.2, CC2.3, CC7.3 | DSS02 | [PCI] 12.10.1 · [HIPAA] §164.308(a)(6)(ii) |
| RES-001.5.3 Incident Commander and authority |  | A.5.26 | RS.MA-01, RS.MA-03, RS.MI-01, RS.MI-02 | IR-4 | 17.5 | CC7.4 | DSS02, DSS05 | — |
| RES-001.5.4 Evidence preservation and forensics |  | A.5.28 | RS.AN-03, RS.AN-07 | AU-9, AU-11, IR-4 | 17.4 | CC7.4 | DSS05 | [HIPAA] §164.308(a)(6)(ii) · [GDPR] Art. 33(5) |
| RES-001.5.5 Law enforcement and authority liaison |  | A.5.5, A.5.6 | RS.CO-03 | IR-6, IR-7 | 17.2 | CC2.3 | APO08, MEA03 | [GDPR] Art. 33 |
| RES-001.5.6 External incident response support |  | A.5.19, A.5.24 | GV.SC-01, RS.MA-01 | IR-7 | 17.5 | CC7.4, CC9.2 | APO10 | [PCI] 12.10.1 |
| RES-001.5.7 Ransom and extortion payments |  | A.5.26, A.5.31 | RS.MA-01 | IR-4 | — | CC7.4 | APO12, MEA03 | — |
| RES-001.5.8 Readiness, testing and improvement |  | 10.2; A.5.27 | ID.IM-01, ID.IM-02, ID.IM-04 | IR-2, IR-3, IR-4 | 17.7, 17.8 | CC4.2, CC7.5 | DSS02, MEA01 | [PCI] 12.10.2, 12.10.4, 12.10.6 |
| RES-001.5.9 Confidentiality of incident information |  | A.5.14, A.5.26 | RS.CO-02, RS.CO-03 | IR-4, IR-6 | 17.6 | C1.1, CC2.2 | DSS05 | [SOX] Form 8-K Item 1.05 (via RES-003) |

**RES-002 Incident Response Plan**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| RES-002.5.1 Use of this Plan |  | A.5.24, A.5.25 | DE.AE-08, RS.MA-01, RS.MA-02, RS.MA-03, RS.MA-04 | IR-4, IR-5, IR-8 | 17.4, 17.9 | CC7.3, CC7.4 | DSS02.02, DSS02.03 | [PCI] 12.10.1 · [HIPAA] §164.308(a)(6)(ii) |
| RES-002.5.2 Severity classification |  | A.5.24, A.5.25 | DE.AE-08, RS.MA-01, RS.MA-02, RS.MA-03, RS.MA-04 | IR-4, IR-5, IR-8 | 17.4, 17.9 | CC7.3, CC7.4 | DSS02.02, DSS02.03 | [PCI] 12.10.1 · [HIPAA] §164.308(a)(6)(ii) |
| RES-002.5.3 Response time limits |  | A.5.24, A.5.25 | DE.AE-08, RS.MA-01, RS.MA-02, RS.MA-03, RS.MA-04 | IR-4, IR-5, IR-8 | 17.4, 17.9 | CC7.3, CC7.4 | DSS02.02, DSS02.03 | [PCI] 12.10.1 · [HIPAA] §164.308(a)(6)(ii) |
| RES-002.5.4 Incident Response Team roles |  | A.5.2, A.5.24 | GV.RR-02, RS.MA-01 | IR-4, IR-7, IR-8 | 17.1, 17.5 | CC1.3, CC7.4 | APO07, DSS02 | [PCI] 12.10.3 |
| RES-002.5.5 Phase 1 — Preparation |  | A.5.5, A.5.6, A.5.24 | ID.IM-04, PR.AT-02 | IR-2, IR-7, IR-8 | 17.2, 17.6 | CC7.3, CC7.4 | DSS02, DSS05 | [PCI] 12.10.4, 12.10.5 |
| RES-002.5.6 Phase 2 — Detection and analysis | KC-58 | A.5.25, A.6.8, A.8.16 | DE.AE-02, DE.AE-03, DE.AE-07, RS.AN-03, RS.AN-06, RS.AN-07, RS.AN-08 | IR-4, IR-5, SI-4 | 17.4, 17.9 | CC7.2, CC7.3 | DSS02, DSS05 | [HIPAA] §164.308(a)(6)(ii) |
| RES-002.5.7 Phase 3 — Containment |  | A.5.26 | RS.MI-01, RS.MI-02 | IR-4 | 17.4 | CC7.4 | DSS02, DSS05 | [HIPAA] §164.308(a)(6)(ii) |
| RES-002.5.8 Phase 4 — Eradication |  | A.5.26 | RS.MI-01, RS.MI-02 | IR-4 | 17.4 | CC7.4 | DSS02, DSS05 | [HIPAA] §164.308(a)(6)(ii) |
| RES-002.5.9 Phase 5 — Recovery |  | A.5.26, A.5.29, A.8.13 | RC.RP-01, RC.RP-02, RC.RP-03, RC.RP-05, RC.RP-06 | CP-10, IR-4 | 11.5, 17.4 | CC7.5 | DSS02, DSS04 | [GDPR] Art. 32(1)(c) |
| RES-002.5.10 Phase 6 — Post-incident activity and closure | KC-59 | 10.1, 10.2; A.5.27 | ID.IM-01, ID.IM-02, ID.IM-03, ID.IM-04, RS.MA-05 | IR-4, IR-8 | 17.8 | CC4.2, CC7.5 | DSS02.06, MEA01 | [PCI] 12.10.6 |
| RES-002.5.11 Escalation matrix |  | A.5.5, A.5.24, A.5.26 | RC.CO-03, RC.CO-04, RS.CO-02, RS.CO-03 | IR-4, IR-6 | 17.2, 17.6 | CC2.2, CC2.3, CC7.4 | APO08, DSS02 | [GDPR] Art. 33 (via RES-003) · [SOX] Form 8-K Item 1.05 (via RES-003) |
| RES-002.5.12 Communications plan |  | A.5.5, A.5.24, A.5.26 | RC.CO-03, RC.CO-04, RS.CO-02, RS.CO-03 | IR-4, IR-6 | 17.2, 17.6 | CC2.2, CC2.3, CC7.4 | APO08, DSS02 | [GDPR] Art. 33 (via RES-003) · [SOX] Form 8-K Item 1.05 (via RES-003) |
| RES-002.5.13 Playbook index |  | A.5.24, A.5.26 | RS.MA-01, RS.MI-01, RS.MI-02 | IR-4, IR-8, IR-9 | 17.4 | CC7.4 | DSS02 | [PCI] 12.10.1, 12.10.7 |
| RES-002.5.14 Testing and exercises | KC-60 | A.5.24, A.5.27 | ID.IM-02, ID.IM-04 | IR-3, IR-8 | 17.7 | CC7.4, CC7.5 | DSS02, DSS04 | [PCI] 12.10.2 · [HIPAA] §164.308(a)(6) |
| RES-002.5.15 Plan maintenance |  | A.5.24, A.5.27 | ID.IM-02, ID.IM-04 | IR-3, IR-8 | 17.7 | CC7.4, CC7.5 | DSS02, DSS04 | [PCI] 12.10.2 · [HIPAA] §164.308(a)(6) |

**RES-003 Breach Notification Standard**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| RES-003.5.1 Internal escalation |  | A.5.24, A.5.26 | RS.CO-02, RS.MA-01 | IR-6 | 17.2, 17.6 | CC2.2, CC7.4 | DSS02 | [HIPAA] §164.404(a)(2) · [GDPR] Art. 33(1) |
| RES-003.5.2 Breach determination process | KC-61 | A.5.25, A.5.34 | RS.AN-03, RS.MA-03 | IR-4, IR-6 | 17.9 | CC7.3, P6.6 | APO12, MEA03 | [GDPR] Arts. 4(12), 33, 34, 56 |
| RES-003.5.3 GDPR risk to rights and freedoms [GDPR] |  | A.5.25, A.5.34 | RS.AN-03, RS.MA-03 | IR-4, IR-6 | 17.9 | CC7.3, P6.6 | APO12, MEA03 | [GDPR] Arts. 4(12), 33, 34, 56 |
| RES-003.5.4 HIPAA four-factor risk assessment [HIPAA] |  | A.5.25, A.5.34 | RS.AN-03 | IR-4, IR-6 | 17.9 | CC7.3, P6.6 | MEA03 | [HIPAA] §§164.402, 164.414 |
| RES-003.5.5 SEC materiality determination [SOX] |  | A.5.31 | GV.OC-03, RS.CO-03 | IR-6 | — | CC2.3 | EDM05, MEA03 | [SOX] Form 8-K Item 1.05; Reg. S-K Item 106 (17 CFR 229.106); §302 |
| RES-003.5.6 Notification requirements by regulation |  | A.5.5, A.5.26, A.5.31, A.5.34 | RC.CO-03, RC.CO-04, RS.CO-02, RS.CO-03 | IR-6 | 17.6 | CC2.3, P6.6 | MEA03 | [PCI] 12.10.1 · [HIPAA] §§164.404–164.410 · [GDPR] Arts. 33, 34 · [CPRA] §1798.82 · [SOX] Form 8-K Item 1.05 |
| RES-003.5.7 Notification content templates |  | A.5.26, A.5.34 | RS.CO-03 | IR-6 | 17.6 | CC2.3, P6.6 | MEA03 | [HIPAA] §§164.404(c), 164.410(c) · [GDPR] Arts. 33(3), 34(2) · [CPRA] §1798.82(d) |
| RES-003.5.8 Documentation of decisions not to notify |  | A.5.27, A.5.33 | ID.IM-01 | IR-4, IR-5 | 17.8 | CC7.4, P6.6 | MEA03 | [HIPAA] §§164.412, 164.414 · [GDPR] Art. 33(5) |
| RES-003.5.9 Third-Party breaches |  | A.5.19, A.5.20 | GV.SC-05, GV.SC-08 | IR-6, SR-8 | 15.4 | CC9.2 | APO10 | [HIPAA] §164.504(e) · [GDPR] Art. 28(3)(f), 33(2) |
| RES-003.5.10 Readiness |  | A.5.5, A.5.24 | ID.IM-04, PR.AT-02 | IR-2, IR-3 | 17.2, 17.7 | CC2.3 | DSS02 | [PCI] 12.10.2 |

**RES-004 Business Continuity Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| RES-004.5.1 BCM program and scope |  | 4.3, 5.1, 6.1; A.5.29, A.5.30 | GV.OC-04, GV.RR-02 | CP-1, CP-2, PM-8 | — | A1.2, CC9.1 | DSS04.01 | Other: ISO 22301:2019 cl. 4–6 |
| RES-004.5.2 Business impact analysis and risk assessment |  | 6.1.2, 8.2; A.5.30 | GV.OC-04, ID.RA-01 | CP-2, RA-3 | — | CC3.2, CC9.1 | APO12, DSS04.02 | [HIPAA] §164.308(a)(7)(ii)(E) |
| RES-004.5.3 Continuity strategies |  | A.5.29, A.5.30, A.7.11, A.8.14 | PR.IR-03 | CP-2, CP-6, CP-7, CP-8 | — | A1.2, CC9.1 | DSS04.02, DSS04.03 | [PCI] 12.10.1 · [HIPAA] §164.308(a)(7)(ii)(C) · [SOX] §404 |
| RES-004.5.4 Crisis Management Team |  | 5.3; A.5.29 | GV.RR-02, RS.MA-01 | CP-2, IR-4 | 17.4 | CC7.4, CC7.5 | DSS04.03 | — |
| RES-004.5.5 Business continuity plans |  | A.5.29, A.5.30 | ID.IM-04, RC.RP-01 | CP-2, CP-10 | — | A1.2, CC7.5 | DSS04.03 | [PCI] 12.10.1 · [HIPAA] §164.308(a)(7)(i) |
| RES-004.5.6 Pandemic and widespread illness |  | A.5.29 | GV.OC-04, GV.RR-02 | CP-2, CP-3 | — | CC9.1 | DSS04.03 | — |
| RES-004.5.7 Workforce unavailability |  | A.5.29 | GV.OC-04, GV.RR-02 | CP-2, CP-3 | — | CC9.1 | DSS04.03 | — |
| RES-004.5.8 Supplier and Third Party failure |  | A.5.19, A.5.21, A.5.22, A.5.30 | GV.OC-05, GV.SC-08 | CP-2, SA-9, SR-2 | 15.1 | CC9.2 | APO10, DSS04.03 | — |
| RES-004.5.9 Loss of premises and utilities |  | A.5.29, A.7.5, A.7.11 | RC.CO-03, RC.CO-04 | CP-2, CP-8, PE-1 | 17.6 | A1.2, CC2.3 | DSS04.03 | — |
| RES-004.5.10 Communications during disruption |  | A.5.29, A.7.5, A.7.11 | RC.CO-03, RC.CO-04 | CP-2, CP-8, PE-1 | 17.6 | A1.2, CC2.3 | DSS04.03 | — |
| RES-004.5.11 Exercises | KC-62 | 9.1; A.5.30 | ID.IM-02, ID.IM-04 | CP-3, CP-4 | 17.7 | A1.3, CC7.5 | DSS04.04, DSS04.05 | [PCI] 12.10.2 · [HIPAA] §164.308(a)(7)(ii)(D) |
| RES-004.5.12 Plan maintenance |  | 7.2, 7.3, 10.2; A.5.29 | ID.IM-04, PR.AT-02 | CP-2, CP-3 | — | A1.3 | DSS04.06, DSS04.08 | [HIPAA] §164.308(a)(7)(ii)(D) |
| RES-004.5.13 Training and awareness |  | 7.2, 7.3, 10.2; A.5.29 | ID.IM-04, PR.AT-02 | CP-2, CP-3 | — | A1.3 | DSS04.06, DSS04.08 | [HIPAA] §164.308(a)(7)(ii)(D) |

**RES-005 Disaster Recovery Plan**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| RES-005.5.1 DR organization |  | A.5.29, A.5.30, A.5.37 | GV.RR-02, RC.RP-01 | CP-2, CP-3 | 11.1 | A1.2, CC7.5 | DSS04.03 | [HIPAA] §164.308(a)(7)(ii)(B) |
| RES-005.5.2 Activation and Disaster Declaration |  | A.5.26, A.5.29 | RC.RP-01, RS.MA-01 | CP-2, CP-10, IR-4 | 17.4 | CC7.4, CC7.5 | DSS04.03 | — |
| RES-005.5.3 Recovery procedures by Recovery Tier |  | A.5.30, A.8.13, A.8.14 | PR.DS-11, RC.RP-02, RC.RP-03, RC.RP-05 | CP-9, CP-10 | 11.1, 11.2, 11.3 | A1.2, CC7.5 | BAI04, DSS04.03 | [PCI] 12.10.1 · [HIPAA] §164.308(a)(7)(ii)(A)–(B) · [GDPR] Art. 32(1)(c) · [SOX] §404 |
| RES-005.5.4 Recovery sequencing and dependencies |  | A.5.9, A.5.30 | GV.OC-04, ID.AM-01, RC.RP-01 | CM-8, CP-2 | 1.1 | A1.2 | DSS04.02 | [HIPAA] §164.308(a)(7)(ii)(E) |
| RES-005.5.5 Failover |  | A.8.14, A.8.32 | PR.IR-03, RC.RP-04 | CM-3, CP-7, CP-10 | 11.4 | A1.2, CC8.1 | BAI06, DSS04.03 | [PCI] 12.10.1 |
| RES-005.5.6 Failback |  | A.8.14, A.8.32 | PR.IR-03, RC.RP-04 | CM-3, CP-7, CP-10 | 11.4 | A1.2, CC8.1 | BAI06, DSS04.03 | [PCI] 12.10.1 |
| RES-005.5.7 Recovery from destructive attack |  | A.5.26, A.8.7, A.8.13 | RC.RP-03, RC.RP-04, RS.MI-01 | CP-9, CP-10, IR-4, SI-3 | 11.3, 11.4 | CC7.4, CC7.5 | DSS04.03, DSS05 | — |
| RES-005.5.8 Communications during recovery |  | A.5.27, A.5.29 | ID.IM-03, RC.CO-03, RC.CO-04, RC.RP-06 | CP-2, IR-4 | 17.6, 17.8 | CC2.3, CC7.5 | DSS04.07, DSS04.08 | — |
| RES-005.5.9 Stand-down and post-recovery review |  | A.5.27, A.5.29 | ID.IM-03, RC.CO-03, RC.CO-04, RC.RP-06 | CP-2, IR-4 | 17.6, 17.8 | CC2.3, CC7.5 | DSS04.07, DSS04.08 | — |
| RES-005.5.10 Testing | KC-63 | 9.1, 10.2; A.5.30 | ID.IM-02, ID.IM-04 | CP-2, CP-4 | 11.5 | A1.3 | DSS04.04, DSS04.05, DSS04.06 | [PCI] 12.10.2 · [HIPAA] §164.308(a)(7)(ii)(D) |
| RES-005.5.11 Plan maintenance and records |  | 9.1, 10.2; A.5.30 | ID.IM-02, ID.IM-04 | CP-2, CP-4 | 11.5 | A1.3 | DSS04.04, DSS04.05, DSS04.06 | [PCI] 12.10.2 · [HIPAA] §164.308(a)(7)(ii)(D) |

#### 5.3.7 People

**PPL-001 Human Resources Security Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| PPL-001.5.1 Position risk designation |  | A.6.1 | GV.RR-04 | PS-2, PS-3 | — | CC1.4 | APO07.01 | [PCI] 12.7.1 · [HIPAA] §164.308(a)(3)(ii)(B) · [GDPR] Art. 6, 9, 10, 88 |
| PPL-001.5.2 Screening | KC-64 | A.6.1 | GV.RR-04 | PS-2, PS-3 | — | CC1.4 | APO07.01 | [PCI] 12.7.1 · [HIPAA] §164.308(a)(3)(ii)(B) · [GDPR] Art. 6, 9, 10, 88 |
| PPL-001.5.3 Terms of employment and engagement | KC-65 | A.6.2, A.6.6 | GV.RR-04 | PL-4, PS-6 | — | CC1.1, CC1.4 | APO07.06 | [HIPAA] §164.308(a)(1)(ii)(C) |
| PPL-001.5.4 Onboarding |  | A.5.16, A.6.2 | PR.AA-01 | AC-2, PS-3 | 5.1, 6.1 | CC6.2 | APO07, DSS05.04 | [HIPAA] §164.308(a)(3)(ii)(A) |
| PPL-001.5.5 Role change |  | A.5.18, A.6.5 | PR.AA-05 | AC-2, PS-5 | 6.1, 6.2 | CC6.2, CC6.3 | APO07 | [HIPAA] §164.308(a)(4) |
| PPL-001.5.6 Leave of absence |  | A.5.18, A.6.5 | PR.AA-05 | AC-2, PS-5 | 6.1, 6.2 | CC6.2, CC6.3 | APO07 | [HIPAA] §164.308(a)(4) |
| PPL-001.5.7 Separation |  | A.5.11, A.6.5 | PR.AA-05 | PS-4, PS-7 | 6.2 | CC6.2, CC6.5 | APO07.06, DSS05.04 | [PCI] 8.2.5 · [HIPAA] §164.308(a)(3)(ii)(C) |
| PPL-001.5.8 Disciplinary linkage |  | A.6.4 | GV.RR-04 | PS-8 | — | CC1.5 | APO07 | [HIPAA] §164.308(a)(1)(ii)(C) |
| PPL-001.5.9 Records |  | A.5.33, A.5.34 | PR.DS-01 | PS-1 | 3.3 | C1.1 | APO07 | [GDPR] Art. 5(1)(e), 32 |

**PPL-002 Security Awareness & Training Policy**

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| PPL-002.5.1 Program governance |  | 7.2, 7.3; A.6.3 | PR.AT-01 | AT-1, PM-13, PM-14 | 14.1 | CC1.4, CC2.2 | APO07.03 | [PCI] 12.6.1, 12.6.2 |
| PPL-002.5.2 Training at hire | KC-66 | 7.3; A.6.3 | PR.AT-01 | AT-2, AT-4 | 14.1, 14.2, 14.3, 14.4, 14.5, 14.6, 14.7, 14.8 | CC1.4, CC2.2 | APO07.03 | [PCI] 12.6.3, 12.6.3.2 · [HIPAA] §164.308(a)(5) · [GDPR] Art. 39(1)(b) |
| PPL-002.5.3 Annual training | KC-67 | 7.3; A.6.3 | PR.AT-01 | AT-2, AT-4 | 14.1, 14.2, 14.3, 14.4, 14.5, 14.6, 14.7, 14.8 | CC1.4, CC2.2 | APO07.03 | [PCI] 12.6.3, 12.6.3.2 · [HIPAA] §164.308(a)(5) · [GDPR] Art. 39(1)(b) |
| PPL-002.5.4 Role-based training |  | 7.2; A.6.3 | PR.AT-02 | AT-3 | 14.9, 16.9 | CC1.4 | APO07.03 | [PCI] 6.2.2 · [HIPAA] §164.308(a)(5) · [CPRA] §1798.130(a)(6) |
| PPL-002.5.5 Phishing simulation |  | A.6.3 | PR.AT-01 | AT-2(3) | 14.2 | CC1.4 | APO07.03 | [PCI] 12.6.3.1 |
| PPL-002.5.6 Ongoing awareness |  | A.6.3 | PR.AT-01 | AT-2 | 14.1 | CC2.2 | APO07.03 | [HIPAA] §164.308(a)(5)(ii)(A) |
| PPL-002.5.7 Non-completion |  | 7.2; A.5.19, A.6.3 | GV.SC-05, PR.AT-01 | AT-2, PS-7 | 14.1 | CC1.4, CC9.2 | APO07 | — |
| PPL-002.5.8 Third Parties |  | 7.2; A.5.19, A.6.3 | GV.SC-05, PR.AT-01 | AT-2, PS-7 | 14.1 | CC1.4, CC9.2 | APO07 | — |
| PPL-002.5.9 Records and effectiveness |  | 7.2, 9.1 | ID.IM-01, PR.AT-01 | AT-4 | — | CC1.4 | APO07.03, MEA01 | — |

#### 5.3.8 Templates

| Requirement | KC | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|---|
| TPL-001 Risk Register Template (form; inherits RSK-001.5.2, RSK-001.5.6, RSK-002.5.9) | | 4.1, 4.2, 6.1.2, 7.5.3, 8.2, 9.1, 9.3 | GV.OC-01, GV.OV-01, GV.OV-03, GV.RM-06, ID.IM-01, ID.RA-03, ID.RA-04 | CA-7, PM-9, PM-28, RA-3 | — | CC3.2, CC3.3, CC4.1, CC4.2 | APO12.01, APO12.03, APO12.04, MEA01 | [GDPR] Art. 24, 32 · [SOX] §404 |
| TPL-002 Risk Acceptance Form (form; inherits RSK-001.5.5) | | 6.1.3 | GV.RM-04, ID.RA-07 | PM-9, RA-7 | — | CC3.2 | APO12.06 | [PCI] 12.3.1 |
| TPL-003 Policy Exception Request Form (form; inherits CMP-003.5.3, CMP-003.5.8) | | 6.1.2, 6.1.3, 7.5, 9.1, 9.3; A.5.4, A.5.36 | GV.OV-01, GV.OV-03, GV.RM-01, GV.RM-06, ID.RA-05 | CA-5, PM-4, PM-9, RA-3, RA-7 | — | CC2.1, CC3.2, CC4.1, CC4.2, CC5.2 | APO12, MEA01, MEA02 | [PCI] 12.3.1 · [HIPAA] §164.308(a)(1)(ii)(B) · [SOX] §404 |
| TPL-004 Vendor Security Questionnaire (form; inherits RSK-003.5.3) | | A.5.19, A.5.21 | GV.SC-06, GV.SC-07, ID.RA-10 | SA-9, SR-6 | 15.5 | CC9.2 | APO10.03 | [PCI] 12.8.3 · [GDPR] Art. 28(1) |
| TPL-005 Data Protection Impact Assessment Template (form; inherits CMP-005.5.9) | | 6.1.2; A.5.34 | GV.RM-01, ID.RA-01 | RA-3, RA-8 | — | CC3.2, P3.1 | APO12 | [GDPR] Art. 35, 36 |
| TPL-006 Incident Report Template (form; inherits RES-002.5.6) | | A.5.25, A.6.8, A.8.16 | DE.AE-02, DE.AE-03, DE.AE-07, RS.AN-03, RS.AN-06, RS.AN-07, RS.AN-08 | IR-4, IR-5, SI-4 | 17.4, 17.9 | CC7.2, CC7.3 | DSS02, DSS05 | [HIPAA] §164.308(a)(6)(ii) |
| TPL-007 Post-Incident Review Template (form; inherits RES-002.5.10) | | 10.1, 10.2; A.5.27 | ID.IM-01, ID.IM-02, ID.IM-03, ID.IM-04, RS.MA-05 | IR-4, IR-8 | 17.8 | CC4.2, CC7.5 | DSS02.06, MEA01 | [PCI] 12.10.6 |
| TPL-008 Access Review Template (form; inherits SEC-003.5.12, SEC-005.5.11) | | A.5.18, A.8.2 | ID.IM-01, PR.AA-05 | AC-2, AC-6 | 5.1, 5.3, 5.4, 6.2 | CC4.1, CC6.2, CC6.3 | DSS05.04, MEA02 | [PCI] 7.2.4; 7.2.4, 7.2.5.1 · [HIPAA] §164.308(a)(4)(ii)(C) · [SOX] §404 |
| TPL-009 Policy Acknowledgement Form (form; inherits GOV-002.5.9) | | 7.3; A.5.1, A.6.2 | PR.AT-01 | PL-4, PS-6 | 14.1 | CC1.1, CC2.2 | APO07.06 | [PCI] 12.6.3 · [HIPAA] §164.308(a)(5)(i) |
| TPL-010 Record of Processing Activities Template (form; inherits CMP-005.5.8) | | A.5.9, A.5.34 | ID.AM-07 | PM-5, PT-3 | 3.2 | P3.1 | APO14 | [GDPR] Art. 30 |

### 5.4 Key Controls for the SOC 2 Type II examination

The Key Controls below are designated under REF-001.5.1.4. Each is marked in the KC column of
section 5.3. CMP-002 sets how often each Key Control is self-assessed and tested, and CMP-004
sets how its Evidence is kept. The frequency and any numeric value for each Key Control
are set in the document named in the last column, not here. The SOC 2 TSC column lists the
in-scope criteria mapped to the requirement. `[SOX]` ITGC Key Controls over Financially
Significant Systems are designated separately in CMP-009 sections 5.4 to 5.7.

| KC ID | Requirement | Key Control | SOC 2 TSC | Control Owner | Frequency and values set in |
|---|---|---|---|---|---|
| KC-01 | ISP-000.5.7 Board oversight | The Audit Committee and Board of Directors receive and minute the CISO's program reports at the cadence set in GOV-001 and GOV-003. | CC1.2, CC4.2 | CISO | GOV-003 |
| KC-02 | GOV-001.5.1 Governance structure | Every applicable role is assigned to a named holder and deputy in the role-assignment register, which is updated and reviewed as set in GOV-001. | CC1.2, CC1.3 | Head of GRC | GOV-001 |
| KC-03 | GOV-001.5.3 Information Security Steering Committee (ISSC) charter | The ISSC meets at the cadence set in GOV-001 with quorum recorded; minutes record decisions, votes and actions with owners and due dates. | CC1.2, CC2.2 | CISO | GOV-001 |
| KC-04 | GOV-001.5.7 Segregation of Duties | Conflicting duties in the GOV-001 matrix are enforced in system roles; conflicts found in Access Reviews are removed or covered by an Exception. | CC5.1, CC6.3 | System Owner | GOV-001 |
| KC-05 | GOV-002.5.5 Approval | Each suite document is approved by the approver required by GOV-002 before publication, and the owner is never the approver. | CC5.3 | Head of GRC | GOV-002 |
| KC-06 | GOV-002.5.7 Review | Each suite document is reviewed within the scheduled and event-triggered review periods set in GOV-002; overdue reviews are escalated. | CC5.3 | Head of GRC | GOV-002 |
| KC-07 | GOV-002.5.9 Workforce attestation | Workforce Members attest to their assigned policy set before access is granted and at the frequency set in GOV-002. | CC1.1, CC2.2 | Head of GRC | GOV-002 |
| KC-08 | GOV-003.5.5 Reporting cadence | Operational metrics and the KRI dashboard are reported to the ISSC and Audit Committee at the cadence set in GOV-003. | CC1.2, CC2.2 | CISO | GOV-003 |
| KC-09 | RSK-001.5.3 Risk Appetite and Risk Tolerance | Risk Appetite and Risk Tolerance are reviewed, approved by the ISSC and ratified by the Audit Committee as set in RSK-001. | CC3.1 | Head of GRC | RSK-001 |
| KC-10 | RSK-001.5.5 Risk Acceptance | Each Risk Acceptance is approved at the authority level and within the validity period set in RSK-001, using TPL-002. | CC3.2 | Head of GRC | RSK-001 |
| KC-11 | RSK-001.5.6 Monitoring, review and escalation | The ISSC reviews the Risk Register at the frequency set in RSK-001; overdue treatment plans are escalated. | CC4.1, CC4.2 | Head of GRC | RSK-001 |
| KC-12 | RSK-002.5.6 Assessment frequency and triggers | The enterprise risk assessment is performed at the frequency and on the triggers set in RSK-002, and the report is approved by the CISO. | CC3.4 | Head of GRC | RSK-002 |
| KC-13 | RSK-002.5.10 Fraud risk | Each enterprise risk assessment explicitly assesses fraud risk, including management override of Controls, and records fraud scenarios in the Risk Register (RSK-002.5.10). | CC3.3 | Head of GRC | RSK-002 |
| KC-14 | RSK-003.5.3 Due diligence | Third Parties complete tier-based security due diligence (TPL-004) before contract signature. | CC9.2 | Head of GRC | RSK-003 |
| KC-15 | RSK-003.5.4 Contract requirements | Third-Party contracts contain the security, privacy, notification and audit terms required by RSK-003 before signature. | C1.1, CC9.2 | Head of Procurement | RSK-003 |
| KC-16 | RSK-003.5.5 Ongoing monitoring and reassessment | Third Parties are reassessed, and their assurance reports reviewed, at the frequency set for their vendor tier in RSK-003. | CC4.1, CC9.2 | Head of GRC | RSK-003 |
| KC-17 | RSK-004.5.5 Dependency mapping | Dependency maps for Tier 0 and Tier 1 processes, including Third-Party dependencies, are maintained and updated as set in RSK-004. | CC9.1, CC9.2 | Business Continuity Manager | RSK-004 |
| KC-18 | RSK-004.5.7 Approval, refresh and records | The BIA is approved and refreshed at the frequency set in RSK-004, and Recovery Tier 0 and Tier 1 assignments are approved by the ISSC. | A1.2 | Business Continuity Manager | RSK-004 |
| KC-19 | CMP-001.5.9 Contractual obligations and customer assurance | Security and privacy commitments in customer and Third-Party contracts are reviewed by the Head of GRC before execution and recorded in the Obligations Register. | CC2.3, CC9.2 | Head of GRC | CMP-001 |
| KC-20 | CMP-002.5.5 Control testing methods | Every Key Control is tested for operating effectiveness at the frequency and with the methods set in CMP-002. | CC4.1 | Head of GRC | CMP-002 |
| KC-21 | CMP-002.5.8 Issue management and remediation | Control deficiencies are recorded in the issue register, classified, and remediated within the timelines set in CMP-002. | CC4.2, CC5.1 | Head of GRC | CMP-002 |
| KC-22 | CMP-003.5.4 Assessment and approval | Each Exception is assessed and approved by the authority set in CMP-003 before the deviation starts, using TPL-003, and recorded in the Exception register. | CC3.2, CC5.2 | Head of GRC | CMP-003 |
| KC-23 | CMP-004.5.3 Secure deletion at end of retention | Records and Confidential information are securely deleted at the end of their retention period unless under Legal Hold. | C1.2 | Head of GRC | CMP-004 |
| KC-24 | CMP-004.5.5 Evidence collection and quality | Control Owners collect, label and store Evidence of each Key Control operation within the time set in CMP-004. | CC4.1, CC7.3 | Head of GRC | CMP-004 |
| KC-25 | CMP-007.5.4 Process and due process | Security policy violations are investigated and sanctioned under the documented due process in CMP-007, and each case is recorded. | CC1.5, CC6.2 | CHRO | CMP-007 |
| KC-26 | SEC-001.5.9 Reconciliation and verification | The Asset Inventory is reconciled against discovery sources at the frequency set in SEC-001; unknown assets are triaged. | CC3.2, CC4.1 | CIO | SEC-001 |
| KC-27 | SEC-002.5.3 Data Owner duties | Data Owners classify their data sets and review the classification at the frequency set in SEC-002. | C1.1, CC3.2 | Data Owner | SEC-002 |
| KC-28 | SEC-003.5.3 Mover | Access no longer required after a role change is removed within the time set in SEC-003. | CC6.2, CC6.3 | System Owner | SEC-003 |
| KC-29 | SEC-003.5.4 Access request and approval | Access is granted only on a documented request approved by the System Owner or Data Owner before provisioning. | CC5.2, CC6.1, CC6.3 | System Owner | SEC-003 |
| KC-30 | SEC-003.5.7 Leaver | Accounts of separated Workforce Members are revoked within the time set in SEC-003. | CC6.2, CC6.3 | CIO | SEC-003 |
| KC-31 | SEC-003.5.12 Access Reviews | User Access Reviews are performed at the frequency set in SEC-003 using TPL-008, and findings are remediated. | CC4.1, CC6.2, CC6.3 | System Owner | SEC-003 |
| KC-32 | SEC-004.5.4 Multi-Factor Authentication | MFA is enforced for every access type required by SEC-004. | CC6.1, CC6.6 | Head of Security Engineering | SEC-004 |
| KC-33 | SEC-005.5.3 PAM vaulting | Privileged credentials are vaulted in the PAM system and rotated after use as set in SEC-005. | CC6.1 | Head of Security Engineering | SEC-005 |
| KC-34 | SEC-005.5.11 Privileged access review | Privileged access is reviewed at the frequency set in SEC-005. | CC6.2, CC6.3 | Head of Security Engineering | SEC-005 |
| KC-35 | SEC-006.5.2 Approved algorithms and protocols | Data at rest and in transit is encrypted with the approved algorithms and protocols in SEC-006. | CC6.1, CC6.7 | Head of Security Engineering | SEC-006 |
| KC-36 | SEC-007.5.3 Firewall and security-group rule review | Firewall, security-group and network ACL rules are reviewed at the frequency set in SEC-007; unused rules are removed. | CC6.6, CC7.1 | Head of Security Engineering | SEC-007 |
| KC-37 | SEC-007.5.8 Network documentation | Network and data-flow diagrams are kept current and reviewed as set in SEC-007. | CC2.1 | Head of Security Engineering | SEC-007 |
| KC-38 | SEC-008.5.3 Malware protection and endpoint detection and response (EDR) | EDR is deployed and reporting on every in-scope Endpoint at the coverage set in SEC-008. | CC6.8, CC7.2 | Head of Security Engineering | SEC-008 |
| KC-39 | SEC-008.5.4 Encryption | Full-disk encryption is enforced on Endpoints and Mobile Devices as set in SEC-008. | CC6.1, CC6.7 | CIO | SEC-008 |
| KC-40 | SEC-009.5.5 Cloud security posture management (CSPM/CNAPP) | All cloud accounts are onboarded to CSPM/CNAPP and findings are remediated within the time set in SEC-009. | CC7.1 | Head of Security Engineering | SEC-009 |
| KC-41 | SEC-010.5.4 Code review | Every code change is peer-reviewed and approved by someone other than the author before merge. | CC8.1 | CTO | SEC-010 |
| KC-42 | SEC-010.5.5 Automated security testing gates | Automated security testing gates block releases with findings above the thresholds in SEC-010. | CC7.1, CC8.1 | Head of Security Engineering | SEC-010 |
| KC-43 | SEC-011.5.2 Scanning | Internal and external vulnerability scans are performed at the frequencies set in SEC-011. | CC7.1 | Head of Security Engineering | SEC-011 |
| KC-44 | SEC-011.5.4 Remediation | Vulnerabilities are remediated within the SLA in SEC-011 or covered by an approved Exception. | CC7.1, CC7.4 | System Owner | SEC-011 |
| KC-45 | SEC-011.5.7 Penetration testing | Penetration Tests are performed at the frequency and on the triggers set in SEC-011, and findings are tracked to closure. | CC4.1, CC7.1 | Head of Security Engineering | SEC-011 |
| KC-46 | SEC-012.5.6 Centralization in a SIEM | Required log sources forward to the SIEM, and log-source silence raises an alert. | CC7.2 | SOC Manager | SEC-012 |
| KC-47 | SEC-012.5.8 Alert triage and escalation | Security alerts are triaged within the SLA set in SEC-012 and escalated as Security Incidents where criteria are met. | CC7.3, CC7.4 | SOC Manager | SEC-012 |
| KC-48 | SEC-012.5.9 Log review | Logs are reviewed by automated and manual review as set in SEC-012. | CC4.1, CC7.2 | SOC Manager | SEC-012 |
| KC-49 | SEC-013.5.5 Approval and the Change Advisory Board | Normal Changes are approved by the CAB, and Emergency Changes retrospectively, before or within the time set in SEC-013. | CC8.1 | CIO | SEC-013 |
| KC-50 | SEC-013.5.8 Configuration Baselines and hardening | Systems are built from approved Configuration Baselines that are reviewed at the frequency set in SEC-013. | CC7.1 | Head of Security Engineering | SEC-013 |
| KC-51 | SEC-013.5.9 Drift detection and unauthorized change | Configuration drift and unauthorized Changes are detected and remediated as set in SEC-013. | CC7.1 | Head of Security Engineering | SEC-013 |
| KC-52 | SEC-013.5.12 Capacity management | Capacity thresholds are monitored with automated alerts, and capacity forecasts are produced at the frequency set in SEC-013, for the Information Systems in scope of SEC-013.5.12. | A1.1 | CIO | SEC-013 |
| KC-53 | SEC-016.5.2 Badge and physical access control | Physical access to secure zones is granted on approval, revoked on Separation and reviewed at the frequency set in SEC-016. | CC6.4 | Head of Facilities | SEC-016 |
| KC-54 | SEC-016.5.7 Environmental controls | Environmental protection systems in Tier 0 and Tier 1 facilities are monitored and tested as set in SEC-016. | A1.2 | Head of Facilities | SEC-016 |
| KC-55 | SEC-017.5.5 Records and Certificates of Destruction | Media Sanitization is recorded and reconciled to Certificates of Destruction. | C1.2, CC6.5 | CIO | SEC-017 |
| KC-56 | SEC-018.5.6 Restore testing | Restores are tested at the frequency set in SEC-018 for each Recovery Tier. | A1.3 | CIO | SEC-018 |
| KC-57 | SEC-018.5.7 Monitoring of Backup jobs | Backup jobs are monitored and failures are re-run and escalated as set in SEC-018. | A1.2, CC7.2 | CIO | SEC-018 |
| KC-58 | RES-002.5.6 Phase 2 — Detection and analysis | Security Incidents are recorded (TPL-006), classified by Severity Level and analysed within the SLAs set in RES-002. | CC7.2, CC7.3 | SOC Manager | RES-002 |
| KC-59 | RES-002.5.10 Phase 6 — Post-incident activity and closure | A post-incident review (TPL-007) is completed for each Sev-1 and Sev-2 Security Incident within the time set in RES-002. | CC4.2, CC7.5 | SOC Manager | RES-002 |
| KC-60 | RES-002.5.14 Testing and exercises | The incident response plan is exercised at the frequency set in RES-002. | CC7.4, CC7.5 | SOC Manager | RES-002 |
| KC-61 | RES-003.5.2 Breach determination process | Every suspected Personal Data Breach goes to a breach determination group, whose signed decision is recorded. | CC7.3 | CPO | RES-003 |
| KC-62 | RES-004.5.11 Exercises | Business continuity exercises are performed at the frequency set in RES-004, with after-action reports. | A1.3, CC7.5 | Business Continuity Manager | RES-004 |
| KC-63 | RES-005.5.10 Testing | DR tests of Tier 0 and Tier 1 systems are performed at the frequency set in RES-004, with test reports. | A1.3 | CIO | RES-005 |
| KC-64 | PPL-001.5.2 Screening | Pre-employment screening is completed to the designated level before access to Confidential or Restricted data, as set in PPL-001. | CC1.4 | CHRO | PPL-001 |
| KC-65 | PPL-001.5.3 Terms of employment and engagement | Workforce Members sign terms of employment or engagement, including confidentiality obligations, before their start date. | CC1.1, CC1.4 | CHRO | PPL-001 |
| KC-66 | PPL-002.5.2 Training at hire | New Workforce Members complete security awareness training within the time set in PPL-002. | CC1.4, CC2.2 | CISO | PPL-002 |
| KC-67 | PPL-002.5.3 Annual training | Workforce Members complete annual security awareness training within the time set in PPL-002; non-completion is escalated. | CC1.4, CC2.2 | CISO | PPL-002 |

### 5.5 Reverse view (a): ISO/IEC 27001:2022 to suite requirements

This view lists the implementing suite requirements for every management-system clause and
all 93 Annex A controls. It is the starting point for a Statement of Applicability (REF-001.5.1.7).
"Primary document" is the document with the most implementing subsections for the control.
Status is "Covered" where at least one requirement implements the control, "Partial" where the
implementation is incomplete (section 5.11), and "Not covered" where no requirement exists.

#### 5.5.1 Clauses 4–10

| Clause | Title | Status | Implementing requirements |
|---|---|---|---|
| 4.1 | Understanding the organization and its context | Covered | CMP-001.5.4; ISP-000.5.3; RSK-001.5.2 |
| 4.2 | Understanding the needs and expectations of interested parties | Covered | CMP-001.5.1, 5.2, 5.3, 5.4, 5.8, 5.9; CMP-008.5.1; ISP-000.5.3; RSK-001.5.2; RSK-006.5.9 |
| 4.3 | Determining the scope of the information security management system | Covered | CMP-008.5.1; CMP-009.5.1, 5.2, 5.3; ISP-000.5.3; RES-004.5.1; SEC-019.5.1, 5.2 |
| 4.4 | Information security management system | Covered | ISP-000.5.1 |
| 5.1 | Leadership and commitment | Covered | CMP-002.5.1; CMP-003.5.1, 5.2; CMP-006.5.7; CMP-007.5.1, 5.2, 5.3; GOV-001.5.1, 5.2, 5.3; GOV-003.5.5, 5.6; ISP-000.5.1, 5.7; RES-004.5.1; RSK-006.5.1 |
| 5.2 | Policy | Covered | GOV-002.5.1, 5.2, 5.3, 5.4, 5.5, 5.6; GOV-006.5.1, 5.2; ISP-000.5.6 |
| 5.3 | Organizational roles, responsibilities and authorities | Covered | CMP-001.5.1; CMP-002.5.1; CMP-005.5.1; CMP-008.5.2; GOV-001.5.1, 5.2, 5.4, 5.5, 5.8; ISP-000.5.1, 5.4; RES-004.5.4; RSK-006.5.1 |
| 6.1.1 | Actions to address risks and opportunities: general | Covered | ISP-000.5.5; RES-004.5.1; RSK-001.5.1, 5.3 |
| 6.1.2 | Information security risk assessment | Covered | CMP-003.5.3, 5.4; CMP-005.5.9; CMP-008.5.3; RES-004.5.2; RSK-001.5.1, 5.2, 5.3; RSK-002.5.1, 5.2, 5.3, 5.4, 5.8, 5.10; RSK-004.5.1, 5.2; RSK-006.5.3, 5.10; SEC-019.5.10 |
| 6.1.3 | Information security risk treatment | Covered | CMP-001.5.2, 5.3; CMP-003.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7; CMP-008.5.5; CMP-009.5.1, 5.2, 5.3; RSK-001.5.4, 5.5; RSK-002.5.5, 5.7 |
| 6.2 | Information security objectives and planning to achieve them | Covered | ISP-000.5.2 |
| 6.3 | Planning of changes | Covered | CMP-001.5.4; SEC-013.5.1, 5.2 |
| 7.1 | Resources | Covered | GOV-001.5.9 |
| 7.2 | Competence | Covered | CMP-005.5.17, 5.18; GOV-001.5.9; PPL-002.5.1, 5.4, 5.7, 5.8, 5.9; RES-004.5.12, 5.13; RSK-001.5.7; RSK-006.5.1 |
| 7.3 | Awareness | Covered | CMP-006.5.8, 5.9; CMP-007.5.1, 5.2, 5.3; CMP-008.5.4; GOV-002.5.9; PPL-002.5.1, 5.2, 5.3; RES-004.5.12, 5.13; RSK-001.5.7 |
| 7.4 | Communication | Covered | CMP-006.5.1, 5.2; GOV-002.5.6; RSK-001.5.7 |
| 7.5 | Documented information | Covered | CMP-001.5.10; CMP-002.5.10; CMP-003.5.8, 5.9; CMP-004.5.1, 5.2, 5.5, 5.6, 5.7; CMP-007.5.7; CMP-008.5.10; CMP-010.5.14, 5.15; GOV-002.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.8, 5.10, 5.11; GOV-006.5.1, 5.2, 5.3, 5.4; ISP-000.5.6; RSK-002.5.9; RSK-004.5.6, 5.7; SEC-007.5.8 |
| 8.1 | Operational planning and control | **Not covered** | — |
| 8.2 | Information security risk assessment | Covered | CMP-008.5.3; RES-004.5.2; RSK-001.5.1, 5.6; RSK-002.5.1, 5.6, 5.9 |
| 8.3 | Information security risk treatment | Covered | CMP-003.5.6, 5.7; RSK-001.5.4; RSK-002.5.7 |
| 9.1 | Monitoring, measurement, analysis and evaluation | Covered | CMP-001.5.5, 5.6, 5.7; CMP-002.5.3, 5.4, 5.5, 5.6; CMP-003.5.8, 5.9; CMP-004.5.5, 5.6, 5.7; CMP-006.5.8, 5.9; CMP-007.5.7; CMP-008.5.11; CMP-009.5.10; GOV-003.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7; PPL-002.5.9; RES-004.5.11; RES-005.5.10, 5.11; RSK-001.5.6; RSK-002.5.5 |
| 9.2 | Internal audit | Covered | CMP-001.5.6; CMP-002.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.9; CMP-005.5.17, 5.18; CMP-008.5.11; CMP-009.5.10; SEC-019.5.11, 5.12 |
| 9.3 | Management review | Covered | CMP-003.5.8, 5.9; CMP-006.5.7, 5.8, 5.9; GOV-001.5.3; GOV-003.5.5, 5.6; ISP-000.5.7, 5.8; RSK-001.5.6; RSK-005.5.5 |
| 10.1 | Continual improvement | Covered | CMP-002.5.7, 5.8; GOV-003.5.7; ISP-000.5.8; RES-002.5.10 |
| 10.2 | Nonconformity and corrective action | Covered | CMP-001.5.7; CMP-002.5.7, 5.8; CMP-007.5.7; CMP-009.5.11, 5.12; GOV-003.5.4; RES-001.5.8; RES-002.5.10; RES-004.5.12, 5.13; RES-005.5.10, 5.11; SEC-013.5.7 |

#### 5.5.2 Annex A controls

| Control | Title | Status | Primary document | Implementing requirements | Key Controls | Notes |
|---|---|---|---|---|---|---|
| A.5.1 | Policies for information security | Covered | GOV-002 | CMP-003.5.1, 5.2; GOV-002.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.9; GOV-006.5.1, 5.2, 5.3, 5.4; ISP-000.5.6 | KC-05, KC-06, KC-07 |  |
| A.5.2 | Information security roles and responsibilities | Covered | GOV-001 | CMP-001.5.1; CMP-005.5.1; CMP-008.5.2; GOV-001.5.1, 5.2, 5.4, 5.5; ISP-000.5.4; RES-002.5.4; RSK-006.5.6 | KC-02 |  |
| A.5.3 | Segregation of duties | Covered | GOV-001 | CMP-009.5.4; GOV-001.5.7, 5.8; GOV-004.5.12; SEC-006.5.10; SEC-010.5.10; SEC-013.5.11 | KC-04 |  |
| A.5.4 | Management responsibilities | Covered | CMP-003 | CMP-003.5.3, 5.4; GOV-001.5.1, 5.2 | KC-02, KC-22 |  |
| A.5.5 | Contact with authorities | Covered | RES-002 | CMP-001.5.8, 5.9; GOV-001.5.10; RES-001.5.5; RES-002.5.5, 5.11, 5.12; RES-003.5.6, 5.10; SEC-011.5.8 | KC-19 |  |
| A.5.6 | Contact with special interest groups | Covered | RSK-005 | GOV-001.5.10; RES-001.5.5; RES-002.5.5; RSK-005.5.1, 5.2, 5.4 | — |  |
| A.5.7 | Threat intelligence | Covered | RSK-005 | RSK-005.5.1, 5.2, 5.3, 5.5; SEC-006.5.12, 5.13; SEC-011.5.1; SEC-012.5.7 | — |  |
| A.5.8 | Information security in project management | Covered | CMP-005 | CMP-005.5.10; CMP-009.5.6; GOV-001.5.11; RSK-005.5.6; SEC-010.5.2 | — |  |
| A.5.9 | Inventory of information and other associated assets | Covered | SEC-001 | CMP-005.5.8; CMP-008.5.3; CMP-009.5.1, 5.2, 5.3; RES-005.5.4; RSK-006.5.2; SEC-001.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.9; SEC-002.5.1, 5.2, 5.3; SEC-008.5.1; SEC-009.5.2; SEC-011.5.1, 5.6; SEC-013.5.10; SEC-019.5.1, 5.2, 5.3, 5.5 | KC-26, KC-27 |  |
| A.5.10 | Acceptable use of information and other associated assets | Covered | GOV-004 | GOV-004.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.8, 5.9; RSK-006.5.4, 5.5; SEC-002.5.4; SEC-009.5.7 | — |  |
| A.5.11 | Return of assets | Covered | GOV-004 | GOV-004.5.15; PPL-001.5.7; SEC-001.5.7; SEC-008.5.10 | — |  |
| A.5.12 | Classification of information | Covered | SEC-002 | CMP-006.5.5; CMP-008.5.3; CMP-010.5.6, 5.7, 5.8; RSK-006.5.4, 5.5; SEC-001.5.1, 5.2, 5.3; SEC-002.5.1, 5.2, 5.3, 5.4, 5.6; SEC-019.5.1, 5.2, 5.5 | KC-27 |  |
| A.5.13 | Labelling of information | Covered | SEC-002 | SEC-002.5.4 | — | Single implementing subsection; labelling rules are in the SEC-002 handling matrix. |
| A.5.14 | Information transfer | Covered | SEC-014 | CMP-005.5.12; CMP-010.5.13; GOV-004.5.5, 5.6, 5.7, 5.9; RES-001.5.9; RSK-005.5.4; RSK-006.5.4, 5.5; SEC-002.5.4, 5.7; SEC-014.5.1, 5.2, 5.4, 5.5, 5.6, 5.7, 5.8 | — |  |
| A.5.15 | Access control | Covered | SEC-003 | CMP-005.5.14; CMP-006.5.5; CMP-008.5.6; CMP-009.5.4; GOV-004.5.1, 5.2, 5.3, 5.4; SEC-003.5.1, 5.4, 5.5, 5.6, 5.13; SEC-007.5.3; SEC-009.5.6; SEC-014.5.9 | KC-29, KC-36 |  |
| A.5.16 | Identity management | Covered | SEC-003 | CMP-009.5.4; CMP-010.5.4, 5.5; PPL-001.5.4; SEC-003.5.1, 5.2, 5.3, 5.9, 5.11; SEC-004.5.5; SEC-005.5.1, 5.2; SEC-009.5.6 | KC-28 |  |
| A.5.17 | Authentication information | Covered | SEC-004 | CMP-008.5.8; SEC-003.5.9; SEC-004.5.1, 5.2, 5.3, 5.6, 5.9, 5.10; SEC-005.5.3; SEC-010.5.7 | KC-33 |  |
| A.5.18 | Access rights | Covered | SEC-003 | CMP-008.5.6; CMP-009.5.4; PPL-001.5.5, 5.6; SEC-003.5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.8, 5.12; SEC-005.5.11, 5.12; SEC-016.5.2 | KC-28, KC-29, KC-30, KC-31, KC-34, KC-53 |  |
| A.5.19 | Information security in supplier relationships | Covered | RSK-003 | CMP-005.5.11; CMP-007.5.5; CMP-008.5.9; CMP-009.5.9; CMP-010.5.10, 5.11; PPL-002.5.7, 5.8; RES-001.5.6; RES-003.5.9; RES-004.5.8; RSK-003.5.1, 5.2, 5.3, 5.7; RSK-006.5.7; SEC-003.5.10; SEC-005.5.9, 5.10; SEC-006.5.14; SEC-009.5.1; SEC-017.5.7; SEC-019.5.10 | KC-14 |  |
| A.5.20 | Addressing information security within supplier agreements | Covered | CMP-010 | CMP-005.5.11; CMP-007.5.5; CMP-008.5.9; CMP-009.5.9; CMP-010.5.10, 5.11; RES-003.5.9; RSK-003.5.4; RSK-006.5.7; SEC-002.5.7; SEC-003.5.10; SEC-017.5.7; SEC-019.5.10 | KC-15 |  |
| A.5.21 | Managing information security in the ICT supply chain | Covered | RSK-003 | CMP-008.5.9; RES-004.5.8; RSK-003.5.3, 5.6; SEC-009.5.2; SEC-010.5.8, 5.9; SEC-019.5.10 | KC-14 |  |
| A.5.22 | Monitoring, review and change management of supplier services | Covered | RSK-003 | CMP-007.5.5; CMP-009.5.9; RES-004.5.8; RSK-003.5.5, 5.7; SEC-012.5.11; SEC-016.5.6; SEC-019.5.10 | KC-16 |  |
| A.5.23 | Information security for use of cloud services | Covered | GOV-004 | GOV-004.5.5, 5.6, 5.7; RSK-003.5.1, 5.2; SEC-001.5.6; SEC-006.5.14; SEC-009.5.1, 5.2, 5.3; SEC-014.5.6; SEC-017.5.6; SEC-018.5.8 | — |  |
| A.5.24 | Information security incident management planning and preparation | Covered | RES-002 | CMP-005.5.16; CMP-006.5.3, 5.4; CMP-008.5.6; RES-001.5.1, 5.6; RES-002.5.1, 5.2, 5.3, 5.4, 5.5, 5.11, 5.12, 5.13, 5.14, 5.15; RES-003.5.1, 5.10; RSK-006.5.8; SEC-008.5.9; SEC-015.5.5 | KC-60 |  |
| A.5.25 | Assessment and decision on information security events | Covered | RES-002 | CMP-008.5.6; RES-001.5.2; RES-002.5.1, 5.2, 5.3, 5.6; RES-003.5.2, 5.3, 5.4; SEC-012.5.8 | KC-47, KC-58, KC-61 |  |
| A.5.26 | Response to information security incidents | Covered | RES-002 | CMP-006.5.3, 5.4; CMP-008.5.6; RES-001.5.1, 5.3, 5.7, 5.9; RES-002.5.7, 5.8, 5.9, 5.11, 5.12, 5.13; RES-003.5.1, 5.6, 5.7; RES-005.5.2, 5.7 | — |  |
| A.5.27 | Learning from information security incidents | Covered | RES-002 | CMP-008.5.6; RES-001.5.8; RES-002.5.10, 5.14, 5.15; RES-003.5.8; RES-005.5.8, 5.9 | KC-59, KC-60 |  |
| A.5.28 | Collection of evidence | Covered | CMP-004 | CMP-004.5.5, 5.6, 5.7; CMP-006.5.3, 5.4; CMP-007.5.4; CMP-008.5.6; RES-001.5.4 | KC-24, KC-25 |  |
| A.5.29 | Information security during disruption | Covered | RES-004 | CMP-008.5.6; RES-002.5.9; RES-004.5.1, 5.3, 5.4, 5.5, 5.6, 5.7, 5.9, 5.10, 5.12, 5.13; RES-005.5.1, 5.2, 5.8, 5.9; RSK-004.5.1, 5.2, 5.5; SEC-005.5.7, 5.8 | KC-17 |  |
| A.5.30 | ICT readiness for business continuity | Covered | RSK-004 | RES-004.5.1, 5.2, 5.3, 5.5, 5.8, 5.11; RES-005.5.1, 5.3, 5.4, 5.10, 5.11; RSK-004.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7; SEC-018.5.1, 5.6 | KC-17, KC-18, KC-56, KC-62, KC-63 |  |
| A.5.31 | Legal, statutory, regulatory and contractual requirements | Covered | CMP-001 | CMP-001.5.1, 5.2, 5.3, 5.4, 5.8, 5.9; CMP-003.5.1, 5.2; CMP-004.5.1, 5.2, 5.4; CMP-005.5.3; CMP-006.5.1, 5.2, 5.6; CMP-008.5.1; CMP-009.5.1, 5.2, 5.3; CMP-010.5.1, 5.2, 5.3; RES-001.5.7; RES-003.5.5, 5.6; SEC-009.5.10; SEC-015.5.4 | KC-19 |  |
| A.5.32 | Intellectual property rights | Covered | GOV-004 | GOV-004.5.10; SEC-010.5.9 | — |  |
| A.5.33 | Protection of records | Covered | CMP-004 | CMP-001.5.10; CMP-002.5.10; CMP-004.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.8; CMP-008.5.10; CMP-009.5.8; CMP-010.5.14, 5.15; PPL-001.5.9; RES-003.5.8; SEC-014.5.6, 5.10; SEC-018.5.9 | KC-23, KC-24 |  |
| A.5.34 | Privacy and protection of PII | Covered | CMP-005 | CMP-001.5.2, 5.3; CMP-004.5.1, 5.2; CMP-005.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.8, 5.9, 5.11, 5.12, 5.13, 5.14, 5.15, 5.16; CMP-006.5.5; CMP-010.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.8, 5.9, 5.10, 5.11, 5.12; GOV-001.5.5, 5.6; PPL-001.5.9; RES-003.5.2, 5.3, 5.4, 5.6, 5.7; SEC-009.5.10 | KC-61 |  |
| A.5.35 | Independent review of information security | Covered | CMP-002 | CMP-001.5.6; CMP-002.5.1, 5.2, 5.4, 5.5, 5.6, 5.9; CMP-008.5.11; CMP-009.5.10; SEC-011.5.7; SEC-019.5.11, 5.12 | KC-20, KC-45 |  |
| A.5.36 | Compliance with policies, rules and standards for information security | Covered | CMP-003 | CMP-001.5.5, 5.6, 5.7; CMP-002.5.3, 5.4, 5.5, 5.6; CMP-003.5.1, 5.2, 5.5, 5.8, 5.9; CMP-009.5.10; SEC-019.5.11, 5.12 | KC-20 |  |
| A.5.37 | Documented operating procedures | Covered | SEC-013 | GOV-002.5.11; RES-005.5.1; SEC-013.5.1, 5.2, 5.10 | — |  |
| A.6.1 | Screening | Covered | PPL-001 | CMP-008.5.6; PPL-001.5.1, 5.2; SEC-003.5.2, 5.3 | KC-28, KC-64 |  |
| A.6.2 | Terms and conditions of employment | Covered | GOV-004 | GOV-002.5.9; GOV-004.5.11, 5.12; PPL-001.5.3, 5.4 | KC-07, KC-65 |  |
| A.6.3 | Information security awareness, education and training | Covered | PPL-002 | CMP-005.5.17, 5.18; CMP-008.5.6; PPL-002.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.8; SEC-014.5.2, 5.8 | KC-66, KC-67 |  |
| A.6.4 | Disciplinary process | Covered | CMP-007 | CMP-006.5.6; CMP-007.5.1, 5.2, 5.3, 5.4, 5.6; CMP-008.5.4; PPL-001.5.8 | KC-25 |  |
| A.6.5 | Responsibilities after termination or change of employment | Covered | PPL-001 | CMP-007.5.4; CMP-008.5.6; GOV-004.5.15; PPL-001.5.5, 5.6, 5.7; SEC-003.5.7, 5.8 | KC-25, KC-30 |  |
| A.6.6 | Confidentiality or non-disclosure agreements | Covered | GOV-004 | GOV-004.5.11; PPL-001.5.3 | KC-65 |  |
| A.6.7 | Remote working | Covered | SEC-015 | SEC-007.5.4; SEC-008.5.8; SEC-015.5.1, 5.2, 5.3, 5.4 | — |  |
| A.6.8 | Information security event reporting | Covered | CMP-006 | CMP-006.5.1, 5.2, 5.3, 5.4; GOV-004.5.14; RES-001.5.2; RES-002.5.6; SEC-008.5.9; SEC-011.5.8; SEC-012.5.8; SEC-015.5.8 | KC-47, KC-58 |  |
| A.7.1 | Physical security perimeters | Covered | SEC-016 | CMP-008.5.7; SEC-016.5.1, 5.6 | — |  |
| A.7.2 | Physical entry | Covered | SEC-016 | CMP-008.5.7; SEC-016.5.2, 5.3, 5.8; SEC-019.5.9 | KC-53 |  |
| A.7.3 | Securing offices, rooms and facilities | Covered | SEC-016 | CMP-008.5.7; SEC-016.5.1, 5.5 | — |  |
| A.7.4 | Physical security monitoring | Covered | CMP-008 | CMP-008.5.7; SEC-016.5.4 | — |  |
| A.7.5 | Protecting against physical and environmental threats | Covered | RES-004 | RES-004.5.9, 5.10; SEC-016.5.7 | KC-54 |  |
| A.7.6 | Working in secure areas | Covered | SEC-016 | SEC-016.5.1, 5.5 | — |  |
| A.7.7 | Clear desk and clear screen | Covered | SEC-015 | GOV-004.5.3; SEC-002.5.4; SEC-014.5.7; SEC-015.5.2, 5.6; SEC-016.5.9 | — |  |
| A.7.8 | Equipment siting and protection | Covered | SEC-016 | SEC-016.5.10; SEC-019.5.9 | — |  |
| A.7.9 | Security of assets off-premises | Covered | SEC-015 | CMP-008.5.7; SEC-015.5.2, 5.3, 5.4, 5.5, 5.7; SEC-019.5.9 | — |  |
| A.7.10 | Storage media | Covered | SEC-017 | CMP-004.5.8; CMP-008.5.7; SEC-002.5.4; SEC-008.5.7; SEC-015.5.7; SEC-016.5.11; SEC-017.5.1, 5.2, 5.3, 5.4, 5.5 | KC-55 |  |
| A.7.11 | Supporting utilities | Covered | RES-004 | RES-004.5.3, 5.9, 5.10; SEC-016.5.7 | KC-54 |  |
| A.7.12 | Cabling security | Covered | SEC-016 | SEC-016.5.5 | — | Single implementing subsection (SEC-016.5.5). |
| A.7.13 | Equipment maintenance | Covered | SEC-016 | SEC-016.5.7, 5.10 | KC-54 |  |
| A.7.14 | Secure disposal or re-use of equipment | Covered | SEC-017 | CMP-004.5.3; CMP-008.5.7; SEC-001.5.7; SEC-008.5.10; SEC-015.5.6; SEC-017.5.1, 5.2, 5.3, 5.4, 5.5, 5.7, 5.8, 5.9 | KC-23, KC-55 |  |
| A.8.1 | User endpoint devices | Covered | SEC-008 | CMP-008.5.7; GOV-004.5.1, 5.2, 5.3, 5.4; SEC-005.5.6; SEC-008.5.1, 5.2, 5.4, 5.5, 5.8, 5.9; SEC-015.5.3 | KC-39 |  |
| A.8.2 | Privileged access rights | Covered | SEC-005 | CMP-008.5.8; CMP-009.5.4; SEC-003.5.4, 5.5, 5.6; SEC-005.5.1, 5.2, 5.3, 5.4, 5.6, 5.7, 5.8, 5.9, 5.10, 5.11, 5.12; SEC-008.5.6; SEC-009.5.6; SEC-018.5.5 | KC-29, KC-33, KC-34 |  |
| A.8.3 | Information access restriction | Covered | SEC-003 | SEC-003.5.4, 5.5, 5.6; SEC-009.5.7 | KC-29 |  |
| A.8.4 | Access to source code | Covered | SEC-010 | SEC-004.5.10; SEC-010.5.4, 5.6 | KC-41 |  |
| A.8.5 | Secure authentication | Covered | SEC-004 | CMP-008.5.8; CMP-009.5.4; SEC-004.5.1, 5.2, 5.3, 5.4, 5.5, 5.7, 5.8, 5.11, 5.12; SEC-007.5.4; SEC-009.5.6; SEC-014.5.9 | KC-32 |  |
| A.8.6 | Capacity management | Covered | SEC-013 | CMP-009.5.7; SEC-007.5.7; SEC-013.5.12 | KC-52 |  |
| A.8.7 | Protection against malware | Covered | SEC-014 | CMP-008.5.6; RES-005.5.7; SEC-008.5.3; SEC-014.5.2, 5.3 | KC-38 |  |
| A.8.8 | Management of technical vulnerabilities | Covered | SEC-011 | RSK-005.5.3; SEC-008.5.5; SEC-009.5.5; SEC-010.5.5; SEC-011.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.8, 5.9 | KC-40, KC-42, KC-43, KC-44, KC-45 |  |
| A.8.9 | Configuration management | Covered | SEC-009 | CMP-009.5.5; SEC-007.5.2, 5.9; SEC-008.5.2; SEC-009.5.4, 5.5, 5.11; SEC-013.5.8, 5.9, 5.10 | KC-40, KC-50, KC-51 |  |
| A.8.10 | Information deletion | Covered | SEC-017 | CMP-004.5.3; CMP-005.5.10; SEC-017.5.1, 5.2, 5.6; SEC-018.5.9 | KC-23 |  |
| A.8.11 | Data masking | Covered | SEC-019 | CMP-005.5.7; SEC-002.5.4; SEC-019.5.6, 5.7 | — |  |
| A.8.12 | Data leakage prevention | Covered | SEC-002 | SEC-002.5.5; SEC-008.5.7; SEC-014.5.4; SEC-019.5.5 | — |  |
| A.8.13 | Information backup | Covered | SEC-018 | CMP-008.5.6; CMP-009.5.7; RES-002.5.9; RES-005.5.3, 5.7; SEC-018.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.8 | KC-56, KC-57 |  |
| A.8.14 | Redundancy of information processing facilities | Covered | RES-005 | RES-004.5.3; RES-005.5.3, 5.5, 5.6; RSK-004.5.3, 5.4, 5.5; SEC-018.5.2 | KC-17 |  |
| A.8.15 | Logging | Covered | SEC-012 | CMP-004.5.5, 5.6, 5.7; CMP-008.5.4, 5.8; CMP-009.5.7; GOV-004.5.13; SEC-003.5.13; SEC-005.5.5; SEC-009.5.8; SEC-012.5.1, 5.2, 5.3, 5.5, 5.6, 5.9, 5.10 | KC-24, KC-46, KC-48 |  |
| A.8.16 | Monitoring activities | Covered | SEC-012 | CMP-008.5.4; GOV-004.5.13; RES-002.5.6; RSK-005.5.3, 5.7; RSK-006.5.8; SEC-005.5.5; SEC-009.5.8; SEC-012.5.1, 5.2, 5.6, 5.7, 5.9, 5.10, 5.11; SEC-013.5.9; SEC-018.5.7 | KC-46, KC-48, KC-51, KC-57, KC-58 |  |
| A.8.17 | Clock synchronization | Covered | CMP-004 | CMP-004.5.5, 5.6, 5.7; SEC-012.5.4 | KC-24 |  |
| A.8.18 | Use of privileged utility programs | Covered | SEC-008 | SEC-008.5.6 | — | Single implementing subsection (SEC-008.5.6); privileged utilities on servers are controlled through SEC-005 PAM. |
| A.8.19 | Installation of software on operational systems | Covered | SEC-013 | GOV-004.5.3; SEC-001.5.8; SEC-008.5.2; SEC-009.5.11; SEC-010.5.9; SEC-011.5.5; SEC-013.5.5, 5.6 | KC-49 |  |
| A.8.20 | Networks security | Covered | SEC-007 | SEC-007.5.1, 5.2, 5.3, 5.5, 5.6, 5.7, 5.8, 5.9; SEC-009.5.9; SEC-010.5.12; SEC-014.5.1; SEC-019.5.3, 5.4 | KC-36, KC-37 |  |
| A.8.21 | Security of network services | Covered | SEC-007 | SEC-007.5.2, 5.9; SEC-014.5.1 | — |  |
| A.8.22 | Segregation of networks | Covered | SEC-009 | SEC-007.5.1; SEC-009.5.3, 5.9, 5.11; SEC-019.5.4 | — |  |
| A.8.23 | Web filtering | Covered | SEC-007 | SEC-007.5.6; SEC-014.5.3 | — |  |
| A.8.24 | Use of cryptography | Covered | SEC-006 | CMP-008.5.8; CMP-010.5.13; RSK-006.5.10; SEC-004.5.9; SEC-006.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.8, 5.9, 5.10, 5.11, 5.12, 5.13; SEC-008.5.4; SEC-009.5.7; SEC-010.5.7; SEC-014.5.5; SEC-018.5.4; SEC-019.5.6, 5.7 | KC-35, KC-39 |  |
| A.8.25 | Secure development life cycle | Covered | SEC-010 | CMP-005.5.10; CMP-009.5.6; RSK-005.5.6; RSK-006.5.7; SEC-010.5.1, 5.8 | — |  |
| A.8.26 | Application security requirements | Covered | SEC-010 | SEC-010.5.1, 5.12; SEC-019.5.8 | — |  |
| A.8.27 | Secure system architecture and engineering principles | Covered | RSK-005 | RSK-005.5.6; SEC-007.5.1; SEC-010.5.2 | — |  |
| A.8.28 | Secure coding | Covered | SEC-010 | SEC-010.5.3, 5.4; SEC-019.5.8 | KC-41 |  |
| A.8.29 | Security testing in development and acceptance | Covered | SEC-010 | CMP-009.5.6; RSK-006.5.8; SEC-010.5.4, 5.5; SEC-011.5.7; SEC-013.5.4 | KC-41, KC-42, KC-45 |  |
| A.8.30 | Outsourced development | Covered | RSK-003 | RSK-003.5.6; SEC-010.5.13 | — |  |
| A.8.31 | Separation of development, test and production environments | Covered | SEC-010 | CMP-009.5.5; SEC-009.5.3; SEC-010.5.6, 5.10; SEC-013.5.4 | — |  |
| A.8.32 | Change management | Covered | SEC-013 | CMP-009.5.5, 5.8; RES-005.5.5, 5.6; SEC-009.5.4; SEC-010.5.6, 5.14; SEC-011.5.5; SEC-013.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.11; SEC-019.5.8 | KC-49 |  |
| A.8.33 | Test information | Covered | CMP-005 | CMP-005.5.7; CMP-009.5.6; SEC-010.5.11 | — |  |
| A.8.34 | Protection of information systems during audit testing | Covered | SEC-011 | CMP-002.5.9; SEC-011.5.2, 5.7 | KC-43, KC-45 | Mapped by REF-001 (appendix A, correction C-11 to C-13). |

Result: 93 of 93 Annex A controls have at least one implementing requirement; 0 are not covered.
Gaps found in earlier versions are listed in section 5.11.

### 5.6 Reverse view (b): SOC 2 Trust Services Criteria to suite requirements

The default examination scope is Security (CC1.1–CC9.2), Availability (A1.1–A1.3) and
Confidentiality (C1.1–C1.2), per SUITE-REGISTER decision #2. Where the Organization adds Privacy
to scope, the P-series entries in section 5.3 (mainly CMP-005, CMP-010 and RES-003) apply.

| Criterion | Criterion (summary) | Status | Suite requirements | Key Controls | Notes |
|---|---|---|---|---|---|
| CC1.1 | The entity demonstrates a commitment to integrity and ethical values | Covered | CMP-006.5.1, 5.2, 5.6; CMP-007.5.1, 5.2, 5.3; CMP-008.5.1; GOV-002.5.9; GOV-004.5.1, 5.2, 5.3, 5.4, 5.11, 5.12; PPL-001.5.3 | KC-07, KC-65 |  |
| CC1.2 | The board of directors demonstrates independence from management and exercises oversight | Covered | CMP-002.5.1; CMP-006.5.7; GOV-001.5.1, 5.2, 5.3; GOV-003.5.5, 5.6; ISP-000.5.1, 5.7 | KC-01, KC-02, KC-03, KC-08 |  |
| CC1.3 | Management establishes structures, reporting lines, authorities and responsibilities | Covered | CMP-001.5.1; CMP-003.5.1, 5.2; CMP-005.5.1; CMP-008.5.2; GOV-001.5.1, 5.2, 5.4, 5.5, 5.6, 5.8; ISP-000.5.1, 5.4; RES-002.5.4; RSK-006.5.1, 5.6; SEC-001.5.4 | KC-02 |  |
| CC1.4 | The entity demonstrates a commitment to attract, develop and retain competent individuals | Covered | CMP-005.5.17, 5.18; CMP-006.5.8, 5.9; CMP-009.5.1, 5.2, 5.3; GOV-001.5.9; PPL-001.5.1, 5.2, 5.3; PPL-002.5.1, 5.2, 5.3, 5.4, 5.5, 5.7, 5.8, 5.9 | KC-64, KC-65, KC-66, KC-67 |  |
| CC1.5 | The entity holds individuals accountable for their internal control responsibilities | Covered | CMP-002.5.1; CMP-006.5.6; CMP-007.5.1, 5.2, 5.3, 5.4, 5.6, 5.7; CMP-008.5.4; GOV-001.5.4; PPL-001.5.8 | KC-25 |  |
| CC2.1 | The entity obtains or generates and uses relevant, quality information | Covered | CMP-001.5.10; CMP-003.5.8, 5.9; CMP-004.5.1, 5.2, 5.4; CMP-009.5.1, 5.2, 5.3, 5.8; SEC-007.5.8 | KC-37 |  |
| CC2.2 | The entity internally communicates information, including objectives and responsibilities for internal control | Covered | CMP-001.5.1; CMP-006.5.1, 5.2, 5.3, 5.4, 5.8, 5.9; CMP-008.5.1, 5.10; GOV-001.5.3; GOV-002.5.6, 5.9; GOV-003.5.5, 5.6; GOV-004.5.1, 5.2, 5.3, 5.4, 5.8, 5.9, 5.10; GOV-006.5.1, 5.2, 5.3, 5.4; ISP-000.5.3; PPL-002.5.1, 5.2, 5.3, 5.6; RES-001.5.2, 5.9; RES-002.5.11, 5.12; RES-003.5.1; RSK-001.5.7; RSK-005.5.5; RSK-006.5.1 | KC-03, KC-07, KC-08, KC-66, KC-67 |  |
| CC2.3 | The entity communicates with external parties regarding matters affecting internal control | Covered | CMP-001.5.2, 5.3, 5.6, 5.8, 5.9; CMP-002.5.9; CMP-006.5.1, 5.2, 5.7; GOV-001.5.10; GOV-004.5.14; RES-001.5.2, 5.5; RES-002.5.11, 5.12; RES-003.5.5, 5.6, 5.7, 5.10; RES-004.5.9, 5.10; RES-005.5.8, 5.9; RSK-001.5.7; RSK-005.5.4; RSK-006.5.9; SEC-011.5.8, 5.9 | KC-19 |  |
| CC3.1 | The entity specifies objectives with sufficient clarity to enable identification and assessment of risks | Covered | CMP-001.5.2, 5.3; CMP-008.5.3; CMP-009.5.1, 5.2, 5.3; ISP-000.5.2, 5.5; RSK-001.5.1, 5.3 | KC-09 |  |
| CC3.2 | The entity identifies and analyzes risks to the achievement of its objectives | Covered | CMP-003.5.3, 5.4, 5.6, 5.7; CMP-005.5.9; CMP-008.5.3, 5.5; ISP-000.5.5; RES-004.5.2; RSK-001.5.1, 5.2, 5.4, 5.5; RSK-002.5.1, 5.2, 5.3, 5.4, 5.5, 5.7, 5.8, 5.9; RSK-005.5.1, 5.2, 5.5, 5.6; RSK-006.5.3; SEC-001.5.1, 5.2, 5.3, 5.9; SEC-002.5.1, 5.2, 5.3; SEC-006.5.12, 5.13; SEC-010.5.2; SEC-011.5.3; SEC-015.5.4; SEC-019.5.1, 5.2, 5.10 | KC-10, KC-22, KC-26, KC-27 |  |
| CC3.3 | The entity considers the potential for fraud in assessing risks | Covered | RSK-001.5.2; RSK-002.5.10 | KC-13 |  |
| CC3.4 | The entity identifies and assesses changes that could significantly impact internal control | Covered | CMP-001.5.4; GOV-001.5.11; RSK-002.5.6; RSK-006.5.10; SEC-009.5.2; SEC-013.5.3 | KC-12 |  |
| CC4.1 | The entity selects, develops and performs ongoing and/or separate evaluations | Covered | CMP-001.5.5, 5.6, 5.7; CMP-002.5.2, 5.3, 5.4, 5.5, 5.6, 5.9, 5.10; CMP-003.5.5, 5.8, 5.9; CMP-004.5.5, 5.6, 5.7; CMP-005.5.17, 5.18; CMP-006.5.8, 5.9; CMP-007.5.7; CMP-008.5.11; CMP-009.5.10; GOV-003.5.1, 5.2, 5.3, 5.7; ISP-000.5.8; RSK-001.5.6; RSK-002.5.5; RSK-003.5.5; RSK-005.5.7; RSK-006.5.8; SEC-001.5.9; SEC-003.5.12; SEC-011.5.7; SEC-012.5.9; SEC-019.5.11, 5.12 | KC-11, KC-16, KC-20, KC-24, KC-26, KC-31, KC-45, KC-48 |  |
| CC4.2 | The entity evaluates and communicates internal control deficiencies in a timely manner | Covered | CMP-001.5.6, 5.7; CMP-002.5.7, 5.8; CMP-003.5.8, 5.9; CMP-008.5.11; CMP-009.5.11, 5.12; GOV-003.5.4; ISP-000.5.7; RES-001.5.8; RES-002.5.10; RSK-001.5.6 | KC-01, KC-11, KC-21, KC-59 |  |
| CC5.1 | The entity selects and develops control activities that mitigate risks | Covered | CMP-002.5.7, 5.8; CMP-003.5.5; CMP-008.5.5; CMP-009.5.11, 5.12; GOV-001.5.7; RSK-001.5.4; RSK-002.5.7 | KC-04, KC-21 |  |
| CC5.2 | The entity selects and develops general control activities over technology | Covered | CMP-003.5.3, 5.4, 5.6, 5.7; SEC-003.5.4, 5.5, 5.6 | KC-22, KC-29 |  |
| CC5.3 | The entity deploys control activities through policies and procedures | Covered | CMP-003.5.1, 5.2; GOV-002.5.1, 5.2, 5.3, 5.4, 5.5, 5.7, 5.8, 5.10, 5.11; GOV-006.5.1, 5.2; ISP-000.5.6 | KC-05, KC-06 |  |
| CC6.1 | Logical access security software, infrastructure and architectures over protected information assets | Covered | CMP-006.5.5; CMP-008.5.8; CMP-009.5.4; RSK-006.5.2, 5.4, 5.5; SEC-001.5.1, 5.2, 5.3, 5.4, 5.5; SEC-002.5.4; SEC-003.5.1, 5.4, 5.5, 5.6, 5.9, 5.11, 5.13; SEC-004.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.8, 5.9, 5.10, 5.11, 5.12; SEC-005.5.1, 5.2, 5.3, 5.6, 5.7, 5.8, 5.9, 5.10; SEC-006.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.8, 5.9, 5.10, 5.11, 5.12, 5.13; SEC-007.5.1, 5.4, 5.9; SEC-008.5.1, 5.4, 5.6, 5.8; SEC-009.5.3, 5.6, 5.7, 5.11; SEC-010.5.6, 5.7, 5.10; SEC-014.5.6, 5.8, 5.9; SEC-015.5.1; SEC-018.5.4, 5.5; SEC-019.5.1, 5.2, 5.5, 5.6, 5.7 | KC-29, KC-32, KC-33, KC-35, KC-39 |  |
| CC6.2 | Registration and authorization of users before credentials are issued; removal when no longer authorized | Covered | CMP-007.5.4; CMP-008.5.6; CMP-009.5.4; GOV-004.5.15; PPL-001.5.4, 5.5, 5.6, 5.7; SEC-003.5.1, 5.2, 5.3, 5.7, 5.8, 5.9, 5.10, 5.12; SEC-005.5.11, 5.12; SEC-009.5.6 | KC-25, KC-28, KC-30, KC-31, KC-34 |  |
| CC6.3 | Authorization, modification and removal of access based on roles, least privilege and segregation of duties | Covered | CMP-005.5.14; CMP-008.5.6; CMP-009.5.4; GOV-001.5.7; PPL-001.5.5, 5.6; SEC-003.5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.8, 5.12; SEC-005.5.1, 5.2, 5.4, 5.11, 5.12; SEC-008.5.6; SEC-009.5.6; SEC-018.5.5 | KC-04, KC-28, KC-29, KC-30, KC-31, KC-34 |  |
| CC6.4 | Restriction of physical access to facilities and protected information assets | Covered | CMP-008.5.7; SEC-015.5.2, 5.7; SEC-016.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.8, 5.9, 5.10, 5.11; SEC-019.5.9 | KC-53 |  |
| CC6.5 | Discontinuation of logical and physical protections only after the ability to read or recover data is removed | Covered | CMP-008.5.7; GOV-004.5.15; PPL-001.5.7; SEC-001.5.7; SEC-008.5.10; SEC-015.5.6; SEC-017.5.1, 5.2, 5.3, 5.4, 5.5 | KC-55 |  |
| CC6.6 | Logical access security measures against threats from sources outside system boundaries | Covered | SEC-004.5.4; SEC-007.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7; SEC-009.5.3, 5.9; SEC-010.5.12; SEC-019.5.3, 5.4 | KC-32, KC-36 |  |
| CC6.7 | Restriction of transmission, movement and removal of information to authorized users and processes | Covered | CMP-008.5.8; GOV-004.5.5, 5.6, 5.7; SEC-002.5.4, 5.5; SEC-006.5.1, 5.2, 5.11; SEC-008.5.4, 5.7, 5.8, 5.9; SEC-014.5.1, 5.4, 5.5, 5.7; SEC-015.5.3, 5.4, 5.7; SEC-019.5.6, 5.7 | KC-35, KC-39 |  |
| CC6.8 | Prevention or detection of unauthorized or malicious software | Covered | GOV-004.5.3; SEC-001.5.6, 5.8; SEC-005.5.6; SEC-007.5.6; SEC-008.5.2, 5.3; SEC-009.5.11; SEC-014.5.2, 5.3 | KC-38 |  |
| CC7.1 | Detection and monitoring procedures for configuration changes and newly discovered vulnerabilities | Covered | RSK-005.5.3; SEC-001.5.5; SEC-007.5.3, 5.9; SEC-008.5.2, 5.5; SEC-009.5.4, 5.5, 5.11; SEC-010.5.5; SEC-011.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7; SEC-013.5.8, 5.9; SEC-019.5.8 | KC-36, KC-40, KC-42, KC-43, KC-44, KC-45, KC-50, KC-51 |  |
| CC7.2 | Monitoring of system components for anomalies indicative of malicious acts, natural disasters and errors | Covered | CMP-008.5.4, 5.8; CMP-009.5.7; GOV-004.5.13; RES-002.5.6; RSK-005.5.3, 5.7; RSK-006.5.8; SEC-003.5.13; SEC-005.5.5; SEC-008.5.3; SEC-009.5.8; SEC-012.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.9, 5.10; SEC-014.5.2; SEC-016.5.4; SEC-018.5.7 | KC-38, KC-46, KC-48, KC-57, KC-58 |  |
| CC7.3 | Evaluation of security events to determine whether they are security incidents | Covered | CMP-004.5.5, 5.6, 5.7; CMP-005.5.16; CMP-006.5.3, 5.4; RES-001.5.1, 5.2; RES-002.5.1, 5.2, 5.3, 5.5, 5.6; RES-003.5.2, 5.3, 5.4; SEC-008.5.9; SEC-011.5.8; SEC-012.5.7, 5.8; SEC-015.5.5, 5.8 | KC-24, KC-47, KC-58, KC-61 |  |
| CC7.4 | Response to identified security incidents through a defined incident response program | Covered | CMP-006.5.3, 5.4; CMP-008.5.6; RES-001.5.1, 5.3, 5.4, 5.6, 5.7; RES-002.5.1, 5.2, 5.3, 5.4, 5.5, 5.7, 5.8, 5.11, 5.12, 5.13, 5.14, 5.15; RES-003.5.1, 5.8; RES-004.5.4; RES-005.5.2, 5.7; SEC-011.5.4; SEC-012.5.8 | KC-44, KC-47, KC-60 |  |
| CC7.5 | Identification, development and implementation of activities to recover from security incidents | Covered | RES-001.5.8; RES-002.5.9, 5.10, 5.14, 5.15; RES-004.5.4, 5.5, 5.11; RES-005.5.1, 5.2, 5.3, 5.7, 5.8, 5.9 | KC-59, KC-60, KC-62 |  |
| CC8.1 | Authorization, design, development, testing, approval and implementation of changes | Covered | CMP-005.5.10; CMP-009.5.5, 5.6, 5.8; RES-005.5.5, 5.6; RSK-003.5.6; RSK-005.5.6; SEC-001.5.7; SEC-004.5.10; SEC-009.5.4; SEC-010.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.10, 5.11, 5.14; SEC-011.5.5; SEC-013.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.10, 5.11; SEC-019.5.8 | KC-41, KC-42, KC-49 |  |
| CC9.1 | Identification, selection and development of risk mitigation activities for business disruptions | Covered | RES-004.5.1, 5.2, 5.3, 5.6, 5.7; RSK-004.5.1, 5.2, 5.5 | KC-17 |  |
| CC9.2 | Assessment and management of risks associated with vendors and business partners | Covered | CMP-001.5.8, 5.9; CMP-005.5.11; CMP-007.5.5; CMP-008.5.9; CMP-009.5.9; CMP-010.5.10, 5.11; PPL-002.5.7, 5.8; RES-001.5.6; RES-003.5.9; RES-004.5.8; RSK-003.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7; RSK-004.5.5; RSK-006.5.7; SEC-001.5.6; SEC-002.5.4, 5.7; SEC-003.5.10; SEC-005.5.9, 5.10; SEC-006.5.14; SEC-007.5.9; SEC-009.5.1, 5.2; SEC-010.5.8, 5.9, 5.13; SEC-012.5.11; SEC-014.5.6; SEC-016.5.6; SEC-017.5.6, 5.7; SEC-018.5.8; SEC-019.5.10 | KC-14, KC-15, KC-16, KC-17, KC-19 |  |
| A1.1 | Maintenance, monitoring and evaluation of current processing capacity and use | Covered | SEC-007.5.7; SEC-013.5.12 | KC-52 |  |
| A1.2 | Environmental protections, software, data backup processes and recovery infrastructure | Covered | CMP-008.5.6; CMP-009.5.7; RES-004.5.1, 5.3, 5.5, 5.9, 5.10; RES-005.5.1, 5.3, 5.4, 5.5, 5.6; RSK-004.5.1, 5.2, 5.3, 5.4, 5.6, 5.7; SEC-005.5.7, 5.8; SEC-016.5.7, 5.10; SEC-018.5.1, 5.2, 5.3, 5.4, 5.7, 5.8 | KC-18, KC-54, KC-57 |  |
| A1.3 | Testing of recovery plan procedures | Covered | CMP-008.5.6; CMP-009.5.7; RES-004.5.11, 5.12, 5.13; RES-005.5.10, 5.11; RSK-004.5.3, 5.4; SEC-018.5.6 | KC-56, KC-62, KC-63 |  |
| C1.1 | Identification and maintenance of confidential information | Covered | CMP-004.5.1, 5.2, 5.8; CMP-005.5.7; CMP-006.5.5; CMP-010.5.13; GOV-004.5.11; PPL-001.5.9; RES-001.5.9; RSK-003.5.4; RSK-006.5.4, 5.5; SEC-002.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7; SEC-009.5.7, 5.10; SEC-010.5.11; SEC-014.5.5; SEC-019.5.5, 5.6, 5.7 | KC-15, KC-27 |  |
| C1.2 | Disposal of confidential information | Covered | CMP-004.5.1, 5.2, 5.3; RSK-003.5.7; SEC-014.5.10; SEC-017.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.8, 5.9; SEC-018.5.9 | KC-23, KC-55 |  |

### 5.7 Reverse view (c): NIST CSF 2.0 functions and categories to suite documents

| Function | Category | Suite documents | Subcategories cited | Subcategories not cited |
|---|---|---|---|---|
| GOVERN | GV.OC Organizational Context | CMP-001, CMP-004, CMP-005, CMP-006, CMP-008, CMP-009, CMP-010, GOV-001, GOV-004, ISP-000, RES-003, RES-004, RES-005, RSK-001, RSK-004, RSK-006, SEC-009, SEC-014, SEC-015, SEC-019 | GV.OC-01, GV.OC-02, GV.OC-03, GV.OC-04, GV.OC-05 | — |
| GOVERN | GV.RM Risk Management Strategy | CMP-002, CMP-003, CMP-005, CMP-008, GOV-001, GOV-003, ISP-000, RSK-001, RSK-002 | GV.RM-01, GV.RM-02, GV.RM-03, GV.RM-04, GV.RM-06 | GV.RM-05, GV.RM-07 |
| GOVERN | GV.RR Roles, Responsibilities, and Authorities | CMP-001, CMP-002, CMP-005, CMP-006, CMP-007, CMP-008, GOV-001, GOV-003, GOV-004, ISP-000, PPL-001, RES-002, RES-004, RES-005, RSK-001, RSK-006, SEC-001 | GV.RR-01, GV.RR-02, GV.RR-03, GV.RR-04 | — |
| GOVERN | GV.PO Policy | CMP-001, CMP-002, CMP-003, CMP-005, CMP-007, CMP-008, GOV-002, GOV-004, GOV-006, ISP-000, RSK-006 | GV.PO-01, GV.PO-02 | — |
| GOVERN | GV.OV Oversight | CMP-001, CMP-002, CMP-003, CMP-006, CMP-007, CMP-008, CMP-009, CMP-010, GOV-001, GOV-003, ISP-000, RSK-001, RSK-005, SEC-013, SEC-019 | GV.OV-01, GV.OV-02, GV.OV-03 | — |
| GOVERN | GV.SC Cybersecurity Supply Chain Risk Management | CMP-001, CMP-002, CMP-005, CMP-007, CMP-008, CMP-009, CMP-010, PPL-002, RES-001, RES-003, RES-004, RSK-003, RSK-004, RSK-006, SEC-001, SEC-002, SEC-003, SEC-005, SEC-006, SEC-009, SEC-010, SEC-014, SEC-016, SEC-017, SEC-018, SEC-019 | GV.SC-01, GV.SC-04, GV.SC-05, GV.SC-06, GV.SC-07, GV.SC-08, GV.SC-09, GV.SC-10 | GV.SC-02, GV.SC-03 |
| IDENTIFY | ID.AM Asset Management | CMP-005, CMP-009, CMP-010, GOV-004, RES-005, RSK-004, RSK-006, SEC-001, SEC-002, SEC-006, SEC-007, SEC-008, SEC-009, SEC-010, SEC-011, SEC-013, SEC-014, SEC-017, SEC-018, SEC-019 | ID.AM-01, ID.AM-02, ID.AM-03, ID.AM-04, ID.AM-05, ID.AM-07, ID.AM-08 | — |
| IDENTIFY | ID.RA Risk Assessment | CMP-003, CMP-005, CMP-008, GOV-001, RES-004, RSK-001, RSK-002, RSK-003, RSK-004, RSK-005, RSK-006, SEC-006, SEC-008, SEC-009, SEC-010, SEC-011, SEC-013, SEC-015, SEC-019 | ID.RA-01, ID.RA-02, ID.RA-03, ID.RA-04, ID.RA-05, ID.RA-06, ID.RA-07, ID.RA-08, ID.RA-09, ID.RA-10 | — |
| IDENTIFY | ID.IM Improvement | CMP-001, CMP-002, CMP-005, CMP-007, CMP-008, CMP-009, GOV-003, ISP-000, PPL-002, RES-001, RES-002, RES-003, RES-004, RES-005, RSK-001, RSK-002, RSK-004, RSK-005, SEC-003, SEC-006, SEC-011, SEC-013 | ID.IM-01, ID.IM-02, ID.IM-03, ID.IM-04 | — |
| PROTECT | PR.AA Identity Management, Authentication, and Access Control | CMP-005, CMP-006, CMP-008, CMP-009, CMP-010, GOV-004, PPL-001, RSK-006, SEC-003, SEC-004, SEC-005, SEC-006, SEC-007, SEC-008, SEC-009, SEC-010, SEC-014, SEC-015, SEC-016, SEC-018, SEC-019 | PR.AA-01, PR.AA-02, PR.AA-03, PR.AA-04, PR.AA-05, PR.AA-06 | — |
| PROTECT | PR.AT Awareness and Training | CMP-005, CMP-006, CMP-008, GOV-002, GOV-004, PPL-002, RES-002, RES-003, RES-004, RSK-001, RSK-006 | PR.AT-01, PR.AT-02 | — |
| PROTECT | PR.DS Data Security | CMP-004, CMP-005, CMP-006, CMP-008, CMP-009, CMP-010, PPL-001, RES-005, RSK-006, SEC-002, SEC-004, SEC-006, SEC-008, SEC-009, SEC-010, SEC-012, SEC-014, SEC-015, SEC-016, SEC-017, SEC-018, SEC-019 | PR.DS-01, PR.DS-02, PR.DS-10, PR.DS-11 | — |
| PROTECT | PR.PS Platform Security | CMP-004, CMP-005, CMP-008, CMP-009, GOV-004, RSK-005, SEC-001, SEC-004, SEC-005, SEC-007, SEC-008, SEC-009, SEC-010, SEC-011, SEC-012, SEC-013, SEC-014, SEC-016, SEC-017, SEC-019 | PR.PS-01, PR.PS-02, PR.PS-03, PR.PS-04, PR.PS-05, PR.PS-06 | — |
| PROTECT | PR.IR Technology Infrastructure Resilience | RES-004, RES-005, SEC-007, SEC-009, SEC-010, SEC-013, SEC-016, SEC-019 | PR.IR-01, PR.IR-02, PR.IR-03, PR.IR-04 | — |
| DETECT | DE.CM Continuous Monitoring | CMP-008, CMP-009, GOV-004, RSK-005, RSK-006, SEC-001, SEC-002, SEC-003, SEC-005, SEC-007, SEC-008, SEC-009, SEC-011, SEC-012, SEC-013, SEC-014, SEC-016, SEC-018, SEC-019 | DE.CM-01, DE.CM-02, DE.CM-03, DE.CM-06, DE.CM-09 | — |
| DETECT | DE.AE Adverse Event Analysis | CMP-008, RES-001, RES-002, RSK-005, SEC-012, SEC-014 | DE.AE-02, DE.AE-03, DE.AE-06, DE.AE-07, DE.AE-08 | DE.AE-04 |
| RESPOND | RS.MA Incident Management | CMP-006, CMP-008, GOV-004, RES-001, RES-002, RES-003, RES-004, RES-005, RSK-006, SEC-008, SEC-012, SEC-015 | RS.MA-01, RS.MA-02, RS.MA-03, RS.MA-04, RS.MA-05 | — |
| RESPOND | RS.AN Incident Analysis | CMP-004, CMP-006, RES-001, RES-002, RES-003 | RS.AN-03, RS.AN-06, RS.AN-07, RS.AN-08 | — |
| RESPOND | RS.CO Incident Response Reporting and Communication | CMP-005, RES-001, RES-002, RES-003, RSK-005 | RS.CO-02, RS.CO-03 | — |
| RESPOND | RS.MI Incident Mitigation | RES-001, RES-002, RES-005 | RS.MI-01, RS.MI-02 | — |
| RECOVER | RC.RP Incident Recovery Plan Execution | CMP-008, RES-002, RES-004, RES-005, RSK-004, SEC-005, SEC-018 | RC.RP-01, RC.RP-02, RC.RP-03, RC.RP-04, RC.RP-05, RC.RP-06 | — |
| RECOVER | RC.CO Incident Recovery Communication | RES-002, RES-003, RES-004, RES-005 | RC.CO-03, RC.CO-04 | — |

Subcategories not cited by any document: GV.RM-05, GV.RM-07, GV.SC-02, GV.SC-03, DE.AE-04. These are covered in substance where noted in
section 5.11; otherwise they are candidates for mapping at the next document revision.

### 5.8 Reverse view (d): `[PCI]` PCI DSS v4.0.1 principal requirements to suite documents

SEC-019 is the CDE home document. Its section 5.12 cross-reference maps every PCI DSS
requirement to the suite document that implements it, and is authoritative for the PCI DSS
assessment. The table below is derived from the regulation column of section 5.3. Appendix A1
(multi-tenant service providers), A2 (SSL/early TLS for POS POI terminals) and A3 (Designated
Entities Supplemental Validation) apply only where the Organization's entity type requires them,
as recorded by the GC in the Obligations Register (CMP-001).

| Req. | PCI DSS principal requirement | Suite documents | Suite requirements citing it |
|---|---|---|---|
| 1 | Install and maintain network security controls | SEC-007, SEC-009, SEC-013, SEC-019 | SEC-007.5.1, 5.2, 5.3, 5.6, 5.8, 5.9; SEC-009.5.3, 5.9; SEC-013.5.10; SEC-019.5.3, 5.4 |
| 2 | Apply secure configurations to all system components | SEC-003, SEC-007, SEC-008, SEC-009, SEC-013 | SEC-003.5.11; SEC-007.5.5, 5.9; SEC-008.5.2; SEC-009.5.4, 5.11; SEC-013.5.8 |
| 3 | Protect stored account data | CMP-003, CMP-004, RSK-006, SEC-002, SEC-006, SEC-012, SEC-014, SEC-017, SEC-018, SEC-019 | CMP-003.5.1, 5.2; CMP-004.5.1, 5.2, 5.3; RSK-006.5.4, 5.5; SEC-002.5.4; SEC-006.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.8, 5.9, 5.10; SEC-012.5.3; SEC-014.5.8; SEC-017.5.8; SEC-018.5.4; SEC-019.5.5, 5.6, 5.7 |
| 4 | Protect cardholder data with strong cryptography during transmission over open, public networks | GOV-004, SEC-002, SEC-006, SEC-014, SEC-019 | GOV-004.5.1, 5.2, 5.3, 5.4; SEC-002.5.4; SEC-006.5.1, 5.2, 5.11; SEC-014.5.5; SEC-019.5.6, 5.7 |
| 5 | Protect all systems and networks from malicious software | SEC-008, SEC-014 | SEC-008.5.3, 5.7; SEC-014.5.2, 5.3 |
| 6 | Develop and maintain secure systems and software | GOV-001, PPL-002, RSK-005, SEC-001, SEC-002, SEC-008, SEC-009, SEC-010, SEC-011, SEC-013, SEC-019 | GOV-001.5.7; PPL-002.5.4; RSK-005.5.3, 5.6; SEC-001.5.1, 5.2, 5.3; SEC-002.5.4; SEC-008.5.5; SEC-009.5.4, 5.11; SEC-010.5.1, 5.3, 5.4, 5.5, 5.6, 5.8, 5.10, 5.11, 5.12, 5.14; SEC-011.5.1, 5.3, 5.4, 5.5; SEC-013.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7; SEC-019.5.8 |
| 7 | Restrict access to system components and cardholder data by business need to know | GOV-001, SEC-003, SEC-005, SEC-008, SEC-009 | GOV-001.5.7; SEC-003.5.2, 5.3, 5.4, 5.5, 5.6, 5.9, 5.12; SEC-005.5.1, 5.2, 5.4, 5.11, 5.12; SEC-008.5.6; SEC-009.5.6 |
| 8 | Identify users and authenticate access to system components | PPL-001, SEC-003, SEC-004, SEC-005, SEC-007, SEC-009, SEC-010, SEC-015 | PPL-001.5.7; SEC-003.5.1, 5.2, 5.3, 5.7, 5.8, 5.9, 5.10, 5.11; SEC-004.5.1, 5.2, 5.3, 5.4, 5.7, 5.8, 5.9, 5.10, 5.11, 5.12; SEC-005.5.1, 5.2, 5.3, 5.9, 5.10; SEC-007.5.4; SEC-009.5.6; SEC-010.5.7; SEC-015.5.1 |
| 9 | Restrict physical access to cardholder data | CMP-004, SEC-002, SEC-015, SEC-016, SEC-017, SEC-018, SEC-019 | CMP-004.5.3; SEC-002.5.4; SEC-015.5.7; SEC-016.5.1, 5.2, 5.3, 5.4, 5.5, 5.10, 5.11; SEC-017.5.3, 5.4, 5.5, 5.8; SEC-018.5.3; SEC-019.5.9 |
| 10 | Log and monitor all access to system components and cardholder data | CMP-004, SEC-003, SEC-005, SEC-009, SEC-012 | CMP-004.5.1, 5.2, 5.5, 5.6, 5.7; SEC-003.5.13; SEC-005.5.5; SEC-009.5.8; SEC-012.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.8, 5.9, 5.10 |
| 11 | Test security of systems and networks regularly | SEC-007, SEC-009, SEC-010, SEC-011, SEC-013, SEC-019 | SEC-007.5.5; SEC-009.5.5; SEC-010.5.5; SEC-011.5.2, 5.7; SEC-013.5.9; SEC-019.5.4, 5.8 |
| 12 | Support information security with organizational policies and programs | CMP-001, CMP-002, CMP-003, CMP-007, GOV-001, GOV-002, GOV-004, ISP-000, PPL-001, PPL-002, RES-001, RES-002, RES-003, RES-004, RES-005, RSK-001, RSK-002, RSK-003, SEC-001, SEC-002, SEC-006, SEC-007, SEC-008, SEC-009, SEC-011, SEC-012, SEC-015, SEC-019 | CMP-001.5.1, 5.5, 5.6, 5.8, 5.9; CMP-002.5.1, 5.3, 5.4, 5.5, 5.6, 5.9; CMP-003.5.1, 5.2, 5.3, 5.4; CMP-007.5.1, 5.2, 5.3, 5.5; GOV-001.5.1, 5.2, 5.4; GOV-002.5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.9; GOV-004.5.1, 5.2, 5.3, 5.4; ISP-000.5.1, 5.4, 5.6, 5.8; PPL-001.5.1, 5.2; PPL-002.5.1, 5.2, 5.3, 5.5; RES-001.5.1, 5.2, 5.6, 5.8; RES-002.5.1, 5.2, 5.3, 5.4, 5.5, 5.10, 5.13, 5.14, 5.15; RES-003.5.6, 5.10; RES-004.5.3, 5.5, 5.11; RES-005.5.3, 5.5, 5.6, 5.10, 5.11; RSK-001.5.1, 5.5; RSK-002.5.6, 5.8; RSK-003.5.1, 5.2, 5.3, 5.4, 5.5; SEC-001.5.1, 5.2, 5.3, 5.5, 5.9; SEC-002.5.5; SEC-006.5.1, 5.2, 5.12, 5.13; SEC-007.5.4; SEC-008.5.1; SEC-009.5.1, 5.3; SEC-011.5.6; SEC-012.5.8; SEC-015.5.1; SEC-019.5.1, 5.2, 5.5, 5.10 |

### 5.9 Reverse view (e): `[HIPAA]` Security Rule to CMP-008

The HIPAA Security Rule mapping is maintained by reference only. CMP-008 is the home document.
Its implementation matrices (sections 5.6 to 5.10) map each standard and implementation
specification, required or addressable, to the implementing suite document and record each
addressable decision. REF-001 does not reproduce them, so that the documentation required by
45 CFR §164.316 has one home.

| Security Rule part | CMP-008 location |
|---|---|
| §164.306 General requirements; §164.306(d)(3) addressable specifications | CMP-008.5.1, CMP-008.5.5 |
| §164.308(a)(1) Security management process | CMP-008.5.3 (risk analysis and risk management), CMP-008.5.4 (sanctions and information system activity review) |
| §164.308(a)(2) Assigned security responsibility | CMP-008.5.2 |
| §164.308(a)(3)–(a)(7) Workforce security to contingency plan | CMP-008.5.6 (administrative safeguards matrix) |
| §164.308(a)(8) Evaluation | CMP-008.5.11 |
| §164.308(b), §164.314 Business associate contracts and organizational requirements | CMP-008.5.9 |
| §164.310 Physical safeguards | CMP-008.5.7 |
| §164.312 Technical safeguards | CMP-008.5.8 |
| §164.316 Policies, procedures and documentation | CMP-008.5.10 |
| §§164.400–164.414 Breach notification | RES-003 (by reference from CMP-008.5.9) |

### 5.10 Reverse view (f): `[SOX]` IT general control domains to suite documents

CMP-009 is the home of the ITGC Key Controls (ITGC-APD, -PC, -PD and -CO) over Financially
Significant Systems. The documents listed hold the underlying requirements those Key Controls rely on.

| ITGC domain | CMP-009 location | Underlying suite requirements |
|---|---|---|
| Scoping of Financially Significant Systems | CMP-009.5.1, 5.2 | SEC-001.5.1–5.4 (Asset Inventory, ownership); RSK-004.5.3 (Recovery Tiers) |
| Access to programs and data (APD) | CMP-009.5.4 | SEC-003.5.2–5.12 (provisioning, revocation, Access Reviews); SEC-004 (authentication); SEC-005.5.3, 5.4, 5.7, 5.11 (privileged access); GOV-001.5.7 (Segregation of Duties); SEC-012.5.9 (privileged activity review); TPL-008 |
| Program change (PC) | CMP-009.5.5 | SEC-013.5.2–5.7, 5.11 (change classes, approval, `[SOX]` program change); SEC-010.5.4, 5.6, 5.10, 5.14 (code review, pipeline integrity, environment segregation) |
| Program development (PD) | CMP-009.5.6 | SEC-010.5.1–5.5, 5.11 (SDLC, testing, test data); SEC-013.5.4 (testing) |
| Computer operations (CO) | CMP-009.5.7 | SEC-018.5.2, 5.6, 5.7 (Backup, restore testing, job monitoring); SEC-012.5.8 (alert triage); RES-002 (incident handling); RES-005 (recovery) |
| Information produced by the entity (IPE) and reports | CMP-009.5.8 | CMP-004.5.5–5.6 (Evidence quality and integrity) |
| Service organizations and SOC 1 reliance | CMP-009.5.9 | RSK-003.5.3–5.5 (due diligence, contracts, assurance report review) |
| Testing, §302 support, deficiency evaluation and remediation | CMP-009.5.10–5.12 | CMP-002.5.5–5.8 (testing, sampling, deficiency classification, remediation); CMP-006.5.7 (Audit Committee complaint procedures) |
| Year-end retention | CMP-009 section 7 | CMP-004 (`[SOX]` year-end Backup retention) |

### 5.11 Coverage gaps and thin coverage

The reverse views found the following gaps. Each open gap SHALL be carried in REF-003 section 5.2.2 until
closed under REF-001.5.1.6. Closed gaps stay listed for traceability.

| Gap ID | Framework reference | Finding | Recommended home and owner |
|---|---|---|---|
| G-01 | ISO A.8.6; SOC 2 A1.1 | **Closed in the suite.** Capacity management was missing; SEC-013 section 5.12 (SEC-013.5.12.1 – 5.12.4, values in SEC-013.7.16 – 7.17) now covers it, and KC-52 is designated. Adopters SHALL still implement and evidence it. | SEC-013. Owner: CIO (policy); System Owners (operation). |
| G-02 | SOC 2 CC3.3 | **Closed in the suite.** Fraud risk was not required in risk assessment; RSK-002 section 5.10 (RSK-002.5.10.1 – 5.10.3) now requires it, and KC-13 is designated. Adopters SHALL still implement and evidence it. | RSK-002. Owner: Head of GRC. |
| G-03 | ISO A.5.13 | Labelling relies on a single subsection (SEC-002.5.4 handling matrix). Sufficient for the default scope; confirm the labelling rules are evidenced (DLP and labelling tool reports) before an ISO/IEC 27001 Stage 2 audit. | SEC-002. Owner: CISO. |
| G-04 | NIST CSF 2.0 (see section 5.7) | Five subcategories are not cited by any document. Four are addressed in substance but not mapped: GV.RM-05 (risk communication lines, RSK-001.5.7), GV.SC-02 (supply chain roles, RSK-003.5.1), GV.SC-03 (supply chain risk integrated into enterprise risk, RSK-003.5.1 with RSK-001), DE.AE-04 (estimated impact and scope of adverse events, RES-002.5.6). GV.RM-07 (strategic opportunities as positive risks) is not addressed; the Organization MAY leave it out of scope. | Map GV.RM-05, GV.SC-02, GV.SC-03 and DE.AE-04 at the next revision of RSK-001, RSK-003 and RES-002. Record a scope decision for GV.RM-07. Owner: Head of GRC. |
| G-05 | ISO A.8.34 | Was unmapped in all section 11 tables; mapped by this document (appendix A). | Align section 11 of CMP-002 and SEC-011 at next revision. Owner: Head of GRC. |

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| Head of GRC | Owns this document; maintains the matrix, reverse views and Key Control list; records corrections in appendix A; derives the Statement of Applicability when ISO/IEC 27001 is pursued; provides the matrix to auditors and assessors. |
| CISO | Approves this document and the Key Control list before each SOC 2 Type II Observation Period; approves Statement of Applicability exclusions. |
| Document Owners | Maintain section 11 of their documents; align section 11 with corrections notified under REF-001.5.1.3. |
| Control Owners | Operate the Key Controls designated in section 5.4 and produce Evidence under CMP-004. |
| Head of Security Engineering | `[PCI]` Keeps SEC-019 section 5.12 consistent with section 5.8. |
| HIPAA Security Officer | `[HIPAA]` Keeps CMP-008 matrices consistent with section 5.9. |
| CFO | `[SOX]` Confirms CMP-009 ITGC Key Controls are consistent with section 5.10. |
| Internal Audit Director | Uses this matrix to plan coverage under CMP-002; reports mapping errors to the Head of GRC. |

Activity-level assignments are consolidated in REF-002.

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| REF-001.7.1 | Matrix update after approval of a new or revised suite document | Within 10 business days |
| REF-001.7.2 | Policy-statement subsections with a mapping row | 100% of section 5.x subsections of every non-template suite document; every template mapped through its parent requirements |
| REF-001.7.3 | Control IDs verified to exist in the framework version in section 4 | 100% before publication |
| REF-001.7.4 | Key Control list approval | By the CISO, before the start of each SOC 2 Type II Observation Period |
| REF-001.7.5 | Key Control additions during an Observation Period notified to the service auditor | Within 10 business days |
| REF-001.7.6 | Key Control testing frequency | As set in CMP-002 |
| REF-001.7.7 | Review of reverse-coverage views | Every 12 months and on any change of framework version |
| REF-001.7.8 | Annex A controls with a recorded applicability decision when ISO/IEC 27001 is pursued | 93 of 93 |
| REF-001.7.9 | Notification to Document Owner of a correction to their section 11 | Within 10 business days of the correction |
| REF-001.7.10 | Document review | As set in GOV-002, and on approval of any new suite document |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Subsections without a mapping row | 0 | On each update | Head of GRC |
| Mapping updates completed within REF-001.7.1 | 100% | Quarterly | Head of GRC |
| Annex A controls "Not covered" | 0 | Every 12 months | Head of GRC |
| SOC 2 in-scope criteria with at least one Key Control | 100% | Before each Observation Period | Head of GRC |
| Open coverage gaps (section 5.11) past their REF-003 target date | 0 | Quarterly | Head of GRC |
| Mapping errors found by auditors or assessors | 0 | After each external assessment | Head of GRC |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003. The rule that every
control ID is verified to exist (REF-001.5.1.2), and the restriction on changing Key Controls during
an Observation Period (REF-001.5.1.5), SHALL NOT receive an Exception.

## 10. Enforcement

Non-compliance is handled under CMP-007. A mapping error that causes an external assessment
scoping error SHALL be recorded as an issue under CMP-002.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| REF-001.5.1 – 5.3 | 4.2, 7.5.1, 7.5.2; A.5.31, A.5.36 | GV.OC-03, GV.PO-01 | PM-1, CA-2 | — | CC2.1, CC5.3 | APO01, MEA03 | `[PCI]` 12.4; `[HIPAA]` §164.316 |
| REF-001.5.4 | 9.1; A.5.36 | GV.OV-01 | CA-2, CA-7 | — | CC4.1, CC5.1 | MEA01, MEA02 | `[SOX]` §404 |
| REF-001.5.5 – 5.10 | 6.1.3, 9.1; A.5.35, A.5.36 | GV.OV-01, ID.IM-01 | CA-2, PM-14 | — | CC4.1 | MEA02, MEA03 | `[PCI]` 12.4 |
| REF-001.5.11 | 6.1.3, 10.2 | ID.IM-01 | CA-5, PM-4 | — | CC4.2 | MEA02 | — |

## 12. Related documents

ISP-000, GOV-001, GOV-002, GOV-006, RSK-001, CMP-001, CMP-002, CMP-003, CMP-004, CMP-007, CMP-008,
CMP-009, SEC-019, REF-002, REF-003, and every suite document listed in section 4.

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Head of GRC | | | |
| Approver: CISO | | | |

## Appendix A. Mapping corrections and additions

These are the corrections REF-001 made when normalizing each document's section 11
(REF-001.5.1.3). Every control ID cited in section 11 of every suite document was checked to
confirm it exists in the framework versions in section 4. **No cited control ID was found not to
exist.** The corrections below normalize notation that is not a citable ID, and add
mappings the source tables omitted.

| # | Location | Framework | As cited | As mapped in REF-001 | Reason |
|---|---|---|---|---|---|
| C-01 | CMP-006 §11 row CMP-006.5.5 | SOC 2 TSC | P-series (if in scope) | — (removed) | "P-series" is not a criterion ID. Privacy criteria are outside the default SOC 2 scope (SUITE-REGISTER decision #2); C1.1 already covers the requirement |
| C-02 | CMP-008 §11 row CMP-008.5.6 | ISO/IEC 27001:2022 | A.5.24–5.29 | A.5.24, A.5.25, A.5.26, A.5.27, A.5.28, A.5.29 | Range notation expanded to individual IDs (each verified to exist) |
| C-03 | CMP-008 §11 row CMP-008.5.7 | ISO/IEC 27001:2022 | A.7.1–7.4 | A.7.1, A.7.2, A.7.3, A.7.4 | Range notation expanded to individual IDs (each verified to exist) |
| C-04 | GOV-003 §11 row GOV-003.5.1 – 5.3 | COBIT 2019 | MEA01.01–MEA01.04 | MEA01.01, MEA01.02, MEA01.03, MEA01.04 | Range notation expanded to individual IDs (each verified to exist) |
| C-05 | ISP-000 §11 row ISP-000.5.3 | ISO/IEC 27001:2022 | 4.1–4.3 | 4.1, 4.2, 4.3 | Range notation expanded to individual IDs (each verified to exist) |
| C-06 | PPL-002 §11 row PPL-002.5.2 – 5.3 | CIS v8.1 | 14.1–14.8 | 14.1, 14.2, 14.3, 14.4, 14.5, 14.6, 14.7, 14.8 | Range notation expanded to individual IDs (each verified to exist) |
| C-07 | RSK-001 §11 row RSK-001.5.3 | ISO/IEC 27001:2022 | 6.1.2(a) | 6.1.2 | Lettered list item is not a citable control ID; cited the parent clause |
| C-08 | RSK-001 §11 row RSK-001.5.5 | ISO/IEC 27001:2022 | 6.1.3(f) | 6.1.3 | Lettered list item is not a citable control ID; cited the parent clause |
| C-09 | RSK-002 §11 row RSK-002.5.2 – 5.4 | ISO/IEC 27001:2022 | 6.1.2(c)–(d) | 6.1.2 | Lettered list item is not a citable control ID; cited the parent clause |
| C-10 | SEC-019 §11 row SEC-019.5.10 | ISO/IEC 27001:2022 | A.5.19–5.22 | A.5.19, A.5.20, A.5.21, A.5.22 | Range notation expanded to individual IDs (each verified to exist) |
| C-11 | CMP-002.5.9 | ISO/IEC 27001:2022 | (not mapped) | A.8.34 | Requirement protects production systems during audit or security testing (read-only, time-bound auditor access; non-disruptive scanning; rules of engagement), which is ISO/IEC 27001:2022 A.8.34. A.8.34 was otherwise unmapped in the suite |
| C-12 | SEC-011.5.2 | ISO/IEC 27001:2022 | (not mapped) | A.8.34 | Requirement protects production systems during audit or security testing (read-only, time-bound auditor access; non-disruptive scanning; rules of engagement), which is ISO/IEC 27001:2022 A.8.34. A.8.34 was otherwise unmapped in the suite |
| C-13 | SEC-011.5.7 | ISO/IEC 27001:2022 | (not mapped) | A.8.34 | Requirement protects production systems during audit or security testing (read-only, time-bound auditor access; non-disruptive scanning; rules of engagement), which is ISO/IEC 27001:2022 A.8.34. A.8.34 was otherwise unmapped in the suite |
| C-14 | GOV-004 §11 row GOV-004.5.15 | All frameworks | (subsection absent from GOV-004 §11 in the draft reviewed for REF-001 v1.0) | A.5.11, A.6.5 · PR.AA-05 · PS-4 · CIS 6.2 · CC6.2, CC6.5 · APO07.06 · [HIPAA] §164.308(a)(3)(ii)(C) | Source document fixed: GOV-004 section 11 now carries this row; REF-001 uses it as the source |

Structural normalizations (no change to control IDs):

| # | Location | Normalization |
|---|---|---|
| N-01 | GOV-004 section 11 | Rows "5.1 – 5.4" and "5.3" overlap; the mappings for subsection 5.3 were merged. |
| N-02 | SEC-002 section 11 | Two rows for subsection 5.4 ("Handling matrix" and "Generative AI row") were merged. |
| N-03 | GOV-006 section 11 | The table has no CIS v8.1 or Regulations column; shown as "—". |
| N-04 | RSK-006 section 11.1 | ISO/IEC 42001 and NIST AI RMF alignment left in RSK-006 (outside REF-001 scope). |
| N-05 | All documents | Regulation citations normalized to tag form (`[PCI]`, `[HIPAA]`, `[GDPR]`, `[CPRA]`, `[SOX]`, Other); "PCI DSS", "45 CFR" and "Cal. Civ. Code" prefixes dropped after tagging. |
