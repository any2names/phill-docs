# SEC-001 — Asset Management Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | SEC-001 |
| Title | Asset Management Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Information Officer (CIO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-004, GOV-006, RSK-003, RSK-004, RSK-006, CMP-004, CMP-009, SEC-002, SEC-003, SEC-008, SEC-009, SEC-010, SEC-011, SEC-013, SEC-017, SEC-019, PPL-001 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CIO | Initial release |

## 3. Purpose

This Policy establishes the Asset Inventory as the authoritative record of the Organization's
Information Assets and sets the requirements for identifying, owning, approving, tracking and
retiring them. An accurate Asset Inventory is the foundation for classification (SEC-002),
access control (SEC-003), vulnerability management (SEC-011), change management (SEC-013),
recovery planning (RSK-004) and regulatory scoping (CMP-009, SEC-019). Assets that are not
known cannot be protected, monitored or recovered.

## 4. Scope

| Dimension | In scope |
|---|---|
| People | All Workforce Members and Third Parties who acquire, deploy, operate, use or dispose of Information Assets on behalf of the Organization |
| Systems | All hardware, software, Cloud Services, data stores, SaaS applications, network and security devices, operational technology connected to Organization networks, and identities, whether Organization-owned, leased, subscribed, or personally owned and enrolled under SEC-008 |
| Data | All data stores holding information at any Classification Level (SEC-002) |
| Locations | All Organization premises, data centers, colocation facilities, Cloud Service tenants and accounts, remote work locations, and Third-Party facilities hosting Organization Information Assets |
| Third parties | Third Parties that provide, host or operate Information Assets for the Organization, and Third Parties whose services are recorded in the Asset Inventory as Cloud Services or SaaS |

Out of scope: consumables with no storage or processing capability (for example, keyboards
without firmware storage, cables). Media containing data is in scope regardless of value.

## 5. Policy statements

### 5.1 Asset Inventory

- **SEC-001.5.1.1** The CIO SHALL maintain a single authoritative Asset Inventory covering every asset category in section 5.2. Where several tools hold inventory data (for example, a configuration management database, a cloud asset service, a mobile device management console and an Identity Provider), the CIO SHALL designate one system of record per category and document how the records are federated into the Asset Inventory.
- **SEC-001.5.1.2** The Asset Inventory SHALL be populated by automated discovery wherever a discovery method exists for the asset category. Manual entry SHALL be used only for asset categories listed in the Asset Inventory procedure as having no automated discovery method.
- **SEC-001.5.1.3** Automated discovery SHALL run at the frequency in SEC-001.7.3 and SHALL cover every network segment, Cloud Service account or subscription, and identity directory in scope.
- **SEC-001.5.1.4** The Asset Inventory SHALL be classified Confidential under SEC-002 and access to modify it SHALL be restricted under SEC-003 to Data Custodians assigned by the CIO.
- **SEC-001.5.1.5** Changes to Asset Inventory records SHALL be logged with the identity of the person or process making the change, the date and time, and the before and after values.
- **SEC-001.5.1.6** The Asset Inventory SHALL be updated within the time in SEC-001.7.4 of any acquisition, deployment, transfer, change of owner, change of location, change of Classification Level, or retirement of an asset.
- **SEC-001.5.1.7** The Asset Inventory SHALL be capable of producing, on request and within 1 business day, the population of assets for any audit, assessment or regulatory scope (for example, `[PCI]` system components in the CDE, `[SOX]` Financially Significant Systems, `[HIPAA]` systems that create, receive, maintain or transmit ePHI).

### 5.2 Inventory scope by asset category

The Asset Inventory SHALL include the following categories. Each category SHALL have a
designated system of record (SEC-001.5.1.1).

| Category | Includes | Minimum discovery source |
|---|---|---|
| Hardware | Servers, Endpoints, Mobile Devices, network devices, security appliances, storage arrays, removable Media issued by the Organization, printers and multifunction devices with storage, IoT and operational technology on Organization networks | Network discovery, endpoint management agent, mobile device management, procurement records |
| Software | Operating systems, installed applications, firmware, databases engines, middleware, libraries in Organization-developed software (via SBOM under SEC-010), browser extensions approved for use | Endpoint agent software inventory, SBOM, license management records |
| Cloud Services (IaaS / PaaS) | Cloud Service accounts, subscriptions and projects; compute instances, containers and container images, serverless functions, managed databases, object storage buckets, key vaults, network constructs | Cloud provider asset APIs, cloud security posture management tooling |
| SaaS | Every SaaS application used for Organization business, including free-tier and trial subscriptions, and integrations (OAuth grants, API connections) between SaaS applications | Identity Provider application catalogue, procurement and expense records, SaaS discovery tooling, network egress logs |
| Data stores | Databases, file shares, object storage, data warehouses and lakes, collaboration repositories, backup repositories, logs containing Personal Data, and AI System training and retrieval data sets | Data discovery tooling, Data Owner attestation, ROPA (`[GDPR]` TPL-010) |
| Identities | Workforce Member accounts, Privileged Accounts, Service Accounts, Break-glass Accounts, Third-Party accounts, and machine identities (certificates, workload identities, API keys) | Identity directories, Identity Provider, PAM vault (SEC-005), certificate inventory (SEC-006) |

- **SEC-001.5.2.1** Identities SHALL be inventoried as Information Assets so that each account is attributable to an owner. The lifecycle and access controls for identities are governed by SEC-003 and SEC-005; this Policy governs only their inclusion and attributes in the Asset Inventory.
- **SEC-001.5.2.2** Data stores SHALL be linked in the Asset Inventory to the Information System that hosts them and to the Data Owner of the data they hold.
- **SEC-001.5.2.3** Cloud Services and SaaS provided by a Third Party SHALL be linked in the Asset Inventory to the Third Party's record and vendor tier under RSK-003.
- **SEC-001.5.2.4** AI Systems, including Generative AI tools procured as SaaS, SHALL be recorded as SaaS or software assets and flagged as AI Systems so that RSK-006 can be applied.

### 5.3 Required inventory attributes

- **SEC-001.5.3.1** Every Asset Inventory record SHALL contain the mandatory attributes in the table below. A record missing a mandatory attribute SHALL be reported as an inventory defect (section 8).
- **SEC-001.5.3.2** Attributes marked "Conditional" SHALL be populated where the condition applies.

| Attribute | Applies to | Mandatory / Conditional |
|---|---|---|
| Unique asset identifier | All | Mandatory |
| Asset category and type | All | Mandatory |
| Name / hostname / application name | All | Mandatory |
| Asset Owner (named individual) | All | Mandatory |
| Data Custodian (team or individual) | All except identities | Mandatory |
| Business function or service supported | All | Mandatory |
| Highest Classification Level of data stored, processed or transmitted (SEC-002) | All | Mandatory |
| Recovery Tier (RSK-004) | Hardware, Cloud Services, SaaS, data stores supporting a business process in the BIA | Mandatory |
| Dependency map reference (RSK-004) | Assets supporting a Recovery Tier 0, 1 or 2 process | Conditional: supports a tiered process |
| AI System flag and RSK-006 inventory reference (SEC-001.5.2.4) | Software, SaaS, Cloud Services | Conditional: is or embeds an AI System |
| Lifecycle state (section 5.7) | All | Mandatory |
| Location (physical site, cloud region, or "remote") | Hardware, Cloud Services, data stores | Mandatory |
| Network address(es) and network zone | Hardware and Cloud Services with network interfaces | Mandatory |
| Manufacturer / publisher / provider, model, version | Hardware, software, SaaS | Mandatory |
| Serial number or cloud resource identifier | Hardware, Cloud Services | Mandatory |
| End-of-support / end-of-life date | Hardware, software | Mandatory |
| Linked Third Party and vendor tier (RSK-003) | Cloud Services, SaaS, Third-Party-hosted assets | Conditional: Third-Party provided |
| Regulatory scope flags: `[PCI]` CDE, `[HIPAA]` ePHI, `[SOX]` Financially Significant System, `[GDPR]`/`[CPRA]` Personal Data | All | Conditional: in regulatory scope |
| Encryption status at rest (SEC-006) | Hardware with storage, data stores, Cloud Services | Conditional: holds Confidential or Restricted data |
| Endpoint protection / management agent status | Endpoints, servers | Conditional: agent-capable |
| Authentication method (SSO / local) | SaaS, applications | Mandatory |
| Acquisition date and acquisition reference (purchase order or contract) | Hardware, software, SaaS | Mandatory |
| License entitlement and count | Licensed software and SaaS | Conditional: licensed |
| Date last seen by discovery | All automatically discovered assets | Mandatory |
| Date of last attribute verification by Asset Owner | All | Mandatory |
| Disposal method and Media Sanitization certificate reference (SEC-017) | Hardware, Media, data stores | Conditional: lifecycle state "Disposed" |

### 5.4 Ownership assignment

- **SEC-001.5.4.1** Every Information Asset SHALL have exactly one Asset Owner, who SHALL be a named individual employed by the Organization at the level of manager or above. Teams, distribution lists and Third Parties SHALL NOT be recorded as Asset Owner.
- **SEC-001.5.4.2** The Asset Owner SHALL be assigned before the asset enters the "In use" lifecycle state (section 5.7). Assets discovered without an owner SHALL be handled under section 5.5.
- **SEC-001.5.4.3** The Asset Owner is accountable for: confirming the Classification Level with the Data Owner (SEC-002); ensuring the asset's Recovery Tier is recorded (RSK-004); approving access to the asset under SEC-003; verifying the accuracy of the asset's inventory record at the frequency in SEC-001.7.6; and initiating retirement under section 5.7.
- **SEC-001.5.4.4** The Asset Owner MAY delegate operational tasks to a Data Custodian. Accountability SHALL NOT be delegated.
- **SEC-001.5.4.5** When an Asset Owner changes role or separates, the Asset Owner's Line Manager SHALL nominate a replacement Asset Owner, and the Asset Inventory SHALL be updated, before the Asset Owner's access is changed or revoked under SEC-003. The CIO SHALL be the interim Asset Owner of any asset left without an owner.
- **SEC-001.5.4.6** The CIO SHALL report to the ISSC monthly the count of assets with no valid Asset Owner (section 8).
- **SEC-001.5.4.7** Endpoints and Mobile Devices issued to an individual SHALL additionally record the assigned Workforce Member. Return of assets on Separation is governed by PPL-001.

### 5.5 Unknown and unauthorized assets

- **SEC-001.5.5.1** An asset detected by discovery that does not match an Asset Inventory record SHALL be logged as an unknown asset and triaged by the Data Custodian for the relevant category within the time in SEC-001.7.5.
- **SEC-001.5.5.2** Triage SHALL result in one of: (a) the asset is registered with an Asset Owner and all mandatory attributes; (b) the asset is isolated from Organization networks or Cloud Service accounts pending registration; or (c) the asset is removed or decommissioned under section 5.7.
- **SEC-001.5.5.3** An unknown asset that stores, processes or transmits Restricted data, or that is in `[PCI]` CDE or `[SOX]` Financially Significant System scope, SHALL be reported to the SOC Manager as a Security Event within 1 business day of detection.
- **SEC-001.5.5.4** Hardware that is not registered in the Asset Inventory SHALL NOT be granted network access beyond a quarantine or guest segment, where network access control is technically available (SEC-007).

### 5.6 Shadow IT

- **SEC-001.5.6.1** Workforce Members SHALL NOT acquire, subscribe to, deploy or use any Information System or Cloud Service for Organization business, including free and trial offerings, unless it has been approved and registered in the Asset Inventory under this Policy and assessed under RSK-003. Acceptable Use obligations of individual Workforce Members are in GOV-004.
- **SEC-001.5.6.2** The approval route for a new SaaS or Cloud Service SHALL require: (a) a named Asset Owner; (b) the highest Classification Level of data to be processed (SEC-002); (c) a Third-Party risk assessment under RSK-003; (d) integration with the Organization's SSO where the service supports it (SEC-004); and (e) `[GDPR]` `[CPRA]` a privacy review under CMP-005 where Personal Data is processed.
- **SEC-001.5.6.3** The CIO SHALL operate Shadow IT detection that, at the frequency in SEC-001.7.7, compares the Asset Inventory against at least: Identity Provider application consent and OAuth grant logs, network or secure web gateway egress logs, procurement card and expense records, and endpoint software inventory.
- **SEC-001.5.6.4** Each instance of Shadow IT detected SHALL be resolved within the time in SEC-001.7.8 by one of: (a) retroactive approval and registration under SEC-001.5.6.2; (b) migration of data to an approved Information System and termination of the service; or (c) an approved Exception under CMP-003.
- **SEC-001.5.6.5** Where Shadow IT has processed Restricted data, the CIO SHALL notify the CISO within 1 business day, and the CISO SHALL determine whether a Security Incident is declared under RES-001.
- **SEC-001.5.6.6** The Head of Procurement SHALL ensure that procurement and expense processes route any purchase of software, SaaS or Cloud Services to the approval route in SEC-001.5.6.2 before payment is approved.

### 5.7 Asset lifecycle

The Organization recognizes the following lifecycle states. Each state transition SHALL be
recorded in the Asset Inventory within the time in SEC-001.7.4.

| State | Entry criteria | Exit criteria |
|---|---|---|
| Requested | Business need documented by the prospective Asset Owner | Approved under SEC-001.5.7.1 or rejected |
| Acquired | Purchase, subscription or provisioning completed | Inventory record created with mandatory attributes |
| In use | Configured to the Configuration Baseline (SEC-013), owner assigned, classification recorded | Change of owner, transfer, retirement decision |
| In storage | Hardware or Media held in a secured location awaiting reuse or disposal (SEC-016) | Redeployment, or retirement |
| Retired | Removed from service; no production workload; access revoked | Data migrated or deleted, Media Sanitization completed under SEC-017 |
| Disposed | Media Sanitization or destruction evidenced under SEC-017; licenses and subscriptions terminated | Terminal state; record retained per CMP-004 |

- **SEC-001.5.7.1** Acquisition of any hardware, software, SaaS or Cloud Service SHALL be approved by the prospective Asset Owner and the CIO or the CIO's documented delegate, and, where the asset will hold Confidential or Restricted data, reviewed by the Head of Security Engineering before purchase.
- **SEC-001.5.7.2** Before entering the "In use" state, hardware and software SHALL be configured to the applicable Configuration Baseline under SEC-013 and enrolled in endpoint management, vulnerability scanning (SEC-011) and logging (SEC-012) where those controls apply to the asset type.
- **SEC-001.5.7.3** The Asset Owner SHALL plan replacement or retirement of hardware and software no later than the time in SEC-001.7.9 before the end-of-support date recorded in the Asset Inventory.
- **SEC-001.5.7.4** Hardware and software past its end-of-support date SHALL NOT remain in the "In use" state unless covered by an approved Exception under CMP-003 that documents Compensating Controls. Vulnerability remediation for such assets remains subject to SEC-011.
- **SEC-001.5.7.5** Hardware moved between sites, or removed from Organization premises other than Endpoints and Mobile Devices issued to individuals, SHALL be authorized by the Asset Owner and recorded in the Asset Inventory before the move. Physical removal controls are in SEC-016.
- **SEC-001.5.7.6** On retirement, the Asset Owner SHALL ensure: (a) data is migrated, retained or deleted in accordance with CMP-004 and any Legal Hold; (b) accounts, Service Accounts, certificates and keys associated with the asset are revoked under SEC-003 and SEC-006; (c) Media Sanitization or destruction is performed under SEC-017; and (d) licenses, subscriptions and SaaS tenants are terminated and Organization data return or deletion is confirmed by the Third Party under RSK-003.
- **SEC-001.5.7.7** Asset Inventory records for disposed assets SHALL be retained, not deleted, for the period for control evidence in CMP-004.

### 5.8 Software allowlisting

- **SEC-001.5.8.1** Only software on the Organization's Authorized Software List SHALL be installed or executed on Organization Endpoints and servers. The CIO SHALL maintain the Authorized Software List as part of the Asset Inventory.
- **SEC-001.5.8.2** Software SHALL be added to the Authorized Software List only after: (a) the Asset Owner documents the business need; (b) the Head of Security Engineering, or a documented delegate, confirms that the software is supported by its publisher, obtained from a trusted source with integrity verified, and has no unremediated Critical or High vulnerability under SEC-011; and (c) license entitlement is confirmed.
- **SEC-001.5.8.3** Technical allowlisting enforcement (application control) SHALL be applied, at minimum, to: servers in the `[PCI]` CDE and `[SOX]` Financially Significant Systems; Privileged Access Workstations (SEC-005); and servers hosting Restricted data. The technical configuration of application control on Endpoints is governed by SEC-008.5.2.9, and on cloud workloads by SEC-009.5.11.13.
- **SEC-001.5.8.4** Where technical enforcement is not applied, software not on the Authorized Software List SHALL be detected through the endpoint software inventory and removed or approved within the time in SEC-001.7.8.
- **SEC-001.5.8.5** The Authorized Software List SHALL record, for each entry: software name, publisher, approved version range, approved asset scope, Asset Owner, approval date, and end-of-support date.
- **SEC-001.5.8.6** The Head of Security Engineering SHALL review the Authorized Software List at the frequency in SEC-001.7.10 and remove software that is unsupported, no longer used, or no longer meets SEC-001.5.8.2.
- **SEC-001.5.8.7** Libraries and dependencies used in Organization-developed software are governed by SEC-010 and recorded via SBOM; browser extensions and Mobile Device applications are governed by SEC-008.

### 5.9 Reconciliation and verification

- **SEC-001.5.9.1** The CIO SHALL reconcile the Asset Inventory against each discovery source at the frequencies in SEC-001.7.11. Each reconciliation SHALL identify: assets discovered but not inventoried; inventory records not seen by discovery within the staleness threshold in SEC-001.7.12; and records with missing mandatory attributes.
- **SEC-001.5.9.2** Each reconciliation SHALL be evidenced by a dated report retained as control evidence under CMP-004, showing exceptions found and their resolution.
- **SEC-001.5.9.3** Inventory records not seen by discovery for longer than the staleness threshold SHALL be investigated by the Data Custodian and either confirmed by the Asset Owner as in use, located, or transitioned to "Retired". Hardware that cannot be located SHALL be reported to the CISO as a potential Security Incident within 1 business day of the reconciliation that identified it.
- **SEC-001.5.9.4** Each Asset Owner SHALL verify the accuracy of the attributes of every asset they own at the frequency in SEC-001.7.6 and record the verification date.
- **SEC-001.5.9.5** The CIO SHALL perform a physical verification of hardware in data centers, colocation facilities and secured storage at the frequency in SEC-001.7.13.
- **SEC-001.5.9.6** `[PCI]` The inventory of system components in scope for PCI DSS, including a description of function and use, SHALL be maintained and kept current as part of the Asset Inventory and reconciled at the frequency in SEC-001.7.11 (PCI DSS 12.5.1). Scope confirmation for the CDE is governed by SEC-019.
- **SEC-001.5.9.7** `[SOX]` The population of Financially Significant Systems and their supporting infrastructure SHALL be derived from the Asset Inventory and confirmed with the Head of GRC at least every 12 months and before each fiscal year-end under CMP-009.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CIO | Owns this Policy; maintains the Asset Inventory and Authorized Software List; designates systems of record; runs discovery, reconciliation and Shadow IT detection; is interim Asset Owner of unowned assets; reports inventory metrics to the ISSC. |
| ISSC | Approves this Policy; reviews monthly inventory metrics. |
| CISO | Receives escalations of unknown assets holding Restricted data, Shadow IT processing Restricted data and lost hardware; decides on Security Incident declaration. |
| Head of Security Engineering | Security review of acquisitions holding Confidential or Restricted data; security approval of authorized software; reviews the Authorized Software List; specifies technical allowlisting enforcement. |
| CTO | Ensures Organization-developed software and cloud workloads are registered and SBOMs are produced (SEC-010, SEC-009). |
| Head of Procurement | Routes all software, SaaS and Cloud Service purchases through SEC-001.5.6.2; provides procurement and expense data for Shadow IT detection. |
| Head of GRC | Uses the Asset Inventory to define audit and regulatory populations; confirms `[SOX]` Financially Significant System population. |
| Head of Facilities | Supports physical verification and secured storage of hardware awaiting reuse or disposal (SEC-016). |
| SOC Manager | Receives Security Events for unknown assets in sensitive scope. |
| Asset Owner | Accountable for the asset's record, classification, Recovery Tier, access approval, attribute verification, end-of-support planning and retirement. |
| Data Owner | Confirms Classification Level of data stores and links them to hosting systems. |
| Data Custodian | Maintains inventory records, triages unknown assets, investigates stale records, operates discovery tooling. |
| Workforce Member | Does not acquire or use Shadow IT; reports unknown or lost assets to the CISO. |
| Third Party | Provides asset information for Organization assets it hosts or operates, as required by contract (RSK-003). |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| SEC-001.7.1 | Asset Inventory systems of record | One designated per asset category in section 5.2 |
| SEC-001.7.2 | Assets with a named Asset Owner | 100% of records |
| SEC-001.7.3 | Automated discovery frequency | Cloud Services and SaaS: continuous or at least daily · Hardware and software on networks and Endpoints: at least daily · Identities: at least daily synchronization from identity directories |
| SEC-001.7.4 | Inventory update after acquisition, change or state transition | Automated sources: within 1 business day · Manual entries: within 5 business days |
| SEC-001.7.5 | Triage of an unknown asset | Within 5 business days of detection; within 1 business day where Restricted data or `[PCI]` / `[SOX]` scope is involved |
| SEC-001.7.6 | Asset Owner attribute verification | Every 12 months; every 6 months for assets holding Restricted data or in `[PCI]` / `[SOX]` scope |
| SEC-001.7.7 | Shadow IT detection run | Monthly |
| SEC-001.7.8 | Resolution of Shadow IT or unauthorized software | Within 30 days of detection; within 5 business days where Restricted data is involved |
| SEC-001.7.9 | End-of-support replacement planning lead time | At least 6 months before end-of-support date |
| SEC-001.7.10 | Authorized Software List review | Every 6 months |
| SEC-001.7.11 | Reconciliation of Asset Inventory against discovery sources | Cloud Services and SaaS: monthly · Hardware, software and identities: quarterly · `[PCI]` CDE system components: quarterly |
| SEC-001.7.12 | Staleness threshold for records not seen by discovery | 30 days |
| SEC-001.7.13 | Physical verification of data center, colocation and secured-storage hardware | Every 12 months |
| SEC-001.7.14 | Mandatory attribute completeness | ≥ 98% of records complete; 100% for Restricted, `[PCI]` and `[SOX]` scope records |
| SEC-001.7.15 | Escalation to CISO of Shadow IT with Restricted data, or unlocated hardware | Within 1 business day |
| SEC-001.7.16 | Retention of disposed-asset records and reconciliation reports | Per CMP-004 (control evidence) |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Inventory records with all mandatory attributes | ≥ 98% overall; 100% for Restricted / `[PCI]` / `[SOX]` scope | Monthly | CIO |
| Assets without a valid Asset Owner | 0 | Monthly | CIO |
| Unknown assets triaged within SEC-001.7.5 | 100% | Monthly | CIO |
| Shadow IT instances detected / resolved within SEC-001.7.8 | 100% resolved within target | Monthly | CIO |
| Stale records (not seen > 30 days) open > 30 days | 0 | Monthly | CIO |
| In-use assets past end-of-support without approved Exception | 0 | Monthly | CIO |
| Reconciliations completed on schedule | 100% | Quarterly | CIO |
| Asset Owner verifications completed on schedule | ≥ 95% | Quarterly | CIO |
| Endpoints and servers with unauthorized software | ≤ 1% of devices; 0 on application-controlled systems | Monthly | Head of Security Engineering |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following requirements SHALL NOT receive an Exception: SEC-001.5.4.1 (single named Asset
Owner) and SEC-001.5.5.3 (reporting unknown assets in Restricted, `[PCI]` or `[SOX]` scope).
An Exception under SEC-001.5.7.4 for end-of-support assets SHALL document Compensating
Controls and a funded replacement date.

## 10. Enforcement

Non-compliance is handled under CMP-007.

The CIO MAY direct the isolation, suspension or termination of any unregistered asset or
Shadow IT service, without notice to the user, where it presents a Risk to Restricted data
or to regulated scope.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| SEC-001.5.1 – 5.3 Inventory and attributes | A.5.9, A.5.12 | ID.AM-01, ID.AM-02, ID.AM-04, ID.AM-07 | CM-8, PM-5 | 1.1, 2.1, 3.2, 5.1, 15.1 | CC3.2, CC6.1 | BAI09, BAI10 | `[PCI]` 6.3.2, 12.5.1; `[HIPAA]` §164.310(d)(1); `[SOX]` §404 |
| SEC-001.5.4 Ownership | A.5.9 | ID.AM-01, GV.RR-02 | CM-8, PM-5 | 1.1 | CC1.3, CC6.1 | BAI09 | `[HIPAA]` §164.310(d)(2)(iii) |
| SEC-001.5.5 Unknown assets | A.5.9 | ID.AM-01, DE.CM-01 | CM-8 | 1.2, 1.3, 1.4 | CC6.1, CC7.1 | BAI09 | `[PCI]` 12.5.1 |
| SEC-001.5.6 Shadow IT | A.5.9, A.5.23 | ID.AM-02, ID.AM-04, GV.SC-04 | CM-10, CM-11, SA-9 | 2.3, 15.1 | CC6.8, CC9.2 | BAI09, APO10 | `[GDPR]` Art. 28, 30 |
| SEC-001.5.7 Lifecycle | A.5.9, A.5.11, A.7.14 | ID.AM-08 | CM-8, SA-22 | 1.1, 2.2 | CC6.5, CC8.1 | BAI09 | `[HIPAA]` §164.310(d)(2)(ii) |
| SEC-001.5.8 Software allowlisting | A.8.19 | PR.PS-05 | CM-7, CM-10, CM-11 | 2.5, 2.6, 2.7 | CC6.8 | DSS05 | — |
| SEC-001.5.9 Reconciliation | A.5.9 | ID.AM-01, ID.AM-02, ID.AM-08 | CM-8 | 1.1, 2.1 | CC3.2, CC4.1 | BAI09, MEA01 | `[PCI]` 12.5.1, 12.5.2; `[SOX]` §404 |

## 12. Related documents

ISP-000, GOV-004, GOV-006, RSK-003, RSK-004, RSK-006, CMP-003, CMP-004, CMP-005, CMP-007,
CMP-009, SEC-002, SEC-003, SEC-005, SEC-006, SEC-007, SEC-008, SEC-009, SEC-010, SEC-011,
SEC-012, SEC-013, SEC-016, SEC-017, SEC-019, RES-001, PPL-001, TPL-010

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CIO | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
