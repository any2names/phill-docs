# SEC-005 — Privileged Access Management Standard

## 1. Document control

| Field | Value |
|---|---|
| Document ID | SEC-005 |
| Title | Privileged Access Management Standard |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 2 — Standard |
| Classification | Internal |
| Owner | Head of Security Engineering |
| Approver | Chief Information Security Officer (CISO) |
| Effective date | [DECISION REQUIRED: Date of CISO approval] |
| Next review date | Effective date + 12 months |
| Parent document | SEC-003 Identity & Access Management Policy |
| Related documents | GOV-001, GOV-006, CMP-004, CMP-008, CMP-009, SEC-001, SEC-003, SEC-004, SEC-006, SEC-008, SEC-009, SEC-012, SEC-013, SEC-019, TPL-008 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Head of Security Engineering | Initial release |

## 3. Purpose

This Standard sets measurable requirements for the issuance, use, protection, monitoring and
review of Privileged Accounts, so that elevated access is held by the fewest individuals, for
the shortest time, through controlled and recorded paths. Compromise of privileged access is
the most direct route to a material Security Incident; these controls reduce both the
likelihood and the impact of that compromise.

## 4. Scope

| Dimension | In scope |
|---|---|
| People | All Workforce Members and Third-Party personnel who hold or request privileged access |
| Systems | All Privileged Accounts on Information Systems, including operating system administrators and root, directory and Identity Provider administrators, database administrators, network and security device administrators, hypervisor and container orchestration administrators, Cloud Service root, owner, global and organization administrators, SaaS tenant administrators, CI/CD and source repository administrators, security tool administrators, and Service Accounts with privileged entitlements |
| Data | Credentials and Secrets for Privileged Accounts (Restricted under SEC-002), privileged session recordings and PAM logs |
| Locations | All locations from which privileged access is exercised |
| Third parties | Third Parties providing administrative support, managed services or vendor maintenance with privileged access |

## 5. Requirements

### 5.1 Privileged Account inventory

- **SEC-005.5.1.1** The Head of Security Engineering SHALL maintain an inventory of all Privileged Accounts and privileged roles, as part of the identity records in the Asset Inventory (SEC-001), recording: account identifier; owner (individual or, for Service Accounts, Asset Owner); systems and privilege level; account type (personal admin, Service Account, built-in, Break-glass, cloud root/owner); whether vaulted; whether JIT-eligible or standing; and last review date.
- **SEC-005.5.1.2** Automated discovery of privileged groups, roles and local administrator accounts SHALL run at least weekly on directories, Cloud Service tenants, SaaS tenants and servers, and SHALL be reconciled to the inventory. Unrecorded Privileged Accounts SHALL be disabled or brought under PAM control within the time in SEC-005.7.12.
- **SEC-005.5.1.3** The number of individuals holding each class of privileged role SHALL be kept to the minimum needed for operations and resilience. The maximum number of permanently assigned highest-level tenant administrators per Cloud Service or SaaS tenant is set in SEC-005.7.9.

### 5.2 Separate administrative accounts

- **SEC-005.5.2.1** Each individual who requires privileged access SHALL be issued a dedicated administrative account, separate from their standard account. Privileged rights SHALL NOT be assigned to standard accounts.
- **SEC-005.5.2.2** Administrative accounts SHALL NOT have mailboxes, SHALL NOT be used for web browsing, email, messaging or document editing, and SHALL NOT be licensed for productivity applications.
- **SEC-005.5.2.3** Administrative accounts SHALL be scoped by tier: accounts that administer identity infrastructure, PAM, and security tooling (Tier 0) SHALL NOT be used to administer servers or applications, and server and application administrative accounts SHALL NOT be used to administer Endpoints.
- **SEC-005.5.2.4** Administrative accounts in Cloud Services and SaaS administering production SHALL be cloud-only identities or identities sourced from a directory that is not itself administered by those cloud accounts, so that compromise of one environment does not grant control of the other. [DECISION REQUIRED: Whether cloud administrative identities are cloud-only or synchronized from the on-premises directory. Recommended default: cloud-only for highest-privilege tenant roles]
- **SEC-005.5.2.5** Administrative accounts SHALL authenticate using phishing-resistant MFA as required by SEC-004.

### 5.3 PAM vaulting

- **SEC-005.5.3.1** The Organization SHALL operate a PAM system that stores Privileged Account credentials in an encrypted vault, using keys managed under SEC-006, and brokers privileged sessions.
- **SEC-005.5.3.2** The following credentials SHALL be held in the PAM vault: built-in and local administrator accounts; root accounts; network device and appliance administrative credentials; Break-glass Account credentials; privileged Service Account credentials; database owner accounts; and Cloud Service root or owner credentials where a credential exists.
- **SEC-005.5.3.3** Vaulted credentials for shared built-in accounts SHALL be checked out only through an approved request, attributed to the requesting individual, and rotated automatically after each check-in or at the end of the checkout period, whichever is earlier.
- **SEC-005.5.3.4** Vaulted credentials that are not rotated after each use SHALL be rotated at the frequency in SEC-005.7.7. Lengths and randomness for vaulted passwords are in SEC-004.
- **SEC-005.5.3.5** Local administrator passwords on Endpoints and servers SHALL be unique per device and rotated automatically by the PAM system or an equivalent local administrator password solution.
- **SEC-005.5.3.6** Privileged Service Account credentials SHALL be retrieved programmatically from the vault or a secrets manager at run time and SHALL NOT be stored in code or configuration (SEC-004.5.10).
- **SEC-005.5.3.7** Administrative access to the PAM system itself SHALL be restricted to named Tier 0 administrators, require phishing-resistant MFA, and be subject to dual approval for changes to vault policy, safe permissions or rotation settings.
- **SEC-005.5.3.8** The PAM system SHALL be deployed for availability consistent with Recovery Tier 0 under RSK-004, with Break-glass access to it tested under section 5.7.

### 5.4 Just-in-Time access

- **SEC-005.5.4.1** Privileged roles SHALL be granted through JIT elevation, with no standing assignment, except: Break-glass Accounts; Service Accounts whose function requires persistent privilege; and roles listed with justification in the Standing-Privilege Register approved by the CISO.
- **SEC-005.5.4.2** Each JIT grant SHALL be limited to max 8 hours per grant and SHALL be revoked automatically at expiry.
- **SEC-005.5.4.3** Each JIT request SHALL record a business justification and, where applicable, a change or incident reference (SEC-013, RES-002). Elevation to Tier 0 roles, to roles on systems holding Restricted data, and to `[PCI]` CDE or `[SOX]` Financially Significant System administrative roles SHALL require approval by a second individual (the System Owner or a delegated approver) before activation. Elevation to other privileged roles MAY be self-activated after MFA re-authentication if pre-approved eligibility exists.
- **SEC-005.5.4.4** Eligibility for a JIT role SHALL be requested and approved under SEC-003.5.4 and SHALL be included in privileged Access Reviews.
- **SEC-005.5.4.5** The Standing-Privilege Register SHALL be reviewed by the CISO at the privileged access review frequency in SEC-005.7.1.

### 5.5 Session management and recording

- **SEC-005.5.5.1** Interactive privileged sessions to servers, network devices, databases, hypervisors and Cloud Service management consoles holding Restricted data or in `[PCI]` CDE or `[SOX]` Financially Significant System scope SHALL be brokered through the PAM system and recorded (video or keystroke and command capture, plus metadata).
- **SEC-005.5.5.2** Privileged sessions on other systems SHALL be brokered through the PAM system and SHALL at minimum log session metadata (who, what target, when, duration, source).
- **SEC-005.5.5.3** Direct privileged access that bypasses the PAM system (for example, direct RDP or SSH to a target from a workstation) SHALL be blocked by network controls (SEC-007) wherever technically feasible, and attempted bypass SHALL be alerted to the SOC.
- **SEC-005.5.5.4** Session recordings and PAM logs SHALL be forwarded to or indexed by the SIEM, protected from modification and deletion by the administrators recorded, and retained as security logs under CMP-004.
- **SEC-005.5.5.5** The SOC Manager SHALL review a sample of recorded privileged sessions at the frequency and sample size in SEC-005.7.10, prioritizing sessions flagged by analytics (commands on high-risk lists, sessions outside change windows, sessions without change references).
- **SEC-005.5.5.6** Privileged sessions SHALL be subject to the idle timeout in SEC-004 and SHALL be terminable in real time by the SOC.
- **SEC-005.5.5.7** All privileged actions SHALL be logged under SEC-012. `[PCI]` All actions taken by any individual with administrative access, including interactive use of application or system accounts, SHALL be logged (PCI DSS 10.2.1.2).

### 5.6 Privileged Access Workstations

- **SEC-005.5.6.1** Tier 0 administration and administration of Cloud Service tenants, `[PCI]` CDE components and systems holding Restricted data SHALL be performed only from Privileged Access Workstations (PAWs).
- **SEC-005.5.6.2** PAWs SHALL be Organization-owned, managed Endpoints hardened to a dedicated Configuration Baseline under SEC-013, with: application allowlisting enforced (SEC-001.5.8.3); no email client, general web browsing or productivity applications; local administrator rights removed from the user; full-disk Encryption (SEC-006); EDR (SEC-008); and outbound network access restricted to administrative targets, the PAM system and required update services.
- **SEC-005.5.6.3** A PAW SHALL be a physical device or a hardened virtual machine whose host is itself at least as trusted as the PAW. A virtual PAW SHALL NOT run on a standard-user Endpoint.
- **SEC-005.5.6.4** Conditional access policies SHALL restrict sign-in of Tier 0 and cloud tenant administrative accounts to PAWs by device identity.
- **SEC-005.5.6.5** Other privileged administration SHALL be performed from managed, compliant Endpoints (SEC-008) through the PAM system. Privileged access from BYOD SHALL NOT be permitted.

### 5.7 Break-glass Accounts

- **SEC-005.5.7.1** Break-glass Accounts SHALL exist for the Identity Provider, each Cloud Service tenant or organization, the PAM system, and each Recovery Tier 0 system that would otherwise be unrecoverable if normal privileged access paths failed. The number per platform SHALL NOT exceed the value in SEC-005.7.11.
- **SEC-005.5.7.2** Break-glass Account credentials SHALL be stored under dual control and split knowledge: for example, the password split between two sealed envelopes or vault safes held by different custodians, and phishing-resistant hardware authenticators held in a locked safe with access logged. No single individual SHALL be able to use a Break-glass Account alone.
- **SEC-005.5.7.3** Break-glass Accounts SHALL be excluded from conditional access policies that could themselves cause lockout, SHALL NOT be dependent on the federated Identity Provider they are intended to recover, and SHALL be named so that they are identifiable in logs.
- **SEC-005.5.7.4** Every Break-glass Account sign-in SHALL generate a Critical alert to the SOC under SEC-012.
- **SEC-005.5.7.5** Break-glass Accounts SHALL be tested quarterly, and every use SHALL be reviewed within 1 business day. The test SHALL confirm that the credential works, that alerting fires, and that the credential is rotated and re-sealed after the test.
- **SEC-005.5.7.6** Every use (other than a test) SHALL be documented with the reason, the individuals involved, the actions taken and the incident or change reference; the review SHALL be performed by the CISO or delegate who was not a participant, and the credential SHALL be rotated and re-sealed before the review is closed.
- **SEC-005.5.7.7** `[HIPAA]` Break-glass procedures for systems holding ePHI implement the emergency access procedure under §164.312(a)(2)(ii) and are documented in CMP-008.

### 5.8 Cloud root and owner accounts

- **SEC-005.5.8.1** Cloud Service root, management account owner, tenant global administrator and organization owner accounts SHALL be used only for tasks that cannot be performed by a lesser role, as listed in the Cloud Service provider's documentation and recorded in the Organization's cloud administration procedure (SEC-009).
- **SEC-005.5.8.2** Cloud root accounts SHALL have no programmatic access keys. Any existing root access keys SHALL be deleted.
- **SEC-005.5.8.3** Cloud root and owner accounts SHALL be protected by at least two registered phishing-resistant hardware authenticators, held under the dual-control arrangements in SEC-005.5.7.2, and SHALL be registered with an Organization-controlled distribution-list email address and telephone number not tied to any individual.
- **SEC-005.5.8.4** Organization-level guardrails (for example, service control policies or equivalent) SHALL deny root or owner activity in member accounts except for listed root-only tasks, where the Cloud Service supports it.
- **SEC-005.5.8.5** Every cloud root or owner sign-in SHALL generate a Critical alert to the SOC under SEC-012 and be reviewed within 1 business day as for Break-glass Accounts.

### 5.9 Privileged Service Accounts

- **SEC-005.5.9.1** Service Accounts with privileged entitlements SHALL meet SEC-003.5.9 and, in addition: have credentials vaulted or replaced by short-lived workload identity (SEC-004.5.11.1); be restricted to the source hosts or workloads that need them; and be monitored for interactive use and anomalous activity.
- **SEC-005.5.9.2** Membership of Tier 0 groups by Service Accounts SHALL require CISO approval and be listed in the Standing-Privilege Register.

### 5.10 Third-Party privileged access

- **SEC-005.5.10.1** Third-Party privileged access SHALL be brokered exclusively through the PAM system with session recording, SHALL be JIT, and SHALL be approved per session by the System Owner.
- **SEC-005.5.10.2** Third-Party privileged sessions to Restricted, `[PCI]` CDE or `[SOX]` systems SHALL be monitored in real time or reviewed within 1 business day of the session by the System Owner.

### 5.11 Privileged access review

- **SEC-005.5.11.1** Privileged access SHALL be reviewed quarterly using TPL-008, covering every Privileged Account, JIT eligibility, Standing-Privilege Register entry, Break-glass Account, cloud root or owner account, and privileged Service Account.
- **SEC-005.5.11.2** The reviewer SHALL be the System Owner, with the Head of Security Engineering reviewing Tier 0 roles. The reviewer SHALL confirm continued need, privilege scope, JIT versus standing status, and that the account owner has completed role-based training under PPL-002.
- **SEC-005.5.11.3** Review completion and remediation times follow SEC-003.7.8.
- **SEC-005.5.11.4** `[SOX]` Privileged access reviews for Financially Significant Systems SHALL include review of privileged activity logs for unauthorized changes to financial data or configuration, as specified in CMP-009.

### 5.12 Privileged access lifecycle

- **SEC-005.5.12.1** Privileged access SHALL be requested under SEC-003.5.4 and approved by the System Owner and the Head of Security Engineering (or delegate) for Tier 0 roles, and by the System Owner for other roles.
- **SEC-005.5.12.2** Workforce Members in privileged roles SHALL complete role-based training (PPL-002) before privileged access is granted, and rescreening under PPL-001 where applicable.
- **SEC-005.5.12.3** Privileged access SHALL be removed on role change or Separation within the times in SEC-003. All vaulted shared credentials the individual checked out in the preceding 90 days, and every other shared Secret the individual knew, SHALL be rotated by the System Owner within the time in SEC-005.7.16.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| Head of Security Engineering | Owns this Standard; operates the PAM system and privileged inventory; approves Tier 0 access; reviews Tier 0 roles; defines PAW baseline. |
| CISO | Approves this Standard; approves the Standing-Privilege Register and Tier 0 Service Account membership; reviews Break-glass and root use. |
| CIO | Implements separate admin accounts, local administrator password rotation and PAW provisioning. |
| CTO | Implements cloud root controls, guardrails and workload identity (SEC-009). |
| SOC Manager | Monitors privileged activity, Break-glass and root sign-ins; reviews session recording samples; terminates suspicious sessions. |
| Head of GRC | Tracks privileged access review completion; provides evidence for audit. |
| System Owner | Approves privileged access and JIT activations; reviews Third-Party privileged sessions; performs privileged access reviews. |
| Asset Owner | Owns privileged Service Accounts. |
| Break-glass custodians (Workforce Members designated by the CISO) | Hold split credentials and authenticators; participate in tests; log every access. |
| Workforce Member (privileged) | Uses admin accounts only for administration, only from PAWs where required, only through the PAM system. |
| Third Party | Uses only brokered, recorded, JIT privileged access. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| SEC-005.7.1 | Privileged access review | Quarterly |
| SEC-005.7.2 | Privileged elevation (just-in-time) | Max 8 hours per grant |
| SEC-005.7.3 | Break-glass accounts | Tested quarterly; every use reviewed within 1 business day |
| SEC-005.7.4 | MFA for privileged access | Phishing-resistant, per SEC-004 |
| SEC-005.7.5 | Standing privileged assignments outside the approved Standing-Privilege Register | 0 |
| SEC-005.7.6 | Rotation of shared built-in account credentials after checkout | After each check-in or end of checkout period, whichever is earlier |
| SEC-005.7.7 | Rotation of vaulted credentials not rotated after use (including privileged Service Accounts) | Every 90 days, and on suspected compromise or custodian departure |
| SEC-005.7.8 | Privileged account discovery | At least weekly |
| SEC-005.7.9 | Maximum permanently assigned highest-level administrators per Cloud Service or SaaS tenant (excluding Break-glass) | 0 standing; at most 5 JIT-eligible individuals |
| SEC-005.7.10 | Privileged session recording review | Weekly; at least 10 sessions or 5% of recorded sessions, whichever is greater, plus 100% of analytics-flagged sessions |
| SEC-005.7.11 | Break-glass Accounts per platform | 2 |
| SEC-005.7.12 | Remediation of unrecorded Privileged Accounts found by discovery | Within 2 business days |
| SEC-005.7.13 | Cloud root programmatic access keys | 0 |
| SEC-005.7.14 | Review of root/owner sign-in | Within 1 business day |
| SEC-005.7.15 | Session recording and PAM log retention | Per CMP-004 (security logs) |
| SEC-005.7.16 | Rotation of shared credentials and Secrets after a privileged user's role change or Separation | Within 5 business days |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Privileged Accounts vaulted or under JIT | 100% | Monthly | Head of Security Engineering |
| Individuals with privileged rights on their standard account | 0 | Monthly | Head of Security Engineering |
| Standing privileged assignments not on the register | 0 | Monthly | Head of Security Engineering |
| Privileged access reviews completed on schedule | 100% | Quarterly | Head of GRC |
| Break-glass tests completed and passed | 100% | Quarterly | Head of Security Engineering |
| Break-glass and root uses reviewed within 1 business day | 100% | Monthly | CISO |
| Tier 0 and cloud tenant admin sign-ins from non-PAW devices | 0 | Monthly | SOC Manager |
| Privileged sessions bypassing PAM (detected) | 0 | Monthly | SOC Manager |
| Session recording samples reviewed | 100% of required sample | Weekly | SOC Manager |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following SHALL NOT receive an Exception: phishing-resistant MFA for privileged access;
dual control over Break-glass Account credentials (SEC-005.5.7.2); alerting on Break-glass
and cloud root sign-in (SEC-005.5.7.4, SEC-005.5.8.5); and deletion of cloud root access
keys (SEC-005.5.8.2).

## 10. Enforcement

Non-compliance is handled under CMP-007.

Use of a Privileged Account outside an approved purpose, bypass of the PAM system, or misuse
of Break-glass Accounts SHALL result in immediate suspension of privileged access by the
CISO pending investigation, and SHALL be handled as a Security Incident under RES-001.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| SEC-005.5.1 – 5.2 Inventory and separate accounts | A.8.2, A.5.16 | PR.AA-01, PR.AA-05 | AC-2, AC-6 | 5.4, 6.6 | CC6.1, CC6.3 | DSS05.04 | `[PCI]` 7.2.1, 7.2.2, 8.2.1 |
| SEC-005.5.3 PAM vaulting | A.8.2, A.5.17 | PR.AA-01 | IA-5, AC-2 | 5.2, 5.5 | CC6.1 | DSS05.04 | `[PCI]` 8.3.2, 8.6.2, 8.6.3 |
| SEC-005.5.4 JIT | A.8.2 | PR.AA-05 | AC-2, AC-6 | 6.8 | CC6.3 | DSS05.04 | `[PCI]` 7.2.2 |
| SEC-005.5.5 Session recording | A.8.15, A.8.16 | DE.CM-03, PR.PS-04 | AU-2, AU-12, AU-14 | 8.2, 8.5 | CC7.2 | DSS05.07 | `[PCI]` 10.2.1.2; `[HIPAA]` §164.312(b); `[SOX]` §404 |
| SEC-005.5.6 PAWs | A.8.2, A.8.1 | PR.PS-01, PR.AA-05 | AC-6, SC-7 | 12.8 | CC6.1, CC6.8 | DSS05.03 | — |
| SEC-005.5.7 – 5.8 Break-glass and cloud root | A.8.2, A.5.29 | PR.AA-05, RC.RP-01 | AC-2, AC-6, CP-2 | 5.4, 6.5 | CC6.1, A1.2 | DSS04, DSS05 | `[HIPAA]` §164.312(a)(2)(ii) |
| SEC-005.5.9 – 5.10 Service Accounts, Third Parties | A.5.19, A.8.2 | GV.SC-05, PR.AA-05 | AC-6, IA-9, PS-7 | 5.5, 6.5 | CC6.1, CC9.2 | APO10, DSS05 | `[PCI]` 8.2.7, 8.6.1 |
| SEC-005.5.11 – 5.12 Review and lifecycle | A.5.18, A.8.2 | PR.AA-05 | AC-2, AC-6 | 5.4, 6.2 | CC6.2, CC6.3 | DSS05.04 | `[PCI]` 7.2.4, 7.2.5.1; `[SOX]` §404 |

## 12. Related documents

GOV-001, GOV-006, RSK-004, CMP-003, CMP-004, CMP-007, CMP-008, CMP-009, SEC-001, SEC-003,
SEC-004, SEC-006, SEC-007, SEC-008, SEC-009, SEC-012, SEC-013, SEC-019, RES-001, RES-002,
PPL-001, PPL-002, TPL-008

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Head of Security Engineering | | | |
| Approver: CISO | | | |
