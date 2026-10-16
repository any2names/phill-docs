# SEC-019 — Cardholder Data Environment Standard

## 1. Document control

| Field | Value |
|---|---|
| Document ID | SEC-019 |
| Title | Cardholder Data Environment Standard |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 2 — Standard |
| Classification | Internal |
| Owner | Head of Security Engineering |
| Approver | Chief Information Security Officer (CISO) |
| Effective date | [DECISION REQUIRED: Date of CISO approval] |
| Next review date | Effective date + 12 months, and on the event-triggered reviews in GOV-002.7.4 |
| Parent document | SEC-002 Data Classification & Handling Policy |
| Related documents | ISP-000, GOV-001, RSK-002, RSK-003, CMP-002, CMP-004, SEC-001, SEC-003, SEC-004, SEC-005, SEC-006, SEC-007, SEC-008, SEC-009, SEC-010, SEC-011, SEC-012, SEC-013, SEC-014, SEC-016, SEC-017, RES-002, RES-003, PPL-001, PPL-002, REF-001 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Head of Security Engineering | Initial release |

## 3. Purpose

This Standard defines, scopes and protects the Organization's Cardholder Data Environment (CDE)
under PCI DSS v4.0.1. It:

- sets how the CDE is scoped and how that scope is confirmed (PCI DSS 12.5.2, 12.5.2.1);
- requires current network and data-flow diagrams (1.2.3, 1.2.4);
- sets segmentation design requirements and links them to the segmentation testing in SEC-011;
- holds the PCI DSS requirements that are specific to the CDE and have no other home in the
  suite (e.g. PAN masking, rendering PAN unreadable, Payment Page script integrity, POI device
  inspection); and
- maps every other PCI DSS requirement to the suite document that implements it (section 5.12),
  so that the CDE is protected by the suite as a whole without restating it.

## 4. Scope

**This entire document is a conditional module. It applies only where the Organization stores,
processes or transmits payment card data `[PCI]`**, as recorded in the Obligations Register
(CMP-001). Where PCI DSS does not apply, the Organization removes this document and all clauses
tagged `[PCI]` (README "Conditional modules").

| Dimension | In scope |
|---|---|
| People | Workforce Members and Third Party personnel with access to the CDE, to CHD or SAD, or to POI devices; personnel who develop or change Payment Pages |
| Systems | All system components in the CDE; all system components connected to, or able to affect the security of, the CDE; segmentation controls; Payment Pages and the scripts they load; POI devices |
| Data | CHD and SAD in any form (electronic, paper, voice recording), and truncated, hashed, tokenized or encrypted PAN |
| Locations | Every facility, data center, Cloud Service region, store, call center and remote location where CHD is stored, processed or transmitted, or where POI devices are used |
| Third parties | Third-Party service providers (TPSPs) that store, process or transmit CHD for the Organization, or that can affect the security of the CDE |

- **SEC-019.4.1** `[PCI]` The GC SHALL record in the Obligations Register whether the Organization is a merchant, a service provider, or both, and its validation level and method. [DECISION REQUIRED: PCI DSS entity type. Recommended default: merchant] [DECISION REQUIRED: PCI DSS validation level (SUITE-REGISTER section E, decision 4). Recommended default: Report on Compliance (ROC) by a QSA; SAQ for lower-volume merchants]
- **SEC-019.4.2** `[PCI]` Requirements marked "service provider" apply only where SEC-019.4.1 records that the Organization is a service provider.

## 5. Requirements

### 5.1 CDE scope definition

- **SEC-019.5.1.1** `[PCI]` The Head of Security Engineering SHALL classify every system component in the Organization's environment into one of three scope categories, and record the category in the Asset Inventory (SEC-001):

| Category | Definition for this Standard | Examples |
|---|---|---|
| CDE | Stores, processes or transmits CHD or SAD, or is on the same network segment without segmentation from such components | Payment application servers, databases holding PAN, payment gateways, POI devices |
| Connected-to / security-impacting | Has connectivity to the CDE, or can affect the security of the CDE or CHD, without itself storing, processing or transmitting CHD | Directory services, SSO, jump hosts, logging and SIEM, patch and configuration management, key management, CI/CD pipelines that deploy to the CDE, web servers hosting Payment Page redirects |
| Out of scope | Cannot connect to the CDE and cannot affect its security, as confirmed by segmentation testing | Corporate systems on segmented networks with no access path to the CDE |

- **SEC-019.5.1.2** `[PCI]` A system component SHALL be treated as CDE until the Head of Security Engineering documents the evidence (segmentation design and segmentation test result) that places it in a lower category.
- **SEC-019.5.1.3** `[PCI]` The Organization SHOULD minimize CDE scope by using tokenization, point-to-point encryption, hosted Payment Pages or iframes from PCI DSS-validated TPSPs, and by eliminating PAN storage where there is no documented business need. Each scope-reduction decision SHALL be documented with the PCI DSS requirements it removes from scope and approved by the CISO.
- **SEC-019.5.1.4** `[PCI]` Cloud Service components SHALL be categorized at the level of account, subscription, project, virtual network and workload, and the shared-responsibility split SHALL be recorded in the TPSP responsibility matrix (SEC-019.5.10.6). Cloud-specific controls are in SEC-009.
- **SEC-019.5.1.5** `[PCI]` A Change that could alter CDE scope (new data flow, new system connected to the CDE, new acceptance channel, change to a segmentation control, new TPSP) SHALL be flagged `[PCI]` in the Change record under SEC-013 and SHALL NOT be implemented until the Head of Security Engineering has assessed its scope impact and approved it in the Change record.

### 5.2 Scope confirmation (PCI DSS 12.5.2, 12.5.2.1, 12.5.3)

- **SEC-019.5.2.1** `[PCI]` The Head of Security Engineering SHALL document and confirm PCI DSS scope at least once every 12 months and upon Significant Change to the in-scope environment (PCI DSS 12.5.2).
- **SEC-019.5.2.2** `[PCI]` Service provider: scope SHALL be documented and confirmed at least once every 6 months and upon Significant Change to the in-scope environment (PCI DSS 12.5.2.1).
- **SEC-019.5.2.3** `[PCI]` Each scope confirmation SHALL, at minimum:
  1. identify all data flows for the various payment stages (authorization, capture, settlement, chargebacks, refunds) and acceptance channels (card-present, card-not-present, e-commerce, mail and telephone order);
  2. update all data-flow diagrams (section 5.3);
  3. identify all locations where account data is stored, processed and transmitted, including any locations outside the currently defined CDE, any unexpected locations, and any locations found by the data discovery in section 5.5;
  4. identify all system components in the CDE, connected to the CDE, or that could affect the security of the CDE;
  5. identify all segmentation controls in use and the environments from which the CDE is segmented, with justification for any environment being out of scope;
  6. identify all connections from third-party entities with access to the CDE; and
  7. confirm that all identified data flows, account data, system components, segmentation controls and third-party connections are included in scope.
- **SEC-019.5.2.4** `[PCI]` The scope confirmation SHALL be recorded in a scope document signed by the Head of Security Engineering and approved by the CISO, and retained as Evidence under CMP-004.
- **SEC-019.5.2.5** `[PCI]` For the purposes of this section, Significant Change (GOV-006) SHALL include at minimum: a new acceptance channel or payment flow; a new or replaced payment application or TPSP; a new network connection to the CDE; a change to a segmentation control; a data center or Cloud Service region move; a merger or acquisition; and a Sev-1 or Sev-2 Security Incident involving the CDE. The scope update SHALL be completed within 30 days of the Significant Change going live.
- **SEC-019.5.2.6** `[PCI]` Service provider: significant changes to organizational structure (e.g. a company merger or acquisition, or a change or reassignment of personnel responsible for security controls) SHALL result in a documented, CISO-approved review of the impact to PCI DSS scope and the applicability of controls, with results communicated to executive management, within 30 days of the change (PCI DSS 12.5.3).

### 5.3 Network and data-flow diagrams (PCI DSS 1.2.3, 1.2.4)

- **SEC-019.5.3.1** `[PCI]` The Head of Security Engineering SHALL maintain an accurate network diagram that shows all connections between the CDE and other networks, including any wireless networks, and all segmentation controls (PCI DSS 1.2.3).
- **SEC-019.5.3.2** `[PCI]` The Head of Security Engineering SHALL maintain accurate data-flow diagrams that show all account data flows across systems and networks, for every payment stage and acceptance channel (PCI DSS 1.2.4).
- **SEC-019.5.3.3** `[PCI]` Each diagram SHALL show: system components or zones by scope category; trust boundaries; network security controls; encryption points and protocols for CHD in transit; points where PAN is tokenized, truncated, hashed or encrypted; TPSP connections; and the date of last update and approver.
- **SEC-019.5.3.4** `[PCI]` Diagrams SHALL be updated before the Change record of any Change that alters them is closed under SEC-013, and SHALL be reviewed for accuracy by the Head of Security Engineering at least every 6 months and at each scope confirmation.
- **SEC-019.5.3.5** `[PCI]` Diagrams SHALL be classified Confidential under SEC-002 and stored with access restricted under SEC-003.

### 5.4 Segmentation

- **SEC-019.5.4.1** `[PCI]` Where segmentation is used to reduce PCI DSS scope, the CDE SHALL be isolated from all out-of-scope networks by network security controls configured under SEC-007 that deny all traffic not specifically authorized, in both directions.
- **SEC-019.5.4.2** `[PCI]` Every permitted connection into or out of the CDE SHALL have a documented business justification, a named owner and an approval recorded under SEC-013. The rule set for segmentation controls SHALL be reviewed at the frequency in SEC-007.
- **SEC-019.5.4.3** `[PCI]` Connected-to and security-impacting system components SHALL be configured and protected to the same PCI DSS requirements as the CDE components they connect to or affect, unless the Head of Security Engineering documents why a requirement does not apply.
- **SEC-019.5.4.4** `[PCI]` Administrative access into the CDE SHALL be only through dedicated, hardened jump hosts or privileged access management tooling under SEC-005, with MFA as required by SEC-004.
- **SEC-019.5.4.5** `[PCI]` Segmentation controls SHALL be tested by penetration testing at the segmentation-testing frequency set in SEC-011.7.3 and after any change to segmentation controls or methods, to confirm that they are operational and effective and isolate all out-of-scope systems from the CDE (PCI DSS 11.4.5; service provider 11.4.6). Testing SHALL cover every segmentation control and method in use, and SHALL be performed by a qualified internal resource or qualified external third party with organizational independence from the controls tested.
- **SEC-019.5.4.6** `[PCI]` A segmentation test that shows an out-of-scope system can reach the CDE SHALL be treated as a Sev-2 Security Incident under RES-002, and the affected system SHALL be treated as in scope until the gap is remediated and retested.

### 5.5 CDE inventory and cardholder data inventory

- **SEC-019.5.5.1** `[PCI]` The Head of Security Engineering SHALL maintain, within the Asset Inventory (SEC-001), an inventory of all system components in PCI DSS scope, including a description of their function and use (PCI DSS 12.5.1), with: identifier; function; scope category; network zone; location or Cloud Service region; System Owner; whether CHD or SAD is stored; and the hardware and software versions.
- **SEC-019.5.5.2** `[PCI]` The Head of Security Engineering SHALL maintain a cardholder data inventory recording, for every location where CHD is stored (database, table, file share, Backup, log, paper, voice recording):

| Field | Content |
|---|---|
| Data store identifier | Asset Inventory ID and logical location |
| Data elements | PAN, cardholder name, expiration date, service code; SAD before authorization (issuers only) |
| Form of PAN | Full (rendered unreadable under 5.7), truncated, tokenized, hashed, encrypted |
| Protection method | Encryption algorithm and key reference (SEC-006), hashing method, or token vault |
| Business justification | Documented need for storage |
| Retention | Reference to the CHD retention rule in CMP-004 row R-13, and the purge mechanism |
| Data Owner and System Owner | Named individuals |
| Last verified | Date of last data discovery confirmation |

- **SEC-019.5.5.3** `[PCI]` The SOC Manager SHALL run automated data discovery for unencrypted PAN across the CDE, connected-to systems and out-of-scope systems where PAN could plausibly reside (file shares, collaboration tools, ticketing systems, email, log stores, data lakes, developer environments), at least every 3 months and before each scope confirmation.
- **SEC-019.5.5.4** `[PCI]` PAN found in any location not recorded in the cardholder data inventory, or found unprotected, SHALL be reported to the SOC within 24 hours of discovery and handled as a Security Incident under RES-002 (PCI DSS 12.10.7). The response SHALL determine how the PAN got there, securely delete or migrate it into the CDE, and remediate the data leak or process gap.
- **SEC-019.5.5.5** `[PCI]` Retention, purge frequency and the prohibition on storing SAD after authorization are set in CMP-004. Secure deletion follows SEC-017.

### 5.6 PAN display and copying (PCI DSS 3.4)

- **SEC-019.5.6.1** `[PCI]` PAN SHALL be masked when displayed, on screens, reports, receipts, logs and exports, so that at most the BIN and the last four digits are displayed (PCI DSS 3.4.1).
- **SEC-019.5.6.2** `[PCI]` Only roles with a documented business need to see more than the masked PAN MAY view it. The Data Owner SHALL maintain a list of such roles, each with its business justification and the number of digits it may see, approved by the CISO, and access SHALL be granted under SEC-003.
- **SEC-019.5.6.3** `[PCI]` When personnel use remote-access technologies to reach the CDE, technical controls SHALL prevent copying or relocating PAN (e.g. clipboard, file transfer, drive mapping, print, screen capture) except for personnel with documented, explicit authorization and a legitimate, defined business need (PCI DSS 3.4.2).
- **SEC-019.5.6.4** `[PCI]` PAN SHALL NOT be sent by end-user messaging technologies (e.g. email, instant messaging, SMS, chat). Where a documented business need exists and the CISO approves it, the PAN SHALL be secured with strong cryptography meeting SEC-006 (PCI DSS 4.2.2). Inbound PAN received by these channels SHALL be handled under SEC-019.5.5.4.

### 5.7 Rendering PAN unreadable (PCI DSS 3.3.2, 3.5)

- **SEC-019.5.7.1** `[PCI]` PAN SHALL be rendered unreadable anywhere it is stored, including on removable Media, in Backups and in logs, using one of the following (PCI DSS 3.5.1):
  1. one-way hashes based on strong cryptography of the entire PAN, which SHALL be keyed cryptographic hashes with associated key-management processes (PCI DSS 3.5.1.1);
  2. truncation (hashing SHALL NOT be used to replace the truncated segment);
  3. index tokens, with the token vault itself protected as CDE; or
  4. strong cryptography with associated key-management processes under SEC-006.
- **SEC-019.5.7.2** `[PCI]` Where both hashed and truncated versions of the same PAN are present in the environment, additional controls SHALL be in place so that the two versions cannot be correlated to reconstruct the original PAN.
- **SEC-019.5.7.3** `[PCI]` Disk-level or partition-level encryption SHALL be used to render PAN unreadable only on removable electronic Media, or, for non-removable Media, only in combination with one of the mechanisms in SEC-019.5.7.1 (PCI DSS 3.5.1.2). Where disk-level or partition-level encryption is used, logical access SHALL be managed separately and independently of native operating system authentication and access control, and decryption keys SHALL NOT be associated with user accounts (PCI DSS 3.5.1.3).
- **SEC-019.5.7.4** `[PCI]` SAD stored electronically before completion of authorization SHALL be encrypted using strong cryptography under SEC-006 (PCI DSS 3.3.2).
- **SEC-019.5.7.5** `[PCI]` Issuers and companies that support issuing services: any storage of SAD SHALL be limited to that needed for a legitimate issuing business need, documented, approved by the CISO, and secured (PCI DSS 3.3.3).
- **SEC-019.5.7.6** `[PCI]` Cryptographic algorithms, key lengths, cryptoperiods and key management for CHD protection are set in SEC-006.

### 5.8 Payment Page script integrity and tamper detection (PCI DSS 6.4.3, 11.6.1)

- **SEC-019.5.8.1** `[PCI]` This section applies to every Payment Page, and to every page that hosts an embedded payment form (e.g. an iframe), that is delivered to a consumer's browser by the Organization or on its behalf.
- **SEC-019.5.8.2** `[PCI]` The System Owner of each Payment Page SHALL manage all scripts loaded and executed in the consumer's browser on that page (PCI DSS 6.4.3):
  1. a method is implemented to confirm that each script is authorized (e.g. an approval recorded under SEC-013);
  2. a method is implemented to assure the integrity of each script (e.g. Subresource Integrity hashes, Content Security Policy with allow-listed sources and nonces or hashes); and
  3. an inventory of all scripts is maintained with a written business or technical justification for why each is necessary.
- **SEC-019.5.8.3** `[PCI]` The System Owner SHALL review the script inventory against the scripts actually executed on each Payment Page at least every 3 months and before each release that changes the Payment Page.
- **SEC-019.5.8.4** `[PCI]` A change- and tamper-detection mechanism SHALL be deployed that alerts personnel to unauthorized modification (including indicators of compromise, changes, additions and deletions) to the security-impacting HTTP headers and the script contents of Payment Pages as received by the consumer browser (PCI DSS 11.6.1). The mechanism SHALL evaluate the received HTTP headers and Payment Pages at least every 24 hours.
- **SEC-019.5.8.5** `[PCI]` Alerts from the mechanism in SEC-019.5.8.4 SHALL be sent to the SOC and triaged as Critical under the alert triage SLA in SEC-012. A confirmed unauthorized script or header change SHALL be handled as a Sev-1 Security Incident under RES-002 and the page SHALL be taken offline or reverted until resolved.
- **SEC-019.5.8.6** `[PCI]` Where the Organization fully outsources the Payment Page to a PCI DSS-validated TPSP (e.g. full redirect or embedded iframe), the System Owner SHALL obtain written confirmation that the TPSP meets 6.4.3 and 11.6.1 for its pages, and SHALL apply SEC-019.5.8.2 to SEC-019.5.8.5 to the Organization's page that embeds or redirects to the TPSP, to the extent required by the Organization's validation method.

### 5.9 POI device protection (PCI DSS 9.5.1)

- **SEC-019.5.9.1** `[PCI]` POI devices that capture payment card data via direct physical interaction with the card SHALL be protected from tampering and unauthorized substitution (PCI DSS 9.5.1).
- **SEC-019.5.9.2** `[PCI]` The Head of Security Engineering SHALL maintain an up-to-date list of POI devices, including make and model, location, and device serial number or other unique identifier (PCI DSS 9.5.1.1), as part of the Asset Inventory, and SHALL reconcile it to physical devices at least every 3 months.
- **SEC-019.5.9.3** `[PCI]` POI device surfaces SHALL be inspected to detect tampering and unauthorized substitution (PCI DSS 9.5.1.2) at the following minimum frequencies, confirmed by a Targeted Risk Analysis under RSK-002.5.8.1 (PCI DSS 9.5.1.2.1):

| Device type | Minimum inspection frequency |
|---|---|
| Unattended devices (e.g. kiosks, unattended payment terminals) | At the start of each day the location operates |
| Attended devices in public-facing locations | At least weekly, and at each shift change where devices are left unattended |
| Devices in storage or back-office locations | Before deployment and at least every 3 months |

- **SEC-019.5.9.4** `[PCI]` Each inspection SHALL check the serial number against the list, tamper-evident seals, external casing, cabling and attached devices (e.g. skimmers or overlays), and SHALL be recorded with the inspector, date, time and result.
- **SEC-019.5.9.5** `[PCI]` Personnel at POI locations SHALL be trained to: verify the identity of any third-party person claiming to be repair or maintenance personnel before granting access to modify or troubleshoot devices; not install, replace or return devices without verification; recognize suspicious behavior around devices; and report suspected tampering or substitution (PCI DSS 9.5.1.3). Training is delivered under PPL-002 role-based training.
- **SEC-019.5.9.6** `[PCI]` Suspected tampering or substitution SHALL be reported to the SOC immediately, the device SHALL be removed from use, and the event SHALL be handled as a Security Incident under RES-002.

### 5.10 PCI-specific governance

- **SEC-019.5.10.1** `[PCI]` Targeted Risk Analyses for PCI DSS requirements that allow the entity to set a frequency (PCI DSS 12.3.1) SHALL be performed and reviewed under RSK-002.5.8.1 to RSK-002.5.8.3. The Head of Security Engineering SHALL perform them for technical Controls in the CDE.
- **SEC-019.5.10.2** `[PCI]` Targeted Risk Analyses for requirements met using the customized approach (PCI DSS 12.3.2) SHALL be performed and approved under RSK-002.5.8.4 and RSK-002.5.8.5.
- **SEC-019.5.10.3** `[PCI]` The Head of Security Engineering SHALL review the hardware and software technologies in use in the CDE at least every 12 months, confirming that they continue to receive security fixes, are supported by the vendor, and still meet the Organization's PCI DSS needs, and SHALL document a remediation plan for any technology approaching end of life (PCI DSS 12.3.4). Cryptographic cipher suite and protocol review (12.3.3) is under SEC-006.
- **SEC-019.5.10.4** `[PCI]` The Head of Procurement SHALL maintain, with the Head of Security Engineering, a list of all TPSPs with which account data is shared or that could affect the security of account data, including a description of each service (PCI DSS 12.8.1). Contract and due diligence requirements for these TPSPs (12.8.2, 12.8.3) are set in RSK-003.
- **SEC-019.5.10.5** `[PCI]` The Head of Security Engineering SHALL monitor each TPSP's PCI DSS compliance status at least every 12 months, by obtaining its current Attestation of Compliance or equivalent evidence (PCI DSS 12.8.4).
- **SEC-019.5.10.6** `[PCI]` The Head of Security Engineering SHALL maintain a responsibility matrix recording, for each TPSP, which PCI DSS requirements are managed by the TPSP, which by the Organization, and which are shared (PCI DSS 12.8.5), and SHALL review it at least every 12 months and when a TPSP service changes.
- **SEC-019.5.10.7** `[PCI]` Service provider: the CISO SHALL be the executive accountable for the protection of CHD and the PCI DSS compliance program, including defining a charter that covers accountability and communication to executive management (PCI DSS 12.4.1), recorded under GOV-001.5.5.7.
- **SEC-019.5.10.8** `[PCI]` Service provider: the Head of Security Engineering SHALL perform reviews at least every 3 months to confirm that personnel are performing their tasks under the suite, covering at minimum daily log reviews (SEC-012), configuration reviews of network security controls (SEC-007), application of Configuration Baselines (SEC-013), responses to security alerts (SEC-012), and change management (SEC-013). Results SHALL be documented and signed off by the CISO (PCI DSS 12.4.2, 12.4.2.1).
- **SEC-019.5.10.9** `[PCI]` Service provider: the Organization SHALL acknowledge in writing to customers its responsibility for the security of account data it possesses or otherwise stores, processes or transmits on their behalf, or to the extent it could affect the security of the customer's CDE, and SHALL support customers' requests for its PCI DSS compliance status and responsibility matrix (PCI DSS 12.9.1, 12.9.2).

### 5.11 Compliance validation

- **SEC-019.5.11.1** `[PCI]` The Head of Security Engineering SHALL coordinate the annual PCI DSS assessment by the validation method recorded under SEC-019.4.1, and SHALL deliver the resulting Report on Compliance or Self-Assessment Questionnaire and Attestation of Compliance to the acquirer, payment brands or customers, as required, by the due date they set.
- **SEC-019.5.11.2** `[PCI]` The CISO SHALL sign the Attestation of Compliance as the Organization's executive officer, after confirming that all findings are remediated or recorded with a remediation plan.
- **SEC-019.5.11.3** `[PCI]` Quarterly ASV scans and internal and external vulnerability scans are performed under SEC-011, and their results SHALL be included in the assessment evidence.
- **SEC-019.5.11.4** `[PCI]` The Internal Audit Director SHALL include PCI DSS controls in the control testing plan under CMP-002 so that each requirement is tested at least once between annual assessments.

### 5.12 PCI DSS requirement cross-reference

- **SEC-019.5.12.1** `[PCI]` Every PCI DSS v4.0.1 requirement not implemented in sections 5.1 to 5.11 SHALL be implemented by the home document listed below, and SHALL apply to all system components in the CDE and connected-to / security-impacting categories. REF-001 holds the requirement-level mapping.

| PCI DSS requirement | Topic | Home document(s) |
|---|---|---|
| 1 (except 1.2.3, 1.2.4) | Network security controls | SEC-007; SEC-009 (cloud) |
| 1.2.3, 1.2.4 | Network and data-flow diagrams | SEC-019 section 5.3 |
| 2 | Secure configurations, vendor defaults | SEC-013 (Configuration Baselines); SEC-009 |
| 3.1 | Policies and roles for stored account data | SEC-002; this Standard |
| 3.2 | Account data retention | CMP-004 |
| 3.3.1 | No SAD after authorization | CMP-004; SEC-002 |
| 3.3.2, 3.3.3, 3.4, 3.5 | SAD before authorization; PAN masking and copying; rendering PAN unreadable | SEC-019 sections 5.6 and 5.7 |
| 3.6, 3.7 | Cryptographic key protection and management | SEC-006 |
| 4 (except 4.2.2) | Strong cryptography in transit | SEC-006; SEC-007 |
| 4.2.2 | PAN in end-user messaging | SEC-019.5.6.4; SEC-014 |
| 5 | Anti-malware and anti-phishing | SEC-008; SEC-014 |
| 6.1–6.3 | Secure development; vulnerability identification and patching | SEC-010; SEC-011 |
| 6.4.1, 6.4.2 | Protection of public-facing web applications | SEC-010; SEC-007 |
| 6.4.3 | Payment Page scripts | SEC-019 section 5.8 |
| 6.5 | Change management, separation of environments | SEC-013; SEC-010 |
| 7 | Access by business need to know | SEC-003 |
| 8 | Identification and authentication | SEC-004; SEC-005; SEC-003 |
| 9.1–9.4 | Physical access, Media handling and destruction | SEC-016; SEC-001; SEC-017 |
| 9.5 | POI devices | SEC-019 section 5.9 |
| 10 | Logging and monitoring; time synchronization | SEC-012; CMP-004 (log retention) |
| 11.1–11.4 | Wireless detection; vulnerability scans; penetration and segmentation testing | SEC-011; SEC-007 (wireless) |
| 11.5 | Intrusion detection, change detection on critical files | SEC-012 (intrusion detection); SEC-013.5.9.3 (change detection) |
| 11.6 | Payment Page tamper detection | SEC-019 section 5.8 |
| 12.1, 12.2 | Information security policy; acceptable use | ISP-000; GOV-002; GOV-004 |
| 12.3.1, 12.3.2, 12.3.4 | Targeted risk analyses; technology review | RSK-002 section 5.8 (TRAs); SEC-019.5.10.3 (technology review) |
| 12.3.3 | Cipher suites and protocols review | SEC-006 |
| 12.4 | Executive responsibility; service provider quarterly reviews | GOV-001; SEC-019 section 5.10 |
| 12.5 | Scope, inventory | SEC-019 sections 5.1, 5.2, 5.5 |
| 12.6 | Security awareness | PPL-002 |
| 12.7 | Personnel screening | PPL-001 |
| 12.8 | TPSP management | RSK-003; SEC-019 section 5.10 |
| 12.9 | Service provider support for customers | SEC-019 section 5.10 |
| 12.10 | Incident response | RES-001; RES-002; RES-003; SEC-019.5.5.4 |
| Appendix A1 | Multi-tenant service providers | SEC-009 |
| Appendix A2 | SSL / early TLS for card-present POS POI terminals | SEC-006 |
| Appendix A3 | Designated Entities Supplemental Validation | SEC-019 (applies only if the Organization is designated by an acquirer or payment brand) |

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| Head of Security Engineering | Owns this Standard; classifies scope; performs scope confirmations; maintains diagrams, CDE inventory, cardholder data inventory, POI list, targeted risk analyses, TPSP compliance monitoring and responsibility matrix; coordinates the annual assessment |
| CISO | Approves this Standard, scope confirmations and scope-reduction decisions; approves roles that see unmasked PAN; signs the Attestation of Compliance; is the accountable executive for PCI DSS (service provider) |
| SOC Manager | Runs PAN data discovery; triages Payment Page tamper alerts; handles unexpected PAN and POI tampering as Security Incidents |
| System Owners of Payment Pages and CDE systems | Manage Payment Page scripts; implement masking and PAN protection; keep components recorded in the inventory |
| Data Owner of CHD | Justifies CHD storage; maintains the list of roles that may see unmasked PAN |
| Head of Procurement | Maintains the TPSP list with the Head of Security Engineering; applies RSK-003 contract terms |
| Head of Facilities | Supports POI device inspections at Organization locations |
| Workforce Members at POI locations | Perform and record POI inspections; report suspected tampering |
| Internal Audit Director | Includes PCI DSS controls in the CMP-002 testing plan |
| GC | Records PCI entity type and validation level in the Obligations Register |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| SEC-019.7.1 | Scope confirmation (merchant) | At least every 12 months and upon Significant Change |
| SEC-019.7.2 | Scope confirmation (service provider) | At least every 6 months and upon Significant Change |
| SEC-019.7.3 | Scope update after Significant Change | Within 30 days of the change going live |
| SEC-019.7.4 | Organizational change scope review (service provider) | Within 30 days of the change |
| SEC-019.7.5 | Diagram update | Before the Change record is closed; accuracy review every 6 months and at each scope confirmation |
| SEC-019.7.6 | Segmentation testing | At the frequency in SEC-011.7.3 and after any change to segmentation controls |
| SEC-019.7.7 | PAN data discovery | At least every 3 months and before each scope confirmation |
| SEC-019.7.8 | Unexpected PAN reported to SOC | Within 24 hours of discovery |
| SEC-019.7.9 | PAN display | BIN and last four digits maximum, unless a CISO-approved role with documented business need |
| SEC-019.7.10 | Stored PAN | Rendered unreadable (keyed hash, truncation, token, or strong cryptography under SEC-006) |
| SEC-019.7.11 | Payment Page script inventory review | At least every 3 months and before each Payment Page release |
| SEC-019.7.12 | Payment Page tamper-detection evaluation | At least every 24 hours |
| SEC-019.7.13 | Payment Page tamper alert triage | Critical, under the SEC-012 alert triage SLA |
| SEC-019.7.14 | POI list reconciliation | At least every 3 months |
| SEC-019.7.15 | POI inspection | Table in SEC-019.5.9.3 |
| SEC-019.7.16 | Targeted Risk Analysis review | Per RSK-002.7.12 and RSK-002.7.13 |
| SEC-019.7.17 | CDE technology review | At least every 12 months |
| SEC-019.7.18 | TPSP PCI DSS compliance monitoring and responsibility matrix review | At least every 12 months |
| SEC-019.7.19 | Service provider personnel task reviews | At least every 3 months |
| SEC-019.7.20 | PCI DSS assessment | Every 12 months, by the validation method recorded under SEC-019.4.1 |
| SEC-019.7.21 | CHD retention, purge and SAD storage | As set in CMP-004 |
| SEC-019.7.22 | MFA for CDE access; password rules where a password is the only factor | As set in SEC-004 |
| SEC-019.7.23 | ASV and internal/external vulnerability scanning | As set in SEC-011 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Scope confirmation completed within the required interval | 100% | Quarterly | Head of Security Engineering |
| In-scope system components recorded in the Asset Inventory with a scope category | 100% | Quarterly | Head of Security Engineering |
| Unexpected PAN locations found by data discovery | 0 | Each discovery run | SOC Manager |
| Segmentation tests passed with no out-of-scope path to the CDE | 100% | Each test | Head of Security Engineering |
| Payment Page scripts in the inventory with authorization and integrity control | 100% | Quarterly | Head of Security Engineering |
| Unauthorized Payment Page changes detected and not resolved within the Sev-1 SLA in RES-002.7.2 | 0 | Monthly | SOC Manager |
| POI inspections completed on schedule | 100% | Monthly | Head of Security Engineering |
| TPSPs with a current Attestation of Compliance or equivalent evidence | 100% | Quarterly | Head of Security Engineering |
| Open PCI DSS assessment findings past remediation date | 0 | Monthly | CISO |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

In addition:

- A PCI DSS requirement that cannot be met as stated MAY be addressed only by a Compensating
  Control documented to the PCI DSS Appendix B and C worksheet, approved through CMP-003 and
  accepted by the assessor. An Exception without an accepted Compensating Control does not
  change PCI DSS compliance status.
- No Exception MAY be granted for storage of SAD after authorization, for storing PAN in a
  readable form, or for an out-of-scope system with an untested path to the CDE.

## 10. Enforcement

Non-compliance is handled under CMP-007.

PCI DSS non-compliance can result in fines from acquirers or payment brands, increased
transaction fees, mandatory forensic investigation, or loss of the ability to accept payment
cards. Deliberate storage of SAD or bypassing of segmentation controls SHALL be escalated to the
CISO within 1 business day of discovery.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| SEC-019.5.1 – 5.2 | 4.3; A.5.9, A.5.12 | ID.AM-01, ID.AM-07, GV.OC-03 | CM-8, PM-5, RA-2 | 1.1, 3.2 | CC3.2, CC6.1 | APO03, BAI09 | `[PCI]` 12.5.1, 12.5.2, 12.5.2.1, 12.5.3 |
| SEC-019.5.3 | A.5.9, A.8.20 | ID.AM-03 | CM-8, PL-8, AC-4 | 3.8, 12.4 | CC6.6 | APO03 | `[PCI]` 1.2.3, 1.2.4 |
| SEC-019.5.4 | A.8.20, A.8.22 | PR.IR-01 | SC-7, AC-4, CA-8 | 12.2, 13.4, 18.2 | CC6.6 | DSS05 | `[PCI]` 1.3, 1.4, 11.4.5, 11.4.6 |
| SEC-019.5.5 | A.5.9, A.5.12, A.8.12 | ID.AM-07, DE.CM-09 | CM-8, PM-5, SI-4 | 3.1, 3.2 | CC6.1, C1.1 | BAI09 | `[PCI]` 12.5.1, 12.10.7, 3.2.1 |
| SEC-019.5.6 – 5.7 | A.8.11, A.8.24 | PR.DS-01, PR.DS-02 | SC-28, SC-13, AC-3 | 3.11, 3.10, 3.3 | CC6.1, CC6.7, C1.1 | DSS05 | `[PCI]` 3.3.2, 3.3.3, 3.4.1, 3.4.2, 3.5.1, 3.5.1.1–3.5.1.3, 4.2.2 |
| SEC-019.5.8 | A.8.26, A.8.28, A.8.32 | PR.PS-06, DE.CM-09 | SI-7, CM-7, SI-4 | 16.1, 2.7 | CC7.1, CC8.1 | BAI06 | `[PCI]` 6.4.3, 11.6.1 |
| SEC-019.5.9 | A.7.2, A.7.8, A.7.9 | PR.AA-06, DE.CM-02 | PE-3, PE-6, MA-5 | 1.1 | CC6.4 | DSS05 | `[PCI]` 9.5.1, 9.5.1.1, 9.5.1.2, 9.5.1.2.1, 9.5.1.3 |
| SEC-019.5.10 | 6.1.2; A.5.19–5.22 | GV.SC-07, ID.RA-01 | RA-3, SA-9, SR-6, PM-9 | 15.1, 15.5 | CC3.2, CC9.2 | APO10, APO12 | `[PCI]` 12.3.1–12.3.4, 12.4.1, 12.4.2, 12.8.1, 12.8.4, 12.8.5, 12.9 |
| SEC-019.5.11 – 5.12 | 9.2; A.5.35, A.5.36 | GV.OV-01 | CA-2, CA-7 | 18.1 | CC4.1 | MEA03 | `[PCI]` PCI DSS v4.0.1 (all requirements) |

## 12. Related documents

ISP-000, GOV-001, GOV-002, GOV-004, RSK-002, RSK-003, CMP-001, CMP-002, CMP-003, CMP-004,
CMP-007, SEC-001, SEC-002, SEC-003, SEC-004, SEC-005, SEC-006, SEC-007, SEC-008, SEC-009,
SEC-010, SEC-011, SEC-012, SEC-013, SEC-014, SEC-016, SEC-017, RES-001, RES-002, RES-003,
PPL-001, PPL-002, REF-001

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Head of Security Engineering | | | |
| Approver: Chief Information Security Officer (CISO) | | | |
