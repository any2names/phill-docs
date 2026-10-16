# Suite Register

This is the single source of truth for consistency across the policy suite. Update it each time a document is
drafted or revised. Document metadata (owner, approver, tier, priority) is listed in [README.md](README.md).

## A. Suite-wide conventions (binding on all documents)

| Convention | Value |
|---|---|
| Entity reference | Always "the Organization" (defined in GOV-006). No company names, logos, domains, or entity-specific facts in any document |
| Adopter decisions | Written as `[DECISION REQUIRED: <question>. Recommended default: <value>]`. Where a default exists, the document uses it so it reads as complete |
| Conditional clauses | Regulation-specific clauses tagged `[PCI]`, `[HIPAA]`, `[SOX]`, `[GDPR]`, `[CPRA]` (see README "Conditional modules") |
| Requirement numbering | `<DOC-ID>.<section>.<subsection>.<item>`, e.g. `SEC-003.5.2.1` (section 5 = policy statements, section 7 = minimum standards) |
| Time units | "Business day" and "calendar day" as defined in GOV-006; a bare "day" means calendar day; "hours" are clock hours, 24×7 |
| Normative language | SHALL / SHALL NOT / SHOULD / MAY per RFC 2119 / RFC 8174 (uppercase only) |
| Review cycle | Every document reviewed at most every 12 months (PCI DSS 12.1.2), plus the event-triggered reviews defined in GOV-002 |
| Segregation of duties | A document's owner SHALL NOT be its approver |
| Retired IDs | Never reused (GOV-005 is retired) |
| Definitions | Terms are defined only in GOV-006; other documents reference GOV-006 and never redefine a term |
| Single home | Each requirement and value lives in exactly one document (see section C); other documents cite it by ID |
| Framework versions | ISO/IEC 27001:2022 (+Amd 1:2024) & 27002:2022; NIST CSF 2.0; NIST SP 800-53 Rev. 5; CIS Controls v8.1; SOC 2 TSC (2017, revised points of focus 2022); COBIT 2019; ISO 31000:2018; NIST SP 800-30 Rev. 1; ISO/IEC 42001:2023; NIST AI RMF 1.0; PCI DSS v4.0.1; HIPAA Security Rule (45 CFR 164 Subpart C); GDPR; CCPA/CPRA; SOX §§301/302/404 |
| Assurance terminology | "SOC 2 Type II examination" (an attestation report, not a certification) |

## B. Canonical role names

Use these names exactly in every document.

| Group | Roles |
|---|---|
| Governance bodies | Board of Directors · Audit Committee · Chief Executive Officer (CEO) · Information Security Steering Committee (ISSC) |
| Executives | Chief Financial Officer (CFO) · Chief Information Officer (CIO) · Chief Technology Officer (CTO) · Chief Information Security Officer (CISO) · Chief Privacy Officer (CPO) · General Counsel (GC) · Chief Human Resources Officer (CHRO) |
| Statutory designations | Data Protection Officer (DPO) · HIPAA Security Officer · HIPAA Privacy Officer |
| Functional leads | Head of GRC · Head of Security Engineering · SOC Manager · Internal Audit Director · Business Continuity Manager · Head of Facilities · Head of Procurement |
| Generic roles (defined in GOV-006) | Asset Owner · Data Owner · System Owner · Data Custodian · Line Manager · Workforce Member · Third Party |

## C. Value ownership map

Each value is set in exactly one document, its **home document**. The values below are
**pre-set**: the home document SHALL state them exactly as written here. Every other
document cites the home document by ID (e.g. "within the SLA in SEC-011") and SHALL NOT
restate the number. A home document may add further values of its own, which are recorded
in section D when it is drafted.

### C.1 Governance and policy management

| Value | Home | Pre-set value |
|---|---|---|
| All defined terms | GOV-006 | See GOV-006 |
| ISSC composition | GOV-001 | Chair: CISO. Voting: CIO, CTO, CPO, GC, CFO, CHRO, Head of GRC. Non-voting: Internal Audit Director, DPO, HIPAA Security Officer |
| ISSC quorum and cadence | GOV-001 | Quorum = majority of voting members incl. Chair or delegate; meets at least quarterly; extraordinary meeting within 5 business days of a Sev-1 incident |
| CISO reporting line | GOV-001 | Reports to the CEO; reports to the Audit Committee at least quarterly; reports to the Board of Directors at least annually |
| Document approval rule | GOV-002 | As in README "Document hierarchy"; owner ≠ approver |
| Workforce policy attestation | GOV-002 | Before system access is granted at hire, then every 12 months |
| Publication after approval | GOV-002 | Within 10 business days |
| Event-triggered review | GOV-002 | Started within 30 days of: material organizational change, new or changed legal obligation, Sev-1 incident with a policy-related root cause, or audit finding against the document |
| Metrics reporting cadence | GOV-003 | Operational metrics monthly to ISSC; KRI dashboard quarterly to Audit Committee; annual program report to Board of Directors |

### C.2 Risk

| Value | Home | Pre-set value |
|---|---|---|
| Risk scoring | RSK-002 | 5×5 likelihood × impact, score 1–25 |
| Risk levels | RSK-002 | Low 1–4 · Medium 5–9 · High 10–16 · Critical 17–25 |
| Enterprise risk assessment | RSK-002 | At least every 12 months, plus triggers (significant change, new Tier 1 vendor, Sev-1/Sev-2 incident, new legal obligation, merger or acquisition) |
| Risk treatment plan deadline | RSK-002 | Critical 30 days · High 60 days · Medium 90 days · Low next annual assessment |
| Risk acceptance authority | RSK-001 | Low: Risk Owner · Medium: CISO · High: ISSC · Critical: CEO, with Audit Committee notified within 10 business days |
| Risk acceptance validity | RSK-001 | Max 12 months; Critical max 90 days |
| Risk register review | RSK-001 | ISSC reviews quarterly |
| Risk appetite | RSK-001 | Conservative (adopter decision #1): no residual risk above Medium outside an approved acceptance |
| Vendor tiers | RSK-003 | Tier 1 Critical · Tier 2 High · Tier 3 Moderate · Tier 4 Low |
| Vendor reassessment | RSK-003 | Tier 1 and Tier 2 every 12 months · Tier 3 every 24 months · Tier 4 at onboarding and contract renewal |
| Recovery tiers | RSK-004 | Tier 0 Mission-critical: RTO 4 h / RPO 15 min · Tier 1 Critical: RTO 24 h / RPO 4 h · Tier 2 Important: RTO 72 h / RPO 24 h · Tier 3 Deferrable: RTO 7 days / RPO 7 days |
| BIA refresh | RSK-004 | Every 12 months and on significant change |

### C.3 Compliance and records

| Value | Home | Pre-set value |
|---|---|---|
| Exception maximum duration | CMP-003 | 12 months; 90 days where residual risk is Critical |
| Exception renewals | CMP-003 | Max 2 consecutive renewals, then remediate or obtain risk acceptance per RSK-001 |
| Exception decision time | CMP-003 | Within 10 business days of a complete request |
| Exception approval authority | CMP-003 | Same as risk acceptance authority in RSK-001, by residual risk level |
| Obligations register review | CMP-001 | Quarterly; new or changed obligation assessed within 30 days of publication |
| Policy documents and prior versions | CMP-004 | 7 years after superseded |
| Control evidence, audit workpapers, access reviews | CMP-004 | 7 years |
| Security logs | CMP-004 | 12 months minimum, of which the most recent 90 days immediately available; `[HIPAA]` logs from ePHI systems 6 years |
| Incident records and post-incident reviews | CMP-004 | 7 years after closure |
| Risk register entries, risk acceptances, exceptions | CMP-004 | 7 years after closure or expiry |
| Training records and policy acknowledgements | CMP-004 | Employment or engagement + 7 years |
| Third-party assessments and contracts | CMP-004 | Contract term + 7 years |
| Data subject request records | CMP-004 | 3 years after closure |
| Whistleblower reports | CMP-004 | 7 years after closure |
| Backups | CMP-004 | Daily 35 days · monthly 13 months · `[SOX]` year-end backups of financially significant systems 7 years |
| CCTV recordings / visitor logs | CMP-004 | 90 days / 12 months |
| Personal data | CMP-004 | Per the purpose in the ROPA; deleted or anonymized within 30 days after the purpose ends, unless under legal hold |
| `[PCI]` Cardholder data | CMP-004 | Only as long as the documented business need; purge process run at least every 3 months; sensitive authentication data never stored after authorization |
| DSR response deadlines `[GDPR]` `[CPRA]` | CMP-010 | GDPR: 1 month, extendable by 2 months · CPRA: acknowledge within 10 business days, respond within 45 days, extendable by 45 days |

### C.4 Security controls

| Value | Home | Pre-set value |
|---|---|---|
| Classification levels | SEC-002 | Public · Internal · Confidential · Restricted (Restricted includes PHI, cardholder data, authentication secrets, special-category and sensitive personal information, government identifiers) |
| User access review | SEC-003 | Quarterly for systems holding Restricted data and `[SOX]` financially significant systems; every 6 months for all others |
| Access revocation on separation | SEC-003 | Within 4 hours of the separation time; involuntary separations at or before notification |
| Access change on role change | SEC-003 | Within 5 business days |
| Inactive accounts | SEC-003 | Disabled after 90 days of inactivity |
| Privileged access review | SEC-005 | Quarterly |
| Privileged elevation (just-in-time) | SEC-005 | Max 8 hours per grant |
| Break-glass accounts | SEC-005 | Tested quarterly; every use reviewed within 1 business day |
| Password length | SEC-004 | Min 12 characters for user accounts with MFA; 15 without MFA (exception only); 32 random characters for service accounts |
| Password rotation | SEC-004 | No forced periodic rotation where MFA is enforced; change on suspected compromise; `[PCI]` 90 days where a password is the only factor |
| MFA | SEC-004 | Required for all remote access, all privileged access, all CDE access, and all SSO applications; phishing-resistant MFA for privileged access |
| Account lockout | SEC-004 | After max 10 failed attempts, for min 30 minutes or until identity is verified |
| Idle session timeout | SEC-004 | 15 minutes |
| Encryption minimums | SEC-006 | AES-256 at rest (AES-128-GCM minimum); TLS 1.2 minimum, TLS 1.3 preferred; RSA ≥ 3072 bits; ECC ≥ P-256; SHA-256 or stronger. Prohibited: SSL, TLS < 1.2, DES, 3DES, RC4, MD5, SHA-1 for signatures |
| Key cryptoperiod | SEC-006 | Data-encryption keys 12 months; key-encryption keys 24 months; immediate rotation on suspected compromise |
| TLS certificate lifetime | SEC-006 | No longer than the CA/Browser Forum maximum in force (200 days from 15 March 2026) |
| Vulnerability remediation SLA | SEC-011 | Critical (CVSS 9.0–10.0) 15 days; vulnerabilities in the CISA KEV catalog on internet-facing assets 7 days · High 30 days · Medium 90 days · Low 180 days |
| Vulnerability scanning | SEC-011 | Internal authenticated weekly; external monthly; `[PCI]` ASV external scan every 3 months and after significant change |
| Penetration testing | SEC-011 | External and internal every 12 months and after significant change; `[PCI]` segmentation testing every 12 months (6 months for service providers) |
| Alert triage SLA | SEC-012 | Critical 15 minutes (24×7) · High 1 hour · Medium 8 business hours · Low 5 business days |
| Change classes | SEC-013 | Standard (pre-approved) · Normal (CAB approval) · Emergency (retrospective approval within 2 business days) |
| Backup frequency | SEC-018 | Tier 0 continuous replication or ≤ 15 min · Tier 1 every 4 h · Tier 2 daily · Tier 3 weekly (matches RSK-004 RPO) |
| Restore testing | SEC-018 | Tier 0 and Tier 1 quarterly · Tier 2 and Tier 3 every 12 months |

### C.5 Resilience and people

| Value | Home | Pre-set value |
|---|---|---|
| Incident severity levels | RES-002 | Sev-1 Critical · Sev-2 High · Sev-3 Medium · Sev-4 Low |
| Incident response SLAs | RES-002 | Sev-1: incident commander within 15 min, executive notification within 1 h, updates hourly · Sev-2: commander within 1 h, updates every 4 h · Sev-3: within 1 business day · Sev-4: within 5 business days |
| Post-incident review | RES-002 | Required for Sev-1 and Sev-2, completed within 10 business days of closure |
| IR plan testing | RES-002 | Tabletop or functional exercise every 12 months |
| Internal legal escalation | RES-003 | GC and CPO notified within 24 hours of a suspected personal-data breach |
| `[GDPR]` notification | RES-003 | Supervisory authority within 72 hours of awareness; data subjects without undue delay where risk is high; as processor, notify controller within 24 hours |
| `[HIPAA]` notification | RES-003 | Individuals within 60 days of discovery; HHS concurrently if ≥ 500 individuals, otherwise within 60 days after calendar-year end; media if > 500 residents of a state or jurisdiction; as business associate, notify covered entity within 10 business days (or sooner by contract) |
| `[PCI]` notification | RES-003 | Acquirer and payment brands per brand rules, internal target within 24 hours of confirmed compromise |
| `[SOX]` public disclosure | RES-003 | Form 8-K Item 1.05 within 4 business days of determining an incident is material |
| US state breach laws `[CPRA]` | RES-003 | Internal target 30 days from discovery, or the shortest applicable statutory deadline if shorter |
| BC/DR exercise | RES-004 | BC exercise every 12 months; DR test of Tier 0 and Tier 1 every 12 months |
| Pre-employment screening | PPL-001 | Completed before access to Confidential or Restricted data; rescreening every 3 years for privileged and CDE roles, where lawful |
| Asset return on separation | PPL-001 | Within 5 business days |
| Training at hire | PPL-002 | Within 30 days of start, and before access to Restricted data |
| Annual training | PPL-002 | Every 12 months, completed within 30 days of assignment |
| Phishing simulation | PPL-002 | At least quarterly |
| Role-based training | PPL-002 | Every 12 months for developers, privileged users, incident responders, and staff handling PHI or cardholder data |

## D. Document status

Key values are the values each document sets beyond its pre-set values in section C; long tables are cited by section. "bd" = business days.

| ID | Title | Owner | Status | File | Key values defined |
|---|---|---|---|---|---|
| CMP-001 | Compliance Management Policy | Head of GRC | Drafted | [CMP/CMP-001-compliance-management-policy.md](CMP/CMP-001-compliance-management-policy.md) | Regulatory scan monthly; GC applicability decision 10 bd; calendar reminders 90/30/7 days; SOC 2 period 12 months (first 6); management response to findings within 30 days |
| CMP-002 | Internal Audit & Control Testing Policy | Internal Audit Director | Drafted | [CMP/CMP-002-internal-audit-and-control-testing-policy.md](CMP/CMP-002-internal-audit-and-control-testing-policy.md) | Audit coverage (7.8); sample sizes (5.6.1); remediation: Critical Deficiency 60 · Significant Deficiency 90 · Deficiency 180 days · Observation 12 months; `[SOX]` per CMP-009 |
| CMP-003 | Policy Exception & Waiver Policy | Head of GRC | Drafted | [CMP/CMP-003-policy-exception-and-waiver-policy.md](CMP/CMP-003-policy-exception-and-waiver-policy.md) | Completeness check 3 bd; Compensating Control Evidence quarterly (monthly High/Critical); emergency Exception max 10 bd; KEV Exceptions need CISO (5.4.9); register reviewed monthly |
| CMP-004 | Evidence Management & Records Retention Policy | Head of GRC | Drafted | [CMP/CMP-004-evidence-management-and-records-retention-policy.md](CMP/CMP-004-evidence-management-and-records-retention-policy.md) | Retention schedule rows R-14–R-27 (5.2.1); disposal within 30 days of end of retention; Legal Hold notice 1 bd; Evidence produced within 2 bd; leaver mailbox 90 days (decision) |
| CMP-005 | Data Privacy & Protection Policy | CPO | Drafted | [CMP/CMP-005-data-privacy-and-protection-policy.md](CMP/CMP-005-data-privacy-and-protection-policy.md) | Consent withdrawal within 15 bd; ROPA updated within 30 days; DPIA review every 24 months; TIA every 24 months; Processor deletion certificate within 30 days |
| CMP-006 | Whistleblower & Security Concern Reporting Policy | GC | Drafted | [CMP/CMP-006-whistleblower-and-security-concern-reporting-policy.md](CMP/CMP-006-whistleblower-and-security-concern-reporting-policy.md) | Acknowledgement within 7 days; triage 2 bd; `[SOX]` Category A to Audit Committee Chair within 5 bd; investigation target 90 days; feedback within 3 months; channels tested every 6 months |
| CMP-007 | Enforcement & Disciplinary Policy | CHRO | Drafted | [CMP/CMP-007-enforcement-and-disciplinary-policy.md](CMP/CMP-007-enforcement-and-disciplinary-policy.md) | Violation categories 1–4 and Sanctions S1–S4; look-back 12/24/36 months; response window ≥ 5 bd; decision within 10 bd; appeal 10 bd, decided within 15 bd |
| CMP-008 | HIPAA Security Rule Implementation Standard | HIPAA Security Officer | Drafted | [CMP/CMP-008-hipaa-security-rule-implementation-standard.md](CMP/CMP-008-hipaa-security-rule-implementation-standard.md) | HIPAA implementation matrix (5.6–5.9); ePHI inventory review every 6 months; risk analysis updates within 30 days; evaluation every 12 months and within 90 days of change |
| CMP-009 | SOX IT General Controls Standard | Head of GRC | Drafted | [CMP/CMP-009-sox-it-general-controls-standard.md](CMP/CMP-009-sox-it-general-controls-standard.md) | ITGC Key Controls (5.4–5.9); scoping within 60 days of FY start; samples (5.10.3); sub-certification 10 bd after quarter-end; deficiency report 2 bd; remediation plan 30 days |
| CMP-010 | Data Subject Request Procedure | DPO | Drafted | [CMP/CMP-010-data-subject-request-procedure.md](CMP/CMP-010-data-subject-request-procedure.md) | Logging 1 bd; verification tiers V0–V2; search tasks 3 bd, completed 10 bd; Processor forwarding 2 bd; `[CPRA]` opt-out/limit within 15 bd; intake channels tested every 3 months |
| GOV-001 | Security Governance & Organization Policy | CISO | Drafted | [GOV/GOV-001-security-governance-and-organization-policy.md](GOV/GOV-001-security-governance-and-organization-policy.md) | ISSC Vice-Chair GC; papers 5 bd before meeting, minutes within 10 bd; recusal rule (5.3.9); SoD matrix SOD-01–SOD-18; role combinations (5.8); key-role vacancy > 90 days to Audit Committee |
| GOV-002 | Policy Management Policy | Head of GRC | Drafted | [GOV/GOV-002-policy-management-policy.md](GOV/GOV-002-policy-management-policy.md) | Consultation ≥ 10 bd; review reminder 60 days; overdue review to ISSC > 30 days, AC > 90 days; re-attestation within 30 days of a Material Change; attestation escalation 1/15/30 days |
| GOV-003 | Security Metrics & Reporting Policy | CISO | Drafted | [GOV/GOV-003-security-metrics-and-reporting-policy.md](GOV/GOV-003-security-metrics-and-reporting-policy.md) | KPI-01–KPI-28 and KRI-01–KRI-18 with thresholds (section 5.3); data due 5 bd after period end; ISSC report 10 bd after month end; Board report within 90 days of FYE |
| GOV-004 | Acceptable Use Policy (absorbs GOV-005) | CISO | Drafted | [GOV/GOV-004-acceptable-use-policy.md](GOV/GOV-004-acceptable-use-policy.md) | Clear desk when unattended > 30 min; personal storage ≤ 1 GB; conflict-of-interest disclosure and decision within 10 bd; post-Separation confidentiality (decision) |
| GOV-005 | Code of Conduct, Information Security Addendum | — | Retired | — | — |
| GOV-006 | Glossary & Definitions | Head of GRC | Drafted | [GOV/GOV-006-glossary-and-definitions.md](GOV/GOV-006-glossary-and-definitions.md) | All defined terms (section 5.3) and acronyms (5.4); submitted terms added within 10 bd |
| ISP-000 | Information Security Program Charter | CISO | Drafted | [ISP/ISP-000-information-security-program-charter.md](ISP/ISP-000-information-security-program-charter.md) | Program objectives O1–O6; CISO emergency isolation reported to CEO within 24 h; ISSC management review every 12 months; Audit Committee reports oversight to the Board every 12 months |
| PPL-001 | Human Resources Security Policy | CHRO | Drafted | [PPL/PPL-001-human-resources-security-policy.md](PPL/PPL-001-human-resources-security-policy.md) | Standard/Enhanced Screening Levels (5.2); 5-year employment history; HRIS record ≥ 2 bd before start; mover notice 1 bd; non-employee term ≤ 12 months; leave > 30 days notified 1 bd |
| PPL-002 | Security Awareness & Training Policy | CISO | Drafted | [PPL/PPL-002-security-awareness-and-training-policy.md](PPL/PPL-002-security-awareness-and-training-policy.md) | Pass mark 80% (3 attempts); role-based training within 30 days of assignment; remedial training 14 days after 3rd phishing failure; overdue escalation 1/15/30 days |
| REF-001 | Control Mapping Matrix | Head of GRC | Drafted | [REF/REF-001-control-mapping-matrix.md](REF/REF-001-control-mapping-matrix.md) | 501 rows; 67 Key Controls (KC-01–KC-67); reverse views for ISO Annex A (93/93 covered), SOC 2, CSF 2.0, PCI, HIPAA, SOX |
| REF-002 | Master RACI Matrix | Head of GRC | Drafted | [REF/REF-002-master-raci-matrix.md](REF/REF-002-master-raci-matrix.md) | 117 activities, one A each; 27 role columns; role-to-document ownership and SoD check (0 violations) |
| REF-003 | Gap Analysis & Implementation Roadmap | CISO | Drafted | [REF/REF-003-gap-analysis-and-implementation-roadmap.md](REF/REF-003-gap-analysis-and-implementation-roadmap.md) | 86+ self-assessment rows; Phases 0–5 with entry/exit criteria; reviewed quarterly |
| RES-001 | Incident Response Policy | CISO | Drafted | [RES/RES-001-incident-response-policy.md](RES/RES-001-incident-response-policy.md) | Report within 1 h; ≥ 2 on-call Incident Commanders; Tier 0/1 shutdown retrospective approval 1 h; retainer remote 4 h / on-site 48 h; ransom payment CEO only |
| RES-002 | Incident Response Plan | SOC Manager | Drafted | [RES/RES-002-incident-response-plan.md](RES/RES-002-incident-response-plan.md) | Severity matrix (5.2); CISO notified 30 min / 2 h; containment strategy 2 h / 8 h; IC shift ≤ 12 h; playbooks PB-01–PB-11 reviewed every 12 months; Audit Committee Chair Sev-1 24 h |
| RES-003 | Breach Notification Standard | CPO | Drafted | [RES/RES-003-breach-notification-standard.md](RES/RES-003-breach-notification-standard.md) | Determination group within 24 h; `[PCI]` escalation 4 h; `[SOX]` materiality group within 48 h; insurer and customer notice 72 h (decision); identity protection 24 months |
| RES-004 | Business Continuity Policy | Business Continuity Manager | Drafted | [RES/RES-004-business-continuity-policy.md](RES/RES-004-business-continuity-policy.md) | CMT chaired by CEO, convenes within 1 h; BCP for every Tier 0–2 process; exercises Tier 0–1 12 months, Tier 2 24 months; after-action report 30 days; contact tests 6 months |
| RES-005 | Disaster Recovery Plan | CIO | Drafted | [RES/RES-005-disaster-recovery-plan.md](RES/RES-005-disaster-recovery-plan.md) | Disaster declared at 50% of RTO; impact assessment 30 min / 1 h; failback plan 10 bd, failback within 90 days; failed test retested within 90 days; destructive tabletop 12 months |
| RSK-001 | Risk Management Policy | Head of GRC | Drafted | [RSK/RSK-001-risk-management-policy.md](RSK/RSK-001-risk-management-policy.md) | Risk categories C1–C9 with appetite and tolerance (5.3.2); review: Critical/High monthly, Medium quarterly, Low 12 months; Critical to CISO within 1 bd; acceptance expiry notice 30 days |
| RSK-002 | Risk Assessment Standard | Head of GRC | Drafted | [RSK/RSK-002-risk-assessment-standard.md](RSK/RSK-002-risk-assessment-standard.md) | Likelihood and impact scales (5.2–5.3); triggered assessment within 30 days; system reassessment 12/24 months; enterprise report to ISSC within 30 days; `[PCI]` TRAs (5.8) |
| RSK-003 | Third-Party & Supply Chain Risk Management Policy | Head of GRC | Drafted | [RSK/RSK-003-third-party-and-supply-chain-risk-management-policy.md](RSK/RSK-003-third-party-and-supply-chain-risk-management-policy.md) | Tiering criteria (5.2.1); due diligence 15 bd; vendor incident notice Tier 1–2 24 h, Tier 3 72 h; vendor findings 30/60/90/180 days; data return 30 days; offboarding recorded 45 days |
| RSK-004 | Business Impact Analysis Standard | Business Continuity Manager | Drafted | [RSK/RSK-004-business-impact-analysis-standard.md](RSK/RSK-004-business-impact-analysis-standard.md) | MTPD Tier 0 24 h · Tier 1 72 h · Tier 2 7 days · Tier 3 30 days; impact points 1 h–30 days; owner validation 10 bd; BIA results to ISSC within 30 days |
| RSK-005 | Threat Intelligence & Threat Modeling Standard | SOC Manager | Drafted | [RSK/RSK-005-threat-intelligence-and-threat-modeling-standard.md](RSK/RSK-005-threat-intelligence-and-threat-modeling-standard.md) | PIRs reviewed every 12 months; ATT&CK list every 6 months; indicators deployed within 24 h, expire 90 days; ≥ 1 hunt per quarter; validated detection coverage ≥ 80% |
| RSK-006 | AI & Emerging Technology Risk Policy | CISO | Drafted | [RSK/RSK-006-ai-and-emerging-technology-risk-policy.md](RSK/RSK-006-ai-and-emerging-technology-risk-policy.md) | AI Risk Classes Prohibited/High/Limited/Minimal; tool list reviewed every 6 months; vendor retention ≤ 30 days; High-class monitoring monthly; failed High system withdrawn within 5 bd |
| SEC-001 | Asset Management Policy | CIO | Drafted | [SEC/SEC-001-asset-management-policy.md](SEC/SEC-001-asset-management-policy.md) | Discovery at least daily; inventory updated 1/5 bd; unknown assets triaged 5 bd (1 bd regulated); reconciliation monthly/quarterly; Asset Owner verification 12 months (6 regulated) |
| SEC-002 | Data Classification & Handling Policy | CISO | Drafted | [SEC/SEC-002-data-classification-and-handling-policy.md](SEC/SEC-002-data-classification-and-handling-policy.md) | External sharing links expire within 30 days; DLP coverage 100%; discovery scans quarterly; misplaced Restricted data remediated 10 bd; aggregated Personal Data Restricted > 10,000 (decision) |
| SEC-003 | Identity & Access Management Policy | CISO | Drafted | [SEC/SEC-003-identity-and-access-management-policy.md](SEC/SEC-003-identity-and-access-management-policy.md) | Leaver accounts deleted within 90 days; Access Reviews completed 30 days, findings 5 bd; Third-Party accounts max 12 months; enablement ≤ 3 bd before start; orphans disabled 1 bd |
| SEC-004 | Password & Authentication Standard | Head of Security Engineering | Drafted | [SEC/SEC-004-password-and-authentication-standard.md](SEC/SEC-004-password-and-authentication-standard.md) | IdP session ≤ 12 h; push MFA lock after 3 prompts; remember-device ≤ 30 days; hashing parameters (5.5); access tokens ≤ 60 min; API keys rotated every 12 months |
| SEC-005 | Privileged Access Management Standard | Head of Security Engineering | Drafted | [SEC/SEC-005-privileged-access-management-standard.md](SEC/SEC-005-privileged-access-management-standard.md) | Vaulted credentials rotated every 90 days; ≤ 5 JIT-eligible top admins; session review weekly; 2 Break-glass Accounts per platform; shared Secrets rotated 5 bd after leaver (7.16) |
| SEC-006 | Cryptography & Key Management Policy | Head of Security Engineering | Drafted | [SEC/SEC-006-cryptography-and-key-management-policy.md](SEC/SEC-006-cryptography-and-key-management-policy.md) | Other cryptoperiods (7.3, incl. DKIM 12 months); private-CA certificate lifetimes; compromised key revoked 24 h, replaced 72 h; FIPS 140-3 levels; PQC inventory +12 months |
| SEC-007 | Network Security Policy | Head of Security Engineering | Drafted | [SEC/SEC-007-network-security-policy.md](SEC/SEC-007-network-security-policy.md) | Trust Zones (5.1); rule review every 6 months; temporary rules ≤ 90 days; diagrams updated within 30 days; exposure scan daily; DDoS on-demand within 15 min |
| SEC-008 | Endpoint & Mobile Device Security Policy (incl. BYOD) | CIO | Drafted | [SEC/SEC-008-endpoint-and-mobile-device-security-policy.md](SEC/SEC-008-endpoint-and-mobile-device-security-policy.md) | No check-in 14 days non-compliant, 30 days lost; passcode ≥ 6 digits, wipe after 10 attempts; OS N-1; remote lock/wipe within 1 h; application control (5.2.9) |
| SEC-009 | Cloud Security Policy | CTO | Drafted | [SEC/SEC-009-cloud-security-policy.md](SEC/SEC-009-cloud-security-policy.md) | Shared responsibility review 12 months; CSPM onboarding 24 h, daily assessment; drift reconciled 5 bd; images rebuilt every 30 days; pre-signed URLs 7 days / 24 h |
| SEC-010 | Secure Software Development Lifecycle Policy | CTO | Drafted | [SEC/SEC-010-secure-software-development-lifecycle-policy.md](SEC/SEC-010-secure-software-development-lifecycle-policy.md) | ASVS levels by classification (7.1); DAST every 30 days; exposed Secret revoked 24 h (4 h if public); SLSA L2, L3 target; SBOM SPDX 2.3+/CycloneDX 1.5+; license categories (7.10) |
| SEC-011 | Vulnerability & Patch Management Policy | Head of Security Engineering | Drafted | [SEC/SEC-011-vulnerability-and-patch-management-policy.md](SEC/SEC-011-vulnerability-and-patch-management-policy.md) | CVSS bands (7.18); EPSS ≥ 0.10 raises severity; Emergency Vulnerability mitigated 72 h; scanner coverage ≥ 98%; monthly patch cycle; VDP acknowledge 3 bd, disclose 90 days |
| SEC-012 | Logging & Monitoring Policy | SOC Manager | Drafted | [SEC/SEC-012-logging-and-monitoring-policy.md](SEC/SEC-012-logging-and-monitoring-policy.md) | SOC 24×7×365; SIEM latency 5/60 min; clock drift ≤ 1 s; log silence alerts 60 min / 24 h; use cases tested every 12 months; Log Source table (5.2.1); SIEM Recovery Tier ≥ 1 |
| SEC-013 | Change & Configuration Management Policy | CIO | Drafted | [SEC/SEC-013-change-and-configuration-management-policy.md](SEC/SEC-013-change-and-configuration-management-policy.md) | Emergency Change recorded 1 bd; CAB weekly; approval valid 30 days; post-implementation review 5 bd; Change Risk Rating (5.3.1); drift daily/weekly, fixed 30 days; capacity alert 80%, forecast every 12 months |
| SEC-014 | Email & Communications Security Policy | CIO | Drafted | [SEC/SEC-014-email-and-communications-security-policy.md](SEC/SEC-014-email-and-communications-security-policy.md) | SPF -all, ≤ 10 lookups; DMARC staged to p=reject; aggregate reports weekly; lookalike takedown 2 bd; malicious mail removed within 60 min; guest accounts expire 90 days |
| SEC-015 | Remote Work & Travel Security Policy | CISO | Drafted | [SEC/SEC-015-remote-work-and-travel-security-policy.md](SEC/SEC-015-remote-work-and-travel-security-policy.md) | Home network rules when remote > 5 days/month; travel notice ≥ 10 bd; Loaner Device for High-risk Jurisdictions, returned 2 bd; credentials reset 1 bd after high-risk travel |
| SEC-016 | Physical & Environmental Security Policy | Head of Facilities | Drafted | [SEC/SEC-016-physical-and-environmental-security-policy.md](SEC/SEC-016-physical-and-environmental-security-policy.md) | Security Zones 0–3; Zone 3 review quarterly, Zone 2 every 6 months; lost badge off within 1 h; UPS ≥ 15 min, fuel ≥ 24 h; environmental test schedule (5.11) |
| SEC-017 | Media Sanitization & Secure Disposal Policy | CIO | Drafted | [SEC/SEC-017-media-sanitization-and-secure-disposal-policy.md](SEC/SEC-017-media-sanitization-and-secure-disposal-policy.md) | Media held ≤ 30 days; Certificates of Destruction within 30 days; vendor destruction 10 bd; shredding DIN 66399 P-4 (P-5 Restricted); SSD particles ≤ 2 mm |
| SEC-018 | Backup Policy | CIO | Drafted | [SEC/SEC-018-backup-policy.md](SEC/SEC-018-backup-policy.md) | Tier 0 point-in-time daily; full Backup weekly (Tier 0–2); 3-2-1-1-0 rule; off-site ≥ 100 km; Immutable Backup lock = CMP-004 period; per-system restore test 12/24 months |
| SEC-019 | Cardholder Data Environment Standard | Head of Security Engineering | Drafted | [SEC/SEC-019-cardholder-data-environment-standard.md](SEC/SEC-019-cardholder-data-environment-standard.md) | Scope update within 30 days of Significant Change; PAN discovery every 3 months; Payment Page tamper check every 24 h; POI inspection table (5.9.3); failed segmentation test Sev-2 |
| TPL-001 | Risk Register Template | Head of GRC | Drafted | [TPL/TPL-001-risk-register-template.md](TPL/TPL-001-risk-register-template.md) | Risk register fields; scoring per RSK-002.7.1–7.2 |
| TPL-002 | Risk Acceptance Form | Head of GRC | Drafted | [TPL/TPL-002-risk-acceptance-form.md](TPL/TPL-002-risk-acceptance-form.md) | Head of GRC validates the form within 5 bd |
| TPL-003 | Policy Exception Request Form | Head of GRC | Drafted | [TPL/TPL-003-policy-exception-request-form.md](TPL/TPL-003-policy-exception-request-form.md) | Exception request fields; scoring per RSK-002 |
| TPL-004 | Vendor Security Questionnaire | Head of GRC | Drafted | [TPL/TPL-004-vendor-security-questionnaire.md](TPL/TPL-004-vendor-security-questionnaire.md) | Core/Standard/Full question sets by vendor tier; Yes 2 / Partial 1 / No 0; rating bands 90/75/60%; blocking questions; responses due within 15 bd |
| TPL-005 | Data Protection Impact Assessment Template | DPO | Drafted | [TPL/TPL-005-data-protection-impact-assessment-template.md](TPL/TPL-005-data-protection-impact-assessment-template.md) | Full DPIA where ≥ 2 WP248 criteria apply; High/Critical residual risk triggers Art. 36 consultation; Medium+ to Risk Register |
| TPL-006 | Incident Report Template | SOC Manager | Drafted | [TPL/TPL-006-incident-report-template.md](TPL/TPL-006-incident-report-template.md) | Times in UTC; form classified Confidential or higher; CISO signs off Sev-1/Sev-2 closure |
| TPL-007 | Post-Incident Review Template | SOC Manager | Drafted | [TPL/TPL-007-post-incident-review-template.md](TPL/TPL-007-post-incident-review-template.md) | Corrective actions High 30 · Medium 90 · Low 180 days (decision); CISO signs off Sev-1/Sev-2 reviews |
| TPL-008 | Access Review Template | Head of Security Engineering | Drafted | [TPL/TPL-008-access-review-template.md](TPL/TPL-008-access-review-template.md) | Access Review form fields; values per SEC-003 and SEC-005 |
| TPL-009 | Policy Acknowledgement Form | Head of GRC | Drafted | [TPL/TPL-009-policy-acknowledgement-form.md](TPL/TPL-009-policy-acknowledgement-form.md) | Acknowledgement points per GOV-002.7.2 and 7.9; Attestation Set sections |
| TPL-010 | Record of Processing Activities Template | DPO | Drafted | [TPL/TPL-010-record-of-processing-activities-template.md](TPL/TPL-010-record-of-processing-activities-template.md) | ROPA updated within 10 bd of change; full review every 12 months; regulator export within 2 bd |

## E. Adopter decisions

These are left for each adopting organization to resolve. The documents carry them as
`[DECISION REQUIRED]` placeholders with the recommended default shown.

| # | Decision | Recommended default | Affects |
|---|---|---|---|
| 1 | Risk appetite | **Conservative** for organizations handling regulated data | ISP-000, RSK-001 |
| 2 | SOC 2 Trust Services Criteria in scope | Security + Availability + Confidentiality; Privacy optional because CMP-005 covers GDPR/CPRA directly | ISP-000, CMP-001, REF-001 |
| 3 | HIPAA status `[HIPAA]` | Business associate (the more common case for service providers) | CMP-001, CMP-005, CMP-008, RES-003, RSK-003 |
| 4 | PCI DSS validation level `[PCI]` | Report on Compliance (ROC) by a QSA; SAQ for lower-volume merchants | SEC-019, CMP-001, CMP-002 |
| 5 | HIPAA Security Officer designation `[HIPAA]` | The CISO; CMP-008 approval then moves to the ISSC | GOV-001, CMP-008 |
| 6 | CISO reporting line | Reports to the CEO, for independence from IT operations | GOV-001 |
| 7 | Regions in scope | United States and EU/EEA; add UK GDPR and other local laws as needed | CMP-001, CMP-005, RES-003 |
| 8 | DPO appointment `[GDPR]` | Required where GDPR Art. 37(1) applies (e.g. large-scale special-category data) | GOV-001, CMP-005 |
| 9 | Legal entities excluded from the program | None excluded | ISP-000 |
| 10 | Accepted CISO certifications | CISSP, CISM or an equivalent approved by the CEO | GOV-001 |
| 11 | ISSC Vice-Chair | The GC | GOV-001 |
| 12 | HIPAA Privacy Officer designation `[HIPAA]` | The CPO | GOV-001 |
| 13 | Timing of the annual Board of Directors report | Within 90 days after fiscal year end | GOV-003 |
| 14 | Duration of post-Separation confidentiality | Indefinite for Restricted information and trade secrets; 5 years for other Confidential and Internal information | GOV-004 |
| 15 | Training languages | Every primary working language of at least 50 Workforce Members | PPL-002 |
| 16 | Access consequence of overdue training | Suspend Restricted-data and Privileged Account access at 30 days overdue | PPL-002 |
| 17 | Financial impact thresholds | 0.1 / 0.5 / 1 / 5% of annual consolidated revenue, or CFO-approved currency amounts | RSK-002 |
| 18 | EU AI Act applicability | Applies as a deployer; provider obligations only if the Organization places its own AI System on the market | RSK-006 |
| 19 | Length of the first SOC 2 Type II period | 6 months, then contiguous 12-month periods | CMP-001 |
| 20 | Administrative reporting line of the Internal Audit Director | The CEO (functional line to the Audit Committee) | CMP-002 |
| 21 | Retention of screening results for candidates not hired | 12 months from decision | CMP-004 |
| 22 | Retention of a former Workforce Member's mailbox and files | 90 days after Separation | CMP-004, PPL-001, SEC-003 |
| 23 | Minimum Subprocessor change notice in Data Processing Agreements `[GDPR]` | 30 days | CMP-005 |
| 24 | Lead Supervisory Authority `[GDPR]` | Authority of the Member State of the EU main establishment | CMP-005, RES-003 |
| 25 | Hotline language coverage | Every language spoken by 50 or more Workforce Members, plus English | CMP-006 |
| 26 | Financial consequences in Sanction level S3 | Yes, where lawful | CMP-007 |
| 27 | Quantitative threshold for a significant account `[SOX]` | Performance materiality set by the CFO, plus qualitatively significant accounts | CMP-009 |
| 28 | PCI DSS entity type `[PCI]` | Merchant | SEC-019 |
| 29 | Threshold at which aggregated Personal Data becomes Restricted | 10,000 Data Subjects | SEC-002 |
| 30 | Cloud administrative identities: cloud-only or synchronized | Cloud-only for the highest-privilege tenant roles | SEC-005 |
| 31 | Customer-held keys (BYOK / external key management) | Customer-managed keys in the provider's FIPS 140-3 validated KMS; external key management only where a contract or regulator requires it | SEC-006 |
| 32 | Target date for hybrid post-quantum key establishment on external endpoints | Effective date + 24 months | SEC-006 |
| 33 | "Keep your drive" support in hardware contracts | Required for hardware that will hold Confidential or Restricted data | SEC-017 |
| 34 | Full ASVS Level 3 for all Restricted-data systems | Level 2, plus Level 3 for authentication, session, access control and cryptography in CDE and Tier 0 systems | SEC-010 |
| 35 | SLSA Build Level 3 target date | Effective date + 12 months | SEC-010 |
| 36 | EPSS elevation threshold | 0.10 | SEC-011 |
| 37 | Maximum remote work from another country per 12 months | 30 days | SEC-015 |
| 38 | Security reporting channel identifiers | Security mailbox, 24×7 SOC hotline and service-portal form | RES-001 |
| 39 | Primary law enforcement contacts per region | National federal investigative agency's cyber division and national cyber agency in each country | RES-001 |
| 40 | Incident response retainer commitments | Remote within 4 hours; on-site within 48 hours | RES-001 |
| 41 | Sev-1 financial loss threshold | USD 250,000 or equivalent | RES-002 |
| 42 | Insurer notification where the policy is silent | 72 hours | RES-003 |
| 43 | Customer notification where the contract is silent | 72 hours of confirmation | RES-003 |
| 44 | Identity protection offer period | 24 months | RES-003 |
| 45 | Pre-contracted notification services | Yes, through outside counsel or the cyber insurer's panel | RES-003 |
| 46 | Minimum separation between primary and alternate premises | Different utility grid and flood zone, and at least 50 km apart | RES-004 |
| 47 | CMT emergency spending limit per activation | CEO's delegated authority; above that, CFO approval | RES-004 |
| 48 | Full failover test of Tier 1 systems | Every 36 months | RES-005 |
| 49 | Corrective-action due-date bands after a Post-Incident Review | High 30 days · Medium 90 days · Low 180 days | TPL-007 |
| 50 | Effective date of each document | Date of approval by the document's approver | All documents |

## F. Assumptions

Assumptions are marked `[ASSUMPTION: …]` in the documents. Each SHALL be confirmed or corrected by the adopter before approval of the document it affects.

| # | Assumption | Affects |
|---|---|---|
| 1 | The standard reflects 45 CFR Part 164 Subpart C as in force on its effective date; the January 2025 proposed Security Rule amendments are not final. | CMP-008 |
| 2 | Management assesses ICFR against the COSO Internal Control — Integrated Framework (2013). | CMP-009 |
| 3 | Under GDPR Art. 12(6), the response deadline runs from receipt of requested identity information (EDPB Guidelines 01/2022); the GC is to confirm. | CMP-010 |
| 4 | The California Privacy Protection Agency risk-assessment regulations (Cal. Code Regs. tit. 11, §7150 et seq.) are in force; the GC is to confirm. | TPL-005 |
| 5 | FIPS 140-2 certificates moved to the CMVP historical list in September 2026; modules relying only on one need an Exception under CMP-003. | SEC-006 |
| 6 | The Organization has a corporate communications function. | RES-002 |
| 7 | The leader of the corporate communications function attends the CMT as a non-voting member. | RES-004 |
| 8 | The DR Coordinator is a senior infrastructure or IT operations leader reporting to the CIO. | RES-005 |
