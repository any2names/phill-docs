# SEC-008 — Endpoint & Mobile Device Security Policy (incl. BYOD)

## 1. Document control

| Field | Value |
|---|---|
| Document ID | SEC-008 |
| Title | Endpoint & Mobile Device Security Policy (incl. BYOD) |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Information Officer (CIO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-004, SEC-001, SEC-002, SEC-003, SEC-004, SEC-005, SEC-006, SEC-007, SEC-011, SEC-012, SEC-013, SEC-015, SEC-017, PPL-001, RES-001, RES-002, RES-003 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CIO | Initial release |

## 3. Purpose

This Policy sets the Organization's mandatory requirements for securing Endpoints and Mobile
Devices that access Organization Information Assets, whether Organization-owned or
personally owned under BYOD. It ensures that every such device is enrolled, hardened,
encrypted, protected against Malware, kept current, and can be locked or wiped if lost,
stolen or no longer authorized.

## 4. Scope

| Dimension | In scope |
|---|---|
| People | All Workforce Members and Third Parties who use an Endpoint to access Organization Information Assets |
| Systems | Organization-owned laptops, desktops, workstations, virtual desktops, tablets and Mobile Devices; personally owned devices used under BYOD; Third-Party-owned devices used to access Organization Information Assets. Section 5.3 (Malware protection) also applies to servers and cloud workloads |
| Data | All Organization data stored on, processed by or accessed from in-scope devices, at every Classification Level |
| Locations | All locations from which in-scope devices are used, including offices, homes and travel (travel-specific requirements are in SEC-015) |
| Third parties | Third Parties whose personnel access Organization Information Assets from their own devices, through contract terms set under RSK-003 |

Network-level remote access methods are governed by SEC-007. Disposal and sanitization of
devices are governed by SEC-017.

## 5. Policy statements

### 5.1 Device enrolment and inventory

- **SEC-008.5.1.1** Every Organization-owned Endpoint SHALL be enrolled in the Organization's unified endpoint management (UEM) or mobile device management (MDM) platform before it is issued to a Workforce Member.
- **SEC-008.5.1.2** Enrolment SHALL be performed through an automated provisioning service (for example, a zero-touch or autopilot enrolment program) so that the device cannot be used without enrolment after a reset.
- **SEC-008.5.1.3** Every enrolled Endpoint SHALL be recorded in the Asset Inventory (SEC-001) with its assigned User, serial number, operating system version and encryption status, synchronized from the UEM/MDM platform at least daily.
- **SEC-008.5.1.4** Access to Organization applications through single sign-on SHALL be conditioned on device compliance: only Endpoints that are enrolled and meet the compliance policy in this section, or BYOD devices meeting section 5.8, SHALL be granted access to Confidential or Restricted data.
- **SEC-008.5.1.5** The UEM/MDM compliance policy SHALL evaluate, at minimum: enrolment status, EDR agent health, disk encryption, operating system version, screen lock configuration, jailbreak/root detection, and host firewall status.
- **SEC-008.5.1.6** An Endpoint that has not checked in with the UEM/MDM platform for the period in SEC-008.7.3 SHALL be marked non-compliant and lose access under SEC-008.5.1.4. An Endpoint that has not checked in for the longer period in SEC-008.7.3 SHALL be investigated by the IT Service Desk as potentially lost under section 5.9.

### 5.2 Configuration and hardening

- **SEC-008.5.2.1** Endpoints SHALL be configured from an approved Configuration Baseline for each operating system, maintained under SEC-013 and derived from a recognized hardening benchmark (for example, CIS Benchmarks).
- **SEC-008.5.2.2** Host-based firewalls SHALL be enabled on all Endpoints as required by SEC-007.
- **SEC-008.5.2.3** Endpoints SHALL lock automatically after the idle session timeout set in SEC-004 and SHALL require re-authentication to unlock. Workforce Members' duty to lock an unattended Endpoint is set in GOV-004.5.3.2.
- **SEC-008.5.2.4** Mobile Devices SHALL require a device passcode of at least 6 digits, or biometric unlock backed by such a passcode, and SHALL erase Organization data after the number of consecutive failed unlock attempts in SEC-008.7.7.
- **SEC-008.5.2.5** Only software from the Organization's approved software catalog SHALL be installed on Organization-owned Endpoints. Software installation SHALL be delivered through the UEM/MDM platform or the approved self-service catalog.
- **SEC-008.5.2.6** Web browsers on Organization-owned Endpoints SHALL be centrally managed, with automatic updates enabled and browser extensions restricted to an approved list.
- **SEC-008.5.2.7** Jailbroken, rooted or otherwise compromised operating systems SHALL be detected by the UEM/MDM platform and SHALL be blocked from accessing Organization Information Assets.
- **SEC-008.5.2.8** Bluetooth discoverable mode, AirDrop/nearby sharing from unknown contacts, and auto-join to open wireless networks SHALL be disabled by configuration profile where the operating system supports it.
- **SEC-008.5.2.9** On Endpoints and servers in the scope set by SEC-001.5.8.3, including Privileged Access Workstations, application control SHALL run in blocking mode and SHALL permit execution only of software on the Authorized Software List (SEC-001). Changes to the allowlist SHALL be made under SEC-013.

### 5.3 Malware protection and endpoint detection and response (EDR)

- **SEC-008.5.3.1** The Organization's approved EDR agent SHALL be installed and active on every Organization-owned laptop, desktop, workstation, virtual desktop and server, and on every cloud workload where the agent or an agentless equivalent is supported.
- **SEC-008.5.3.2** The EDR agent SHALL use behavior-based detection in addition to signatures, SHALL update its detection content automatically at least daily, and SHALL be configured in prevention (block) mode for known-malicious activity.
- **SEC-008.5.3.3** The EDR agent SHALL be tamper-protected so that Users, including local administrators, cannot disable or uninstall it without an authorized uninstall token held by Workforce Members designated by the Head of Security Engineering.
- **SEC-008.5.3.4** EDR telemetry and alerts SHALL be sent to the SOC and SIEM as specified in SEC-012.
- **SEC-008.5.3.5** The SOC Manager SHALL maintain the capability to isolate an Endpoint from the network remotely through the EDR platform, and SHALL use it under RES-002.
- **SEC-008.5.3.6** Mobile Devices SHALL run mobile threat defense where the UEM/MDM platform supports it, and SHALL in any case be subject to the jailbreak/root detection in SEC-008.5.2.7.
- **SEC-008.5.3.7** `[PCI]` A CDE system component MAY be excluded from SEC-008.5.3.1 only where the Head of Security Engineering has documented that it is not at risk from Malware, and re-evaluates evolving Malware threats to it at the frequency set by a Targeted Risk Analysis under RSK-002.5.8.1 (PCI DSS 5.2.3, 5.2.3.1).
- **SEC-008.5.3.8** `[HIPAA]` Endpoints that store or access ePHI SHALL meet section 5.3 without exception, as a protection from malicious software under 45 CFR §164.308(a)(5)(ii)(B).

### 5.4 Encryption

- **SEC-008.5.4.1** All Organization-owned laptops, desktops, workstations, tablets and Mobile Devices SHALL use full-disk or full-device encryption meeting the algorithm minimums in SEC-006, enabled before the device is issued.
- **SEC-008.5.4.2** Disk encryption recovery keys SHALL be escrowed automatically to the UEM/MDM platform or the identity service, and access to recovery keys SHALL be logged and limited to the IT Service Desk and Workforce Members designated by the Head of Security Engineering.
- **SEC-008.5.4.3** An Endpoint whose encryption is disabled or not verified SHALL be marked non-compliant and lose access under SEC-008.5.1.4.
- **SEC-008.5.4.4** Pre-boot authentication or a hardware-bound key (for example, a TPM or Secure Enclave) SHALL protect the encryption key so that removed storage cannot be read on another device.

### 5.5 Operating system support and patching

- **SEC-008.5.5.1** Endpoints SHALL run an operating system version that receives security updates from its vendor, and no older than the minimum version in SEC-008.7.10.
- **SEC-008.5.5.2** Operating system, browser and application security updates SHALL be deployed automatically through the UEM/MDM platform and installed within the remediation SLA in SEC-011.
- **SEC-008.5.5.3** The UEM/MDM compliance policy SHALL mark as non-compliant any Endpoint that has not installed an available security update by the end of the remediation SLA in SEC-011, and the Endpoint SHALL lose access under SEC-008.5.1.4 until updated.
- **SEC-008.5.5.4** Endpoints running an operating system that has reached vendor end of support SHALL be handled under the end-of-support requirements in SEC-001 and SEC-011.
- **SEC-008.5.5.5** Endpoint firmware (BIOS/UEFI) updates SHALL be deployed through the UEM/MDM platform or vendor management tool within the remediation SLA in SEC-011.

### 5.6 Local administrator restrictions

- **SEC-008.5.6.1** Workforce Members SHALL NOT have standing local administrator rights on Organization-owned Endpoints.
- **SEC-008.5.6.2** Where a Workforce Member requires elevated rights on an Endpoint, elevation SHALL be granted through an endpoint privilege management tool or Just-in-Time Access under SEC-005, scoped to the specific application or task, and logged.
- **SEC-008.5.6.3** Local administrator accounts on Endpoints SHALL have unique, randomly generated passwords per device, rotated automatically by a local administrator password solution, with retrieval logged.
- **SEC-008.5.6.4** Developers who require persistent administrative capability for build and test tooling SHALL be provided with it through a separate, isolated environment (for example, a managed virtual machine or cloud development environment) in preference to local administrator rights on the primary Endpoint. Any standing exception SHALL be approved under CMP-003.

### 5.7 Removable media

- **SEC-008.5.7.1** Writing to removable storage Media (USB mass storage, external drives, memory cards) from Organization-owned Endpoints SHALL be blocked by default.
- **SEC-008.5.7.2** Write access MAY be granted to a named Workforce Member for a stated business purpose, approved by their manager and the Head of Security Engineering, for a maximum of 90 days per approval, and only to Organization-issued, hardware-encrypted Media registered in the Asset Inventory.
- **SEC-008.5.7.3** Restricted data SHALL NOT be written to removable Media unless the Data Owner has approved the transfer and the Media is encrypted per SEC-006.
- **SEC-008.5.7.4** Autorun and autoplay SHALL be disabled for all removable Media.
- **SEC-008.5.7.5** Removable Media SHALL be scanned automatically by the EDR agent when connected. `[PCI]` This includes all removable electronic Media connected to CDE systems (PCI DSS 5.3.3).
- **SEC-008.5.7.6** Removable Media that is no longer needed SHALL be returned to the IT Service Desk for sanitization under SEC-017.

### 5.8 Bring Your Own Device (BYOD)

- **SEC-008.5.8.1** BYOD SHALL be permitted only for the device types and access in SEC-008.7.12. Any other use of a personally owned device to access Organization Information Assets SHALL be prohibited.
- **SEC-008.5.8.2** Before using BYOD, the Workforce Member SHALL accept the Organization's BYOD terms, which state the controls applied to the device, the data the Organization can and cannot see, and the selective wipe right in SEC-008.5.8.6. Acceptance SHALL be recorded and retained under CMP-004.
- **SEC-008.5.8.3** BYOD Mobile Devices SHALL access Organization data only through managed applications protected by an application protection (MAM) policy or a separate managed work profile/container. The policy SHALL enforce: an application PIN or device passcode, encryption of Organization data, blocking of copy/paste and save-as from managed to unmanaged applications, and blocking of backups of Organization data to personal cloud storage.
- **SEC-008.5.8.4** BYOD laptops and desktops SHALL access Organization applications only through a virtual desktop, browser isolation, or a managed browser session that prevents download of Confidential and Restricted data to the device.
- **SEC-008.5.8.5** BYOD devices SHALL meet minimum requirements checked at each sign-in: a vendor-supported operating system version, a device passcode, and no jailbreak or root.
- **SEC-008.5.8.6** The Organization SHALL be able to selectively wipe Organization data and managed applications from a BYOD device. The Organization SHALL NOT perform a full device wipe of a personally owned device.
- **SEC-008.5.8.7** The Organization SHALL NOT collect personal content (personal email, photos, messages, browsing history or location) from BYOD devices. `[GDPR]` `[CPRA]` The CPO SHALL confirm that BYOD telemetry collected is limited to the device attributes needed for the compliance checks in SEC-008.5.8.5, recorded in the ROPA (TPL-010).
- **SEC-008.5.8.8** Restricted data SHALL NOT be stored on BYOD devices. `[PCI]` BYOD devices SHALL NOT access the CDE. `[HIPAA]` BYOD devices SHALL NOT store ePHI outside the managed container.
- **SEC-008.5.8.9** BYOD access SHALL be revoked and Organization data selectively wiped at Separation, within the access revocation timeline in SEC-003.

### 5.9 Lost or stolen devices and remote wipe

- **SEC-008.5.9.1** Workforce Members SHALL report the loss or theft of any Organization-owned device or BYOD device holding Organization data to the security reporting channel and the IT Service Desk within the reporting time limit in RES-001 (RES-001.5.2.5).
- **SEC-008.5.9.2** On receiving the report, the IT Service Desk SHALL, within the time in SEC-008.7.15: lock the device remotely; revoke the device's certificates and session tokens; and, for Organization-owned devices, issue a remote wipe command, or for BYOD devices, issue a selective wipe.
- **SEC-008.5.9.3** The IT Service Desk SHALL notify the SOC of every lost or stolen device report. The SOC SHALL assess the report as a potential Security Incident under RES-002, taking into account the device's encryption status and the Classification Level of data accessible from it.
- **SEC-008.5.9.4** Where a lost or stolen device held or could access Restricted data and encryption cannot be confirmed from UEM/MDM records, the SOC SHALL escalate the case under RES-001, and the CPO SHALL assess notification obligations under RES-003.
- **SEC-008.5.9.5** A police report SHOULD be filed for stolen devices, and the reference recorded in the incident record.
- **SEC-008.5.9.6** A recovered device SHALL be re-imaged before reuse.

### 5.10 Device lifecycle and return

- **SEC-008.5.10.1** Organization-owned Endpoints SHALL be returned at Separation within the period set in PPL-001, and SHALL be sanitized under SEC-017 before reissue or disposal.
- **SEC-008.5.10.2** Endpoints SHALL be removed from the UEM/MDM platform and the Asset Inventory only after sanitization is confirmed.
- **SEC-008.5.10.3** Third-Party-owned devices used to access Organization Information Assets SHALL meet the requirements of section 5.8 (BYOD) or SHALL access through a virtual desktop only, as stated in the Third-Party contract under RSK-003.
- **SEC-008.5.10.4** When an Endpoint is sanitized by Cryptographic Erase under SEC-017.5.2.4, its escrowed recovery keys (SEC-008.5.4.2) SHALL be deleted as part of the sanitization, and the deletion SHALL be recorded before the Endpoint is removed under SEC-008.5.10.2.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CIO | Owns this Policy; operates the UEM/MDM platform, approved software catalog and IT Service Desk; ensures device enrolment, encryption, patching and lifecycle requirements are met. |
| Head of Security Engineering | Defines EDR and hardening configuration; approves removable Media write access; holds EDR uninstall tokens; reviews compliance policy settings. |
| SOC Manager | Monitors EDR alerts; isolates Endpoints; assesses lost or stolen device reports under RES-002. |
| CISO | Approves BYOD terms and Exceptions within the authority in CMP-003. |
| CPO | Confirms BYOD data collection is limited and recorded; assesses notification obligations for lost devices under RES-003. |
| CHRO | Ensures device return and BYOD revocation are part of the Separation process (PPL-001). |
| Workforce Member | Keeps the device enrolled and updated; does not disable controls; locks unattended devices; reports loss or theft within the required time. |
| Third Party | Complies with contractual device requirements; reports loss of devices holding Organization data. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| SEC-008.7.1 | UEM/MDM enrolment | 100% of Organization-owned Endpoints, before issue |
| SEC-008.7.2 | Asset Inventory synchronization from UEM/MDM | At least daily |
| SEC-008.7.3 | Endpoint check-in | No check-in for 14 days → non-compliant; 30 days → investigated as potentially lost |
| SEC-008.7.4 | EDR coverage | 100% of Organization-owned laptops, desktops, workstations, virtual desktops and servers; supported cloud workloads |
| SEC-008.7.5 | EDR detection content updates | At least daily, automatic |
| SEC-008.7.6 | Screen lock | Idle session timeout per SEC-004 |
| SEC-008.7.7 | Mobile Device passcode and failed attempts | ≥ 6 digits; Organization data erased after 10 failed attempts |
| SEC-008.7.8 | Full-disk encryption | Required on all Organization-owned Endpoints; algorithms per SEC-006; recovery keys escrowed |
| SEC-008.7.9 | Security update installation | Within the remediation SLA in SEC-011 |
| SEC-008.7.10 | Minimum operating system version | Vendor-supported and no more than one major version behind the current general-availability release (N-1) |
| SEC-008.7.11 | Removable Media write access | Blocked by default; approval max 90 days; Organization-issued encrypted Media only |
| SEC-008.7.12 | BYOD eligibility | Mobile Devices: email, calendar, collaboration and approved managed applications through MAM/work profile. Laptops/desktops: virtual desktop, browser isolation or managed browser only. No Restricted data storage; `[PCI]` no CDE access |
| SEC-008.7.13 | Standing local administrator rights | 0 for standard Users |
| SEC-008.7.14 | Lost or stolen device report | Within the reporting time limit in RES-001 |
| SEC-008.7.15 | Remote lock and wipe after report | Within 1 hour of the report |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Organization-owned Endpoints enrolled in UEM/MDM | 100% | Monthly | CIO |
| Endpoints and servers with healthy, reporting EDR agent | ≥ 99% | Weekly | Head of Security Engineering |
| Endpoints with verified full-disk encryption | 100% | Monthly | CIO |
| Endpoints within the SEC-011 SLA for security updates | ≥ 95% | Monthly | CIO |
| Endpoints on an operating system below the N-1 minimum | 0 | Monthly | CIO |
| Users with standing local administrator rights | 0 (excluding approved Exceptions) | Monthly | Head of Security Engineering |
| Active removable Media write approvals past 90 days | 0 | Monthly | Head of Security Engineering |
| Lost or stolen device reports with lock/wipe issued within 1 hour | 100% | Monthly | CIO |
| Separated Workforce Members with BYOD access remaining after the SEC-003 deadline | 0 | Monthly | CIO |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following SHALL NOT receive an Exception: disabling EDR on an Endpoint that accesses
Restricted data (SEC-008.5.3.1); operating an Organization-owned laptop or Mobile Device
without full-disk encryption (SEC-008.5.4.1); and storage of Restricted data on a BYOD
device (SEC-008.5.8.8).

## 10. Enforcement

Non-compliance is handled under CMP-007.

Devices that fail the compliance policy lose access automatically under SEC-008.5.1.4.
Deliberate tampering with EDR, encryption or UEM/MDM controls, and failure to report a lost
or stolen device, SHALL be referred to CMP-007.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| SEC-008.5.1 Enrolment & inventory | A.8.1, A.5.9 | ID.AM-01, PR.AA-05 | CM-8, AC-19 | 1.1, 4.6 | CC6.1 | DSS05.03, BAI09 | PCI DSS 12.5.1; 45 CFR §164.310(b) |
| SEC-008.5.2 Hardening | A.8.1, A.8.9, A.8.19 | PR.PS-01, PR.PS-05 | CM-6, CM-7, AC-11, CM-11 | 4.1, 4.3, 4.10, 2.5 | CC6.8, CC7.1 | DSS05.03, BAI10 | PCI DSS 2.2; 45 CFR §164.310(c), §164.312(a)(2)(iii) |
| SEC-008.5.3 Malware & EDR | A.8.7 | DE.CM-09, PR.PS-01 | SI-3, SI-4 | 10.1, 10.2, 10.7, 13.2 | CC6.8, CC7.2 | DSS05.01 | PCI DSS 5.2, 5.3; 45 CFR §164.308(a)(5)(ii)(B) |
| SEC-008.5.4 Encryption | A.8.1, A.8.24 | PR.DS-01 | SC-28, SC-12 | 3.6 | CC6.1, CC6.7 | DSS05.03 | 45 CFR §164.312(a)(2)(iv); GDPR Art. 32 |
| SEC-008.5.5 OS support & patching | A.8.8, A.8.1 | PR.PS-02, ID.RA-01 | SI-2, SA-22 | 7.3, 7.4, 2.2 | CC7.1 | DSS05.03 | PCI DSS 6.3.3 |
| SEC-008.5.6 Local admin | A.8.2, A.8.18 | PR.AA-05 | AC-6, AC-2 | 5.4 | CC6.1, CC6.3 | DSS05.04 | PCI DSS 7.2.1 |
| SEC-008.5.7 Removable media | A.7.10, A.8.12 | PR.DS-01 | MP-7, MP-2 | 10.3, 10.4 | CC6.7 | DSS05.06 | PCI DSS 5.3.3; 45 CFR §164.310(d)(1) |
| SEC-008.5.8 BYOD | A.8.1, A.6.7 | PR.AA-05, PR.DS-01 | AC-19, AC-20 | 4.12 | CC6.1, CC6.7 | DSS05.03 | GDPR Art. 5(1)(c), Art. 32; Cal. Civ. Code §1798.100 |
| SEC-008.5.9 Lost/stolen & wipe | A.8.1, A.6.8, A.5.24 | RS.MA-01, PR.DS-01 | AC-19, IR-6 | 4.11 | CC6.7, CC7.3 | DSS02 | 45 CFR §164.308(a)(6); RES-003 obligations |
| SEC-008.5.10 Lifecycle & return | A.5.11, A.7.14 | ID.AM-08 | MP-6, PS-4 | 3.5 | CC6.5 | BAI09 | 45 CFR §164.310(d)(2) |

## 12. Related documents

ISP-000, GOV-004, GOV-006, SEC-001, SEC-002, SEC-003, SEC-004, SEC-005, SEC-006, SEC-007,
SEC-011, SEC-012, SEC-013, SEC-015, SEC-017, SEC-019, PPL-001, RES-001, RES-002, RES-003,
RSK-003, TPL-010, CMP-003, CMP-004, CMP-007

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CIO | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
