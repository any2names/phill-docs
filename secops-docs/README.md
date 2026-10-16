# Information Security & GRC Policy Suite

A **generic, reusable** policy library that any organization can adopt: a set of
standalone, separately approvable documents that together form one information security
and GRC framework. Documents cross-reference each other by document ID and never restate
each other's requirements.

No document names a specific company. The adopting entity is always referred to as
**"the Organization"** (defined in GOV-006). Organization-specific choices are written as
`[DECISION REQUIRED: … Recommended default: …]` for the adopter to resolve.

- **Suite register** (conventions, roles, value ownership, document status): [SUITE-REGISTER.md](SUITE-REGISTER.md)
- **File layout:** `<DOMAIN>/<DOC-ID>-<kebab-title>.md`, e.g. `GOV/GOV-006-glossary-and-definitions.md`

## Design baseline

The suite is written for the most demanding common profile, so it is a **superset** of what
any one company needs. Adopters remove what does not apply rather than writing missing
material.

| Attribute | Baseline the suite is written to | If it does not apply to the adopter |
|---|---|---|
| Size & operating model | Enterprise, 1,000+ workforce; hybrid cloud + on-prem; multi-region | Smaller organizations MAY combine roles (combinations allowed by GOV-001) |
| Regions | United States and EU/EEA | Add local law to CMP-001's obligations register; extend RES-003 timelines |
| Regulated data | PII (GDPR, CCPA/CPRA), payment card data (PCI DSS v4.0.1), PHI (HIPAA), public-company financial reporting (SOX) | Remove the matching conditional module below |
| First assurance target | SOC 2 Type II examination | Mappings in REF-001 also cover ISO/IEC 27001:2022 |
| Starting maturity | No formal program | REF-003 maps existing artifacts to suite IDs |

### Conditional modules

| Applies only if the Organization… | Documents / sections to remove otherwise |
|---|---|
| Stores, processes or transmits payment card data | SEC-019; PCI DSS rows in REF-001; PCI clauses tagged `[PCI]` |
| Is a HIPAA covered entity or business associate | CMP-008; HIPAA rows in RES-003 and REF-001; clauses tagged `[HIPAA]` |
| Is publicly listed (SEC registrant) | CMP-009; SOX §301 elements of CMP-006; clauses tagged `[SOX]` |
| Processes personal data of EU/EEA residents or California consumers | CMP-010, TPL-005, TPL-010; clauses tagged `[GDPR]` / `[CPRA]` |
| Develops or deploys AI systems | RSK-006 (recommended for all adopters that use third-party AI tools) |

Regulation-specific clauses inside shared documents carry the tags above, so adopters can
find and remove them consistently.

## Document hierarchy

| Tier | Type | Content | Approval |
|---|---|---|---|
| 0 | Charter | What and why; board mandate | Board of Directors (via Audit Committee) |
| 1 | Policies | What is required, one per topic | ISSC |
| 2 | Standards | Measurable technical requirements supporting a policy | CISO |
| 3 | Procedures & plans | How to do it | Owner of parent document (CISO if the same role as the owner) |
| T | Templates | Forms | Owner of parent document (CISO if the same role as the owner) |
| Ref | Master references | Mappings, RACI, roadmap | As listed below |

Exceptions to the approval rule are marked † (required by regulation or governance independence).
‡ If the CISO is designated HIPAA Security Officer, the approver becomes the ISSC.

## Tailoring decisions

### Removed

| ID | Reason |
|---|---|
| GOV-005 Code of Conduct, Information Security Addendum | Duplicates other documents: workforce behavior is covered by GOV-004, reporting duties by CMP-006, sanctions by CMP-007. Its remaining content (confidentiality and conflict-of-interest pledges) moves into GOV-004. The ID is retired and never reused. |

### Added

| ID | Title | Reason |
|---|---|---|
| CMP-008 | HIPAA Security Rule Implementation Standard | 45 CFR §164.316 requires documented decisions for each addressable specification; §164.308(a)(2) requires a designated Security Official. |
| CMP-009 | SOX IT General Controls Standard | SOX §404 requires defined ITGC scope (financially significant systems) and controls to support management's assertion. |
| CMP-010 | Data Subject Request Procedure | GDPR Art. 12–22 (1 month) and CPRA (45 days) impose legal response deadlines. |
| SEC-019 | Cardholder Data Environment Standard | PCI DSS 12.5.2 requires documented scope, confirmed at least every 12 months, and segmentation controls kept separate from the general network policy. |
| TPL-010 | Record of Processing Activities Template | Required by GDPR Art. 30; the Art. 30(5) small-organization exemption is narrow and rarely applies. |

### Considered and not added

- **ISO 27001 Statement of Applicability / ISMS Scope:** deferred to P3 until ISO 27001 is pursued. The SoA can then be derived from REF-001.
- **A separate cross-border transfer standard:** GDPR Chapter V requirements are included in CMP-005, so privacy requirements stay in one document.

## Document library (61 documents)

**Priority:** P1 = required for the SOC 2 Type II period **or** for a legal or contractual
obligation already in force (PCI DSS, HIPAA, SOX, GDPR, CPRA). P2 = next-wave maturity. P3 = optimization.

| ID | Title | Tier | Owner | Approver | Review | Pri | Build # |
|---|---|---|---|---|---|---|---|
| ISP-000 | Information Security Program Charter | 0 | CISO | Board of Directors (via Audit Committee) | 12 mo | P1 | 2 |
| GOV-001 | Security Governance & Organization Policy | 1 | CISO | CEO † (creates the ISSC) | 12 mo | P1 | 3 |
| GOV-002 | Policy Management Policy | 1 | Head of GRC | ISSC | 12 mo | P1 | 4 |
| GOV-003 | Security Metrics & Reporting Policy | 1 | CISO | ISSC | 12 mo | P2 | 53 |
| GOV-004 | Acceptable Use Policy (absorbs GOV-005) | 1 | CISO | ISSC | 12 mo | P1 | 22 |
| ~~GOV-005~~ | *Retired, merged into GOV-004* | — | — | — | — | — | — |
| GOV-006 | Glossary & Definitions | 1 (Ref) | Head of GRC | ISSC | 12 mo + each new document | P1 | 1 |
| RSK-001 | Risk Management Policy | 1 | Head of GRC | ISSC (appetite ratified by Audit Committee) | 12 mo | P1 | 5 |
| RSK-002 | Risk Assessment Standard | 2 | Head of GRC | CISO | 12 mo | P1 | 6 |
| RSK-003 | Third-Party & Supply Chain Risk Management Policy | 1 | Head of GRC | ISSC | 12 mo | P1 | 43 |
| RSK-004 | Business Impact Analysis Standard | 2 | Business Continuity Manager | CISO | 12 mo | P1 | 39 |
| RSK-005 | Threat Intelligence & Threat Modeling Standard | 2 | SOC Manager | CISO | 12 mo | P3 | 57 |
| RSK-006 | AI & Emerging Technology Risk Policy | 1 | CISO | ISSC | 12 mo | P2 | 58 |
| CMP-001 | Compliance Management Policy | 1 | Head of GRC | ISSC | 12 mo | P1 | 14 |
| CMP-002 | Internal Audit & Control Testing Policy | 1 | Internal Audit Director | Audit Committee † | 12 mo | P2 | 54 |
| CMP-003 | Policy Exception & Waiver Policy | 1 | Head of GRC | ISSC | 12 mo | P1 | 7 |
| CMP-004 | Evidence Management & Records Retention Policy | 1 | Head of GRC | ISSC (GC concurrence) | 12 mo | P1 | 15 |
| CMP-005 | Data Privacy & Protection Policy | 1 | CPO | ISSC | 12 mo | P1 | 16 |
| CMP-006 | Whistleblower & Security Concern Reporting Policy | 1 | GC | Audit Committee † (SOX §301) | 12 mo | P1 | 52 |
| CMP-007 | Enforcement & Disciplinary Policy | 1 | CHRO | ISSC | 12 mo | P1 | 8 |
| CMP-008 | HIPAA Security Rule Implementation Standard | 2 | HIPAA Security Officer | CISO ‡ | 12 mo | P1 | 20 |
| CMP-009 | SOX IT General Controls Standard | 2 | Head of GRC | CFO † (SOX §404) | 12 mo | P1 | 21 |
| CMP-010 | Data Subject Request Procedure | 3 | DPO | CPO | 12 mo | P1 | 17 |
| SEC-001 | Asset Management Policy | 1 | CIO | ISSC | 12 mo | P1 | 13 |
| SEC-002 | Data Classification & Handling Policy | 1 | CISO | ISSC | 12 mo | P1 | 12 |
| SEC-003 | Identity & Access Management Policy | 1 | CISO | ISSC | 12 mo | P1 | 26 |
| SEC-004 | Password & Authentication Standard | 2 | Head of Security Engineering | CISO | 12 mo | P1 | 27 |
| SEC-005 | Privileged Access Management Standard | 2 | Head of Security Engineering | CISO | 12 mo | P1 | 28 |
| SEC-006 | Cryptography & Key Management Policy | 1 | Head of Security Engineering | ISSC | 12 mo | P1 | 30 |
| SEC-007 | Network Security Policy | 1 | Head of Security Engineering | ISSC | 12 mo | P1 | 31 |
| SEC-008 | Endpoint & Mobile Device Security Policy (incl. BYOD) | 1 | CIO | ISSC | 12 mo | P1 | 33 |
| SEC-009 | Cloud Security Policy | 1 | CTO | ISSC | 12 mo | P1 | 34 |
| SEC-010 | Secure Software Development Lifecycle Policy | 1 | CTO | ISSC | 12 mo | P1 | 35 |
| SEC-011 | Vulnerability & Patch Management Policy | 1 | Head of Security Engineering | ISSC | 12 mo | P1 | 36 |
| SEC-012 | Logging & Monitoring Policy | 1 | SOC Manager | ISSC | 12 mo | P1 | 37 |
| SEC-013 | Change & Configuration Management Policy | 1 | CIO | ISSC | 12 mo | P1 | 38 |
| SEC-014 | Email & Communications Security Policy | 1 | CIO | ISSC | 12 mo | P2 | 55 |
| SEC-015 | Remote Work & Travel Security Policy | 1 | CISO | ISSC | 12 mo | P3 | 56 |
| SEC-016 | Physical & Environmental Security Policy | 1 | Head of Facilities | ISSC | 12 mo | P1 | 41 |
| SEC-017 | Media Sanitization & Secure Disposal Policy | 1 | CIO | ISSC | 12 mo | P1 | 42 |
| SEC-018 | Backup Policy | 1 | CIO | ISSC | 12 mo | P1 | 40 |
| SEC-019 | Cardholder Data Environment Standard | 2 | Head of Security Engineering | CISO | 12 mo | P1 | 32 |
| RES-001 | Incident Response Policy | 1 | CISO | ISSC | 12 mo | P1 | 45 |
| RES-002 | Incident Response Plan | 3 | SOC Manager | CISO | 12 mo + after each Sev-1 | P1 | 46 |
| RES-003 | Breach Notification Standard | 2 | CPO | CISO (GC concurrence) | 12 mo | P1 | 47 |
| RES-004 | Business Continuity Policy | 1 | Business Continuity Manager | ISSC | 12 mo | P1 | 50 |
| RES-005 | Disaster Recovery Plan | 3 | CIO | Business Continuity Manager | 12 mo + after each test | P1 | 51 |
| PPL-001 | Human Resources Security Policy | 1 | CHRO | ISSC | 12 mo | P1 | 23 |
| PPL-002 | Security Awareness & Training Policy | 1 | CISO | ISSC | 12 mo | P1 | 24 |
| TPL-001 | Risk Register Template | T | Head of GRC | CISO | 12 mo | P1 | 9 |
| TPL-002 | Risk Acceptance Form | T | Head of GRC | CISO | 12 mo | P1 | 10 |
| TPL-003 | Policy Exception Request Form | T | Head of GRC | CISO | 12 mo | P1 | 11 |
| TPL-004 | Vendor Security Questionnaire | T | Head of GRC | CISO | 12 mo | P1 | 44 |
| TPL-005 | Data Protection Impact Assessment Template | T | DPO | CPO | 12 mo | P1 | 18 |
| TPL-006 | Incident Report Template | T | SOC Manager | CISO | 12 mo | P1 | 48 |
| TPL-007 | Post-Incident Review Template | T | SOC Manager | CISO | 12 mo | P2 | 49 |
| TPL-008 | Access Review Template | T | Head of Security Engineering | CISO | 12 mo | P1 | 29 |
| TPL-009 | Policy Acknowledgement Form | T | Head of GRC | CISO | 12 mo | P1 | 25 |
| TPL-010 | Record of Processing Activities Template | T | DPO | CPO | 12 mo | P1 | 19 |
| REF-001 | Control Mapping Matrix | Ref | Head of GRC | CISO | 12 mo + each new document | P1 | 60 |
| REF-002 | Master RACI Matrix | Ref | Head of GRC | ISSC | 12 mo + each new document | P1 | 59 |
| REF-003 | Gap Analysis & Implementation Roadmap | Ref | CISO | ISSC | Quarterly | P1 | 61 |

### Build order

Documents are built in dependency order:

1. Terms and governance (1–4)
2. Risk method and the exception and enforcement mechanics every document references (5–11)
3. Classification, retention, privacy, and regulatory standards (12–21)
4. People and access (22–29)
5. Technical controls (30–42). The BIA (39) comes before Backup (40) and DR (51) so that RTO and RPO values come from one source.
6. Third parties and resilience (43–52)
7. P2 and P3 documents (53–58)
8. Master references last (59–61)
