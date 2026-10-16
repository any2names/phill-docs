# SEC-009 — Cloud Security Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | SEC-009 |
| Title | Cloud Security Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Technology Officer (CTO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | SEC-001, SEC-002, SEC-003, SEC-004, SEC-005, SEC-006, SEC-007, SEC-010, SEC-011, SEC-012, SEC-013, SEC-018, SEC-019, RSK-003, RSK-004, CMP-005, RES-005 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CTO | Initial release |

## 3. Purpose

This Policy sets the Organization's mandatory requirements for the secure adoption,
configuration and operation of Cloud Services. It establishes the shared responsibility
model, the approved Cloud Service Provider list and onboarding route, the Landing Zone
and account structure, Infrastructure as Code and preventive guardrails, continuous posture
management, cloud identity federation, storage exposure controls, cloud logging, data
residency, and the Kubernetes and container security baseline.

## 4. Scope

| Dimension | In scope |
|---|---|
| People | All Workforce Members and Third Parties who procure, provision, configure, deploy to or administer Cloud Services for the Organization |
| Systems | All IaaS and PaaS accounts, subscriptions and projects; container platforms and Kubernetes clusters (managed and self-managed); serverless functions; and SaaS applications used for Organization business |
| Data | All Organization data stored in or processed by Cloud Services, at every Classification Level |
| Locations | All Cloud Service Provider regions and availability zones used by the Organization |
| Third parties | Cloud Service Providers and their Subprocessors; managed service providers operating cloud environments on the Organization's behalf |

Cloud virtual network zoning and traffic controls are governed by SEC-007. Application
development and pipeline requirements are governed by SEC-010. Cloud resilience and
recovery are governed by SEC-018 and RES-005.

## 5. Policy statements

### 5.1 Shared responsibility

- **SEC-009.5.1.1** For each approved Cloud Service Provider and each service model in use (IaaS, PaaS, SaaS), the CTO SHALL maintain a shared responsibility matrix that assigns every control area in this Policy to the Cloud Service Provider, the Organization, or both, and names the Organization's System Owner for each Organization responsibility.
- **SEC-009.5.1.2** The shared responsibility matrix SHALL be reviewed at least every 12 months and within 30 days of adopting a new service model or a new Cloud Service Provider.
- **SEC-009.5.1.3** Controls the Cloud Service Provider performs SHALL be evidenced by its current independent assurance reports (for example, a SOC 2 Type II examination report or ISO/IEC 27001 certificate), obtained and reviewed under RSK-003. Complementary user entity controls listed in those reports SHALL be mapped to Organization controls and assigned owners.
- **SEC-009.5.1.4** `[PCI]` For each Cloud Service Provider that is a third-party service provider for the CDE, the responsibility matrix SHALL meet PCI DSS 12.8.5 and SEC-019. `[HIPAA]` A Business Associate Agreement SHALL be in place before ePHI is placed in any Cloud Service.
- **SEC-009.5.1.5** `[PCI]` Where the Organization acts as a multi-tenant service provider, the CTO SHALL ensure that each customer's environment and account data are logically separated from other customers' and from the Organization's own, that customer access is limited to its own environment, that logging and incident response capabilities are available for each customer, and that the Organization supports forensic investigation of a suspected compromise of any customer (PCI DSS Appendix A1.1, A1.2).

### 5.2 Approved Cloud Service Providers and onboarding

- **SEC-009.5.2.1** Only Cloud Services listed on the approved Cloud Service list maintained by the CTO SHALL be used for Organization business. Use of any other Cloud Service is Shadow IT and SHALL be handled under SEC-001.
- **SEC-009.5.2.2** A new Cloud Service Provider or SaaS application SHALL be onboarded only after: a Third-Party risk assessment and tiering under RSK-003; a security review by the Head of Security Engineering; registration in the Asset Inventory (SEC-001) with a System Owner and Data Owner; and confirmation of data residency under section 5.10.
- **SEC-009.5.2.3** The approved list SHALL record, for each Cloud Service, the highest Classification Level of data permitted, the approved regions, and any conditions of use.
- **SEC-009.5.2.4** SaaS applications holding Confidential or Restricted data SHALL be integrated with the Organization's Identity Provider for single sign-on and, where supported, automated account provisioning and deprovisioning (SEC-003).
- **SEC-009.5.2.5** Cloud Services with access to Organization data through OAuth grants or API integrations SHALL be approved under this section before the grant is authorized. The Head of Security Engineering SHALL review third-party OAuth grants to Organization tenants at least every 6 months and revoke grants that are unapproved or unused for 90 days.
- **SEC-009.5.2.6** An exit plan covering data retrieval and deletion SHALL exist for every Cloud Service supporting a Recovery Tier 0 or Tier 1 process (RSK-004), maintained under RES-005.

### 5.3 Landing Zone and account structure

- **SEC-009.5.3.1** Each IaaS/PaaS Cloud Service Provider SHALL be operated through a Landing Zone: a centrally governed organization hierarchy (for example, organizations, management groups or folders) with guardrails inherited by every account, subscription or project.
- **SEC-009.5.3.2** Workloads SHALL be separated into distinct accounts, subscriptions or projects by environment (production, non-production, sandbox) and, for production, by System or business service. The Landing Zone SHALL include dedicated accounts for security tooling, centralized log archive, network connectivity and identity.
- **SEC-009.5.3.3** `[PCI]` CDE workloads SHALL run in dedicated accounts, subscriptions or projects scoped and segmented under SEC-019. `[SOX]` Financially Significant Systems SHALL run in production accounts whose change path is subject to CMP-009.
- **SEC-009.5.3.4** New accounts, subscriptions or projects SHALL be created only through the Landing Zone's automated account-vending process, which applies baseline guardrails, logging, CSPM onboarding and tagging before the account is released to its owner.
- **SEC-009.5.3.5** The cloud organization root or tenant owner credentials SHALL be protected as Break-glass Accounts under SEC-005, with Phishing-resistant MFA, no programmatic access keys, and alerts to the SOC on any use.
- **SEC-009.5.3.6** Every cloud resource SHALL carry the mandatory tags in SEC-009.7.4. Resources without mandatory tags SHALL be detected by CSPM and remediated within the remediation SLA in SEC-011 for a Low-severity finding.
- **SEC-009.5.3.7** Sandbox accounts SHALL NOT hold Confidential or Restricted data, SHALL NOT have network connectivity to production, and SHALL have automated budget limits and resource expiry.

### 5.4 Infrastructure as Code and guardrails

- **SEC-009.5.4.1** Production cloud infrastructure SHALL be defined in Infrastructure as Code (IaC) held in version control and deployed through an approved pipeline that meets SEC-010.
- **SEC-009.5.4.2** Manual changes to production cloud resources through the console or command line SHALL be prohibited, except Emergency Changes under SEC-013 and Break-glass Account use under SEC-005. Any such change SHALL be reconciled into IaC within 5 business days.
- **SEC-009.5.4.3** IaC SHALL be scanned for misconfiguration in the pipeline before deployment. Deployments introducing a Critical or High misconfiguration SHALL be blocked unless an Exception is approved under CMP-003.
- **SEC-009.5.4.4** Preventive guardrails SHALL be implemented as Policy-as-code at the organization level (for example, service control policies, organization policies or Azure Policy) and SHALL at minimum enforce: approved regions only; block of public access to storage at the account level; mandatory encryption at rest; prevention of disabling audit logging; prevention of creation of long-lived access keys for human Users; and restriction of root/owner account use.
- **SEC-009.5.4.5** Changes to organization-level guardrails SHALL be Normal Changes under SEC-013, approved by the Head of Security Engineering.
- **SEC-009.5.4.6** Drift between deployed resources and IaC SHALL be detected at least daily for production accounts, and unapproved drift SHALL be remediated or reconciled within 5 business days.
- **SEC-009.5.4.7** Golden images and base container images SHALL be built through a pipeline from approved Configuration Baselines (SEC-013) and SHALL be rebuilt at least every 30 days to include current security updates.

### 5.5 Cloud security posture management (CSPM/CNAPP)

- **SEC-009.5.5.1** Every IaaS/PaaS account, subscription and project SHALL be onboarded to the Organization's CSPM or CNAPP platform within 24 hours of creation.
- **SEC-009.5.5.2** The CSPM/CNAPP platform SHALL continuously assess configurations against a recognized benchmark (for example, CIS Foundations Benchmarks for the Cloud Service Provider) and the guardrails in this Policy, with a full assessment of every account at least daily.
- **SEC-009.5.5.3** CSPM/CNAPP findings SHALL be assigned a severity under the rating method in SEC-011 and remediated by the System Owner within the remediation SLA in SEC-011.
- **SEC-009.5.5.4** The following findings SHALL be raised as alerts to the SOC and triaged within the alert triage SLA in SEC-012: storage holding Confidential or Restricted data made publicly accessible; disabling of audit logging; creation of access keys for a root or owner account; and security-group rules that expose administrative ports to the internet.
- **SEC-009.5.5.5** SaaS applications holding Confidential or Restricted data SHOULD be monitored by a SaaS security posture management capability for misconfiguration, excessive sharing and unapproved third-party integrations.
- **SEC-009.5.5.6** Cloud workloads (virtual machines, containers, serverless functions) SHALL be scanned for Vulnerabilities as specified in SEC-011 and protected by EDR or workload protection as specified in SEC-008.

### 5.6 Identity federation and cloud access

- **SEC-009.5.6.1** Human access to cloud consoles, APIs and command-line tools SHALL be federated through the Organization's central Identity Provider with MFA (SEC-004). Local cloud User accounts for humans SHALL NOT be created, except Break-glass Accounts under SEC-005.
- **SEC-009.5.6.2** Human access SHALL use short-lived credentials issued through federation. Long-lived access keys for human Users SHALL NOT be issued.
- **SEC-009.5.6.3** Workloads SHALL authenticate to cloud APIs using platform-managed workload identities (for example, instance roles, managed identities or workload identity federation). Static Service Account keys SHALL be used only where no workload identity option exists, SHALL be stored in the secrets manager under SEC-010, and SHALL meet SEC-004.
- **SEC-009.5.6.4** Cloud IAM roles and policies SHALL be granted under Least Privilege. Wildcard permissions on all actions and all resources SHALL NOT be granted to any principal other than Break-glass Accounts.
- **SEC-009.5.6.5** Privileged cloud roles (organization administrator, account owner, IAM administrator, security administrator) SHALL be granted through Just-in-Time Access under SEC-005 and reviewed under SEC-005.
- **SEC-009.5.6.6** Cross-account and Third-Party access to Organization cloud accounts SHALL use role assumption with an external identifier or equivalent, approved under RSK-003, and SHALL be reviewed in the access reviews under SEC-003.
- **SEC-009.5.6.7** Unused cloud identities and permissions SHALL be identified by the CSPM/CNAPP platform, and permissions unused for 90 days SHALL be removed at the next access review under SEC-003.

### 5.7 Storage exposure controls

- **SEC-009.5.7.1** Public access to object storage SHALL be blocked at the organization or account level by default.
- **SEC-009.5.7.2** Public access to a storage resource MAY be enabled only for data classified Public, in a dedicated account designated for public content, with written approval from the Data Owner and the Head of Security Engineering recorded in the change record.
- **SEC-009.5.7.3** Storage resources, databases and snapshots holding Confidential or Restricted data SHALL be encrypted at rest per SEC-006. Restricted data SHALL be encrypted with customer-managed keys managed under SEC-006.
- **SEC-009.5.7.4** Pre-signed or shared-access URLs to Confidential or Restricted data SHALL expire within 7 days, and within 24 hours for Restricted data.
- **SEC-009.5.7.5** Database and storage service endpoints holding Confidential or Restricted data SHALL NOT be reachable from the internet and SHALL be accessed through private endpoints or the virtual network controls in SEC-007.
- **SEC-009.5.7.6** Snapshots, images and backups SHALL NOT be shared publicly or with accounts outside the Organization's cloud organization, except to approved Third Parties under RSK-003.
- **SEC-009.5.7.7** Data Loss Prevention or data security posture management SHOULD be used to discover Restricted data in cloud storage and to alert where it is found in a location not approved for Restricted data.

### 5.8 Cloud logging

- **SEC-009.5.8.1** Control-plane audit logging (for example, management API activity logs) SHALL be enabled in every account, subscription and project and in every region, through organization-level configuration that account owners cannot disable.
- **SEC-009.5.8.2** Cloud audit logs, CSPM findings, network flow logs for production and Restricted-data networks, Identity Provider logs and Kubernetes audit logs SHALL be forwarded to the centralized log archive account and to the SIEM, as specified in SEC-012.
- **SEC-009.5.8.3** The log archive SHALL be write-once or otherwise immutable, and access SHALL be limited to the security team and auditors. Retention is set in CMP-004.
- **SEC-009.5.8.4** Data-plane access logging (object access, database audit) SHALL be enabled for storage and databases holding Restricted data.

### 5.9 Network controls in the cloud

- **SEC-009.5.9.1** Cloud virtual networks, security groups, network ACLs and private connectivity SHALL meet SEC-007, and SHALL be deployed through the Landing Zone's network connectivity account and IaC.
- **SEC-009.5.9.2** Direct internet ingress to workloads SHALL be provided only through managed load balancers, API gateways or content delivery services designated as DMZ components under SEC-007.

### 5.10 Data residency

- **SEC-009.5.10.1** Organization data SHALL be stored and processed only in Cloud Service regions approved for that data under CMP-005. The CTO SHALL record approved regions per Cloud Service in the approved Cloud Service list.
- **SEC-009.5.10.2** The region-restriction guardrail in SEC-009.5.4.4 SHALL enforce the approved regions for each account.
- **SEC-009.5.10.3** `[GDPR]` Transfers of Personal Data outside the EU/EEA through a Cloud Service, including transfers to Cloud Service Provider support personnel and Subprocessors, SHALL meet CMP-005.
- **SEC-009.5.10.4** Backups and DR replicas SHALL be held only in regions approved under SEC-009.5.10.1 for the same data.

### 5.11 Kubernetes and container security baseline

- **SEC-009.5.11.1** Managed Kubernetes services SHALL be used in preference to self-managed control planes. Self-managed clusters SHALL be approved by the Head of Security Engineering.
- **SEC-009.5.11.2** Kubernetes API server endpoints for production clusters SHALL be private or restricted to the Management zone (SEC-007). Anonymous authentication SHALL be disabled.
- **SEC-009.5.11.3** Human access to clusters SHALL be federated through the Identity Provider (section 5.6), authorized by Kubernetes RBAC under Least Privilege. Standing cluster-admin bindings SHALL NOT be granted to humans; cluster-admin SHALL be obtained through Just-in-Time Access under SEC-005.
- **SEC-009.5.11.4** Production namespaces SHALL enforce the Kubernetes Pod Security Standards "restricted" profile through admission control. Workloads requiring a less restrictive profile SHALL be approved under CMP-003.
- **SEC-009.5.11.5** Containers SHALL NOT run as privileged, SHALL run as a non-root user, SHALL NOT mount the host filesystem, host network or container runtime socket, and SHALL use a read-only root filesystem where the application supports it.
- **SEC-009.5.11.6** Each namespace SHALL have a default-deny network policy for ingress and egress, with permitted flows defined explicitly, consistent with SEC-007.
- **SEC-009.5.11.7** Container images deployed to production SHALL come only from the Organization's approved registries, SHALL be signed in the pipeline under SEC-010, and SHALL have their signature verified by admission control before deployment.
- **SEC-009.5.11.8** Container images SHALL be scanned for Vulnerabilities in the pipeline and in the registry as specified in SEC-011. Images with a Critical Vulnerability that has an available fix SHALL be blocked from deployment to production unless an Exception is approved under CMP-003.
- **SEC-009.5.11.9** Kubernetes Secrets holding Restricted data SHALL be encrypted at rest with a key managed under SEC-006, or SHALL be supplied from the external secrets manager under SEC-010.
- **SEC-009.5.11.10** Runtime threat detection SHALL be deployed on production clusters, with alerts sent to the SOC under SEC-012.
- **SEC-009.5.11.11** Cluster versions SHALL remain within the Cloud Service Provider's or upstream project's supported versions, and worker nodes SHALL be patched within the remediation SLA in SEC-011.
- **SEC-009.5.11.12** Cluster configurations SHALL be assessed against a recognized benchmark (for example, the CIS Kubernetes Benchmark) by the CSPM/CNAPP platform under section 5.5.
- **SEC-009.5.11.13** Cloud workloads in the scope set by SEC-001.5.8.3 SHALL enforce application control, either through immutable images with runtime controls that block execution of binaries not present in the signed image, or through a host-based application control agent in blocking mode.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CTO | Owns this Policy; maintains the approved Cloud Service list and shared responsibility matrices; owns the Landing Zone and platform engineering. |
| Head of Security Engineering | Defines and approves guardrails and Policy-as-code; performs security reviews of new Cloud Services; operates CSPM/CNAPP; approves public storage and self-managed clusters. |
| CIO | Ensures SaaS applications are onboarded through section 5.2 and integrated with SSO. |
| CISO | Approves Exceptions within the authority in CMP-003; receives cloud posture reporting. |
| CPO | Approves regions for Personal Data under CMP-005. |
| Head of GRC | Runs Third-Party risk assessment of Cloud Service Providers under RSK-003; tracks complementary user entity controls. |
| Head of Procurement | Ensures no Cloud Service is purchased without approval under section 5.2. |
| SOC Manager | Monitors cloud alerts and runtime detections; triages within SEC-012 SLAs. |
| System Owner | Remediates CSPM findings within SLA; maintains IaC for their systems; maintains mandatory tags. |
| Data Owner | Approves the Cloud Services and regions in which their data is held; approves public access for Public data. |
| Workforce Member | Uses only approved Cloud Services; does not create cloud accounts or resources outside the Landing Zone. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| SEC-009.7.1 | Shared responsibility matrix review | Every 12 months and within 30 days of a new service model or Cloud Service Provider |
| SEC-009.7.2 | Account separation | Per environment and, in production, per System; dedicated security, log archive, network and identity accounts |
| SEC-009.7.3 | Account creation | Automated account vending only |
| SEC-009.7.4 | Mandatory resource tags | System Owner · environment · Classification Level · Recovery Tier · cost center · `[PCI]` CDE scope flag |
| SEC-009.7.5 | Production infrastructure | 100% defined in IaC; manual changes reconciled within 5 business days |
| SEC-009.7.6 | Drift detection | At least daily for production accounts; remediation within 5 business days |
| SEC-009.7.7 | Golden and base image rebuild | At least every 30 days |
| SEC-009.7.8 | CSPM/CNAPP onboarding | Within 24 hours of account creation; full assessment at least daily |
| SEC-009.7.9 | CSPM finding remediation | Within the remediation SLA in SEC-011 |
| SEC-009.7.10 | OAuth/third-party integration review | Every 6 months; unused 90 days → revoked |
| SEC-009.7.11 | Human cloud access | Federated, MFA per SEC-004, short-lived credentials; no long-lived access keys |
| SEC-009.7.12 | Unused cloud permissions | Unused for 90 days → removed at next SEC-003 access review |
| SEC-009.7.13 | Public storage | Blocked by default; Public data only, in a designated account, with Data Owner and Head of Security Engineering approval |
| SEC-009.7.14 | Pre-signed URL lifetime | Confidential ≤ 7 days; Restricted ≤ 24 hours |
| SEC-009.7.15 | Restricted data encryption keys | Customer-managed keys per SEC-006 |
| SEC-009.7.16 | Control-plane audit logging | All accounts, all regions, non-disableable; retention per CMP-004 |
| SEC-009.7.17 | Approved regions | Per CMP-005, enforced by guardrail |
| SEC-009.7.18 | Kubernetes Pod Security Standard (production) | "restricted" profile |
| SEC-009.7.19 | Kubernetes namespace network policy | Default-deny ingress and egress |
| SEC-009.7.20 | Production container images | Approved registry, signed, signature verified at admission; vulnerability scanning per SEC-011 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Cloud accounts onboarded to CSPM/CNAPP within 24 hours | 100% | Monthly | Head of Security Engineering |
| CSPM findings remediated within SEC-011 SLA | ≥ 95% | Monthly | CTO |
| Publicly accessible storage holding Confidential or Restricted data | 0 | Weekly | Head of Security Engineering |
| Accounts with control-plane audit logging enabled in all regions | 100% | Monthly | SOC Manager |
| Human cloud Users with long-lived access keys | 0 | Monthly | Head of Security Engineering |
| Production resources managed by IaC | ≥ 98% | Quarterly | CTO |
| Unreconciled production drift older than 5 business days | 0 | Monthly | CTO |
| Production clusters enforcing "restricted" Pod Security Standard | 100% | Quarterly | CTO |
| Cloud Services in use not on the approved list (Shadow IT detections) | 0 unresolved after 30 days | Quarterly | CIO |
| Resources deployed outside approved regions | 0 | Monthly | Head of Security Engineering |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following SHALL NOT receive an Exception: public access to storage holding Confidential
or Restricted data (SEC-009.5.7.1, SEC-009.5.7.2); disabling of control-plane audit
logging (SEC-009.5.8.1); and storage of Personal Data in a region not approved under
CMP-005 (SEC-009.5.10.1).

## 10. Enforcement

Non-compliance is handled under CMP-007.

The Head of Security Engineering MAY immediately revert or block a cloud configuration that
exposes Confidential or Restricted data to the internet, and SHALL record the action as an
Emergency Change under SEC-013. Cloud accounts or Cloud Services created outside the
Landing Zone or the approved list SHALL be brought under management or decommissioned
within 30 days of detection.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| SEC-009.5.1 Shared responsibility | A.5.23, A.5.19 | GV.SC-05, GV.SC-07 | SA-9, SR-6 | 15.4 | CC9.2 | APO10 | PCI DSS 12.8.5, 12.9; 45 CFR §164.314(a) |
| SEC-009.5.2 Approved CSPs & onboarding | A.5.23, A.5.21, A.5.9 | GV.SC-06, ID.AM-02 | SA-4, SA-9, CM-8 | 15.1, 2.1 | CC9.2, CC3.4 | APO10 | GDPR Art. 28 |
| SEC-009.5.3 Landing Zone | A.8.22, A.8.31, A.5.23 | PR.IR-01, PR.PS-01 | SC-7, AC-4, CM-2 | 12.2 | CC6.1, CC6.6 | APO03, BAI10 | PCI DSS 1.2, 12.5.2 |
| SEC-009.5.4 IaC & guardrails | A.8.9, A.8.32 | PR.PS-01 | CM-2, CM-3, CM-6 | 4.1, 16.7 | CC8.1, CC7.1 | BAI06, BAI10 | PCI DSS 2.2, 6.5.1 |
| SEC-009.5.5 CSPM/CNAPP | A.8.8, A.8.9 | ID.RA-01, DE.CM-09 | CA-7, RA-5, CM-6 | 7.5, 4.1 | CC7.1 | DSS05.07 | PCI DSS 11.3 |
| SEC-009.5.6 Identity federation | A.5.15, A.5.16, A.8.2, A.8.5 | PR.AA-01, PR.AA-03, PR.AA-05 | AC-2, AC-6, IA-2, IA-5 | 5.6, 6.3, 6.5, 6.7 | CC6.1, CC6.2, CC6.3 | DSS05.04 | PCI DSS 7.2, 8.4 |
| SEC-009.5.7 Storage exposure | A.8.3, A.8.24, A.5.10 | PR.DS-01 | AC-3, SC-28 | 3.3, 3.11 | CC6.1, C1.1 | DSS05.02 | 45 CFR §164.312(a)(2)(iv); GDPR Art. 32 |
| SEC-009.5.8 Cloud logging | A.8.15, A.8.16 | DE.CM-01, PR.PS-04 | AU-2, AU-9, AU-12 | 8.2, 8.9 | CC7.2 | DSS05.07 | PCI DSS 10.2, 10.3; 45 CFR §164.312(b) |
| SEC-009.5.9 Cloud networking | A.8.20, A.8.22 | PR.IR-01 | SC-7 | 12.2 | CC6.6 | DSS05.02 | PCI DSS 1.3 |
| SEC-009.5.10 Data residency | A.5.31, A.5.34 | GV.OC-03 | SA-9 | — | C1.1 | APO10, MEA03 | GDPR Art. 44–49 |
| SEC-009.5.11 Kubernetes & containers | A.8.9, A.8.19, A.8.22 | PR.PS-01, PR.PS-05 | CM-6, CM-7, AC-6, SI-7 | 4.1, 4.8, 16.7 | CC6.1, CC6.8, CC7.1 | BAI10, DSS05.03 | PCI DSS 2.2, 6.3.2 |

## 12. Related documents

ISP-000, GOV-006, SEC-001, SEC-002, SEC-003, SEC-004, SEC-005, SEC-006, SEC-007, SEC-008,
SEC-010, SEC-011, SEC-012, SEC-013, SEC-018, SEC-019, RSK-003, RSK-004, CMP-004, CMP-005,
CMP-009, RES-005, CMP-003, CMP-007

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CTO | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
