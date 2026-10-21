# SEC-017 — Media Sanitization & Secure Disposal Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | SEC-017 |
| Title | Media Sanitization & Secure Disposal Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Information Officer (CIO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-006, RSK-003, CMP-004, CMP-008, SEC-001, SEC-002, SEC-006, SEC-008, SEC-009, SEC-016, SEC-018, SEC-019 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CIO | Initial release |

## 3. Purpose

This Policy ensures that information cannot be recovered from Media, equipment or Cloud
Services after they are reused, returned, sold, recycled or destroyed, or after the data
reaches the end of its retention period. It requires Media Sanitization methods aligned with
NIST SP 800-88 Rev. 2 (Clear, Purge, Destroy) selected by Classification Level and media
type, controlled custody until sanitization, verification, and auditable records.

## 4. Scope

| Dimension | In scope |
|---|---|
| People | All Workforce Members and Third Parties who handle Media or equipment containing Organization information, or who request deletion of Organization data |
| Systems | All Media: hard disk drives, solid-state drives, NVMe and flash storage, USB and removable Media, memory cards, optical Media, magnetic tape, Endpoints, Mobile Devices, servers, storage arrays, network devices and printers or multifunction devices with storage, virtual disks, snapshots, and Cloud Service storage |
| Data | All Organization information at Internal, Confidential and Restricted levels (SEC-002), in electronic and paper form |
| Locations | All Organization premises, remote work locations, data centers, colocation facilities, Cloud Service regions, and Third-Party disposal facilities |
| Third parties | Disposal and destruction vendors, equipment lessors, repair and warranty providers, Cloud Service Providers, and any Third Party that holds Organization data at contract end |

## 5. Policy statements

### 5.1 General

- **SEC-017.5.1.1** All Media containing Organization information at Internal level or above SHALL be sanitized using the method required by section 5.2 before it is: reused within the Organization for a different purpose or user; released outside Organization control (sale, donation, return to lessor, warranty replacement, recycling); or disposed of.
- **SEC-017.5.1.2** Data SHALL be deleted or Media sanitized when the retention period in CMP-004 expires, unless a Legal Hold applies. Before any sanitization of Media holding records, the Data Custodian SHALL confirm with the GC's Legal Hold Register that no Legal Hold applies.
- **SEC-017.5.1.3** Sanitization methods SHALL follow NIST SP 800-88 Rev. 2 and the device manufacturer's documented sanitize commands. Where Media type or condition prevents the required method, the next stronger method SHALL be used (Clear → Purge → Destroy).
- **SEC-017.5.1.4** Media that is damaged, failed, or cannot be verified as sanitized SHALL be destroyed.
- **SEC-017.5.1.5** Every sanitization or destruction of Media from an asset in the Asset Inventory SHALL be recorded against the asset record under SEC-001, and the asset transitioned to the "Disposed" lifecycle state only after a sanitization record or Certificate of Destruction is received.

### 5.2 Sanitization method by Classification Level and media type

- **SEC-017.5.2.1** The minimum sanitization method SHALL be determined by the highest Classification Level ever stored on the Media (as recorded in the Asset Inventory) and by the disposition, as follows. "Internal reuse" means reuse inside Organization control; "Leaves control" means any release outside the Organization's physical or contractual control.

| Classification Level | Internal reuse | Leaves control | End of life |
|---|---|---|---|
| Public | None required | None required | None required |
| Internal | Clear | Purge | Purge, or Destroy |
| Confidential | Purge | Purge, with verification | Destroy, or Purge with verification |
| Restricted | Purge, with verification | SHALL NOT leave control unless Destroyed; Purge with 100% verification permitted only for lessor or warranty returns with CISO approval | Destroy |

- **SEC-017.5.2.2** The method for each media type SHALL be:

| Media type | Clear | Purge | Destroy |
|---|---|---|---|
| Magnetic hard disk drive (HDD) | Overwrite all user-addressable locations with a single pass of a fixed pattern, using a tool that verifies | ATA Secure Erase / SCSI Sanitize Overwrite; or degaussing with an NSA-listed degausser (renders drive inoperable) | Shred, disintegrate, pulverize or incinerate at a licensed facility |
| Solid-state drive (SATA, SAS, NVMe), flash, hybrid drives | Overwrite via standard read/write commands (limited assurance; Internal only) | Cryptographic Erase via ATA Sanitize Crypto Scramble / NVMe Format with crypto erase / SCSI Sanitize, followed by block erase where supported; or self-encrypting drive key destruction (SEC-006) | Shred or disintegrate to particle size ≤ 2 mm |
| Self-encrypting drives (SED, TCG Opal) | Overwrite | Cryptographic Erase by media encryption key destruction, provided the drive's encryption was enabled for the drive's entire use and is FIPS 140-3 validated | Shred or disintegrate |
| Endpoints and Mobile Devices with full-disk Encryption (SEC-008) | Operating system reset | Cryptographic Erase via the platform's factory reset with Encryption key destruction (managed through mobile device management), where Encryption was enabled for the device's entire use | Destroy storage component, or entire device |
| USB drives, memory cards, removable flash | Overwrite | Not reliable; treat as Destroy | Shred or disintegrate |
| Optical Media (CD, DVD, Blu-ray) | Not applicable | Not applicable | Shred or incinerate |
| Magnetic tape | Overwrite | Degauss with NSA-listed degausser | Shred or incinerate |
| Printers, copiers, multifunction devices, network devices | Manufacturer factory reset | Manufacturer sanitize function meeting NIST SP 800-88 Purge; or remove and Purge or Destroy the storage | Remove and Destroy storage |
| Paper and film | Not applicable | Not applicable | Internal and Confidential: cross-cut shred to DIN 66399 security level P-4 or higher · Restricted: cross-cut shred to P-5 or higher, pulping or incineration |
| Virtual disks, snapshots and images | Delete through platform | Cryptographic Erase by destruction of the volume or tenant key (section 5.6) | Not applicable |

- **SEC-017.5.2.3** Media that has held `[PCI]` CHD, `[HIPAA]` ePHI, or Secrets SHALL be treated as Restricted for this section, regardless of the Classification Level recorded for the system.
- **SEC-017.5.2.4** Cryptographic Erase SHALL be relied on only where: the Encryption algorithm meets SEC-006; the Encryption was active for the entire time the Media held Organization data; the key was not exported outside the device or KMS other than as an escrowed recovery key under SEC-008.5.4.2; and destruction of every copy of the key, including any escrowed recovery key (SEC-008.5.10.4), is evidenced.

### 5.3 Custody and storage before sanitization

- **SEC-017.5.3.1** Media awaiting sanitization or collection SHALL be held in a locked container or locked room under the access controls in SEC-016, recorded by serial number and asset identifier, and sanitized or collected within the time in SEC-017.7.2.
- **SEC-017.5.3.2** `[PCI]` Containers used to store materials awaiting destruction that contain CHD SHALL be secured to prevent access to their contents (PCI DSS 9.4.6).
- **SEC-017.5.3.3** Chain of Custody SHALL be recorded from removal from service to final sanitization or destruction, including each transfer, the individuals involved, date, time and seal number where applicable.
- **SEC-017.5.3.4** Media leaving Organization premises for off-site destruction SHALL be transported in locked or tamper-evident containers by the disposal vendor or by two Workforce Members, and the transfer SHALL be reconciled by serial number at handover.
- **SEC-017.5.3.5** Failed drives under warranty or repair SHALL NOT be returned to manufacturers or repair providers unless Purged with verification or the contract provides for drive retention ("keep your drive") by the Organization. [DECISION REQUIRED: Whether "keep your drive" support is required in all storage and server hardware contracts. Recommended default: required for any hardware that will hold Confidential or Restricted data]

### 5.4 Verification

- **SEC-017.5.4.1** Purge operations SHALL be verified by the sanitization tool's verification function or by an independent read-back of a sample of locations.
- **SEC-017.5.4.2** Verification coverage SHALL be at least the values in SEC-017.7.4.
- **SEC-017.5.4.3** Where verification fails, the Media SHALL be re-sanitized once; on a second failure it SHALL be Destroyed.
- **SEC-017.5.4.4** Personnel performing sanitization SHALL be trained in the tools and methods in this Policy before performing it, and training records SHALL be retained per CMP-004.

### 5.5 Records and Certificates of Destruction

- **SEC-017.5.5.1** For each Media item sanitized in-house, a sanitization record SHALL be created containing: asset identifier and serial number; manufacturer and model; media type; highest Classification Level; sanitization method (Clear, Purge, Destroy) and technique; tool and version; verification method and result; disposition (reuse, release, destruction); date; the individual performing sanitization; and the individual verifying it.
- **SEC-017.5.5.2** For each batch destroyed by a Third Party, a Certificate of Destruction SHALL be obtained within the time in SEC-017.7.5 containing at minimum: vendor name and facility; collection and destruction dates; serial numbers of every item (or, for paper, weight and container identifiers); destruction method and particle size; the name and signature of the vendor's responsible individual; and witness details where witnessed.
- **SEC-017.5.5.3** The Data Custodian SHALL reconcile each Certificate of Destruction against the custody record by serial number. Discrepancies SHALL be reported to the CISO within 1 business day and investigated as a potential Security Incident under RES-001.
- **SEC-017.5.5.4** Sanitization records and Certificates of Destruction SHALL be retained as control evidence per CMP-004 and linked to the asset record in the Asset Inventory.

### 5.6 Cloud Services and logical data deletion

- **SEC-017.5.6.1** Organization data in Cloud Services and SaaS SHALL be deleted at the end of retention (CMP-004), on decommissioning of a workload, and at contract end, using the provider's deletion functions, and covering primary storage, replicas, snapshots, Backups under Organization control, logs and caches.
- **SEC-017.5.6.2** Where data holding Confidential or Restricted information was encrypted with customer-managed keys (SEC-006), the Organization SHALL perform cryptographic erasure by scheduling destruction of the relevant keys after data deletion, once Legal Hold and retention checks are complete.
- **SEC-017.5.6.3** Because physical sanitization of shared cloud Media is performed by the Cloud Service Provider, the Organization SHALL, under RSK-003, obtain and review the provider's independent assurance (for example, a SOC 2 Type II report or ISO/IEC 27001 certificate) confirming that decommissioned Media is sanitized in line with NIST SP 800-88 or equivalent, at the vendor reassessment frequency in RSK-003.
- **SEC-017.5.6.4** At termination of a contract with any Third Party holding Organization Confidential or Restricted data, the Asset Owner SHALL obtain written certification of return or deletion of all Organization data, including Backups, within the time in SEC-017.7.6, or a statement of the data retained under legal obligation and the date of its deletion.
- **SEC-017.5.6.5** Deletion of Personal Data on request of a Data Subject is governed by CMP-010 and CMP-005; this Policy governs the technical method.
- **SEC-017.5.6.6** Deletion of Backups is governed by the retention periods in CMP-004 and the Backup controls in SEC-018; expired Backup Media SHALL be sanitized under section 5.2.

### 5.7 Third-party disposal vendors

- **SEC-017.5.7.1** Disposal and destruction vendors SHALL be assessed under RSK-003 before use and SHALL hold at least one current independent certification for secure data destruction (for example, NAID AAA) and, for electronic equipment recycling, an environmental certification (for example, R2 or e-Stewards).
- **SEC-017.5.7.2** Contracts with disposal vendors SHALL require: background-screened personnel; chain-of-custody records; destruction within the time in SEC-017.7.7 of collection; Certificates of Destruction meeting SEC-017.5.5.2; the Organization's right to witness destruction and to audit facilities; no resale of Media containing Organization data; notification of any loss of Media within 24 hours; and `[HIPAA]` a BAA where Media may contain PHI.
- **SEC-017.5.7.3** Restricted Media SHALL be destroyed on-site by a mobile shredding service, or off-site with a Workforce Member witnessing destruction in person or by live video, for at least the sample in SEC-017.7.8 of collections.

### 5.8 Payment card data `[PCI]`

- **SEC-017.5.8.1** `[PCI]` Hard-copy materials containing CHD SHALL be destroyed when no longer needed for business or legal reasons by cross-cut shredding, incineration or pulping so that CHD cannot be reconstructed, and materials awaiting destruction SHALL be stored in secure containers (PCI DSS 9.4.6).
- **SEC-017.5.8.2** `[PCI]` Electronic Media containing CHD SHALL be destroyed when no longer needed for business or legal reasons, or the CHD rendered unrecoverable so that it cannot be reconstructed (PCI DSS 9.4.7), using the Restricted methods in section 5.2.
- **SEC-017.5.8.3** `[PCI]` Retention and quarterly purge of stored CHD are governed by CMP-004 and SEC-019; the purge SHALL use a deletion method that renders the CHD unrecoverable.

### 5.9 Protected health information `[HIPAA]`

- **SEC-017.5.9.1** `[HIPAA]` Final disposition of ePHI and the hardware or electronic Media on which it is stored, and removal of ePHI before Media is made available for reuse, SHALL follow this Policy, implementing §164.310(d)(2)(i) and (ii). Accountability records for hardware and Media movements are maintained under SEC-001 and section 5.3.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CIO | Owns this Policy; operates in-house sanitization; maintains sanitization records; manages disposal vendor relationships with the Head of Procurement. |
| ISSC | Approves this Policy. |
| CISO | Approves Purge-only release of Restricted Media for lessor or warranty returns; receives discrepancy reports. |
| Head of Facilities | Provides locked storage for Media awaiting sanitization and secure paper-disposal containers; supports on-site shredding (SEC-016). |
| Head of Procurement | Includes disposal, "keep your drive" and data-return clauses in contracts. |
| Head of GRC | Assesses disposal vendors and Cloud Service sanitization assurance under RSK-003. |
| CTO | Implements cloud data deletion and cryptographic erasure for cloud workloads (SEC-009). |
| Head of Security Engineering | Executes key destruction for cryptographic erasure (SEC-006). |
| GC | Maintains the Legal Hold Register checked before sanitization. |
| Asset Owner | Initiates retirement; obtains Third-Party data return or deletion certification at contract end. |
| Data Custodian | Performs or arranges sanitization; maintains Chain of Custody; reconciles Certificates of Destruction. |
| Workforce Member | Places paper and Media for disposal only in designated secure containers; never disposes of Media in general waste. |
| Third Party | Disposal vendors and Cloud Service Providers sanitize per contract and provide evidence. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| SEC-017.7.1 | Sanitization standard | NIST SP 800-88 Rev. 2 Clear / Purge / Destroy per section 5.2 |
| SEC-017.7.2 | Maximum time Media held awaiting sanitization or collection | 30 days from removal from service |
| SEC-017.7.3 | Paper shredding particle security level | Internal and Confidential: DIN 66399 P-4 · Restricted: P-5 (or pulping / incineration) |
| SEC-017.7.4 | Purge verification coverage | Restricted: 100% of items · Confidential: 100% of items leaving control; 10% sample for internal reuse · Internal: 10% sample |
| SEC-017.7.5 | Certificate of Destruction receipt after collection | Within 30 days |
| SEC-017.7.6 | Third-Party certification of data return or deletion at contract end | Within 30 days of contract end |
| SEC-017.7.7 | Vendor destruction after collection | Within 10 business days |
| SEC-017.7.8 | Witnessed destruction of off-site Restricted Media | At least 1 collection in 4, and every collection containing `[PCI]` CHD or `[HIPAA]` ePHI Media |
| SEC-017.7.9 | Solid-state Media Destroy particle size | ≤ 2 mm |
| SEC-017.7.10 | Discrepancy between custody record and Certificate of Destruction reported to CISO | Within 1 business day |
| SEC-017.7.11 | Retention of sanitization records and Certificates of Destruction | Per CMP-004 (control evidence) |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Disposed assets with a sanitization record or Certificate of Destruction | 100% | Monthly | CIO |
| Media held awaiting sanitization > 30 days | 0 | Monthly | CIO |
| Certificates of Destruction received within 30 days | 100% | Monthly | CIO |
| Custody / certificate discrepancies | 0 unresolved | Monthly | CIO |
| Purge verification failures re-sanitized or destroyed | 100% | Quarterly | CIO |
| Disposal vendors with current assessment and certification | 100% | Every 12 months | Head of GRC |
| Contract terminations with data return or deletion certification within 30 days | 100% | Quarterly | Head of GRC |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following SHALL NOT receive an Exception: release of Restricted Media outside
Organization control without Destroy or approved verified Purge (SEC-017.5.2.1); disposal of
any Media in general waste; and `[PCI]` 9.4.6 and 9.4.7 requirements (section 5.8).

## 10. Enforcement

Non-compliance is handled under CMP-007.

Loss of Media awaiting sanitization or in transit to a disposal vendor SHALL be handled as a
Security Incident under RES-001.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| SEC-017.5.1 – 5.2 Methods | A.7.10, A.7.14, A.8.10 | PR.DS-01, PR.PS-03, ID.AM-08 | MP-6 | 3.5 | CC6.5, C1.2 | BAI09, DSS05.06 | `[HIPAA]` §164.310(d)(2)(i), (ii); `[GDPR]` Art. 5(1)(e), 17, 32 |
| SEC-017.5.3 – 5.5 Custody, verification, records | A.7.10, A.7.14 | ID.AM-08 | MP-4, MP-5, MP-6 | 3.5 | CC6.5, C1.2 | BAI09, DSS05.06 | `[PCI]` 9.4.6; `[HIPAA]` §164.310(d)(2)(iii) |
| SEC-017.5.6 Cloud and logical deletion | A.8.10, A.5.23 | PR.DS-01, GV.SC-10 | MP-6, SA-9, SI-12 | 3.4, 3.5 | C1.2, CC9.2 | APO10, DSS06 | `[GDPR]` Art. 17, 28(3)(g); `[CPRA]` §1798.105 |
| SEC-017.5.7 Disposal vendors | A.5.19, A.5.20, A.7.14 | GV.SC-05, GV.SC-07 | SA-9, SR-12 | 15.4 | CC9.2 | APO10 | `[HIPAA]` §164.308(b)(1) |
| SEC-017.5.8 `[PCI]` | A.7.14 | PR.DS-01 | MP-6 | 3.5 | C1.2 | DSS05.06 | `[PCI]` 3.2.1, 9.4.6, 9.4.7 |
| SEC-017.5.9 `[HIPAA]` | A.7.14 | PR.DS-01 | MP-6 | 3.5 | C1.2 | DSS05.06 | `[HIPAA]` §164.310(d)(2)(i), (ii) |

## 12. Related documents

ISP-000, GOV-006, RSK-003, CMP-003, CMP-004, CMP-005, CMP-007, CMP-008, CMP-010, SEC-001,
SEC-002, SEC-006, SEC-008, SEC-009, SEC-016, SEC-018, SEC-019, RES-001

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CIO | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
