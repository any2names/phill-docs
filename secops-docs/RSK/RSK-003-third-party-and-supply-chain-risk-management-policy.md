# RSK-003 — Third-Party & Supply Chain Risk Management Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | RSK-003 |
| Title | Third-Party & Supply Chain Risk Management Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Head of GRC |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | RSK-001 Risk Management Policy |
| Related documents | RSK-002, RSK-004, RSK-006, SEC-001, SEC-002, SEC-003, SEC-010, SEC-017, SEC-019, CMP-004, CMP-005, CMP-008, RES-002, RES-003, TPL-004 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Head of GRC | Initial release |

## 3. Purpose

This Policy sets the Organization's requirements for identifying, tiering, assessing,
contracting with, monitoring and offboarding Third Parties, and for managing Risk in the
software and hardware supply chain. It ensures that each Third Party with access to the
Organization's Information Assets, or on which a critical service depends, is subject to
security and privacy obligations no weaker than the Organization's own, in proportion to
the Risk it presents.

## 4. Scope

- **Third parties:** every Third Party, including vendors, Cloud Service providers, Processors and Subprocessors, `[HIPAA]` Business Associates, `[PCI]` third-party service providers (TPSPs), contractor firms, outsourcers, resellers, and open-source and commercial software suppliers.
- **Engagements:** all new, renewed and materially changed engagements, regardless of contract value or payment method (including free-tier, trial, click-through and credit-card purchases).
- **People:** the Head of Procurement, Business Sponsors who request a Third Party, Data Owners, System Owners, and all Workforce Members who procure or manage Third Parties.
- **Systems and data:** every Information Asset a Third Party accesses, stores, processes, transmits or supports, at every Classification Level.
- **Locations:** all Organization locations and all Third Party locations, including offshore and fourth-party locations.
- **Out of scope:** Workforce Member engagement terms (PPL-001) and individual contractor screening (PPL-001). The secure development of software by the Organization is in SEC-010.

## 5. Policy statements

### 5.1 Governance and inventory

- **RSK-003.5.1.1** No Third Party SHALL be engaged, and no Organization data SHALL be provided to a Third Party, until the Third Party has been tiered, assessed and contracted according to this Policy. Use of a Third Party without completing these steps is Shadow IT and SHALL be reported to the Head of GRC.
- **RSK-003.5.1.2** The Head of Procurement SHALL maintain a third-party inventory recording, for each Third Party: legal name; Business Sponsor; services provided; tier; highest Classification Level of data accessed; Recovery Tier of supported services (RSK-004); data locations; `[GDPR]` role as Processor or Subprocessor; `[HIPAA]` Business Associate status; `[PCI]` TPSP status and the PCI DSS requirements it manages; contract dates; last and next assessment dates; and current Risk rating.
- **RSK-003.5.1.3** The third-party inventory SHALL be reconciled against accounts-payable and corporate-card records at least quarterly. Each Third Party found that is not in the inventory SHALL be tiered within 10 business days of discovery.
- **RSK-003.5.1.4** Each Third Party SHALL have a Business Sponsor at director level or above, who is accountable for the relationship and acts as Risk Owner for Risks arising from it.
- **RSK-003.5.1.5** Third-party Risks rated Medium or above under RSK-002 SHALL be recorded in the Risk Register and managed under RSK-001.

### 5.2 Tiering

- **RSK-003.5.2.1** Each Third Party SHALL be assigned one of the following tiers before due diligence begins. A Third Party SHALL be assigned the highest tier for which any one criterion is met.

| Tier | Name | Criteria (any one) |
|---|---|---|
| Tier 1 | Critical | Stores, processes or transmits Restricted data; or supports a Recovery Tier 0 or Recovery Tier 1 service (RSK-004); or holds privileged or persistent network access to Organization Information Systems; or `[PCI]` is a TPSP that can affect the security of CHD or the CDE; or `[HIPAA]` is a Business Associate or subcontractor Business Associate; or `[SOX]` operates or hosts a Financially Significant System; or provides an AI System classified High under RSK-006; or operates the Ethics Hotline (CMP-006), an outsourced SIEM or managed security service (SEC-012), or the incident response retainer (RES-001) |
| Tier 2 | High | Stores, processes or transmits Confidential data or Personal Data not classified Restricted; or supports a Recovery Tier 2 service; or holds non-privileged access to Organization Information Systems; or `[GDPR]` acts as a Processor; or replacement would take more than 90 days |
| Tier 3 | Moderate | Accesses Internal data only; or supports a Recovery Tier 3 service; or provides software installed on Organization Endpoints or servers without data access |
| Tier 4 | Low | No access to Organization data other than Public, no system access, and no software installed in the Organization's environment |

- **RSK-003.5.2.2** The Head of GRC SHALL confirm each tier assignment on the basis of the information supplied by the Business Sponsor on the intake form, and SHALL re-tier a Third Party within 10 business days of any change in scope, data access or service criticality.
- **RSK-003.5.2.3** Concentration Risk SHALL be assessed whenever a single Third Party, or its parent group, supports more than one Recovery Tier 0 service, or where the Organization has no tested alternative for a vendor Tier 1 Third Party. The result SHALL be recorded in the Risk Register.

### 5.3 Due diligence

- **RSK-003.5.3.1** Due diligence SHALL be completed and the residual third-party Risk rated under RSK-002 before contract signature and before any Organization data or system access is provided.
- **RSK-003.5.3.2** Due diligence SHALL include, at minimum, the activities marked for each tier:

| Activity | Tier 1 | Tier 2 | Tier 3 | Tier 4 |
|---|---|---|---|---|
| Sanctions, adverse-media and financial-viability screening | ☑ | ☑ | ☑ | ☑ |
| TPL-004 Vendor Security Questionnaire | Full | Standard | Core | — |
| Independent assurance report (SOC 2 Type II examination or ISO/IEC 27001 certificate with Statement of Applicability), covering the services in scope, period ending within the last 12 months | Required | Required (or Full TPL-004 if unavailable) | Accepted in place of TPL-004 | — |
| Review of complementary user entity controls in the assurance report | ☑ | ☑ | — | — |
| Penetration test executive summary within the last 12 months | ☑ | ☑ | — | — |
| Business continuity and DR evidence demonstrating RTO and RPO meeting the supported Recovery Tier | ☑ | ☑ (where a Recovery Tier 2 service is supported) | — | — |
| Subprocessor and fourth-party list | ☑ | ☑ | — | — |
| `[GDPR]` `[CPRA]` Privacy review by the CPO or DPO, including transfer mechanism | ☑ (where Personal Data) | ☑ (where Personal Data) | — | — |
| `[PCI]` Attestation of Compliance (AOC) and responsibility matrix | ☑ (TPSP) | — | — | — |
| `[HIPAA]` Review of the Business Associate's HIPAA Security Rule risk analysis summary | ☑ | — | — | — |
| `[SOX]` SOC 1 Type II report for services affecting Financially Significant Systems | ☑ | — | — | — |
| Onsite or virtual assessment by the Organization | MAY, at Head of GRC discretion; required if a Critical or High finding is unresolved | — | — | — |
| Executive sponsor sign-off on residual Risk | ☑ | ☑ | — | — |

- **RSK-003.5.3.3** The Head of GRC SHALL complete the due diligence review within 15 business days of receiving a complete response from the Third Party.
- **RSK-003.5.3.4** Each finding SHALL be scored under RSK-002. A Third Party with an unresolved finding rated Critical SHALL NOT be engaged. A Third Party with an unresolved finding rated High SHALL be engaged only with a remediation commitment in the contract and a Risk Acceptance under RSK-001.
- **RSK-003.5.3.5** Third Parties that will provide AI Systems or AI-enabled features SHALL also be assessed under the model and vendor assessment requirements in RSK-006.
- **RSK-003.5.3.6** Due diligence records SHALL be retained under CMP-004.

### 5.4 Contract requirements

- **RSK-003.5.4.1** The GC SHALL maintain standard contract clauses implementing this section. Contracts with vendor Tier 1, Tier 2 and Tier 3 Third Parties SHALL include the clauses marked below before signature; deviations SHALL be approved by the GC and the Head of GRC and recorded in the Risk Register.

| Clause | Tier 1 | Tier 2 | Tier 3 | Tier 4 |
|---|---|---|---|---|
| Information security obligations no weaker than the suite documents that apply to the service, with reference to the Organization's data classification (SEC-002) | ☑ | ☑ | ☑ | — |
| Confidentiality and permitted-use restrictions | ☑ | ☑ | ☑ | ☑ |
| Right to audit: the Organization or its appointed assessor MAY audit the Third Party's Controls on 30 days' notice, and on 5 business days' notice following a Security Incident affecting Organization data | ☑ | ☑ | — | — |
| Annual delivery of an independent assurance report covering the services in scope | ☑ | ☑ | — | — |
| Security Incident and Personal Data Breach notification to the Organization within 24 hours of discovery, with ongoing cooperation and updates every 24 hours until containment | ☑ | ☑ | — | — |
| Security Incident notification within 72 hours of discovery | — | — | ☑ | — |
| Subprocessor control: prior written notice of at least 30 days of any new Subprocessor or fourth party handling Organization data, with a right to object, and flow-down of equivalent obligations | ☑ | ☑ | — | — |
| Data location: data processed only in locations approved in the contract | ☑ | ☑ | — | — |
| Encryption of Organization data at rest and in transit meeting SEC-006 | ☑ | ☑ | — | — |
| Vulnerability remediation within timeframes no longer than those in SEC-011 for systems processing Organization data | ☑ | ☑ | — | — |
| Business continuity and DR commitments supporting the RTO and RPO of the Recovery Tier served (RSK-004), with test results provided every 12 months | ☑ | Where a Recovery Tier 2 service is supported | — | — |
| Return and certified destruction of Organization data on termination (section 5.7) | ☑ | ☑ | ☑ | — |
| Background screening of Third Party personnel with access to Organization Information Systems or Restricted data, equivalent to the Screening Level of the position under PPL-001 (PPL-001.5.2.12) | ☑ | ☑ | — | — |
| Security awareness training of Third Party personnel with access to Restricted data, equivalent to PPL-002, with Evidence on request (PPL-002.5.8.2) | ☑ | — | — | — |
| Acknowledgement of GOV-004, and any other suite document named in the contract, by personnel with access to Organization Information Systems, before access is granted (GOV-002.5.9.7) | ☑ | ☑ | — | — |
| Enforcement remedies for violations, as listed in CMP-007.5.5.1 | ☑ | ☑ | ☑ | — |
| Cyber insurance coverage | ☑ | ☑ | — | — |
| Termination right for material security breach or failure to remediate a High or Critical finding within the agreed period | ☑ | ☑ | — | — |
| `[GDPR]` Data Processing Agreement meeting GDPR Art. 28(3), including documented instructions, confidentiality of personnel, Art. 32 security, Subprocessor conditions under Art. 28(2) and (4), assistance with Data Subject Requests and DPIAs, deletion or return, and audit cooperation; plus transfer safeguards under GDPR Chapter V per CMP-005 | ☑ (Processors) | ☑ (Processors) | ☑ (Processors) | — |
| `[CPRA]` Service provider or contractor terms meeting Cal. Civ. Code §1798.100(d) and §1798.140 | ☑ | ☑ | ☑ | — |
| `[HIPAA]` Business Associate Agreement meeting 45 CFR §164.504(e) and §164.314(a), executed before any PHI is disclosed | ☑ (Business Associates) | — | — | — |
| `[PCI]` Written agreement under PCI DSS 12.8.2 in which the TPSP acknowledges that it is responsible for the security of account data it possesses, or stores, processes or transmits on behalf of the Organization, or to the extent it could affect the security of the CDE | ☑ (TPSPs) | ☑ (TPSPs) | — | — |
| `[SOX]` Delivery of a SOC 1 Type II report every 12 months covering the financial-reporting period | ☑ (where applicable) | — | — | — |
| Software supply chain clauses (section 5.6) | ☑ (software suppliers) | ☑ (software suppliers) | — | — |

- **RSK-003.5.4.2** `[HIPAA]` [DECISION REQUIRED: HIPAA status of the Organization (SUITE-REGISTER decision #3). Recommended default: Business Associate.] Where the Organization is a Business Associate, it SHALL obtain a subcontractor BAA from each subcontractor that creates, receives, maintains or transmits PHI on its behalf, with breach notification to the Organization in time for the Organization to meet its obligations under RES-003. HIPAA implementation decisions are in CMP-008.
- **RSK-003.5.4.3** `[PCI]` The TPSP list and the responsibility matrix of PCI DSS requirements managed by each TPSP, by the Organization, or shared (PCI DSS 12.8.1, 12.8.5) are maintained under SEC-019.5.10.4 and SEC-019.5.10.6.
- **RSK-003.5.4.4** Contract renewals SHALL be treated as new engagements for the purpose of section 5.4 where the standard clauses have changed since the previous contract.

### 5.5 Ongoing monitoring and reassessment

- **RSK-003.5.5.1** Each Third Party SHALL be reassessed, repeating the due diligence for its tier, at the following frequency: **Tier 1 and Tier 2 every 12 months · Tier 3 every 24 months · Tier 4 at onboarding and contract renewal.**
- **RSK-003.5.5.2** In addition, a Third Party SHALL be reassessed within 30 days of: a Security Incident at the Third Party affecting Organization data or services; a change of ownership, merger or acquisition of the Third Party; a material change in services or data access; a qualified or adverse assurance opinion; or a public disclosure of a Vulnerability or breach affecting the services used.
- **RSK-003.5.5.3** For vendor Tier 1 Third Parties, the Head of GRC SHALL monitor the following on a continuous or at least monthly basis: external security posture signals (for example from an external attack-surface or security-rating service); breach and adverse-media alerts; and financial-distress indicators. Material adverse changes SHALL be scored under RSK-002 within 10 business days.
- **RSK-003.5.5.4** The Business Sponsor SHALL review service performance, open findings and Security Incidents with each vendor Tier 1 Third Party at least quarterly, and with each vendor Tier 2 Third Party at least every 6 months, and SHALL record the review.
- **RSK-003.5.5.5** On receipt of each independent assurance report, the Head of GRC SHALL review exceptions noted by the auditor, scope changes, complementary user entity controls (CUECs) and complementary subservice organization controls (CSOCs) within 30 days, SHALL confirm that the Organization operates the CUECs, and SHALL confirm that each subservice organization performing CSOCs is covered by independent assurance or by the Third Party's own monitoring.
- **RSK-003.5.5.6** Where an assurance report period ends more than 3 months before the Organization's need date, the Head of GRC SHALL obtain a Bridge Letter covering the gap.
- **RSK-003.5.5.7** Third-party findings SHALL be tracked to closure. Third Parties SHALL remediate findings within the following periods, unless the contract states shorter: Critical 30 days; High 60 days; Medium 90 days; Low 180 days. Overdue findings SHALL be escalated by the Head of GRC to the Business Sponsor and recorded in the Risk Register.
- **RSK-003.5.5.8** `[PCI]` Monitoring of each TPSP's PCI DSS compliance status (PCI DSS 12.8.4) is performed under SEC-019.5.10.5.
- **RSK-003.5.5.9** Vendor Tier 1 and Tier 2 Third Parties supporting Recovery Tier 0 or Recovery Tier 1 services SHALL be included in incident response planning (RES-002) and BC/DR exercises (RES-004), with contact details verified at least every 12 months.
- **RSK-003.5.5.10** Third-party access to Organization Information Systems SHALL be provisioned, reviewed and revoked under SEC-003 and, for privileged access, SEC-005.

### 5.6 Software and hardware supply chain

- **RSK-003.5.6.1** Software, firmware, hardware and Cloud Services SHALL be acquired only from sources recorded in the third-party inventory or through the approved package proxy or mirror under SEC-010.5.9.1.
- **RSK-003.5.6.2** Contracts with software suppliers in vendor Tier 1 and Tier 2 SHALL require: provision of an SBOM for delivered software on request, in the format specified in SEC-010.5.8.2; notification of Vulnerabilities affecting delivered software within 5 business days of the supplier's confirmation, and within 24 hours where the Vulnerability is actively exploited; a secure development attestation (for example a self-attestation aligned to the NIST Secure Software Development Framework, SP 800-218); signed releases or published integrity hashes; and a supported-version and end-of-life schedule.
- **RSK-003.5.6.3** The Organization SHALL verify the integrity and authenticity of software and firmware before installation, using signatures or published hashes where provided. Requirements for build-pipeline integrity, dependency management and SBOM generation for Organization-developed software are in SEC-010.
- **RSK-003.5.6.4** Open-source components used in production SHALL be subject to the component approval, licensing and Vulnerability monitoring requirements in SEC-010. Open-source projects are not Third Parties for the purpose of contract clauses, but a Risk Owner SHALL be assigned to each open-source component whose compromise would affect a Recovery Tier 0 service.
- **RSK-003.5.6.5** Hardware for Recovery Tier 0 and Recovery Tier 1 systems and for the `[PCI]` CDE SHALL be purchased from the manufacturer or an authorized reseller, and SHALL be inspected for tampering on receipt.
- **RSK-003.5.6.6** Software or hardware from a supplier subject to a government prohibition applicable to the Organization (for example a sanctions or national-security restriction) SHALL NOT be acquired, and existing use SHALL be reported to the GC within 5 business days of the prohibition being identified.
- **RSK-003.5.6.7** Components that are end-of-life or no longer receiving security updates from the supplier SHALL be recorded in the Risk Register and handled under SEC-001.5.7.4 and SEC-011.

### 5.7 Offboarding

- **RSK-003.5.7.1** The Business Sponsor SHALL notify the Head of Procurement and the Head of GRC at least 30 days before the planned end of a vendor Tier 1 or Tier 2 engagement, and no later than the termination date for all other tiers.
- **RSK-003.5.7.2** Before a vendor Tier 1 or Tier 2 engagement ends, the Business Sponsor SHALL have an exit plan that ensures continuity of any supported Recovery Tier 0, 1 or 2 service. Exit plans for vendor Tier 1 Third Parties SHALL be documented at onboarding and reviewed every 12 months.
- **RSK-003.5.7.3** All Third Party accounts, credentials, keys, network connections and physical access SHALL be revoked no later than the engagement end date, and Secrets shared with the Third Party SHALL be rotated within 5 business days of the end date.
- **RSK-003.5.7.4** The Third Party SHALL return or destroy Organization data within 30 days of the engagement end date, and SHALL provide a written Certificate of Destruction stating the method used. Destruction methods SHALL meet SEC-017.
- **RSK-003.5.7.5** The Head of GRC SHALL record completion of offboarding steps 5.7.3 and 5.7.4 in the third-party inventory within 45 days of the engagement end date, and SHALL record any data not returned or certified destroyed as a Risk.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| ISSC | Approves this Policy; reviews vendor Tier 1 Risk posture at least every 12 months. |
| CISO | Approves Risk Acceptances for Medium third-party Risks; escalates Critical vendor findings. |
| Head of GRC | Owns this Policy; confirms tiers; performs due diligence and reassessment; maintains TPL-004; monitors vendor Tier 1 Third Parties; tracks findings; `[PCI]` maintains TPSP responsibility information and AOCs. |
| Head of Procurement | Maintains the third-party inventory; enforces that no purchase order is issued before due diligence and contracting are complete; reconciles inventory against payments quarterly. |
| GC | Maintains standard clauses; approves contract deviations; advises on government prohibitions. |
| CPO / DPO | `[GDPR]` `[CPRA]` Perform privacy reviews; approve Data Processing Agreements and transfer mechanisms under CMP-005. |
| HIPAA Security Officer / HIPAA Privacy Officer | `[HIPAA]` Confirm BAA execution before PHI disclosure. |
| CFO | `[SOX]` Reviews SOC 1 reports for Third Parties supporting Financially Significant Systems. |
| Business Sponsor (Risk Owner) | Requests and justifies the Third Party; acts as Risk Owner; performs relationship reviews (5.5.4); owns exit plans and offboarding notification. |
| Head of Security Engineering | Supports technical assessment of Tier 1 and Tier 2 Third Parties; verifies software integrity controls. |
| Business Continuity Manager | Confirms Recovery Tier dependencies and reviews Third Party BC/DR evidence. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| RSK-003.7.1 | Vendor tiers | Tier 1 Critical · Tier 2 High · Tier 3 Moderate · Tier 4 Low |
| RSK-003.7.2 | Vendor reassessment | Tier 1 and Tier 2 every 12 months · Tier 3 every 24 months · Tier 4 at onboarding and contract renewal |
| RSK-003.7.3 | Event-driven reassessment | Within 30 days of trigger in 5.5.2 |
| RSK-003.7.4 | Due diligence review turnaround | 15 business days from complete response |
| RSK-003.7.5 | Third Party Security Incident notification (contractual) | Tier 1–2: 24 hours from discovery, updates every 24 hours · Tier 3: 72 hours |
| RSK-003.7.6 | Subprocessor change notice (contractual) | At least 30 days before change, with right to object |
| RSK-003.7.7 | Right-to-audit notice (contractual) | 30 days; 5 business days after a Security Incident |
| RSK-003.7.8 | Assurance report currency | Period ending within the last 12 months; Bridge Letter if gap exceeds 3 months |
| RSK-003.7.9 | Assurance report review | Within 30 days of receipt |
| RSK-003.7.10 | Third Party finding remediation | Critical 30 days · High 60 days · Medium 90 days · Low 180 days |
| RSK-003.7.11 | Vendor Tier 1 external monitoring | Continuous or at least monthly |
| RSK-003.7.12 | Relationship reviews | Tier 1 quarterly · Tier 2 every 6 months |
| RSK-003.7.13 | Inventory reconciliation to payments | Quarterly; unlisted Third Parties tiered within 10 business days |
| RSK-003.7.14 | Supplier Vulnerability notification (contractual) | 5 business days; 24 hours if actively exploited |
| RSK-003.7.15 | Offboarding | Access revoked by end date; shared Secrets rotated within 5 business days; data returned or destroyed within 30 days with certificate |
| RSK-003.7.16 | `[PCI]` TPSP compliance monitoring | AOC obtained at least every 12 months |
| RSK-003.7.17 | Retention of third-party assessments and contracts | As set in CMP-004 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Third Parties in inventory with a confirmed tier | 100% | Quarterly | Head of Procurement |
| Engagements with due diligence completed before contract signature | 100% | Quarterly | Head of GRC |
| Reassessments completed by due date (by tier) | ≥ 95% (Tier 1: 100%) | Quarterly | Head of GRC |
| Tier 1–3 contracts containing all required clauses | 100% | Quarterly (sample) | GC |
| Third Party findings past remediation deadline | 0 Critical; ≤ 5% High | Monthly | Head of GRC |
| `[PCI]` TPSPs with current AOC | 100% | Quarterly | Head of GRC |
| Offboardings with Certificate of Destruction within 30 days | 100% | Quarterly | Head of GRC |
| Shadow IT Third Parties discovered by reconciliation | Trend downward | Quarterly | Head of Procurement |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

No Exception SHALL be granted to: `[HIPAA]` execution of a BAA before PHI disclosure; `[GDPR]` an Art. 28 Data Processing Agreement before Personal Data is processed by a Processor; `[PCI]` the 12.8.2 written acknowledgement; or RSK-003.5.3.4 (no engagement with an unresolved Critical finding).

## 10. Enforcement

Non-compliance is handled under CMP-007.

The Head of Procurement SHALL NOT issue a purchase order, and the CFO SHALL ensure that no invoice is paid, for a Third Party that is not in the third-party inventory with completed due diligence. Third Parties that breach contractual security obligations SHALL be subject to the remedies in their contract, as determined by the GC.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| RSK-003.5.1 – 5.2 | A.5.19, A.5.23 | GV.SC-01, GV.SC-04 | SR-1, SR-2, PM-30 | 15.1, 15.2, 15.3 | CC9.2 | APO10.01, APO10.02 | `[PCI]` 12.8.1 |
| RSK-003.5.3 | A.5.19, A.5.21 | GV.SC-06, GV.SC-07, ID.RA-10 | SR-6, SA-9 | 15.5 | CC9.2 | APO10.03 | `[PCI]` 12.8.3; `[GDPR]` Art. 28(1) |
| RSK-003.5.4 | A.5.20 | GV.SC-05 | SA-4, SA-9, SR-3, SR-8 | 15.4 | CC9.2, C1.1 | APO10.03 | `[GDPR]` Art. 28(3); `[HIPAA]` §164.308(b)(1), §164.314(a), §164.504(e); `[PCI]` 12.8.2, 12.8.5; Cal. Civ. Code §1798.100(d) |
| RSK-003.5.5 | A.5.22 | GV.SC-07, GV.SC-08, GV.SC-09 | SA-9, CA-7, SR-6 | 15.6 | CC9.2, CC4.1 | APO10.05 | `[PCI]` 12.8.4; `[SOX]` §404 |
| RSK-003.5.6 | A.5.21, A.8.30 | GV.SC-09, ID.RA-09 | SR-3, SR-4, SR-5, SR-11, SA-22 | 2.1, 16.4 | CC9.2, CC8.1 | BAI03 | — |
| RSK-003.5.7 | A.5.19, A.5.22 | GV.SC-10 | SA-9, SR-12, PS-7 | 15.7 | CC9.2, C1.2 | APO10.05 | `[GDPR]` Art. 28(3)(g) |

## 12. Related documents

RSK-001, RSK-002, RSK-004, RSK-006, CMP-003, CMP-004, CMP-005, CMP-007, CMP-008, CMP-009, SEC-001, SEC-002, SEC-003, SEC-005, SEC-006, SEC-010, SEC-011, SEC-017, SEC-019, RES-002, RES-003, RES-004, PPL-001, TPL-004, REF-001

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Head of GRC | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
