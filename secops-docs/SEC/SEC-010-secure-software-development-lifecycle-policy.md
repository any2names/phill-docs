# SEC-010 — Secure Software Development Lifecycle Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | SEC-010 |
| Title | Secure Software Development Lifecycle Policy (incl. CI/CD, secrets, SBOM) |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Technology Officer (CTO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | SEC-002, SEC-003, SEC-004, SEC-005, SEC-006, SEC-009, SEC-011, SEC-012, SEC-013, SEC-019, RSK-003, RSK-005, RSK-006, CMP-005, CMP-009, PPL-002 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CTO | Initial release |

## 3. Purpose

This Policy sets the Organization's mandatory requirements for building security into
software from design to release. It covers secure design and threat modeling, secure coding
standards, code review, automated security testing gates, CI/CD pipeline integrity, Secrets
management in development and delivery, Software Bills of Materials, open-source component
and license governance, segregation of environments, and the use of test data.

## 4. Scope

| Dimension | In scope |
|---|---|
| People | All Workforce Members and Third Parties who design, write, review, build, test, package or deploy software for the Organization, including developers, DevOps and platform engineers, QA staff and product owners |
| Systems | All software developed, customized or configured by or for the Organization, including applications, APIs, mobile apps, scripts, Infrastructure as Code, container images, data pipelines, low-code applications and machine-learning code; source code repositories; CI/CD pipelines and build runners; artifact and container registries; secrets managers |
| Data | Source code, build artifacts, Secrets, SBOMs, and test data at every Classification Level |
| Locations | All development, build and deployment locations, including cloud-hosted development environments |
| Third parties | Outsourced development partners and contractors; providers of source control, CI/CD and registry services; maintainers of open-source components consumed by the Organization |

Commercial off-the-shelf software is in scope only for configuration, integration code and
SBOM requirements (section 5.8). Change approval and release management are governed by
SEC-013. Vulnerability severity and remediation SLAs are set in SEC-011.

## 5. Policy statements

### 5.1 Secure development lifecycle

- **SEC-010.5.1.1** The CTO SHALL maintain a documented secure development lifecycle (SDLC) that integrates the security activities of this Policy into each phase: requirements, design, implementation, verification, release and maintenance.
- **SEC-010.5.1.2** Every software project SHALL be registered in the Asset Inventory (SEC-001) with a System Owner and the highest Classification Level of data it processes, which determines its security requirements under SEC-010.7.1.
- **SEC-010.5.1.3** Security requirements derived from SEC-010.7.1, applicable suite documents and the Obligations Register (CMP-001) SHALL be recorded in the backlog for every new system and for every change that alters authentication, authorization, Restricted-data handling, cryptography or external interfaces.
- **SEC-010.5.1.4** Developers SHALL complete role-based secure development training as required by PPL-002 before receiving write access to production repositories.
- **SEC-010.5.1.5** `[PCI]` Bespoke and custom software that stores, processes or transmits account data, or could affect the security of the CDE, SHALL be developed under this Policy in accordance with industry standards for secure development (PCI DSS 6.2.1).
- **SEC-010.5.1.6** `[GDPR]` Data protection by design and by default SHALL be addressed in requirements for any system processing Personal Data, with a DPIA (TPL-005) where CMP-005 requires one.

### 5.2 Secure design and threat modeling

- **SEC-010.5.2.1** A Threat Model SHALL be produced for each trigger in RSK-005.5.6.1, using the method in RSK-005, before implementation begins.
- **SEC-010.5.2.2** Threat Model review and approval, and recording of mitigations as security requirements, SHALL follow RSK-005.5.6.4 and RSK-005.5.6.5, and SHALL be completed before implementation begins.
- **SEC-010.5.2.3** Threat Models SHALL be updated at the frequency and on the triggers in RSK-005.5.6.6.
- **SEC-010.5.2.4** Designs SHALL apply secure design principles, including: Least Privilege; defense in depth; secure defaults; failing securely; complete mediation of authorization; and minimization of attack surface and of Personal Data.
- **SEC-010.5.2.5** Authentication, session management, authorization and cryptography SHALL use the Organization's approved shared services or libraries, which implement SEC-004 and SEC-006. Custom cryptographic algorithms SHALL NOT be developed.
- **SEC-010.5.2.6** A security architecture review by the Head of Security Engineering SHALL be completed before release for every new system processing Restricted data and every new internet-facing system.

### 5.3 Secure coding standards

- **SEC-010.5.3.1** Software SHALL meet the OWASP Application Security Verification Standard (ASVS) level assigned in SEC-010.7.1 by the highest Classification Level of data the software processes.
- **SEC-010.5.3.2** The CTO SHALL publish language-specific secure coding guidelines that address, at minimum, the OWASP Top 10 and OWASP API Security Top 10 risk categories, and SHALL review them at least every 12 months.
- **SEC-010.5.3.3** `[PCI]` Software development personnel working on bespoke and custom software SHALL be trained at least every 12 months on secure coding relevant to their job function and language, including the attack techniques listed in PCI DSS 6.2.4 (PCI DSS 6.2.2). Training is delivered under PPL-002.
- **SEC-010.5.3.4** Software SHALL validate all input from untrusted sources, encode output for its context, use parameterized queries, and SHALL NOT log Secrets, authentication data or Restricted data in clear text.
- **SEC-010.5.3.5** Code generated or suggested by Generative AI tools SHALL be subject to the same review, testing and scanning as human-written code. Only Generative AI tools approved under RSK-006 SHALL be used, and Restricted data and Secrets SHALL NOT be entered into them.

### 5.4 Code review

- **SEC-010.5.4.1** Every change to code, IaC or pipeline configuration merged into a protected branch SHALL be reviewed and approved by at least one person other than the author before merge.
- **SEC-010.5.4.2** Changes to security-sensitive code paths (authentication, authorization, cryptography, payment processing, Restricted-data handling, and pipeline definitions) SHALL additionally be approved by a designated code owner trained in secure code review.
- **SEC-010.5.4.3** Reviewers SHALL confirm that the change meets the secure coding guidelines and that security findings from automated gates (section 5.5) are resolved or have an approved Exception.
- **SEC-010.5.4.4** `[PCI]` Bespoke and custom software SHALL be reviewed before release to production or to customers, to identify and correct potential coding vulnerabilities, by individuals other than the originating author who are knowledgeable in code-review techniques and secure coding practices; code changes SHALL be approved by management before release (PCI DSS 6.2.3, 6.2.3.1).
- **SEC-010.5.4.5** `[SOX]` Changes to Financially Significant Systems SHALL meet the program change controls in CMP-009 in addition to this section.

### 5.5 Automated security testing gates

- **SEC-010.5.5.1** The pipeline for every production application SHALL run the automated security tests in SEC-010.7.5, at the stage and with the blocking threshold stated there.
- **SEC-010.5.5.2** Static application security testing (SAST) SHALL run on every pull or merge request to a protected branch. New findings at or above the blocking threshold SHALL prevent merge.
- **SEC-010.5.5.3** Software composition analysis (SCA) SHALL run on every build, identifying open-source and third-party components and their known Vulnerabilities. Builds introducing a component with a Vulnerability at or above the blocking threshold SHALL fail.
- **SEC-010.5.5.4** Secret scanning SHALL run with push protection on every repository, blocking commits that contain Secrets. Developers SHOULD also run secret scanning in pre-commit hooks.
- **SEC-010.5.5.5** IaC and container image scanning SHALL run in the pipeline as specified in SEC-009.
- **SEC-010.5.5.6** Dynamic application security testing (DAST) SHALL be run against every internet-facing web application and API, authenticated where the application requires authentication, at the frequency in SEC-010.7.5.
- **SEC-010.5.5.7** Severity of findings from all gates SHALL be assigned under SEC-011, and findings not blocked at the gate SHALL be tracked and remediated within the remediation SLA in SEC-011.
- **SEC-010.5.5.8** Disabling, bypassing or downgrading a security gate SHALL require an Exception under CMP-003. Gate overrides SHALL be logged and reported monthly to the Head of Security Engineering.
- **SEC-010.5.5.9** Penetration testing of applications is governed by SEC-011.

### 5.6 CI/CD pipeline integrity

- **SEC-010.5.6.1** Branch protection SHALL be enforced on the default and release branches of every production repository: no direct pushes; required review under section 5.4; required passing status checks under section 5.5; no force pushes or history rewrites; and no deletion of the branch.
- **SEC-010.5.6.2** Repository administrators SHALL NOT be able to bypass branch protection without the bypass being logged and alerted to Workforce Members designated by the Head of Security Engineering.
- **SEC-010.5.6.3** Commits to protected branches of repositories for Recovery Tier 0 and Tier 1 systems, CDE systems and Financially Significant Systems SHALL be signed and the signature verified by the source control platform. Commits to other repositories SHOULD be signed.
- **SEC-010.5.6.4** Production builds SHALL run only on Organization-controlled or Organization-approved hosted build platforms, on ephemeral, isolated build runners that are destroyed after each job.
- **SEC-010.5.6.5** Every production artifact (package, container image, binary, IaC module) SHALL be signed in the pipeline, and its signature and provenance SHALL be verified before deployment to production.
- **SEC-010.5.6.6** The pipeline SHALL produce build provenance meeting the SLSA level in SEC-010.7.8 for every production artifact.
- **SEC-010.5.6.7** Deployment to production SHALL occur only through the approved pipeline, from artifacts held in the Organization's approved artifact or container registry. Developers SHALL NOT have standing write access to production (SEC-005).
- **SEC-010.5.6.8** Pipeline definitions SHALL be stored in version control and changed only through reviewed merge requests under section 5.4.
- **SEC-010.5.6.9** Pipelines SHALL authenticate to cloud and deployment targets using short-lived, workload-identity credentials (for example, OIDC federation) and SHALL NOT store long-lived cloud credentials.
- **SEC-010.5.6.10** Third-party pipeline actions, plugins and base images SHALL be pinned to an immutable reference (commit hash or digest), and SHALL be sourced from an approved list maintained by the Head of Security Engineering.
- **SEC-010.5.6.11** Access to source control, CI/CD and registries SHALL be federated through the Identity Provider with MFA (SEC-004), and reviewed under SEC-003.
- **SEC-010.5.6.12** Audit logs from source control, CI/CD and registries SHALL be forwarded to the SIEM as specified in SEC-012.

### 5.7 Secrets management

- **SEC-010.5.7.1** Secrets used by applications, pipelines and infrastructure SHALL be stored in the Organization's approved secrets manager and retrieved at runtime or deploy time.
- **SEC-010.5.7.2** Secrets SHALL NOT be stored in source code, IaC, configuration files committed to repositories, container images, pipeline logs, tickets, chat messages or documentation.
- **SEC-010.5.7.3** Access to each Secret SHALL be limited under Least Privilege to the workload identities and named administrators that require it, and every access SHALL be logged.
- **SEC-010.5.7.4** Secrets SHALL be rotated in line with the credential requirements in SEC-004 and the Cryptoperiods in SEC-006, and SHOULD be dynamic or short-lived where the target system supports it.
- **SEC-010.5.7.5** Any Secret detected in a repository, image, log or other unapproved location SHALL be treated as compromised and SHALL be revoked and rotated within the time in SEC-010.7.9. Removal from history alone SHALL NOT be treated as remediation.
- **SEC-010.5.7.6** A Secret exposed in a public location SHALL be reported to the SOC as a potential Security Incident under RES-002.
- **SEC-010.5.7.7** Production Secrets SHALL NOT be used in non-production environments.

### 5.8 Software Bill of Materials (SBOM)

- **SEC-010.5.8.1** An SBOM SHALL be generated automatically by the pipeline for every production release of Organization-developed software and every production container image.
- **SEC-010.5.8.2** SBOMs SHALL be produced in SPDX (version 2.3 or later) or CycloneDX (version 1.5 or later) format and SHALL include, for each component: name, version, supplier, unique identifier (for example, package URL), dependency relationship, and license.
- **SEC-010.5.8.3** SBOMs SHALL be stored with the release artifact in the approved registry, signed, and retained for the life of the release plus the period set in CMP-004 for control Evidence.
- **SEC-010.5.8.4** SBOMs SHALL be ingested by the vulnerability management process in SEC-011, so that newly disclosed Vulnerabilities in deployed components are identified without rebuilding.
- **SEC-010.5.8.5** The Organization SHOULD publish Vulnerability Exploitability eXchange (VEX) statements alongside SBOMs supplied to customers, stating whether listed Vulnerabilities affect the product.
- **SEC-010.5.8.6** SBOMs for commercial software and Cloud Services supporting Recovery Tier 0 or Tier 1 processes SHALL be requested from suppliers through RSK-003.
- **SEC-010.5.8.7** `[PCI]` SBOMs SHALL support the inventory of bespoke and custom software and third-party software components required by PCI DSS 6.3.2.

### 5.9 Open-source components and licenses

- **SEC-010.5.9.1** Open-source and third-party components SHALL be obtained only through the Organization's approved package proxy or mirror, which SHALL block packages known to be malicious.
- **SEC-010.5.9.2** Every new direct dependency SHALL be checked before first use for: license compliance under SEC-010.7.10; known Vulnerabilities; evidence of active maintenance; and indicators of typosquatting or dependency confusion.
- **SEC-010.5.9.3** Dependency versions SHALL be pinned through lock files or equivalent in every production repository.
- **SEC-010.5.9.4** Components whose upstream project shows no release or maintainer activity for 24 months SHALL be flagged by SCA and SHALL have a replacement plan recorded by the System Owner. Components that have reached end of support SHALL be handled under the end-of-support requirements in SEC-001 and SEC-011.
- **SEC-010.5.9.5** Licenses SHALL be classified under SEC-010.7.10. Components with licenses in the "GC review" category SHALL NOT be used in distributed software or network-served software until the GC approves the use. Components in the "prohibited" category SHALL NOT be used.
- **SEC-010.5.9.6** Automated dependency update tooling SHOULD be enabled on all production repositories to propose updates for vulnerable or outdated components.
- **SEC-010.5.9.7** Contributions by Workforce Members to external open-source projects on behalf of the Organization SHALL be approved by the CTO and SHALL NOT include Confidential or Restricted information.
- **SEC-010.5.9.8** Open-weight and third-party AI models SHALL be treated as third-party components under this section: they SHALL be obtained only from model sources approved by the Head of Security Engineering and served through the approved package proxy, mirror or registry, SHALL be checked under SEC-010.5.9.2 before first use, and SHALL be recorded in the SBOM. Model development, integrity verification and evaluation requirements are set in RSK-006.5.7.4, RSK-006.5.7.5 and RSK-006 section 5.8.

### 5.10 Segregation of environments

- **SEC-010.5.10.1** Development, test, staging and production environments SHALL be separate, using distinct cloud accounts or subscriptions (SEC-009) and distinct network zones (SEC-007).
- **SEC-010.5.10.2** Access controls SHALL enforce separation of duties between development and production: Workforce Members who develop a change SHALL NOT also deploy it to production outside the approved pipeline, consistent with the Segregation of Duties rules in GOV-001 and the privileged access controls in SEC-005.
- **SEC-010.5.10.3** `[PCI]` Pre-production environments SHALL be separated from production environments and the separation enforced with access controls; roles and functions SHALL be separated between production and pre-production to provide accountability so that only reviewed and approved changes are deployed (PCI DSS 6.5.3, 6.5.4).
- **SEC-010.5.10.4** Production configuration, credentials and data stores SHALL NOT be reachable from non-production environments.

### 5.11 Test data

- **SEC-010.5.11.1** Production data SHALL be used in development, test and staging environments only as permitted for its Classification Level by the non-production use rules in SEC-002. In particular, production Restricted data SHALL NOT be used in non-production environments.
- **SEC-010.5.11.2** Where SEC-002 permits masked or tokenized production data, masking and tokenization SHALL be performed inside the production environment, using tooling approved by the Head of Security Engineering, before the data is copied to non-production. Each copy SHALL be recorded with the Data Owner approval required by SEC-002.
- **SEC-010.5.11.3** Synthetic data SHOULD be used for testing in preference to masked production data.
- **SEC-010.5.11.4** `[PCI]` The prohibition on live PANs in pre-production environments (PCI DSS 6.5.5) is set in SEC-002; pipelines and data-copy jobs SHALL include an automated check that blocks PAN-formatted data from being loaded into pre-production data stores.
- **SEC-010.5.11.5** Test data and test accounts SHALL be removed from system components before every production release. `[PCI]` This meets PCI DSS 6.5.6.
- **SEC-010.5.11.6** `[GDPR]` `[CPRA]` Any use of Personal Data in non-production SHALL have a lawful basis and purpose recorded in the ROPA under CMP-005.

### 5.12 Public-facing web applications `[PCI]`

- **SEC-010.5.12.1** `[PCI]` Public-facing web applications in or connected to the CDE SHALL be protected by an automated technical solution (for example, a web application firewall) that continually detects and prevents web-based attacks, is configured to block or alert, and generates audit logs (PCI DSS 6.4.1, 6.4.2).
- **SEC-010.5.12.2** `[PCI]` All Payment Page scripts loaded and executed in the consumer's browser SHALL be inventoried with written justification, authorized, and protected by a method that assures their integrity (PCI DSS 6.4.3). Change and tamper detection for Payment Pages is specified in SEC-019.

### 5.13 Outsourced development

- **SEC-010.5.13.1** Contracts for outsourced development SHALL require compliance with this Policy, Organization ownership of code, delivery of SBOMs, and the right to perform security testing, and SHALL be put in place under RSK-003.
- **SEC-010.5.13.2** Code delivered by Third Parties SHALL pass the same review and automated gates as internally developed code before deployment.

### 5.14 Program change controls `[SOX]`

- **SEC-010.5.14.1** `[SOX]` For Financially Significant Systems, the program change controls (authorization, testing, approval, segregation of development and migration to production, and post-implementation review) are specified in CMP-009. The pipeline controls in sections 5.4 and 5.6 SHALL produce the Evidence CMP-009 requires.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CTO | Owns this Policy; maintains the SDLC, secure coding guidelines and pipeline platform; approves external open-source contributions. |
| Head of Security Engineering | Operates SAST, SCA, DAST and secret scanning; sets gate thresholds within SEC-010.7.5; reviews Threat Models and performs security architecture reviews; maintains the approved list of pipeline actions; reviews gate overrides. |
| CIO | Ensures internally configured commercial software meets sections 5.4 and 5.8 where applicable. |
| CISO | Approves Exceptions within the authority in CMP-003. |
| GC | Approves "GC review" category licenses. |
| SOC Manager | Handles exposed Secrets and pipeline security alerts under RES-002. |
| Head of GRC | Confirms `[SOX]` pipeline Evidence meets CMP-009. |
| System Owner | Ensures their software meets the assigned ASVS level; owns remediation of findings; maintains Threat Models and replacement plans for unmaintained components. |
| Data Owner | Approves use of masked or Confidential data in non-production. |
| Workforce Member (developer) | Follows secure coding guidelines; does not commit Secrets; completes training; resolves findings before merge. |
| Third Party (outsourced developer) | Complies with this Policy as required by contract. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| SEC-010.7.1 | OWASP ASVS level by highest Classification Level processed | Public / Internal: ASVS Level 1 · Confidential: Level 2 · Restricted: Level 2, plus Level 3 for authentication, session management, access control and cryptography controls of systems in the CDE or supporting Recovery Tier 0 [DECISION REQUIRED: Whether to require full ASVS Level 3 for all Restricted-data systems. Recommended default: Level 2 plus Level 3 for the named control areas] |
| SEC-010.7.2 | Threat Model | Required per RSK-005.5.6.1; review frequency per RSK-005.5.6.6; method per RSK-005 |
| SEC-010.7.3 | Code review | ≥ 1 reviewer other than the author for every protected-branch merge; plus designated code owner for security-sensitive paths |
| SEC-010.7.4 | Secure coding guidelines review | Every 12 months |
| SEC-010.7.5 | Automated security testing gates | SAST: every pull/merge request, block new Critical and High · SCA: every build, block Critical and High with an available fix and any KEV-listed Vulnerability · Secret scanning: push protection on every repository, block all · IaC and image scanning: per SEC-009 · DAST: every internet-facing web application and API at least every 30 days and before each major release |
| SEC-010.7.6 | Signed commits | Required for Tier 0/Tier 1, CDE and `[SOX]` Financially Significant System repositories; recommended elsewhere |
| SEC-010.7.7 | Artifact signing | Every production artifact signed; signature and provenance verified before deployment |
| SEC-010.7.8 | SLSA build level target | SLSA v1.0 Build Level 2 for all production artifacts from the Effective date; Build Level 3 for Tier 0/Tier 1 and CDE artifacts within 12 months of the Effective date [DECISION REQUIRED: SLSA Build Level 3 target date. Recommended default: Effective date + 12 months] |
| SEC-010.7.9 | Exposed Secret revocation and rotation | Within 24 hours of detection; within 4 hours where exposed in a public location |
| SEC-010.7.10 | Open-source license categories | Permitted: permissive licenses (for example, MIT, BSD, Apache-2.0) · GC review: weak and strong copyleft (for example, LGPL, MPL, EPL, GPL, AGPL) and any license not yet categorized · Prohibited: no license, non-commercial or field-of-use-restricted licenses |
| SEC-010.7.11 | Unmaintained component threshold | No upstream release or maintainer activity for 24 months → flagged with replacement plan |
| SEC-010.7.12 | SBOM | Every production release and container image; SPDX ≥ 2.3 or CycloneDX ≥ 1.5; signed; retained with the release |
| SEC-010.7.13 | Test data | Per the non-production use rules in SEC-002; masking performed in production before copy; test data and test accounts removed before production |
| SEC-010.7.14 | Finding remediation (all gates) | Within the remediation SLA in SEC-011 |
| SEC-010.7.15 | Developer secure coding training | Per PPL-002, before write access to production repositories |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Production repositories with SAST, SCA and secret scanning gates enabled | 100% | Monthly | Head of Security Engineering |
| Production repositories with branch protection meeting SEC-010.5.6.1 | 100% | Monthly | CTO |
| Merges to protected branches without independent review | 0 | Monthly | CTO |
| Security gate overrides without an approved Exception | 0 | Monthly | Head of Security Engineering |
| Production releases with a signed SBOM | 100% | Monthly | CTO |
| Production deployments of unsigned or unverified artifacts | 0 | Monthly | CTO |
| Exposed Secrets revoked within SEC-010.7.9 | 100% | Monthly | SOC Manager |
| Application security findings remediated within SEC-011 SLA | ≥ 95% | Monthly | CTO |
| In-scope systems with a current Threat Model | 100% | Quarterly | Head of Security Engineering |
| Internet-facing applications with DAST in the last 30 days | 100% | Monthly | Head of Security Engineering |
| Non-production data stores holding unmasked production Restricted data | 0 | Quarterly | CTO |
| Components in "prohibited" license category in production | 0 | Quarterly | CTO |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following SHALL NOT receive an Exception: use of production Restricted data in
non-production (SEC-010.5.11.1); storage of Secrets in source code or repositories
(SEC-010.5.7.2); and deployment to production outside the approved pipeline other than an
Emergency Change under SEC-013 (SEC-010.5.6.7).

## 10. Enforcement

Non-compliance is handled under CMP-007.

The Head of Security Engineering MAY revoke repository write access or halt a pipeline that
is deploying unsigned artifacts or bypassing security gates without an Exception, and SHALL
notify the CTO within 1 business day.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| SEC-010.5.1 SDLC | A.8.25, A.8.26 | PR.PS-06 | SA-3, SA-8, SA-15 | 16.1, 16.9 | CC8.1 | BAI03 | PCI DSS 6.2.1; GDPR Art. 25 |
| SEC-010.5.2 Secure design & threat modeling | A.8.27, A.5.8 | PR.PS-06, ID.RA-04 | SA-8, SA-11, SA-17 | 16.10, 16.14 | CC3.2, CC8.1 | BAI03 | GDPR Art. 25, Art. 35 |
| SEC-010.5.3 Secure coding | A.8.28 | PR.PS-06 | SA-11, SI-10 | 16.1, 16.9, 16.11 | CC8.1 | BAI03 | PCI DSS 6.2.2, 6.2.4 |
| SEC-010.5.4 Code review | A.8.28, A.8.29, A.8.4 | PR.PS-06 | SA-11, CM-3 | 16.12 | CC8.1 | BAI03, BAI07 | PCI DSS 6.2.3, 6.2.3.1; SOX §404 |
| SEC-010.5.5 Security testing gates | A.8.29, A.8.8 | PR.PS-06, ID.RA-01 | SA-11, RA-5 | 16.12, 16.2 | CC7.1, CC8.1 | BAI07 | PCI DSS 6.2.4, 6.3.1, 11.3 |
| SEC-010.5.6 CI/CD integrity | A.8.4, A.8.32, A.8.31 | PR.PS-06, PR.PS-01 | CM-14, SA-10, SR-4, SR-11, SI-7 | 16.1, 16.7 | CC8.1, CC6.1 | BAI06, BAI03 | PCI DSS 6.5.1 |
| SEC-010.5.7 Secrets | A.5.17, A.8.24 | PR.AA-01, PR.DS-01 | IA-5, SC-12, SC-28 | 3.11, 16.1 | CC6.1 | DSS05.04 | PCI DSS 8.3.2, 8.6.2 |
| SEC-010.5.8 SBOM | A.5.21, A.8.25 | ID.AM-02, GV.SC-04 | SR-4, CM-8 | 16.4, 2.1 | CC9.2 | APO10 | PCI DSS 6.3.2 |
| SEC-010.5.9 Open source & licenses | A.5.21, A.5.32, A.8.19 | GV.SC-05, PR.PS-02 | SA-22, SR-3, CM-10 | 16.4, 16.5, 2.2 | CC9.2 | APO10, MEA03 | — |
| SEC-010.5.10 Environment segregation | A.8.31, A.5.3 | PR.IR-01 | CM-4, AC-5, SA-3 | 16.8 | CC8.1, CC6.1 | BAI03, BAI07 | PCI DSS 6.5.3, 6.5.4 |
| SEC-010.5.11 Test data | A.8.33 | PR.DS-01 | SA-3, SA-11 | 16.8 | C1.1, CC8.1 | BAI07 | PCI DSS 6.5.5, 6.5.6; GDPR Art. 5(1)(b), Art. 25 |
| SEC-010.5.12 Public-facing web apps `[PCI]` | A.8.26, A.8.20 | PR.IR-01 | SC-7, SI-7 | 13.10 | CC6.6 | DSS05.02 | PCI DSS 6.4.1, 6.4.2, 6.4.3 |
| SEC-010.5.13 Outsourced development | A.8.30 | GV.SC-05 | SA-4, SA-11 | 16.1 | CC9.2 | APO10 | — |
| SEC-010.5.14 Program change `[SOX]` | A.8.32 | PR.PS-06 | CM-3 | — | CC8.1 | BAI06 | SOX §404; PCI DSS 6.5.1 |

## 12. Related documents

ISP-000, GOV-001, GOV-006, SEC-001, SEC-002, SEC-003, SEC-004, SEC-005, SEC-006, SEC-007,
SEC-009, SEC-011, SEC-012, SEC-013, SEC-019, RSK-003, RSK-005, RSK-006, CMP-001, CMP-003,
CMP-004, CMP-005, CMP-007, CMP-009, PPL-002, RES-002, TPL-005

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CTO | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
