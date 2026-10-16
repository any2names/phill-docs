# SEC-003 — Identity & Access Management Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | SEC-003 |
| Title | Identity & Access Management Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Information Security Officer (CISO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-001, GOV-006, RSK-003, CMP-004, CMP-008, CMP-009, SEC-001, SEC-002, SEC-004, SEC-005, SEC-010, SEC-012, SEC-019, PPL-001, TPL-008 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CISO | Initial release |

## 3. Purpose

This Policy sets the Organization's requirements for managing digital identities and the
access rights attached to them across their full lifecycle, so that only authorized Users
have access to Information Systems and data, with no more access than their duties require,
for no longer than required. Authentication mechanisms are specified in SEC-004 and
Privileged Account controls in SEC-005; this Policy governs identity lifecycle, access
authorization and review for all accounts.

## 4. Scope

| Dimension | In scope |
|---|---|
| People | All Workforce Members, Third-Party personnel, and any other individual granted an account on an Organization Information System |
| Systems | All Information Systems, Cloud Services, SaaS applications, network devices, databases, directories and Identity Providers that the Organization owns, operates or subscribes to, including customer-facing systems where Workforce Members hold administrative or support access |
| Data | All data at every Classification Level (SEC-002) accessed through those accounts |
| Identities | Workforce Member accounts, Third-Party accounts, Privileged Accounts (further governed by SEC-005), Service Accounts, Break-glass Accounts (SEC-005), and machine identities used for system-to-system access |
| Locations | All locations from which access is made, including remote access |
| Third parties | Third Parties whose personnel access Organization systems, and Third Parties that operate identity or access services for the Organization |

Out of scope: identities of the Organization's customers and end users of its products, which
are governed by product security requirements in SEC-010, except where those identities are
held in systems within this scope.

## 5. Policy statements

### 5.1 Identity principles

- **SEC-003.5.1.1** Every User SHALL have a unique identifier that is attributable to one individual or, for a Service Account, to one Asset Owner. Identifiers SHALL NOT be reassigned to another individual.
- **SEC-003.5.1.2** Access SHALL be granted on the basis of Least Privilege and Need to Know, and SHALL be authorized before it is provisioned.
- **SEC-003.5.1.3** The Organization SHALL maintain an authoritative identity source for Workforce Members, fed from the human resources system of record owned by the CHRO, and an authoritative record of Third-Party personnel, fed from the sponsoring process in section 5.10.
- **SEC-003.5.1.4** Access to Information Systems SHALL be integrated with the Organization's central Identity Provider and SSO wherever the system supports it. Authentication requirements, including MFA, are in SEC-004.
- **SEC-003.5.1.5** Every account SHALL be recorded in the Asset Inventory as an identity asset under SEC-001, linked to its owner.
- **SEC-003.5.1.6** Access SHALL be granted in a manner that enforces the Segregation of Duties rules in GOV-001. Conflicting role combinations defined in the SoD rule set SHALL be blocked at provisioning or approved as an Exception under CMP-003 with a documented mitigating control.

### 5.2 Joiner

- **SEC-003.5.2.1** A Workforce Member account SHALL be created only on receipt of a confirmed hire or engagement record from the authoritative identity source.
- **SEC-003.5.2.2** Before an account is enabled, the individual's identity SHALL be verified against a government-issued photo identity document, in person or by a remote identity-proofing process equivalent to NIST SP 800-63A Identity Assurance Level 2, and pre-employment screening SHALL be complete where required by PPL-001.
- **SEC-003.5.2.3** Before access to any Information System is granted, the Workforce Member SHALL complete policy attestation under GOV-002. Access to Restricted data additionally requires completion of training under PPL-002.
- **SEC-003.5.2.4** Initial access SHALL be limited to the Birthright Role for the individual's job function and location as defined in the Role Catalogue (section 5.5). Any access beyond the Birthright Role SHALL be requested under section 5.4.
- **SEC-003.5.2.5** Initial authenticators SHALL be issued in accordance with SEC-004.
- **SEC-003.5.2.6** Accounts SHALL NOT be enabled earlier than the time in SEC-003.7.11 before the individual's start date.

### 5.3 Mover

- **SEC-003.5.3.1** A change in job function, department, manager, location or employment type recorded in the authoritative identity source SHALL trigger a mover event.
- **SEC-003.5.3.2** On a mover event, the Birthright Role SHALL be updated automatically to the new job function, and all access not part of the new Birthright Role SHALL be reviewed by the new Line Manager.
- **SEC-003.5.3.3** Access no longer required for the new role SHALL be removed within the time in SEC-003.7.5. Access to Restricted data and to `[SOX]` Financially Significant Systems that is not required for the new role SHALL be removed on the effective date of the move.
- **SEC-003.5.3.4** Access retained across a move for a handover period SHALL be approved by the Data Owner or System Owner and SHALL expire automatically no later than the time in SEC-003.7.5.
- **SEC-003.5.3.5** Where the individual held Asset Owner, Data Owner or System Owner responsibilities, the reassignment required by SEC-001 SHALL be completed before the old access is removed.

### 5.4 Access request and approval

- **SEC-003.5.4.1** All access beyond the Birthright Role SHALL be requested through the Organization's access request system, which SHALL record: requester; recipient; system; role or entitlement; business justification; requested duration; approvers; approval timestamps; and provisioning timestamp.
- **SEC-003.5.4.2** Access SHALL be approved by, at minimum, the approvers in the table below. Approvals SHALL be recorded in the access request system; verbal or email-only approvals SHALL NOT be accepted.

| Access requested | Required approvers |
|---|---|
| Role or entitlement on a system holding Public or Internal data | Line Manager |
| Role or entitlement on a system holding Confidential data | Line Manager and System Owner (or Data Owner for data-level access) |
| Role or entitlement on a system holding Restricted data, or a `[SOX]` Financially Significant System | Line Manager and Data Owner; plus System Owner where distinct |
| Privileged Account or privileged role | As required by SEC-005 |
| Third-Party personnel access | Organization sponsor (section 5.10) and System Owner; plus Data Owner for Confidential or Restricted data |
| Access creating an SoD conflict under GOV-001 | Exception approval under CMP-003 in addition to the above |

- **SEC-003.5.4.3** No individual SHALL approve their own access request, or provision access they have approved.
- **SEC-003.5.4.4** Access SHALL be provisioned only as approved. Provisioning SHALL be automated from the access request system wherever the target system supports it; manual provisioning SHALL reference the approved request identifier.
- **SEC-003.5.4.5** Access to Restricted data and to `[PCI]` CDE system components SHALL be time-limited to a maximum duration of SEC-003.7.10 and re-requested at expiry, unless it is part of a Birthright Role.
- **SEC-003.5.4.6** The Head of Security Engineering SHALL reconcile, at the frequency in SEC-003.7.12, entitlements on each system holding Restricted data and each `[SOX]` Financially Significant System against approved requests and role definitions. Entitlements without a corresponding approval SHALL be removed within 5 business days of detection or retroactively approved, and each case SHALL be investigated for cause.

### 5.5 Role-based access

- **SEC-003.5.5.1** Access SHALL be assigned through roles defined in a Role Catalogue wherever the target system supports role or group assignment. Direct assignment of individual entitlements SHALL be used only where no role exists and SHALL be recorded with justification.
- **SEC-003.5.5.2** Each role in the catalogue SHALL record: role name; owning System Owner; constituent entitlements; Classification Level of data accessible; birthright eligibility criteria (if any); SoD conflicts; and date of last review.
- **SEC-003.5.5.3** The System Owner SHALL review the definition of each role on their system at the frequency in SEC-003.7.9, confirming that entitlements are still the minimum required.
- **SEC-003.5.5.4** Changes to role definitions SHALL be approved by the System Owner and, for roles granting access to Restricted data or privileged functions, by the Head of Security Engineering.

### 5.6 Least Privilege and Need to Know

- **SEC-003.5.6.1** Default access to every Information System SHALL be deny; access is granted only by explicit authorization.
- **SEC-003.5.6.2** Access to Confidential and Restricted data SHALL be granted only where the individual has a Need to Know for a specific assigned duty, as attested by the approving Data Owner.
- **SEC-003.5.6.3** Workforce Members SHALL use standard (non-privileged) accounts for all activities that do not require privileged access. Privileged Account separation is governed by SEC-005.
- **SEC-003.5.6.4** Access to production systems by developers SHALL be governed by SEC-010 and SEC-005; access to source code repositories SHALL follow this Policy and SEC-010.
- **SEC-003.5.6.5** `[HIPAA]` Access to ePHI SHALL be limited to the Minimum Necessary for the User's role, and emergency access procedures for ePHI SHALL follow SEC-005 (Break-glass Accounts) and CMP-008.
- **SEC-003.5.6.6** `[PCI]` Access to system components and CHD SHALL be assigned based on job classification and function and the least privileges necessary (PCI DSS 7.2.1, 7.2.2); access to query repositories of stored CHD SHALL be restricted to applications and programmatic methods, with direct User query access limited to database administrators (PCI DSS 7.2.6).

### 5.7 Leaver

- **SEC-003.5.7.1** All access of a separating Workforce Member SHALL be revoked within the time in SEC-003.7.3. For involuntary Separations, access SHALL be revoked at or before the time the individual is notified.
- **SEC-003.5.7.2** The CHRO SHALL ensure that the Separation date and time are recorded in the human resources system of record no later than the Separation time, and, for involuntary Separations, that the CISO's delegate is notified before the individual is informed.
- **SEC-003.5.7.3** Revocation SHALL include: disabling the identity in the central Identity Provider; terminating active sessions and refresh tokens; revoking or disabling accounts on systems not integrated with the central Identity Provider; revoking VPN, remote access and certificate-based credentials; removing MFA registrations; and rotating any shared Secret the individual had access to under SEC-005.
- **SEC-003.5.7.4** Disabled accounts SHALL be deleted or permanently de-provisioned within the time in SEC-003.7.7, unless subject to a Legal Hold or required for evidence under CMP-004, in which case the account SHALL remain disabled.
- **SEC-003.5.7.5** Mailboxes and files of a leaver SHALL be retained under CMP-004.5.2.9 and SHALL be transferred to the Line Manager or Data Owner only as permitted by CMP-005 and with the approval of the Line Manager; access to them SHALL NOT be granted through the leaver's own account.
- **SEC-003.5.7.6** Return of physical assets is governed by PPL-001.
- **SEC-003.5.7.7** The times in SEC-003.7.3 (revocation on Separation) and SEC-003.7.5 (role change) apply to physical access credentials, including badges, keys and combinations, as well as to logical access. Physical access changes are performed under SEC-016.

### 5.8 Inactive and temporary accounts

- **SEC-003.5.8.1** User accounts SHALL be disabled automatically after the inactivity period in SEC-003.7.6. Re-enabling SHALL require a new access request approved under section 5.4.
- **SEC-003.5.8.2** Accounts for Workforce Members on leave of absence longer than 30 days SHALL be disabled for the duration of the leave, on notification from the CHRO.
- **SEC-003.5.8.3** Every account for a contractor, temporary worker or Third Party SHALL have an expiry date no later than the end of the engagement and no later than the maximum in SEC-003.7.10 from creation or last renewal.
- **SEC-003.5.8.4** Accounts created for testing in production systems SHALL be approved by the System Owner, carry an expiry date, and be removed at the earlier of expiry or test completion.
- **SEC-003.5.8.5** Accounts of a Workforce Member suspended pending investigation (PPL-001, CMP-007) SHALL be disabled at the start of the suspension, on notification from the CHRO, and SHALL remain disabled for the period of suspension.

### 5.9 Service Account governance

- **SEC-003.5.9.1** Every Service Account SHALL have a named Asset Owner, a documented purpose, the systems it accesses, its entitlements, its credential type and storage location, and its rotation date recorded in the Asset Inventory under SEC-001.
- **SEC-003.5.9.2** Service Accounts SHALL be created only through an access request approved by the System Owner of each target system and, for Service Accounts with privileged entitlements, as required by SEC-005.
- **SEC-003.5.9.3** Service Accounts SHALL be granted only the entitlements required for their documented purpose. Membership of administrative groups SHALL be prohibited unless approved under SEC-005.
- **SEC-003.5.9.4** Service Accounts SHALL NOT be used for interactive login by individuals. Where a platform cannot technically prevent interactive login, interactive use SHALL be alerted to the SOC through SEC-012 and investigated. `[PCI]` Interactive use of system or application accounts SHALL be prevented unless needed for an exceptional circumstance, time-limited, approved and attributable to an individual (PCI DSS 8.6.1).
- **SEC-003.5.9.5** Workload identities with short-lived, automatically issued credentials (for example, cloud-native workload identity federation or managed identities) SHOULD be used in preference to Service Accounts with static credentials. Credential requirements are in SEC-004; vaulting and rotation of privileged Service Account credentials are in SEC-005.
- **SEC-003.5.9.6** Service Accounts SHALL be included in Access Reviews at the frequency for the system they access (SEC-003.7.1), and the Asset Owner SHALL confirm continued need and entitlement scope. Service Accounts with no authentication activity in the period in SEC-003.7.6 SHALL be disabled after confirmation with the Asset Owner, unless documented as used only for annual or disaster recovery processes.
- **SEC-003.5.9.7** When a Service Account's Asset Owner separates or changes role, ownership SHALL be reassigned under SEC-001.5.4.5 before the leaver's access is revoked.

### 5.10 Third-Party access

- **SEC-003.5.10.1** Third-Party personnel SHALL be granted access only where: the Third Party has been assessed and approved under RSK-003; a contract with security obligations is in force; and a named Organization sponsor, who is a Workforce Member at manager level or above, accepts accountability for the access.
- **SEC-003.5.10.2** Each Third-Party individual SHALL have an individually attributable account. Accounts shared among Third-Party personnel SHALL NOT be issued.
- **SEC-003.5.10.3** Third-Party accounts SHALL expire under SEC-003.5.8.3, and the sponsor SHALL re-confirm need at each renewal.
- **SEC-003.5.10.4** The sponsor SHALL notify the Organization through the access request system within 1 business day of learning that a Third-Party individual no longer requires access; access SHALL then be revoked within the time in SEC-003.7.3. Contracts SHALL require the Third Party to notify the sponsor of personnel separations within 1 business day.
- **SEC-003.5.10.5** Third-Party remote access SHALL be enabled only for the time needed and disabled when not in use, and SHALL be monitored under SEC-012 while in use. `[PCI]` Third-Party remote access to the CDE SHALL meet PCI DSS 8.2.7.
- **SEC-003.5.10.6** Third-Party access to Privileged Accounts SHALL be brokered through the PAM controls in SEC-005.
- **SEC-003.5.10.7** Third-Party accounts SHALL be included in Access Reviews, and the sponsor SHALL be a reviewer of each Third-Party account they sponsor.

### 5.11 Shared and generic accounts

- **SEC-003.5.11.1** Shared, group or generic accounts used by more than one individual SHALL NOT be created or used.
- **SEC-003.5.11.2** Where a system provides a built-in or default account that cannot be removed, the account SHALL be disabled, or, if it must remain enabled, its credentials SHALL be vaulted and its use brokered and attributed to an individual under SEC-005.
- **SEC-003.5.11.3** Shared mailboxes and shared resources SHALL be accessed through delegated permissions granted to individual accounts, not by signing in to the shared resource directly.
- **SEC-003.5.11.4** `[PCI]` Any use of group, shared or generic IDs within the CDE SHALL be limited to exceptional circumstances, time-limited, documented with business justification, explicitly approved by management, and each action attributable to an individual before access is granted (PCI DSS 8.2.2). Such use requires an approved Exception under CMP-003.
- **SEC-003.5.11.5** Vendor-supplied default accounts and passwords SHALL be changed or disabled before a system enters production (SEC-013 Configuration Baselines).

### 5.12 Access Reviews

- **SEC-003.5.12.1** Access Reviews SHALL be performed at the frequencies in SEC-003.7.1 and recorded using TPL-008. Access Reviews of Privileged Accounts are performed at the frequency in SEC-005 and MAY be combined with the Access Review of the same system.
- **SEC-003.5.12.2** Each Access Review SHALL cover all accounts on the system — Workforce Member, Third-Party, Service and privileged accounts — and each role or entitlement assigned to them.
- **SEC-003.5.12.3** The account population used for an Access Review SHALL be extracted directly from the target system (or its authoritative identity source), and the extraction method, date and record count SHALL be recorded to evidence completeness and accuracy. `[SOX]` Population evidence SHALL meet the Information Produced by the Entity (IPE) requirements in CMP-009.
- **SEC-003.5.12.4** The reviewer SHALL be the Line Manager, the System Owner or the Data Owner, as designated for the system in the Access Review schedule. A reviewer SHALL NOT review their own access; such accounts SHALL be reviewed by the reviewer's Line Manager or the System Owner.
- **SEC-003.5.12.5** The reviewer SHALL record a decision for each account and entitlement (retain, modify, revoke) with a justification for retained access to Restricted data and for any exception.
- **SEC-003.5.12.6** Each Access Review SHALL be completed within the time in SEC-003.7.8. Access marked for revocation or modification SHALL be changed within the time in SEC-003.7.8, and the change SHALL be verified against the target system before the review is closed.
- **SEC-003.5.12.7** Accounts that cannot be matched to a current Workforce Member, active Third-Party sponsor or Service Account owner SHALL be disabled within 1 business day of identification and investigated.
- **SEC-003.5.12.8** The Head of GRC SHALL maintain the Access Review schedule listing each in-scope system, its Classification Level, regulatory scope, frequency, reviewer, and due dates; incomplete or late reviews SHALL be escalated to the CISO.
- **SEC-003.5.12.9** Completed Access Reviews, including population evidence and remediation evidence, SHALL be retained per CMP-004.

### 5.13 Access to identity infrastructure

- **SEC-003.5.13.1** Identity Providers, directories, the access request system, and the PAM system are Restricted systems. Administrative access to them is governed by SEC-005.
- **SEC-003.5.13.2** All account creation, modification, privilege assignment, disablement and deletion events SHALL be logged and forwarded to the SIEM under SEC-012.
- **SEC-003.5.13.3** The CISO SHALL maintain an inventory of authentication and authorization systems, including those hosted by Third Parties, and review it at least every 12 months.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CISO | Owns this Policy; owns identity governance; receives escalations of late Access Reviews; maintains the inventory of authentication and authorization systems. |
| ISSC | Approves this Policy; reviews Access Review completion metrics. |
| CHRO | Owns the authoritative human resources record; records joiner, mover, leaver and leave events in the human resources system of record no later than their effective date and time; notifies the CISO's delegate before involuntary Separations. |
| CIO | Operates the Identity Provider, directories and provisioning integrations; executes revocations. |
| Head of Security Engineering | Defines technical identity controls; approves role changes for Restricted or privileged roles; performs entitlement reconciliation. |
| Head of GRC | Maintains the Access Review schedule; tracks completion; provides Access Review evidence to auditors. |
| SOC Manager | Monitors identity events and Service Account interactive use; investigates orphaned accounts. |
| Internal Audit Director | Tests the design and operating effectiveness of access controls under CMP-002. |
| System Owner | Approves access to their system; maintains role definitions; performs or assigns Access Reviews. |
| Data Owner | Approves access to Confidential and Restricted data; attests Need to Know; performs Access Reviews where designated. |
| Asset Owner | Owns Service Accounts and confirms their need and scope. |
| Line Manager | Requests and approves access for direct reports; reviews mover access; performs Access Reviews where designated. |
| Workforce Member | Uses only their own accounts; does not share credentials; reports suspected unauthorized access. |
| Third Party | Notifies the sponsor of personnel changes; ensures its personnel comply with this Policy. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| SEC-003.7.1 | User Access Review frequency | Quarterly for systems holding Restricted data and `[SOX]` financially significant systems; every 6 months for all others |
| SEC-003.7.2 | Privileged Access Review frequency | Per SEC-005 |
| SEC-003.7.3 | Access revocation on separation | Within 4 hours of the separation time; involuntary separations at or before notification |
| SEC-003.7.4 | Third-Party personnel separation notice to sponsor (contractual) | Within 1 business day |
| SEC-003.7.5 | Access change on role change | Within 5 business days |
| SEC-003.7.6 | Inactive accounts | Disabled after 90 days of inactivity |
| SEC-003.7.7 | Deletion or permanent de-provisioning of disabled leaver accounts | Within 90 days of disablement, unless under Legal Hold or required as evidence |
| SEC-003.7.8 | Access Review completion; remediation of review findings | Review completed within 30 days of launch · Revocations and modifications completed within 5 business days of the reviewer's decision |
| SEC-003.7.9 | Role definition review by System Owner | Every 12 months |
| SEC-003.7.10 | Maximum account validity for contractor, temporary and Third-Party accounts; maximum duration of non-birthright access to Restricted data or `[PCI]` CDE | 12 months, or engagement end if sooner |
| SEC-003.7.11 | Earliest account enablement before start date | 3 business days |
| SEC-003.7.12 | Entitlement-to-approval reconciliation for Restricted and `[SOX]` systems | Quarterly |
| SEC-003.7.13 | Orphaned accounts disabled after identification | Within 1 business day |
| SEC-003.7.14 | Shared or generic accounts | 0, except `[PCI]` 8.2.2 cases under approved Exception |
| SEC-003.7.15 | Authentication, MFA, lockout and session values | Per SEC-004 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Leaver accounts revoked within 4 hours of Separation time | 100% | Monthly | CIO |
| Mover access changes completed within 5 business days | ≥ 98% | Monthly | CIO |
| Access Reviews completed on schedule | 100% | Quarterly | Head of GRC |
| Access Review revocations completed within 5 business days | 100% | Quarterly | Head of GRC |
| Accounts active > 90 days without login | 0 | Monthly | CIO |
| Orphaned accounts identified / disabled within 1 business day | 100% disabled within target | Monthly | SOC Manager |
| Entitlements without approval found in reconciliation | 0 | Quarterly | Head of Security Engineering |
| Service Accounts with named owner and recorded purpose | 100% | Quarterly | CIO |
| Shared or generic accounts in use without approved Exception | 0 | Quarterly | CISO |
| Applications integrated with SSO (of those supporting it) | 100% | Quarterly | CIO |
| SoD conflicts provisioned without approved Exception | 0 | Quarterly | Head of GRC |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following SHALL NOT receive an Exception: SEC-003.5.4.3 (no self-approval),
SEC-003.5.7.1 (revocation on Separation), and SEC-003.5.12 (Access Reviews) for systems
holding Restricted data or `[SOX]` Financially Significant Systems.

## 10. Enforcement

Non-compliance is handled under CMP-007.

Sharing of account credentials, use of another individual's account, or use of access for
purposes outside assigned duties SHALL be treated as a violation under CMP-007 and MAY result
in immediate suspension of access by the CISO pending investigation.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| SEC-003.5.1 Identity principles | A.5.15, A.5.16 | PR.AA-01, PR.AA-05 | AC-1, AC-2, IA-2, IA-4 | 5.1, 6.6, 6.7 | CC6.1, CC6.2 | DSS05.04 | `[PCI]` 8.2.1; `[HIPAA]` §164.312(a)(2)(i); `[SOX]` §404 |
| SEC-003.5.2 – 5.3 Joiner and mover | A.5.16, A.5.18, A.6.1 | PR.AA-01, PR.AA-02, PR.AA-05 | AC-2, IA-12, PS-3, PS-5 | 6.1 | CC6.2, CC6.3 | DSS05.04, APO07 | `[PCI]` 7.2.1, 8.2.4; `[HIPAA]` §164.308(a)(3)(ii)(B), (a)(4)(ii)(C) |
| SEC-003.5.4 – 5.6 Request, roles, Least Privilege | A.5.15, A.5.18, A.8.2, A.8.3 | PR.AA-05 | AC-3, AC-5, AC-6 | 6.1, 6.8 | CC6.1, CC6.3, CC5.2 | DSS05.04 | `[PCI]` 7.2.1, 7.2.2, 7.2.3, 7.2.6; `[HIPAA]` §164.308(a)(4)(ii)(B); §164.502(b) |
| SEC-003.5.7 – 5.8 Leaver, inactive, temporary | A.5.18, A.6.5 | PR.AA-01, PR.AA-05 | AC-2, PS-4 | 5.3, 6.2 | CC6.2, CC6.3 | DSS05.04 | `[PCI]` 8.2.5, 8.2.6; `[HIPAA]` §164.308(a)(3)(ii)(C) |
| SEC-003.5.9 Service Accounts | A.5.16, A.5.17 | PR.AA-01, PR.AA-03 | AC-2, IA-9 | 5.5 | CC6.1, CC6.2 | DSS05.04 | `[PCI]` 7.2.5, 7.2.5.1, 8.6.1 |
| SEC-003.5.10 Third-Party access | A.5.19, A.5.20 | GV.SC-05, PR.AA-05 | AC-2, PS-7, AC-17 | 6.1, 6.2 | CC6.2, CC9.2 | APO10, DSS05.04 | `[PCI]` 8.2.3, 8.2.7; `[HIPAA]` §164.308(b)(1) |
| SEC-003.5.11 Shared accounts | A.5.16 | PR.AA-01 | AC-2, IA-2 | 5.1 | CC6.1 | DSS05.04 | `[PCI]` 2.2.2, 8.2.2 |
| SEC-003.5.12 Access Reviews | A.5.18 | PR.AA-05, ID.IM-01 | AC-2, AC-6 | 5.1, 5.3 | CC6.2, CC6.3, CC4.1 | DSS05.04, MEA02 | `[PCI]` 7.2.4; `[SOX]` §404; `[HIPAA]` §164.308(a)(4)(ii)(C) |
| SEC-003.5.13 Identity infrastructure | A.5.15, A.8.15 | PR.AA-01, DE.CM-03 | AC-2, AU-2 | 6.6, 8.2 | CC6.1, CC7.2 | DSS05 | `[PCI]` 10.2.1.5 |

## 12. Related documents

ISP-000, GOV-001, GOV-002, GOV-006, RSK-003, CMP-002, CMP-003, CMP-004, CMP-005, CMP-007,
CMP-008, CMP-009, SEC-001, SEC-002, SEC-004, SEC-005, SEC-010, SEC-012, SEC-013, SEC-019,
PPL-001, PPL-002, TPL-008

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CISO | | | |
| Approver: ISSC Vice-Chair, on behalf of the ISSC (CISO recused as Document Owner under GOV-001.5.3.9) | | | |
