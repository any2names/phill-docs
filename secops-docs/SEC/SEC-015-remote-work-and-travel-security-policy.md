# SEC-015 — Remote Work & Travel Security Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | SEC-015 |
| Title | Remote Work & Travel Security Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Chief Information Security Officer (CISO) |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months, and on the event-triggered reviews in GOV-002.7.4 |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | GOV-004, SEC-002, SEC-007, SEC-008, SEC-014, SEC-016, SEC-017, RES-001, RES-002, PPL-001, PPL-002, CMP-001, CMP-004, CMP-005 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | CISO | Initial release |

## 3. Purpose

This policy sets the Organization's requirements for protecting Information Assets when
Workforce Members work outside Organization facilities, whether at home, in public places
or while travelling, including travel to High-risk Jurisdictions and passage through
border inspection. It addresses the physical and environmental risks of working outside
controlled premises; the technical controls on devices and connections are set in SEC-008
and SEC-007 and are not restated here.

## 4. Scope

- **People:** all Workforce Members and Third Parties who access Organization Information Assets from any location other than an Organization facility.
- **Systems:** Organization-issued Endpoints and Mobile Devices, BYOD devices permitted under SEC-008, Loaner Devices, removable Media, and printed information.
- **Data:** all Organization information accessed, stored, printed or discussed outside Organization facilities, with requirements scaled by Classification Level under SEC-002.
- **Locations:** home and other private residences, co-working spaces, client sites, hotels, transport (air, rail, vehicles), public venues, and all international locations.
- **Third parties:** Third Parties working remotely on Organization Information Assets SHALL meet this policy as a contractual condition.

Device configuration (Encryption, EDR, patching, screen lock, remote wipe, BYOD conditions)
is governed by SEC-008. Remote access methods (VPN, zero-trust access, remote desktop) are
governed by SEC-007. Secure disposal of Media and paper is governed by SEC-017. Physical
security of Organization facilities is governed by SEC-016.

## 5. Policy statements

### 5.1 Eligibility and authorization

- **SEC-015.5.1.1** Remote work SHALL be permitted only for Workforce Members who have completed security awareness training under PPL-002 and acknowledged this policy under GOV-002.
- **SEC-015.5.1.2** Access to Organization Information Assets from a remote location SHALL be made only from devices that meet SEC-008 and only through access paths approved under SEC-007.
- **SEC-015.5.1.3** Roles that require handling of physical Restricted information (e.g. paper records containing PHI or CHD) SHALL NOT perform that handling remotely unless the Data Owner has approved remote handling in writing and the conditions in section 5.6 are met.
- **SEC-015.5.1.4** `[PCI]` Remote access to the CDE SHALL meet SEC-019 in addition to this policy.

### 5.2 Remote work environment

- **SEC-015.5.2.1** Workforce Members SHALL work in a location where screens cannot be viewed, and conversations about Confidential or Restricted information cannot be overheard, by persons not authorized to access that information, including household members and visitors.
- **SEC-015.5.2.2** Workforce Members SHALL NOT allow any other person, including household members, to use an Organization-issued device.
- **SEC-015.5.2.3** Workforce Members SHALL lock their device screen manually whenever they leave it unattended, in addition to the automatic idle timeout in SEC-004.
- **SEC-015.5.2.4** When working remotely for more than 5 days in any calendar month, Workforce Members SHALL use a home or private network that meets these conditions:
  1. the router administrator password is changed from the factory default;
  2. Wi-Fi is protected with WPA2-Personal (AES) or WPA3; WEP, WPA (TKIP) and open networks SHALL NOT be used;
  3. router firmware is set to update automatically or is updated at least every 6 months;
  4. remote administration of the router from the internet is disabled; and
  5. Universal Plug and Play (UPnP) is disabled where the router allows it.
- **SEC-015.5.2.5** Voice-activated smart devices (e.g. smart speakers) SHALL be muted or located out of hearing range during conversations involving Restricted information.
- **SEC-015.5.2.6** Organization-issued devices SHALL NOT be left unattended in vehicles, and SHALL NOT be left visible in a vehicle at any time. Devices left at home SHALL be powered off or locked and stored out of sight.
- **SEC-015.5.2.7** Video calls SHALL use a blurred or virtual background, or a background with no visible Confidential or Restricted information (e.g. whiteboards, documents, screens).
- **SEC-015.5.2.8** Remote workers SHALL NOT connect Organization-issued devices to personal peripherals that store data (e.g. personal USB storage, network-attached storage) except as permitted by SEC-008.

### 5.3 Public places and public Wi-Fi

- **SEC-015.5.3.1** Restricted information SHALL NOT be viewed, discussed or worked on in public places (e.g. cafés, airport lounges, aircraft, trains, hotel lobbies), except where the Workforce Member has a privacy screen fitted, is positioned so no one can see the screen, and holds no conversation about it.
- **SEC-015.5.3.2** Organization-issued laptops used in public places SHALL be fitted with a privacy screen filter. The CIO SHALL issue privacy screens to all Workforce Members with Organization-issued laptops who travel or work in public places.
- **SEC-015.5.3.3** Public, shared or untrusted Wi-Fi networks (including hotel, airport, conference and café networks) SHALL be used only with the Organization's remote access controls under SEC-007 active for all traffic. A personal or Organization-issued mobile hotspot SHOULD be used in preference to public Wi-Fi.
- **SEC-015.5.3.4** Workforce Members SHALL NOT use public or shared computers (e.g. hotel business centers, kiosks) to access Organization Information Systems, and SHALL NOT print Organization information on them.
- **SEC-015.5.3.5** Workforce Members SHALL NOT use public USB charging ports or charging cables they do not own to charge Organization devices; they SHALL use their own charger connected to a mains outlet or a data-blocking adapter.
- **SEC-015.5.3.6** Devices SHALL be kept in the Workforce Member's physical possession or in a locked location (e.g. a hotel safe or locked room) at all times when travelling. Devices SHALL NOT be placed in checked luggage.

### 5.4 International travel and High-risk Jurisdictions

- **SEC-015.5.4.1** The CISO, with the GC, SHALL maintain a list of High-risk Jurisdictions, reviewed at least every 6 months and within 10 business days of a material change in government travel advisories, sanctions or export-control restrictions. The list SHALL consider: national government travel advisories; sanctions and export-control regimes; laws permitting compelled access to devices or data; and threat intelligence produced under RSK-005.
- **SEC-015.5.4.2** Workforce Members SHALL notify the SOC, through the travel notification channel published by the CISO, of international business travel at least 10 business days before departure, stating destinations and dates. For travel to a High-risk Jurisdiction, notification SHALL be acknowledged by the CISO or delegate before travel.
- **SEC-015.5.4.3** The GC SHALL confirm, before travel, that taking any Organization device, software or encryption technology to the destination complies with applicable export-control and import laws, as recorded in the Obligations Register (CMP-001).
- **SEC-015.5.4.4** Working remotely from outside the Workforce Member's country of employment SHALL require prior written approval from the Workforce Member's manager, the CHRO and the CISO. [DECISION REQUIRED: Maximum duration of approved remote work from another country per 12-month period. Recommended default: 30 days.] Remote work from a High-risk Jurisdiction SHALL NOT be approved except for business travel under SEC-015.5.4.5.
- **SEC-015.5.4.5** For travel to a High-risk Jurisdiction, Workforce Members SHALL:
  1. carry only a Loaner Device issued for the trip, and SHALL NOT carry their regular Organization-issued Endpoint or Mobile Device;
  2. carry no Restricted information and only the Confidential information required for the trip, approved by the Data Owner;
  3. access Organization Information Systems only through the remote access path specified by the CISO for the trip;
  4. not connect the Loaner Device to any untrusted Media or accept Media from third parties;
  5. not install software on the Loaner Device; and
  6. carry personal devices only if those devices have no access to Organization Information Systems.
- **SEC-015.5.4.6** The CIO SHALL maintain a pool of Loaner Devices. Each Loaner Device SHALL be built from the Configuration Baseline (SEC-013) with the minimum applications needed for the trip, SHALL meet SEC-008, and SHALL hold no cached credentials or data from prior use.
- **SEC-015.5.4.7** On return from a High-risk Jurisdiction, the Workforce Member SHALL return the Loaner Device to the CIO's team within 2 business days, without connecting it to the Organization network. The device SHALL be quarantined and forensically imaged if the CISO requires, then sanitized under SEC-017 and rebuilt before reissue.
- **SEC-015.5.4.8** On return from a High-risk Jurisdiction, all passwords, Secrets and session tokens used during the trip SHALL be reset within 1 business day of return, and MFA authenticators used on the trip SHALL be re-registered.
- **SEC-015.5.4.9** Workforce Members travelling to any international destination SHOULD minimize the Confidential information stored locally on devices before departure, relying on access to Organization repositories through SEC-007.

### 5.5 Border device inspection

- **SEC-015.5.5.1** Workforce Members SHALL comply with lawful demands by border or law enforcement officials and SHALL NOT physically resist, lie to, or obstruct officials.
- **SEC-015.5.5.2** Where an official requests access to, or the passcode for, an Organization device, the Workforce Member SHALL state that the device is the property of the Organization and contains confidential business information, and SHALL request to contact the Organization's GC before providing access, where the request can be made without breaching local law.
- **SEC-015.5.5.3** Workforce Members SHALL NOT be required by the Organization to risk detention or arrest to protect a device. Where compelled, the Workforce Member MAY provide access.
- **SEC-015.5.5.4** Workforce Members SHALL report to the SOC within 24 hours (or at the earliest opportunity where communication is not possible) any event in which an Organization device was: inspected, taken out of the Workforce Member's sight, or unlocked for an official; or where credentials were disclosed. The report SHALL record the location, time, agency (if known), duration out of sight, and whether data was viewed or copied.
- **SEC-015.5.5.5** The SOC SHALL treat any reported inspection under SEC-015.5.5.4 as a potential Security Incident under RES-002. The device SHALL be treated as compromised: it SHALL be disconnected from Organization networks, its credentials and sessions revoked, and it SHALL be examined and sanitized under SEC-017 before reuse.
- **SEC-015.5.5.6** The GC SHALL assess whether an inspection resulted in access to Personal Data, PHI or other regulated data and whether notification obligations under RES-003 apply.
- **SEC-015.5.5.7** Before crossing a border, Workforce Members SHOULD power devices fully off so that full-disk Encryption under SEC-008 is in its locked state.

### 5.6 Printing at home and away from Organization facilities

- **SEC-015.5.6.1** Restricted information SHALL NOT be printed outside Organization facilities, except where the Data Owner has approved remote handling under SEC-015.5.1.3.
- **SEC-015.5.6.2** Confidential information SHOULD NOT be printed outside Organization facilities. Where printing is necessary, Workforce Members SHALL use a printer connected directly by USB or on a private home network meeting SEC-015.5.2.4, and SHALL collect printouts immediately.
- **SEC-015.5.6.3** Printers used for Organization information SHALL NOT be shared-access printers in public locations, hotels or co-working spaces, and SHALL NOT have cloud-printing services enabled that store print jobs with a third party, unless that service is approved under SEC-001.
- **SEC-015.5.6.4** Printed Confidential or Restricted information SHALL be disposed of only by a shredder meeting the destruction standard in SEC-017, or returned to an Organization facility for secure disposal. Such paper SHALL NOT be placed in household waste or recycling.

### 5.7 Physical security of documents and Media outside Organization facilities

- **SEC-015.5.7.1** Printed documents and removable Media containing Confidential or Restricted information SHALL be removed from Organization facilities only with the approval of the Data Owner and only in the minimum quantity required.
- **SEC-015.5.7.2** When not in use, such documents and Media SHALL be stored in a locked drawer, cabinet or container that household members and visitors cannot access.
- **SEC-015.5.7.3** In transit, such documents and Media SHALL be carried in a closed, opaque container under the Workforce Member's direct control, and SHALL NOT be read or left open in public places or left in vehicles.
- **SEC-015.5.7.4** `[PCI]` Media containing CHD sent or carried outside a facility SHALL be logged, transported by secure courier or another delivery method that can be accurately tracked, and approved by management before it leaves the facility.
- **SEC-015.5.7.5** `[HIPAA]` Paper or Media containing PHI SHALL be tracked from removal to return or destruction, in accordance with the device and media controls documented in CMP-008.
- **SEC-015.5.7.6** Documents and Media SHALL be returned to an Organization facility or securely destroyed under SEC-017 within 10 business days of the end of the purpose for which they were removed, and in all cases on Separation under PPL-001.

### 5.8 Reporting loss, theft and suspicious events

- **SEC-015.5.8.1** Loss or theft of an Organization device, printed Confidential or Restricted information, or removable Media while working remotely or travelling SHALL be reported as set out in SEC-008 for devices, and under RES-001 for documents and Media.
- **SEC-015.5.8.2** Workforce Members SHALL report to the SOC under RES-001 any suspected tampering with a device, unexpected device behavior after it was left unattended, or approaches seeking Organization information while travelling.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| CISO | Owns this policy; maintains the High-risk Jurisdiction list with the GC; acknowledges high-risk travel; specifies trip remote access paths; decides on forensic imaging of returned devices. |
| CIO | Maintains the Loaner Device pool; issues privacy screens; rebuilds and sanitizes returned Loaner Devices. |
| GC | Co-maintains the High-risk Jurisdiction list; confirms export-control compliance; advises Workforce Members facing border inspection; assesses regulatory notification after inspection. |
| CHRO | Approves remote work from outside the country of employment. |
| SOC Manager | Receives and investigates border inspection, loss and tampering reports under RES-002; revokes credentials of compromised devices. |
| Data Owner | Approves removal of Confidential or Restricted documents and Media and remote handling of Restricted paper records. |
| HIPAA Security Officer | `[HIPAA]` Confirms PHI tracking outside facilities meets CMP-008. |
| Workforce Member | Complies with remote environment, public place, travel, printing and document requirements; reports travel and incidents. |
| ISSC | Approves this policy. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| SEC-015.7.1 | Home network threshold | Required when working remotely > 5 days in a calendar month |
| SEC-015.7.2 | Home Wi-Fi security | WPA2-Personal (AES) or WPA3; router default admin password changed; remote admin and UPnP disabled |
| SEC-015.7.3 | Home router firmware | Automatic updates, or updated at least every 6 months |
| SEC-015.7.4 | Privacy screen | Required on Organization laptops used in public places |
| SEC-015.7.5 | Public Wi-Fi | Only with SEC-007 remote access active for all traffic |
| SEC-015.7.6 | High-risk Jurisdiction list review | Every 6 months, and within 10 business days of a material change |
| SEC-015.7.7 | International travel notice | At least 10 business days before departure; CISO acknowledgement for High-risk Jurisdictions |
| SEC-015.7.8 | Remote work from another country | Prior approval by manager, CHRO and CISO; maximum 30 days per 12 months (default, adopter decision) |
| SEC-015.7.9 | Device for High-risk Jurisdictions | Loaner Device only |
| SEC-015.7.10 | Loaner Device return | Within 2 business days of return, not connected to the Organization network |
| SEC-015.7.11 | Credential reset after high-risk travel | Within 1 business day of return |
| SEC-015.7.12 | Border inspection report | Within 24 hours, or at the earliest opportunity |
| SEC-015.7.13 | Restricted printing outside facilities | Prohibited unless Data Owner–approved remote handling |
| SEC-015.7.14 | Return or destruction of removed documents and Media | Within 10 business days of end of purpose; on Separation |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| High-risk Jurisdiction trips using a Loaner Device | 100% | Quarterly | CISO |
| Loaner Devices returned and sanitized within 2 business days | 100% | Quarterly | CIO |
| Credential resets completed within 1 business day of high-risk travel | 100% | Quarterly | SOC Manager |
| Border inspection events reported within 24 hours | 100% | Quarterly | SOC Manager |
| High-risk Jurisdiction list reviewed within 6 months | 100% | Semi-annually | CISO |
| Workforce Members acknowledging this policy | 100% of remote-eligible staff | Annually | CISO |
| Lost or stolen devices and documents while remote or travelling | Reported trend | Quarterly | SOC Manager |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following requirements SHALL NOT receive an Exception: SEC-015.5.4.5 item 1 (Loaner Device only for High-risk Jurisdictions) and SEC-015.5.5.4 (reporting of border inspection).

## 10. Enforcement

Non-compliance is handled under CMP-007.

Failure to report a lost device, a border inspection or a disclosure of credentials SHALL be treated as an aggravating factor in any disciplinary decision under CMP-007.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| SEC-015.5.1 | A.6.7 | PR.AA-05 | AC-17, PE-17 | 12.7 | CC6.1 | DSS05.04 | PCI DSS 8.4.2, 12.3.1 |
| SEC-015.5.2 | A.6.7, A.7.7, A.7.9 | PR.AA-06, PR.DS-01 | PE-17, AC-11 | 12.7 | CC6.4 | DSS05.05 | HIPAA §164.310(b), §164.310(c) |
| SEC-015.5.3 | A.6.7, A.7.9, A.8.1 | PR.DS-02 | AC-17, AC-18, AC-19 | 12.7 | CC6.7 | DSS05.02 | — |
| SEC-015.5.4 | A.5.31, A.6.7, A.7.9 | GV.OC-03, ID.RA-03 | AC-19, PE-17 | 4.1 | CC3.2, CC6.7 | APO12.01, DSS05.03 | Export-control laws recorded in CMP-001 |
| SEC-015.5.5 | A.5.24, A.7.9 | RS.MA-01, PR.DS-01 | IR-6, AC-19 | 17.3 | CC7.3 | DSS02.01 | GDPR Art. 33; HIPAA §164.308(a)(6) |
| SEC-015.5.6 | A.7.7, A.7.14 | PR.DS-01 | MP-4, MP-6 | 3.5 | CC6.5 | DSS05.06 | HIPAA §164.310(d)(1) |
| SEC-015.5.7 | A.7.9, A.7.10 | PR.DS-01 | MP-4, MP-5 | 3.5 | CC6.4, CC6.7 | DSS05.06 | PCI DSS 9.4.2, 9.4.3, 9.4.4; HIPAA §164.310(d)(1) |
| SEC-015.5.8 | A.6.8 | RS.MA-01 | IR-6 | 17.3 | CC7.3 | DSS02.01 | — |

## 12. Related documents

ISP-000, GOV-002, GOV-004, GOV-006, SEC-001, SEC-002, SEC-004, SEC-007, SEC-008, SEC-013, SEC-014, SEC-016, SEC-017, SEC-019, RSK-005, RES-001, RES-002, RES-003, PPL-001, PPL-002, CMP-001, CMP-003, CMP-004, CMP-007, CMP-008, REF-001, REF-002

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: CISO | | | |
| Approver: ISSC Vice-Chair, on behalf of the ISSC (CISO recused as Document Owner under GOV-001.5.3.9) | | | |
