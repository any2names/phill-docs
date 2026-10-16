# CMP-008 — HIPAA Security Rule Implementation Standard

## 1. Document control

| Field | Value |
|---|---|
| Document ID | CMP-008 |
| Title | HIPAA Security Rule Implementation Standard |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 2 — Standard |
| Classification | Internal |
| Owner | HIPAA Security Officer |
| Approver | CISO; the ISSC where the CISO is the designated HIPAA Security Officer (README ‡). Under the recommended default in CMP-008.5.2.1 the approver is the ISSC |
| Effective date | [DECISION REQUIRED: Date of ISSC approval (or CISO approval where the CISO is not the HIPAA Security Officer)] |
| Next review date | Effective date + 12 months, and on the event-triggered reviews in GOV-002.7.4 |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-001, GOV-002, RSK-001, RSK-002, RSK-003, RSK-004, CMP-001, CMP-002, CMP-003, CMP-004, CMP-007, SEC-001 to SEC-018, RES-001 to RES-005, PPL-001, PPL-002, REF-001 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | HIPAA Security Officer | Initial release |

## 3. Purpose

This Standard demonstrates how the Organization meets every standard and implementation
specification of the HIPAA Security Rule (45 CFR Part 164, Subpart C). It:

- designates the HIPAA Security Officer required by §164.308(a)(2) and sets that role's duties;
- sets the requirements for the ePHI risk analysis required by §164.308(a)(1)(ii)(A);
- records, for each Required (R) and Addressable (A) implementation specification, the suite
  document that implements it; and
- records the documented decision for each addressable specification required by
  §164.306(d)(3) and §164.316.

It does not restate the controls themselves. Each control lives in the document named in the
implementation matrix (sections 5.6 to 5.10).

## 4. Scope

**This entire document is a conditional module. It applies only where the Organization is
subject to HIPAA `[HIPAA]`**, as a Covered Entity, a Business Associate, or both, as recorded
in the Obligations Register (CMP-001). Where HIPAA does not apply, the Organization removes this
document and all clauses tagged `[HIPAA]` (README "Conditional modules").

| Dimension | In scope |
|---|---|
| People | All Workforce Members who create, receive, maintain, transmit or can access ePHI, and their managers |
| Systems | Every Information System, Cloud Service, Endpoint and item of Media that creates, receives, maintains or transmits ePHI, and every system that provides security functions for them (identity, logging, backup, key management) |
| Data | All ePHI, in every location and state (at rest, in transit, in use). PHI in non-electronic form is covered by the HIPAA Privacy Rule and is outside this Standard except where it is converted to ePHI |
| Locations | All Organization facilities, data centers and remote work locations where ePHI is accessed, and Cloud Service Provider facilities hosting ePHI |
| Third parties | Every Business Associate and subcontractor that creates, receives, maintains or transmits ePHI on the Organization's behalf, and every Covered Entity for which the Organization acts as a Business Associate |

[ASSUMPTION: This Standard reflects 45 CFR Part 164, Subpart C as in force on the effective
date. HHS published a proposed rule in January 2025 that would, among other changes, remove the
distinction between required and addressable specifications. If a final rule is published, the
HIPAA Security Officer SHALL start an event-triggered review of this document under GOV-002.]

## 5. Requirements

### 5.1 HIPAA status and general requirements (§164.306)

- **CMP-008.5.1.1** `[HIPAA]` The GC SHALL record the Organization's HIPAA status (Covered Entity, Business Associate, hybrid entity, or a combination) in the Obligations Register (CMP-001), together with each Covered Entity customer for which it acts as Business Associate. [DECISION REQUIRED: HIPAA status of the Organization. Recommended default: Business Associate]
- **CMP-008.5.1.2** `[HIPAA]` The Organization SHALL ensure the Confidentiality, Integrity and Availability of all ePHI it creates, receives, maintains or transmits; protect against threats and hazards to the security or Integrity of ePHI and against uses or disclosures not permitted by the HIPAA Privacy Rule that it can anticipate; and ensure Workforce Member compliance (§164.306(a)). The HIPAA Security Officer is accountable for this requirement.
- **CMP-008.5.1.3** `[HIPAA]` In selecting security measures the HIPAA Security Officer SHALL document consideration of the four factors in §164.306(b)(2): the Organization's size, complexity and capabilities; its technical infrastructure, hardware and software security capabilities; the costs of the measures; and the probability and criticality of potential risks to ePHI. This record forms part of each addressable decision (section 5.5).
- **CMP-008.5.1.4** `[HIPAA]` Every Required implementation specification SHALL be implemented. Every Addressable implementation specification SHALL be assessed and decided under section 5.5.
- **CMP-008.5.1.5** `[HIPAA]` Where the Organization is a Business Associate and a Business Associate Agreement imposes a requirement stricter than this Standard, the stricter contractual requirement SHALL apply to the systems in scope of that agreement. The HIPAA Security Officer SHALL record each such stricter requirement against the relevant row of the implementation matrix.

### 5.2 HIPAA Security Officer (§164.308(a)(2))

- **CMP-008.5.2.1** `[HIPAA]` The CEO SHALL designate, in writing, one named individual as HIPAA Security Officer, recorded under GOV-001. [DECISION REQUIRED: Who is designated HIPAA Security Officer. Recommended default: the CISO, in which case this document is approved by the ISSC]
- **CMP-008.5.2.2** `[HIPAA]` The CEO SHALL designate, in writing, a deputy who acts as HIPAA Security Officer when the HIPAA Security Officer is unavailable for more than 5 consecutive business days or the role is vacant. A vacancy SHALL be filled by a new written designation within 30 days.
- **CMP-008.5.2.3** `[HIPAA]` The HIPAA Security Officer SHALL be responsible for the development and implementation of the policies and procedures required by Subpart C, and SHALL:
  1. own this Standard and the implementation matrix (sections 5.6 to 5.10);
  2. direct the ePHI risk analysis (section 5.3) and approve its results;
  3. make and record each addressable decision (section 5.5);
  4. direct the evaluation in section 5.11;
  5. approve the security terms of each Business Associate Agreement before signature (section 5.9);
  6. be consulted on every Security Incident involving ePHI under RES-002 and every breach determination under RES-003;
  7. report HIPAA security posture to the ISSC at least quarterly (CMP-008.7.8); and
  8. act, with the GC, as the Organization's contact for HHS Office for Civil Rights inquiries and for Covered Entity security inquiries.
- **CMP-008.5.2.4** `[HIPAA]` The HIPAA Security Officer SHALL coordinate with the HIPAA Privacy Officer on uses and disclosures of PHI, on breach risk assessments and on Business Associate Agreements. Where one individual holds both designations, that SHALL be recorded under GOV-001.
- **CMP-008.5.2.5** `[HIPAA]` The identity and contact details of the HIPAA Security Officer and deputy SHALL be published on the Organization's intranet and communicated to all in-scope Workforce Members within 10 business days of each designation.

### 5.3 ePHI risk analysis (§164.308(a)(1)(ii)(A)) and risk management (§164.308(a)(1)(ii)(B))

- **CMP-008.5.3.1** `[HIPAA]` The HIPAA Security Officer SHALL conduct an accurate and thorough assessment of the potential risks and vulnerabilities to the Confidentiality, Integrity and Availability of ePHI held by the Organization, using the method in RSK-002.
- **CMP-008.5.3.2** `[HIPAA]` The risk analysis SHALL cover all ePHI the Organization creates, receives, maintains or transmits, in every location, Information System, Cloud Service, Endpoint, item of Media, Business Associate and subcontractor. It SHALL NOT be limited to systems hosting a production ePHI database.
- **CMP-008.5.3.3** `[HIPAA]` The Data Owner of each ePHI data set SHALL maintain, in the Asset Inventory (SEC-001), a record of where that ePHI is stored, processed and transmitted, including flows to and from Business Associates and Covered Entities. The HIPAA Security Officer SHALL review this ePHI inventory every 6 months and before each risk analysis.
- **CMP-008.5.3.4** `[HIPAA]` For each in-scope asset or data flow, the risk analysis SHALL document:
  1. the Threats that could be "reasonably anticipated" (§164.306(a)(2)), including natural, human (intentional and unintentional) and environmental Threats;
  2. the Vulnerabilities that a Threat could exploit;
  3. the current security measures and whether they are configured and operating as intended;
  4. likelihood, impact and resulting risk level, scored under RSK-002; and
  5. the Risk Owner.
- **CMP-008.5.3.5** `[HIPAA]` The ePHI risk analysis SHALL be performed at the frequency of the enterprise risk assessment in RSK-002.5.6.1 and, in addition, SHALL be updated for the affected scope:
  1. before a new Information System or Cloud Service begins to hold ePHI in production;
  2. before ePHI is first shared with a new Business Associate or subcontractor;
  3. within 30 days of a material change to an ePHI data flow, hosting location or security architecture; and
  4. within 30 days of the closure of a Sev-1 or Sev-2 Security Incident involving ePHI.
- **CMP-008.5.3.6** `[HIPAA]` Every risk identified SHALL be entered in the Risk Register (TPL-001) with a `[HIPAA]` tag and treated within the risk treatment plan deadlines in RSK-002. Risk Acceptance SHALL follow RSK-001; a Risk Acceptance that leaves ePHI exposed SHALL also be approved by the HIPAA Security Officer.
- **CMP-008.5.3.7** `[HIPAA]` The risk analysis report SHALL be approved by the HIPAA Security Officer and presented to the ISSC at the next ISSC meeting after approval. The report, its working papers and the ePHI inventory snapshot SHALL be retained as Evidence under section 5.10.

### 5.4 Sanctions and information system activity review (§164.308(a)(1)(ii)(C)–(D))

- **CMP-008.5.4.1** `[HIPAA]` Sanctions against Workforce Members who fail to comply with HIPAA security requirements SHALL be applied under CMP-007. The CHRO SHALL record each sanction relating to ePHI and notify the HIPAA Security Officer within 5 business days of the sanction decision.
- **CMP-008.5.4.2** `[HIPAA]` Records of information system activity on ePHI systems (audit logs, access reports, Security Incident tracking reports) SHALL be collected and reviewed under SEC-012. The SOC Manager SHALL provide the HIPAA Security Officer with a summary of ePHI system log review findings every month.
- **CMP-008.5.4.3** `[HIPAA]` The HIPAA Security Officer SHALL include statistics on sanctions recorded under CMP-008.5.4.1 in the information system activity review under CMP-008.5.4.2.

### 5.5 Addressable implementation specification decisions (§164.306(d)(3))

- **CMP-008.5.5.1** `[HIPAA]` For each Addressable implementation specification, the HIPAA Security Officer SHALL assess whether it is a "reasonable and appropriate" safeguard (the regulatory test in §164.306(d)(3)) in the Organization's environment, with reference to the latest ePHI risk analysis and the factors in CMP-008.5.1.3, and SHALL record exactly one decision:
  1. **Implement**: the specification is implemented as written;
  2. **Equivalent alternative**: the specification is not "reasonable and appropriate" as written, and an equivalent alternative measure that achieves the same objective is implemented; or
  3. **Not reasonable and appropriate**: neither the specification nor an alternative is implemented, because the standard is met without it.
- **CMP-008.5.5.2** `[HIPAA]` Each decision of type 2 or 3 SHALL record why the specification is not "reasonable and appropriate", the risk analysis entry relied on, and (for type 2) the alternative measure and its implementing document.
- **CMP-008.5.5.3** `[HIPAA]` Decisions of type 1 SHALL be approved by the HIPAA Security Officer. Decisions of type 2 or 3 SHALL be approved by the HIPAA Security Officer and ratified by the ISSC.
- **CMP-008.5.5.4** `[HIPAA]` The HIPAA Security Officer SHALL re-assess every addressable decision every 12 months and within 30 days of each risk analysis update under CMP-008.5.3.5. A changed decision SHALL be made by revising this document under GOV-002.
- **CMP-008.5.5.5** `[HIPAA]` "Addressable" SHALL NOT be treated as optional. An Addressable specification that is neither implemented nor decided under this section is non-compliance and is handled under CMP-007.

### 5.6 Implementation matrix: administrative safeguards (§164.308)

- **CMP-008.5.6.1** `[HIPAA]` Each standard and implementation specification in the table below SHALL be implemented by the document listed. The Document Owner of each listed document is the Control Owner for that row and SHALL provide Evidence of operation to the HIPAA Security Officer on request within 10 business days.

| Row | CFR citation | Standard / implementation specification | R/A | Implemented by | Decision and rationale (Addressable only) |
|---|---|---|---|---|---|
| A-01 | §164.308(a)(1)(i) | Security management process (standard) | R | CMP-008.5.3–5.5; RSK-001; RSK-002 | — |
| A-02 | §164.308(a)(1)(ii)(A) | Risk analysis | R | CMP-008.5.3; RSK-002 (method and cadence) | — |
| A-03 | §164.308(a)(1)(ii)(B) | Risk management | R | CMP-008.5.3.6; RSK-001 (acceptance); RSK-002 (treatment deadlines); TPL-001 | — |
| A-04 | §164.308(a)(1)(ii)(C) | Sanction policy | R | CMP-007; CMP-008.5.4.1 | — |
| A-05 | §164.308(a)(1)(ii)(D) | Information system activity review | R | SEC-012 (log collection, review and alert triage); CMP-008.5.4.2 | — |
| A-06 | §164.308(a)(2) | Assigned security responsibility (standard) | R | CMP-008.5.2; GOV-001 (designation record) | — |
| A-07 | §164.308(a)(3)(i) | Workforce security (standard) | R | PPL-001; SEC-003 | — |
| A-08 | §164.308(a)(3)(ii)(A) | Authorization and/or supervision | A | SEC-003 (access approval by Data Owner); SEC-016 (escort of visitors and Workforce Members without ePHI access in ePHI areas) | **Implement.** Every ePHI access is approved under SEC-003; personnel without approved access are supervised in ePHI areas under SEC-016. Low cost; directly mitigates insider and unauthorized access risk |
| A-09 | §164.308(a)(3)(ii)(B) | Workforce clearance procedure | A | PPL-001 (screening before access to Restricted data; rescreening) | **Implement.** PHI is Restricted (SEC-002); screening before access is already required for all Restricted data |
| A-10 | §164.308(a)(3)(ii)(C) | Termination procedures | A | SEC-003 (revocation on Separation and role change); PPL-001 (asset return) | **Implement.** Revocation SLAs in SEC-003 apply to all Users, including ePHI system Users |
| A-11 | §164.308(a)(4)(i) | Information access management (standard) | R | SEC-003 | — |
| A-12 | §164.308(a)(4)(ii)(A) | Isolating health care clearinghouse functions | R | Conditional: SEC-007 (network segmentation) and SEC-003 (separate access) where the Organization is, or contains, a health care clearinghouse | Not an Addressable specification. Under the recommended Business Associate default the Organization does not perform clearinghouse functions; the GC SHALL confirm this in the Obligations Register every 12 months |
| A-13 | §164.308(a)(4)(ii)(B) | Access authorization | A | SEC-003 (role-based access, Data Owner approval, Least Privilege); SEC-005 (privileged access) | **Implement.** Documented authorization is the primary control against unauthorized ePHI access |
| A-14 | §164.308(a)(4)(ii)(C) | Access establishment and modification | A | SEC-003 (provisioning, role change, Access Review); SEC-005; TPL-008 | **Implement.** Access Reviews for ePHI systems run at the Restricted-data frequency in SEC-003.7.1 |
| A-15 | §164.308(a)(5)(i) | Security awareness and training (standard) | R | PPL-002 (training at hire, annual and role-based training for PHI handlers) | — |
| A-16 | §164.308(a)(5)(ii)(A) | Security reminders | A | PPL-002 (phishing simulation and security communications cadence) | **Implement.** Existing awareness program covers ePHI handlers at no material added cost |
| A-17 | §164.308(a)(5)(ii)(B) | Protection from malicious software | A | SEC-008 (anti-malware / EDR on Endpoints and servers); SEC-014 (email filtering); PPL-002 (training content) | **Implement.** Ransomware is a top-rated Threat to ePHI Availability |
| A-18 | §164.308(a)(5)(ii)(C) | Log-in monitoring | A | SEC-012 (failed and anomalous log-in alerting); SEC-004 (account lockout) | **Implement.** Automated through the logging platform; detects credential attacks |
| A-19 | §164.308(a)(5)(ii)(D) | Password management | A | SEC-004 (password, MFA and Secret handling) | **Implement.** Authentication standards in SEC-004 apply to all ePHI systems |
| A-20 | §164.308(a)(6)(i) | Security incident procedures (standard) | R | RES-001; RES-002 | — |
| A-21 | §164.308(a)(6)(ii) | Response and reporting | R | RES-002 (identify, respond, mitigate, document); RES-003 (breach and Covered Entity notification); TPL-006 | — |
| A-22 | §164.308(a)(7)(i) | Contingency plan (standard) | R | RES-004; RES-005 | — |
| A-23 | §164.308(a)(7)(ii)(A) | Data backup plan | R | SEC-018 (Backup frequency and retention for ePHI systems by Recovery Tier) | — |
| A-24 | §164.308(a)(7)(ii)(B) | Disaster recovery plan | R | RES-005 | — |
| A-25 | §164.308(a)(7)(ii)(C) | Emergency Mode Operation plan | R | RES-004 (continuity of critical processes, including security of ePHI while operating in emergency mode) | — |
| A-26 | §164.308(a)(7)(ii)(D) | Testing and revision procedures | A | RES-004 (exercise cadence); SEC-018 (restore testing); RES-005 (update after each test) | **Implement.** Untested plans are a recurring audit finding; testing is already required for Tier 0 and Tier 1 systems |
| A-27 | §164.308(a)(7)(ii)(E) | Applications and data criticality analysis | A | RSK-004 (BIA and Recovery Tier for each ePHI system) | **Implement.** The BIA already assigns a Recovery Tier to every critical system; ePHI systems are flagged in the BIA |
| A-28 | §164.308(a)(8) | Evaluation (standard) | R | CMP-008.5.11; CMP-002 | — |
| A-29 | §164.308(b)(1)–(2) | Business associate contracts and other arrangements (standard), including subcontractors | R | RSK-003 (Third Party due diligence and contracts); CMP-008.5.9 | — |
| A-30 | §164.308(b)(3) | Written contract or other arrangement | R | RSK-003 (BAA requirement before ePHI is shared); CMP-008.5.9 | — |

### 5.7 Implementation matrix: physical safeguards (§164.310)

- **CMP-008.5.7.1** `[HIPAA]` Each standard and implementation specification in the table below SHALL be implemented by the document listed, under the Control Owner rule in CMP-008.5.6.1.

| Row | CFR citation | Standard / implementation specification | R/A | Implemented by | Decision and rationale (Addressable only) |
|---|---|---|---|---|---|
| P-01 | §164.310(a)(1) | Facility access controls (standard) | R | SEC-016 | — |
| P-02 | §164.310(a)(2)(i) | Contingency operations | A | SEC-016 (facility access during emergencies); RES-004; RES-005 | **Implement.** Restoration teams need controlled facility access during DR; covered by existing BC/DR arrangements |
| P-03 | §164.310(a)(2)(ii) | Facility security plan | A | SEC-016 (Organization facilities); RSK-003 (assessment of Cloud Service Provider physical controls) | **Implement** for Organization-controlled facilities. **Equivalent alternative** for Cloud Service Provider data centers: the Organization cannot write the provider's facility plan, so it relies on the provider's independent attestation (e.g. SOC 2 Type II or ISO/IEC 27001 certificate) covering physical security, reviewed under RSK-003 at the reassessment frequency for the vendor's tier |
| P-04 | §164.310(a)(2)(iii) | Access control and validation procedures | A | SEC-016 (role-based facility access, visitor control); SEC-010 (control of access to software for testing and revision) | **Implement.** Badge access and visitor logs already operate at all sites; test-environment access is controlled under SEC-010 |
| P-05 | §164.310(a)(2)(iv) | Maintenance records | A | SEC-016 (records of repairs and modifications to physical security components); RSK-003 (Cloud Service Provider facilities) | **Implement** for Organization-controlled facilities. **Equivalent alternative** for Cloud Service Provider data centers: provider attestation reviewed under RSK-003, for the reason given in row P-03 |
| P-06 | §164.310(b) | Workstation use (standard) | R | GOV-004 (permitted use); SEC-008 (Endpoint configuration); SEC-015 (remote use) | — |
| P-07 | §164.310(c) | Workstation security (standard) | R | SEC-008 (Endpoint controls); SEC-016 (physical placement and screen privacy in ePHI areas) | — |
| P-08 | §164.310(d)(1) | Device and media controls (standard) | R | SEC-001; SEC-017 | — |
| P-09 | §164.310(d)(2)(i) | Disposal | R | SEC-017 (Media Sanitization before disposal) | — |
| P-10 | §164.310(d)(2)(ii) | Media re-use | R | SEC-017 (Media Sanitization before re-use) | — |
| P-11 | §164.310(d)(2)(iii) | Accountability | A | SEC-001 (Asset Inventory records custody and movement of hardware and Media containing ePHI) | **Implement.** The Asset Inventory already tracks custodians; an ePHI flag is added under CMP-008.5.3.3 |
| P-12 | §164.310(d)(2)(iv) | Data backup and storage | A | SEC-018 (Backup); SEC-013.5.1.6 (Change records for equipment moves) | **Implement.** A retrievable exact copy of ePHI is confirmed in the Change record before equipment holding ePHI is moved |

### 5.8 Implementation matrix: technical safeguards (§164.312)

- **CMP-008.5.8.1** `[HIPAA]` Each standard and implementation specification in the table below SHALL be implemented by the document listed, under the Control Owner rule in CMP-008.5.6.1.

| Row | CFR citation | Standard / implementation specification | R/A | Implemented by | Decision and rationale (Addressable only) |
|---|---|---|---|---|---|
| T-01 | §164.312(a)(1) | Access control (standard) | R | SEC-003; SEC-005 | — |
| T-02 | §164.312(a)(2)(i) | Unique user identification | R | SEC-003 (unique User IDs; shared accounts prohibited); SEC-005 | — |
| T-03 | §164.312(a)(2)(ii) | Emergency access procedure | R | SEC-005 (Break-glass Accounts); RES-005 (access to ePHI during DR) | — |
| T-04 | §164.312(a)(2)(iii) | Automatic logoff | A | SEC-004 (idle session timeout) applied to every ePHI application and Endpoint | **Implement.** Supported natively by all in-scope platforms; mitigates unattended-session exposure |
| T-05 | §164.312(a)(2)(iv) | Encryption and decryption | A | SEC-006 (encryption of Restricted data at rest, key management); SEC-008 (full-disk encryption of Endpoints); SEC-002 (handling of Restricted data) | **Implement.** Encryption to the SEC-006 minimums also renders PHI "secured" under HHS guidance for 45 CFR §164.402, reducing breach notification exposure |
| T-06 | §164.312(b) | Audit controls (standard) | R | SEC-012 (logging of ePHI system activity); CMP-004 (`[HIPAA]` log retention for ePHI systems) | — |
| T-07 | §164.312(c)(1) | Integrity (standard) | R | SEC-006; SEC-012; SEC-010 (input validation and data integrity in applications) | — |
| T-08 | §164.312(c)(2) | Mechanism to authenticate electronic protected health information | A | SEC-006 (cryptographic hashing and authenticated encryption); SEC-013.5.9.6 (file integrity monitoring on ePHI stores); SEC-018 (Backup integrity verification) | **Implement.** Database transaction integrity, hashing and integrity monitoring are available on all in-scope platforms |
| T-09 | §164.312(d) | Person or entity authentication (standard) | R | SEC-004 (MFA for all SSO applications and remote access; Service Account authentication) | — |
| T-10 | §164.312(e)(1) | Transmission security (standard) | R | SEC-006; SEC-007; SEC-014 | — |
| T-11 | §164.312(e)(2)(i) | Integrity controls | A | SEC-006 (authenticated TLS cipher suites); SEC-007 (network protections) | **Implement.** Approved TLS configurations provide integrity protection at no added cost |
| T-12 | §164.312(e)(2)(ii) | Encryption | A | SEC-006 (TLS minimums for all ePHI transmissions, including internal networks); SEC-014 (encrypted email for ePHI) | **Implement.** ePHI SHALL NOT be transmitted unencrypted over any network, internal or external, except email to an individual who has requested unencrypted communication after being informed of the risk, recorded by the HIPAA Privacy Officer (SEC-014.5.5.4) |

### 5.9 Implementation matrix: organizational requirements (§164.314)

- **CMP-008.5.9.1** `[HIPAA]` Each standard and implementation specification in the table below SHALL be implemented by the document listed, under the Control Owner rule in CMP-008.5.6.1.

| Row | CFR citation | Standard / implementation specification | R/A | Implemented by | Decision and rationale (Addressable only) |
|---|---|---|---|---|---|
| O-01 | §164.314(a)(1) | Business associate contracts or other arrangements (standard) | R | RSK-003; CMP-008.5.9.2–5.9.5 | — |
| O-02 | §164.314(a)(2)(i) | Business associate contracts | R | RSK-003 (contract requirements); CMP-008.5.9.2 | — |
| O-03 | §164.314(a)(2)(ii) | Other arrangements | R | Conditional: GC, where the Organization is a governmental entity relying on a memorandum of understanding or law | Not an Addressable specification. Not applicable unless the Organization is a governmental entity; recorded in the Obligations Register |
| O-04 | §164.314(a)(2)(iii) | Business associate contracts with subcontractors | R | RSK-003; CMP-008.5.9.3 | — |
| O-05 | §164.314(b)(1)–(2)(i)–(iv) | Requirements for group health plans (plan document provisions) | R | Conditional: GC and CHRO, through group health plan documents, where the Organization sponsors a group health plan that receives ePHI other than summary health information or enrollment information | Not an Addressable specification. The GC SHALL confirm applicability in the Obligations Register every 12 months |

- **CMP-008.5.9.2** `[HIPAA]` Before ePHI is created, received, maintained or transmitted by a Business Associate on the Organization's behalf, or by the Organization on behalf of a Covered Entity, the GC SHALL ensure a signed Business Associate Agreement is in place that requires the other party to: comply with Subpart C; ensure that any subcontractor that handles the ePHI agrees to the same restrictions; and report to the Organization any Security Incident of which it becomes aware, including breaches of Unsecured PHI as required by §164.410.
- **CMP-008.5.9.3** `[HIPAA]` Where the Organization is a Business Associate, the Head of Procurement SHALL ensure that every subcontractor that creates, receives, maintains or transmits ePHI on the Organization's behalf signs a Business Associate Agreement with terms no less protective than the Organization's agreement with the Covered Entity, before the subcontractor receives ePHI.
- **CMP-008.5.9.4** `[HIPAA]` The Head of GRC SHALL maintain a register of every Business Associate Agreement (upstream and downstream), its counterparty, the ePHI systems in scope and its security reporting obligations, and SHALL reconcile it against the Asset Inventory ePHI flows every 6 months.
- **CMP-008.5.9.5** `[HIPAA]` Security Incident reporting to Covered Entities and from Business Associates SHALL follow the timelines in RES-003. Where the Organization learns of a pattern of activity or practice by a Business Associate or subcontractor that is a material breach of its agreement, the HIPAA Security Officer and the GC SHALL require a cure within the period in the agreement and, if it is not cured, terminate the agreement where feasible.

### 5.10 Implementation matrix: policies, procedures and documentation (§164.316)

- **CMP-008.5.10.1** `[HIPAA]` Each standard and implementation specification in the table below SHALL be implemented by the document listed, under the Control Owner rule in CMP-008.5.6.1.

| Row | CFR citation | Standard / implementation specification | R/A | Implemented by | Decision and rationale (Addressable only) |
|---|---|---|---|---|---|
| D-01 | §164.316(a) | Policies and procedures (standard) | R | GOV-002 (suite governance); this Standard; each document named in sections 5.6–5.9 | — |
| D-02 | §164.316(b)(1) | Documentation (standard): written (which may be electronic) policies, procedures, and records of required actions, activities and assessments | R | GOV-002; CMP-004; CMP-008.5.10.2 | — |
| D-03 | §164.316(b)(2)(i) | Time limit | R | CMP-004 (retention of policy documents, prior versions and control Evidence); CMP-008.5.10.3 | — |
| D-04 | §164.316(b)(2)(ii) | Availability | R | GOV-002 (publication to persons responsible for implementation) | — |
| D-05 | §164.316(b)(2)(iii) | Updates | R | GOV-002 (12-month and event-triggered review); CMP-008.5.5.4 | — |

- **CMP-008.5.10.2** `[HIPAA]` The following records SHALL be maintained as Evidence under CMP-004: each ePHI risk analysis and its working papers; each addressable decision and re-assessment; each evaluation report (section 5.11); the HIPAA Security Officer designations; the Business Associate Agreement register; Security Incident records involving ePHI; and every version of this Standard and of each document named in the implementation matrix.
- **CMP-008.5.10.3** `[HIPAA]` The records in CMP-008.5.10.2 SHALL be retained under the `[HIPAA]` minimum in CMP-004.5.2.2 (§164.316(b)(2)(i)). The Head of GRC SHALL confirm this at each review of CMP-004.

### 5.11 Evaluation (§164.308(a)(8))

- **CMP-008.5.11.1** `[HIPAA]` The HIPAA Security Officer SHALL commission a technical and nontechnical evaluation of how well the Organization's security policies and procedures meet Subpart C every 12 months, and within 90 days of an environmental or operational change that affects the security of ePHI (e.g. a new hosting platform, a merger or acquisition, a new Covered Entity customer class, or a change in the rule).
- **CMP-008.5.11.2** `[HIPAA]` The evaluation SHALL test every row of the implementation matrix for design and operating effectiveness, using the testing method in CMP-002, and SHALL be performed by Internal Audit or an independent external assessor, not by the Control Owners of the rows tested.
- **CMP-008.5.11.3** `[HIPAA]` Findings SHALL be entered in the Risk Register and remediated within the risk treatment plan deadlines in RSK-002. The evaluation report SHALL be presented to the ISSC and summarized to the Audit Committee in the next quarterly report under GOV-003.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CEO | Designates the HIPAA Security Officer and deputy in writing (CMP-008.5.2.1–5.2.2) |
| HIPAA Security Officer | Owns this Standard; directs the risk analysis and evaluation; makes and re-assesses addressable decisions; approves BAA security terms; reports quarterly to the ISSC |
| ISSC | Approves this Standard where the CISO is the HIPAA Security Officer; ratifies addressable decisions of type 2 or 3; receives risk analysis and evaluation reports |
| CISO | Approves this Standard where the CISO is not the HIPAA Security Officer; ensures SEC-series controls named in the matrix operate on ePHI systems |
| HIPAA Privacy Officer | Coordinates on PHI uses and disclosures, breach risk assessments and BAAs |
| GC | Records HIPAA status in the Obligations Register; ensures BAAs are in place; co-ordinates regulator contact |
| Head of GRC | Maintains the BAA register; maintains Evidence under CMP-004; maps this Standard in REF-001 |
| Head of Procurement | Ensures subcontractor BAAs are signed before ePHI is shared |
| Data Owners (ePHI) | Maintain ePHI location and flow records in the Asset Inventory |
| Document Owners of documents named in the matrix | Act as Control Owner for their rows; provide Evidence within 10 business days of request |
| SOC Manager | Provides the monthly ePHI log review summary |
| CHRO | Records and reports ePHI-related sanctions |
| Internal Audit Director | Performs or oversees the evaluation in section 5.11 |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| CMP-008.7.1 | HIPAA Security Officer designation | One named individual, designated in writing by the CEO, with a written deputy; vacancy filled within 30 days |
| CMP-008.7.2 | Communication of designation | Within 10 business days of each designation |
| CMP-008.7.3 | ePHI risk analysis frequency | Enterprise risk assessment cadence in RSK-002, plus updates before go-live of a new ePHI system, before ePHI is shared with a new Business Associate, and within 30 days of a material ePHI change or Sev-1/Sev-2 ePHI incident closure |
| CMP-008.7.4 | ePHI inventory review | Every 6 months and before each risk analysis |
| CMP-008.7.5 | Addressable decision re-assessment | Every 12 months and within 30 days of each risk analysis update |
| CMP-008.7.6 | Evaluation (§164.308(a)(8)) | Every 12 months and within 90 days of an environmental or operational change affecting ePHI |
| CMP-008.7.7 | Documentation retention | Per CMP-004.5.2.2 (§164.316(b)(2)(i)) |
| CMP-008.7.8 | HIPAA posture report to ISSC | At least quarterly |
| CMP-008.7.9 | ePHI log review summary to HIPAA Security Officer | Monthly |
| CMP-008.7.10 | BAA in place | Before ePHI is shared, in either direction |
| CMP-008.7.11 | BAA register reconciliation against ePHI flows | Every 6 months |
| CMP-008.7.12 | Evidence provided by Control Owners on request | Within 10 business days |
| CMP-008.7.13 | Sanction notification to HIPAA Security Officer | Within 5 business days of the sanction decision |
| CMP-008.7.14 | Security Incident and breach notification timelines | As set in RES-003 |
| CMP-008.7.15 | Log retention for ePHI systems | As set in CMP-004 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Rows of the implementation matrix with a named implementing document and current Evidence | 100% | Quarterly | HIPAA Security Officer |
| Addressable specifications with a recorded decision re-assessed in the last 12 months | 100% | Quarterly | HIPAA Security Officer |
| ePHI systems covered by a risk analysis completed or updated in the last 12 months | 100% | Quarterly | HIPAA Security Officer |
| New ePHI systems risk-assessed before production go-live | 100% | Quarterly | HIPAA Security Officer |
| Business Associates and subcontractors with ePHI access and a signed BAA | 100% | Quarterly | Head of GRC |
| High and Critical ePHI risks treated within RSK-002 deadlines | 100% | Quarterly | HIPAA Security Officer |
| Evaluation findings open past their treatment deadline | 0 | Quarterly | Internal Audit Director |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

In addition:

- No Exception MAY be granted against a Required implementation specification. A Required
  specification that cannot be met is a compliance gap and SHALL be entered in the Risk Register
  and remediated.
- An Addressable specification is not changed through an Exception. Its decision is changed
  under section 5.5.
- Every Exception to a control named in the implementation matrix that affects ePHI systems
  SHALL be reviewed by the HIPAA Security Officer before approval.

## 10. Enforcement

Non-compliance is handled under CMP-007.

Failure to protect ePHI can expose the Organization to civil monetary penalties under 45 CFR
Part 160, Subpart D, and to contractual liability under Business Associate Agreements. The HIPAA
Security Officer SHALL be informed of every enforcement action under CMP-007 that relates to ePHI.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| CMP-008.5.1 | 4.2, 4.3; A.5.31 | GV.OC-03 | PM-9, PL-2 | — | CC1.1, CC2.2 | APO01, MEA03 | `[HIPAA]` 45 CFR §164.306 |
| CMP-008.5.2 | 5.3; A.5.2 | GV.RR-02 | PM-2 | — | CC1.3 | APO01 | `[HIPAA]` §164.308(a)(2) |
| CMP-008.5.3 | 6.1.2, 8.2; A.5.9, A.5.12 | ID.RA-01, ID.RA-05, GV.RM-01 | RA-3, RA-2, PM-9 | 3.2 | CC3.1, CC3.2 | APO12 | `[HIPAA]` §164.308(a)(1)(ii)(A)–(B) |
| CMP-008.5.4 | 7.3; A.6.4, A.8.15, A.8.16 | DE.CM-01, DE.AE-02 | PS-8, AU-6 | 8.11 | CC1.5, CC7.2 | DSS05 | `[HIPAA]` §164.308(a)(1)(ii)(C)–(D) |
| CMP-008.5.5 | 6.1.3 | GV.RM-01 | PL-2, RA-3 | — | CC3.2, CC5.1 | APO12 | `[HIPAA]` §164.306(d)(3); §164.316 |
| CMP-008.5.6 | A.5.15, A.5.18, A.5.24–5.29, A.6.1, A.6.3, A.6.5, A.8.7, A.8.13 | PR.AA-05, PR.AT-01, RS.MA-01, RC.RP-01 | AC-2, AT-2, IR-4, CP-2, CP-9, PS-3, PS-4 | 5.3, 6.1, 6.2, 10.1, 11.2, 14.1, 17.1 | CC6.2, CC6.3, CC7.4, A1.2, A1.3 | DSS04, DSS05, DSS06 | `[HIPAA]` §164.308 |
| CMP-008.5.7 | A.7.1–7.4, A.7.9, A.7.10, A.7.14, A.8.1 | PR.AA-06, PR.DS-01 | PE-2, PE-3, MP-6, MP-5 | 1.1, 3.5 | CC6.4, CC6.5 | DSS05, DSS01 | `[HIPAA]` §164.310 |
| CMP-008.5.8 | A.5.17, A.8.2, A.8.5, A.8.15, A.8.24 | PR.AA-01, PR.DS-01, PR.DS-02, PR.PS-04 | AC-3, IA-2, AU-2, SC-8, SC-13, SC-28, SI-7 | 3.10, 3.11, 6.3, 8.2 | CC6.1, CC6.7, CC7.2 | DSS05 | `[HIPAA]` §164.312 |
| CMP-008.5.9 | A.5.19, A.5.20, A.5.21 | GV.SC-05, GV.SC-07 | SA-9, SR-3 | 15.4 | CC9.2 | APO10 | `[HIPAA]` §164.308(b), §164.314, §164.410 |
| CMP-008.5.10 | 7.5; A.5.33 | GV.PO-01 | PL-1, AU-11 | — | CC2.2 | APO01, BAI08 | `[HIPAA]` §164.316 |
| CMP-008.5.11 | 9.1, 9.2; A.5.35 | ID.IM-01, GV.OV-01 | CA-2, CA-7 | — | CC4.1, CC4.2 | MEA02, MEA03 | `[HIPAA]` §164.308(a)(8) |

## 12. Related documents

ISP-000, GOV-001, GOV-002, GOV-003, GOV-004, RSK-001, RSK-002, RSK-003, RSK-004, CMP-001,
CMP-002, CMP-003, CMP-004, CMP-007, SEC-001, SEC-002, SEC-003, SEC-004, SEC-005, SEC-006,
SEC-007, SEC-008, SEC-010, SEC-012, SEC-013, SEC-014, SEC-015, SEC-016, SEC-017, SEC-018,
RES-001, RES-002, RES-003, RES-004, RES-005, PPL-001, PPL-002, TPL-001, TPL-006, TPL-008,
REF-001, REF-002

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: HIPAA Security Officer | | | |
| Approver: the ISSC where the CISO is the HIPAA Security Officer, signed by the ISSC Vice-Chair on behalf of the ISSC (CISO recused as Document Owner under GOV-001.5.3.9); otherwise the CISO | | | |
