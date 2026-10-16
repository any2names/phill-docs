# SEC-007 — Network Security Policy

## 1. Document control

| Field | Value |
|---|---|
| Document ID | SEC-007 |
| Title | Network Security Policy |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | 1 — Policy |
| Classification | Internal |
| Owner | Head of Security Engineering |
| Approver | Information Security Steering Committee (ISSC) |
| Effective date | [DECISION REQUIRED: Date of ISSC approval] |
| Next review date | Effective date + 12 months |
| Parent document | ISP-000 Information Security Program Charter |
| Related documents | SEC-001, SEC-003, SEC-004, SEC-005, SEC-006, SEC-009, SEC-011, SEC-012, SEC-013, SEC-015, SEC-019, RSK-003, RES-002 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | Head of Security Engineering | Initial release |

## 3. Purpose

This Policy sets the Organization's mandatory requirements for designing, operating and
monitoring its networks so that only authorized traffic flows between authorized
Information Systems. It establishes network zoning and segmentation, default-deny traffic
control, review of firewall and security-group rules, remote and wireless access, DNS and
egress filtering, denial-of-service resilience and network documentation.

## 4. Scope

| Dimension | In scope |
|---|---|
| People | All Workforce Members and Third Parties who design, build, operate, connect to or administer the Organization's networks |
| Systems | All wired, wireless, virtual and software-defined networks owned, leased or operated by or for the Organization, including on-premises data center and office networks, cloud virtual networks (VPCs, VNets), security groups and network access control lists, Kubernetes network policies, firewalls, routers, switches, load balancers, web application firewalls, VPN and ZTNA gateways, DNS services, proxies and wireless access points |
| Data | All data in transit across the networks above, at every Classification Level |
| Locations | Data centers, offices, colocation facilities, cloud regions, and remote locations connecting to Organization networks |
| Third parties | Third-Party network connections, managed network and security service providers, and Cloud Service Providers to the extent of the customer's responsibility under the shared responsibility model (SEC-009) |

Cloud-specific account structure and guardrails are governed by SEC-009; this Policy governs
the network controls inside those accounts. `[PCI]` Cardholder Data Environment scoping and
segmentation controls are specified in SEC-019; this Policy sets the general network
requirements that SEC-019 builds on.

## 5. Policy statements

### 5.1 Network architecture and zoning

- **SEC-007.5.1.1** The Head of Security Engineering SHALL maintain a documented network security architecture that assigns every network segment to one of the Trust Zones in SEC-007.7.1.
- **SEC-007.5.1.2** Each Trust Zone SHALL be implemented as one or more separate network segments (VLANs, subnets, virtual networks or equivalent), and traffic between zones SHALL pass through a network security control (firewall, security group, network ACL or network policy) that enforces the rules in section 5.2.
- **SEC-007.5.1.3** Production and non-production environments SHALL be in separate zones. Traffic from non-production to production SHALL be denied except for flows approved under SEC-007.5.2.3 and recorded in the rule set.
- **SEC-007.5.1.4** Systems that hold Restricted data SHALL be placed in a zone that is not directly reachable from the internet. Internet-facing services SHALL terminate in the DMZ zone or behind a managed load balancer or reverse proxy that is the only internet-reachable component.
- **SEC-007.5.1.5** Management interfaces of network devices, hypervisors, cloud control planes reachable over private connectivity, and out-of-band management controllers SHALL be reachable only from the Management zone, and access SHALL follow SEC-005.
- **SEC-007.5.1.6** Endpoints in the Corporate zone SHALL NOT have direct network access to the Production zone. Administrative access to production SHALL use a privileged access path defined in SEC-005 (for example, a bastion host or Privileged Access Workstation).
- **SEC-007.5.1.7** `[PCI]` The Cardholder Data Environment SHALL be segmented from all other zones as specified in SEC-019. Segmentation testing frequency is set in SEC-011.
- **SEC-007.5.1.8** `[HIPAA]` Systems that store or process ePHI SHALL be placed in a zone whose inbound and outbound flows are limited to those recorded in the rule set and data-flow diagram for that zone.
- **SEC-007.5.1.9** Each network segment SHALL be recorded in the Asset Inventory (SEC-001) with its zone, System Owner and the highest Classification Level of data it carries.

### 5.2 Default-deny traffic control

- **SEC-007.5.2.1** Every network security control SHALL be configured to deny all inbound and outbound traffic by default. Only traffic explicitly permitted by an approved rule SHALL be allowed.
- **SEC-007.5.2.2** Every permit rule SHALL specify source, destination, protocol and port. Rules permitting "any" source, "any" destination or "any" port SHALL NOT be used except for (a) inbound HTTPS to a published internet-facing service in the DMZ, or (b) a rule approved as an Exception under CMP-003.
- **SEC-007.5.2.3** Each new or changed rule SHALL be requested through SEC-013 change management and SHALL record: business justification, requesting System Owner, approver, ticket reference, and an expiry date where the rule is temporary.
- **SEC-007.5.2.4** Temporary rules SHALL expire automatically, or be removed by Workforce Members designated by the CIO for network operations, no later than the maximum in SEC-007.7.4.
- **SEC-007.5.2.5** Insecure protocols (including Telnet, FTP, TFTP, SNMPv1/v2c, HTTP for authenticated sessions, and SMBv1) SHALL NOT be permitted across zone boundaries. Where a legacy system requires one, an Exception SHALL be obtained under CMP-003 with compensating controls documented.
- **SEC-007.5.2.6** Data in transit across untrusted networks, and Confidential or Restricted data in transit across any network, SHALL be encrypted using the protocols and minimums in SEC-006.
- **SEC-007.5.2.7** Host-based firewalls SHALL be enabled on servers and on Endpoints (SEC-008) with a default-deny inbound policy.
- **SEC-007.5.2.8** Network security controls SHALL be configured from approved Configuration Baselines maintained under SEC-013, with vendor default credentials changed and unused services disabled before connection to any production zone.
- **SEC-007.5.2.9** Intrusion detection or prevention SHALL be deployed at the internet perimeter and at the boundary of each zone holding Restricted data. Signatures SHALL be updated automatically at least daily.
- **SEC-007.5.2.10** `[PCI]` Internet-facing web applications in or connected to the CDE SHALL be protected as required by SEC-010 (web application firewall, PCI DSS 6.4.2).

### 5.3 Firewall and security-group rule review

- **SEC-007.5.3.1** The System Owner of each network security control, with Workforce Members designated by the CIO for network operations, SHALL review every rule set at the frequency in SEC-007.7.3. The review SHALL confirm, for each rule, that the business justification is current, the rule is no broader than required, and the rule is still in use.
- **SEC-007.5.3.2** Rules with no matching traffic for 90 days SHALL be flagged during the review and SHALL be removed unless the System Owner documents a continuing need (for example, a disaster-recovery flow).
- **SEC-007.5.3.3** Rule-review results, including rules removed or tightened, SHALL be recorded and retained as Evidence under CMP-004.
- **SEC-007.5.3.4** `[PCI]` Rule sets on network security controls in, or connected to, the CDE SHALL be reviewed at least once every 6 months (PCI DSS 1.2.7), and the review SHALL confirm that all permitted services, protocols and ports are identified, approved and have a defined business need (PCI DSS 1.2.5).
- **SEC-007.5.3.5** Cloud security groups and network ACLs SHALL be defined through Infrastructure as Code under SEC-009 wherever the Cloud Service supports it, so that rule history is held in version control.
- **SEC-007.5.3.6** Automated tooling SHALL detect, at least daily, any rule that permits inbound traffic from the internet to a non-DMZ zone or to an administrative port (including SSH, RDP and database listener ports). Detections SHALL be raised as alerts to the SOC and triaged within the alert triage SLA in SEC-012.

### 5.4 Remote access

- **SEC-007.5.4.1** Remote access to Organization networks and internal applications SHALL use an approved Zero Trust Network Access (ZTNA) service or an approved VPN service. No other remote access method SHALL be permitted.
- **SEC-007.5.4.2** All remote access SHALL require MFA as specified in SEC-004.
- **SEC-007.5.4.3** ZTNA SHALL be the preferred method for new remote-access use cases. ZTNA policies SHALL grant access per application, not per network, and SHALL evaluate User identity and device posture (SEC-008) on each session.
- **SEC-007.5.4.4** VPN connections from Organization-managed Endpoints SHALL use full tunneling or an equivalent always-on secure web gateway, so that internet traffic from the Endpoint is subject to the controls in section 5.6.
- **SEC-007.5.4.5** Remote access sessions SHALL terminate after the idle session timeout in SEC-004.
- **SEC-007.5.4.6** Personally owned devices SHALL connect only through the methods permitted for BYOD in SEC-008. Full network-level VPN access SHALL NOT be granted to personally owned devices.
- **SEC-007.5.4.7** Third-Party remote access SHALL be approved under RSK-003, granted to named individual accounts (SEC-003), limited to the specific systems required, time-bound, and logged. Vendor access for support of production systems SHALL be enabled only for the duration of the approved support activity.
- **SEC-007.5.4.8** Remote access requirements for travel and working from home are set in SEC-015.

### 5.5 Wireless networks

- **SEC-007.5.5.1** Corporate wireless networks SHALL use WPA3-Enterprise, or WPA2-Enterprise where WPA3 is not supported by the access point, with 802.1X authentication against the central identity service. Pre-shared-key authentication SHALL NOT be used on corporate wireless networks.
- **SEC-007.5.5.2** Guest wireless networks SHALL be placed in the Guest zone, SHALL have internet-only access, and SHALL NOT route to any internal zone.
- **SEC-007.5.5.3** Wireless networks SHALL NOT be connected to the Production zone or the CDE. `[PCI]` Wireless networks at CDE locations SHALL be treated as out-of-scope networks and segmented from the CDE under SEC-019 section 5.4.
- **SEC-007.5.5.4** Wireless access points SHALL be managed centrally, with default credentials, SNMP community strings and administrative passwords changed before deployment.
- **SEC-007.5.5.5** Wireless intrusion detection or a rogue access point scan SHALL operate at every Organization office. `[PCI]` Testing for unauthorized wireless access points at CDE locations SHALL be performed at least every 3 months (PCI DSS 11.2.1), and detected unauthorized access points SHALL be handled as Security Incidents under RES-002.
- **SEC-007.5.5.6** Pre-shared keys on any wireless network that uses them (Guest or IoT) SHALL be changed at least every 12 months and within 5 business days after any Workforce Member with knowledge of the key is separated from a role requiring it.

### 5.6 DNS and egress filtering

- **SEC-007.5.6.1** Organization-managed Endpoints and servers SHALL resolve DNS only through approved resolvers that apply protective DNS filtering (blocking of known malicious, newly registered and uncategorized domains as configured by the Head of Security Engineering).
- **SEC-007.5.6.2** Outbound DNS from any zone to resolvers other than the approved resolvers SHALL be blocked at the network boundary, including DNS over HTTPS to unapproved providers where technically detectable.
- **SEC-007.5.6.3** Outbound traffic from the Production, Management, Restricted-data and CDE zones SHALL be default-deny and limited to destinations recorded in an allow list (by FQDN, IP range or service tag). Direct internet egress from these zones SHALL route through an egress proxy or egress firewall.
- **SEC-007.5.6.4** Web traffic from the Corporate zone and from managed Endpoints SHALL pass through a secure web gateway or equivalent that blocks categories designated in GOV-004 and known-malicious destinations.
- **SEC-007.5.6.5** External DNS zones owned by the Organization SHALL be signed with DNSSEC where the registry supports it, and SHALL be protected by registrar lock and MFA on registrar accounts.
- **SEC-007.5.6.6** Workforce Members designated by the CIO for network operations SHALL review public DNS records at least every 6 months and remove records pointing to decommissioned resources, to prevent subdomain takeover.
- **SEC-007.5.6.7** DNS query logs, proxy logs and egress firewall logs SHALL be forwarded to the SIEM as specified in SEC-012.

### 5.7 Distributed denial-of-service (DDoS) protection

- **SEC-007.5.7.1** Every internet-facing service supporting a Recovery Tier 0 or Tier 1 process (RSK-004) SHALL be protected by a DDoS mitigation service covering network-layer (L3/L4) and application-layer (L7) attacks.
- **SEC-007.5.7.2** DDoS mitigation SHALL be always-on for Tier 0 services. Tier 1 services MAY use on-demand mitigation where activation can be completed within 15 minutes of detection.
- **SEC-007.5.7.3** Origin servers protected by a DDoS or content-delivery service SHALL accept inbound traffic only from that service's published address ranges.
- **SEC-007.5.7.4** The Head of Security Engineering SHALL maintain a DDoS response runbook, aligned with RES-002, and SHALL test it with the mitigation provider at least every 12 months.

### 5.8 Network documentation

- **SEC-007.5.8.1** The Head of Security Engineering SHALL maintain current network diagrams showing every zone, every connection between zones, every connection to the internet and to Third Parties, and the network security controls at each boundary, including cloud virtual networks.
- **SEC-007.5.8.2** Data-flow diagrams SHALL be maintained for every flow of Restricted data across systems and networks. `[PCI]` Network and account-data flow diagrams for the CDE are maintained under SEC-019 section 5.3 (PCI DSS 1.2.3 and 1.2.4).
- **SEC-007.5.8.3** Network and data-flow diagrams SHALL be updated within the period in SEC-007.7.6 after any change that alters a zone, boundary or Restricted-data flow, and SHALL be reviewed and re-approved at the frequency in SEC-007.7.6. `[PCI]` CDE diagrams SHALL meet the stricter update timing in SEC-019.5.3.4.
- **SEC-007.5.8.4** Network diagrams SHALL be classified Confidential under SEC-002.

### 5.9 Network devices and services

- **SEC-007.5.9.1** Every network device and network security appliance SHALL be recorded in the Asset Inventory (SEC-001) with its System Owner and firmware version.
- **SEC-007.5.9.2** Firmware and software on network devices SHALL be maintained within vendor support and patched within the remediation SLA in SEC-011.
- **SEC-007.5.9.3** Administrative access to network devices SHALL use named accounts authenticated by the central identity service with MFA (SEC-004), and privileged access SHALL follow SEC-005. Shared local administrator credentials SHALL be held only as Break-glass Accounts.
- **SEC-007.5.9.4** Network device configurations SHALL be backed up automatically after each change and at least daily, and configuration changes SHALL be detected and alerted to Workforce Members designated by the CIO for network operations.
- **SEC-007.5.9.5** Network devices and security controls SHALL send logs to the SIEM as specified in SEC-012, and SHALL synchronize time from the Organization's approved time sources.
- **SEC-007.5.9.6** Wired network ports in offices SHALL use network access control (802.1X or equivalent) so that only authenticated, Organization-managed devices reach the Corporate zone. Unauthenticated devices SHALL be placed in the Guest zone or denied.
- **SEC-007.5.9.7** Network services provided by Third Parties (including carrier links, SD-WAN, managed firewall and secure web gateway services) SHALL be approved under RSK-003, and their contracts SHALL include the security requirements of this Policy that the Third Party operates.

## 6. Roles & responsibilities

| Role | Responsibility |
|---|---|
| Head of Security Engineering | Owns this Policy; maintains the network security architecture, zone model and diagrams; approves rule changes that cross into Restricted-data zones; approves DNS filtering categories; owns the DDoS runbook. |
| CIO | Provides network operations resources; ensures network operations staff operate controls under this Policy. |
| CTO | Ensures cloud network designs follow this Policy through SEC-009 landing-zone guardrails. |
| CISO | Approves the Trust Zone model; receives non-compliance reporting; approves Exceptions within the authority in CMP-003. |
| SOC Manager | Monitors network alerts, IDS/IPS and rogue wireless detections; triages within SEC-012 SLAs. |
| System Owner | Requests and justifies rules for their systems; participates in each rule review; confirms or removes unused rules. |
| Head of Procurement | Ensures network service contracts are routed through RSK-003. |
| Workforce Member | Uses only approved remote access methods; does not connect unauthorized devices or wireless access points to Organization networks. |
| Third Party | Uses only approved, time-bound remote access; complies with contractual network security requirements. |

## 7. Minimum standards

| ID | Requirement | Value |
|---|---|---|
| SEC-007.7.1 | Trust Zones | Internet · DMZ · Production · Non-production · Management · Corporate · Guest · Restricted-data · `[PCI]` CDE (per SEC-019) |
| SEC-007.7.2 | Default traffic policy | Deny all inbound and outbound; explicit permit rules only |
| SEC-007.7.3 | Firewall, security-group and network ACL rule review | Every 6 months for all rule sets (meets `[PCI]` 1.2.7) |
| SEC-007.7.4 | Temporary rule maximum duration | 90 days |
| SEC-007.7.5 | Unused rule threshold | No matching traffic for 90 days → flagged and removed unless need documented |
| SEC-007.7.6 | Network and data-flow diagrams | Updated within 30 days of a change; reviewed every 6 months |
| SEC-007.7.7 | Remote access methods | Approved ZTNA or VPN only; MFA per SEC-004; idle timeout per SEC-004 |
| SEC-007.7.8 | Corporate wireless security | WPA3-Enterprise (WPA2-Enterprise minimum) with 802.1X; no PSK |
| SEC-007.7.9 | Rogue wireless detection | Continuous at all offices; `[PCI]` testing at CDE locations every 3 months |
| SEC-007.7.10 | Guest/IoT wireless PSK rotation | Every 12 months and within 5 business days of a relevant Separation |
| SEC-007.7.11 | Internet exposure detection | Automated scan at least daily for inbound rules to non-DMZ zones or administrative ports |
| SEC-007.7.12 | IDS/IPS signature updates | At least daily |
| SEC-007.7.13 | DDoS protection | Always-on for Tier 0; on-demand activation ≤ 15 minutes for Tier 1 |
| SEC-007.7.14 | DDoS runbook test | Every 12 months |
| SEC-007.7.15 | Public DNS record review | Every 6 months |
| SEC-007.7.16 | Network device configuration backup | After each change and at least daily |
| SEC-007.7.17 | Encryption in transit | Per SEC-006 |
| SEC-007.7.18 | Network device patching | Within the remediation SLA in SEC-011 |
| SEC-007.7.19 | `[PCI]` Segmentation testing | Per SEC-011 |

## 8. Monitoring, measurement & metrics

| Metric | Target | Frequency | Owner |
|---|---|---|---|
| Rule sets reviewed within the 6-month cycle | 100% | Monthly | Head of Security Engineering |
| Permit rules with source, destination or port "any" (excluding DMZ HTTPS) without an approved Exception | 0 | Monthly | Head of Security Engineering |
| Temporary rules past expiry | 0 | Monthly | Head of Security Engineering |
| Unapproved internet-exposed administrative ports detected | 0 open > 24 hours | Weekly | SOC Manager |
| Network diagrams updated within 30 days of change | 100% | Quarterly | Head of Security Engineering |
| Remote access sessions without MFA | 0 | Monthly | Head of Security Engineering |
| Rogue access points detected and closed within 1 business day | 100% | Monthly | SOC Manager |
| Managed Endpoints and servers using approved DNS resolvers | ≥ 99% | Monthly | Head of Security Engineering |
| Tier 0 and Tier 1 internet-facing services with DDoS protection | 100% | Quarterly | Head of Security Engineering |
| Network devices running vendor-supported firmware | 100% | Quarterly | CIO |

## 9. Exceptions

Exceptions to this document are requested and approved under CMP-003.

The following SHALL NOT receive an Exception: remote access without MFA (SEC-007.5.4.2);
internet-reachable placement of systems holding Restricted data without a DMZ, load
balancer or reverse proxy (SEC-007.5.1.4); and `[PCI]` the 6-month rule review for CDE
network security controls (SEC-007.5.3.4).

## 10. Enforcement

Non-compliance is handled under CMP-007.

Workforce Members designated by the CIO for network operations MAY immediately disable any rule, device, wireless access point
or connection that violates this Policy and creates an internet exposure of a non-DMZ zone,
and SHALL record the action as an Emergency Change under SEC-013. Unauthorized network
devices connected to Organization networks SHALL be disconnected on detection and handled
under RES-002.

## 11. Framework & regulatory mapping

| Requirement | ISO/IEC 27001:2022 | NIST CSF 2.0 | NIST SP 800-53 r5 | CIS v8.1 | SOC 2 TSC | COBIT 2019 | Regulations |
|---|---|---|---|---|---|---|---|
| SEC-007.5.1 Architecture & zoning | A.8.20, A.8.22, A.8.27 | PR.IR-01, ID.AM-03 | SC-7, AC-4 | 12.2, 13.4 | CC6.1, CC6.6 | DSS05.02 | PCI DSS 1.2, 1.3, 1.4; 45 CFR §164.312(e)(1) |
| SEC-007.5.2 Default deny | A.8.20, A.8.21, A.8.9 | PR.IR-01, PR.PS-01 | SC-7, CM-7, CM-6 | 4.4, 4.5, 4.2, 13.4 | CC6.6 | DSS05.02 | PCI DSS 1.2.1, 1.2.5, 1.3.1, 1.3.2 |
| SEC-007.5.3 Rule review | A.8.20, A.5.15 | PR.IR-01 | SC-7, CA-7 | 4.2, 12.3 | CC6.6, CC7.1 | DSS05.02 | PCI DSS 1.2.7 |
| SEC-007.5.4 Remote access | A.6.7, A.8.5 | PR.AA-03, PR.IR-01 | AC-17, IA-2 | 12.7, 6.4 | CC6.1, CC6.6 | DSS05.02, DSS05.04 | PCI DSS 8.4.2, 8.4.3, 12.8; 45 CFR §164.312(d) |
| SEC-007.5.5 Wireless | A.8.20 | PR.IR-01 | AC-18 | 12.6 | CC6.6 | DSS05.02 | PCI DSS 2.3, 11.2.1 |
| SEC-007.5.6 DNS & egress | A.8.23, A.8.20 | PR.IR-01, DE.CM-01 | SC-7, SC-20, SC-21, SC-22 | 9.2, 13.10 | CC6.6, CC6.8 | DSS05.02 | PCI DSS 1.3.2, 1.4.2 |
| SEC-007.5.7 DDoS | A.8.20, A.8.6 | PR.IR-03, PR.IR-04 | SC-5 | 13.10 | A1.1, CC6.6 | DSS05.02 | — |
| SEC-007.5.8 Diagrams | A.8.20, 7.5 | ID.AM-03 | PL-2, CA-3 | 12.4 | CC2.1 | BAI10 | PCI DSS 1.2.3, 1.2.4 |
| SEC-007.5.9 Devices & services | A.8.20, A.8.21, A.8.9 | PR.PS-01, PR.PS-02 | CM-2, CM-8, SI-2, AU-12 | 12.1, 12.3, 12.8, 13.9 | CC6.1, CC7.1, CC9.2 | DSS05.02, APO10 | PCI DSS 1.2.1, 2.2 |

## 12. Related documents

ISP-000, GOV-004, GOV-006, SEC-001, SEC-002, SEC-003, SEC-004, SEC-005, SEC-006, SEC-008,
SEC-009, SEC-010, SEC-011, SEC-012, SEC-013, SEC-015, SEC-019, RSK-003, RSK-004, RES-002,
CMP-003, CMP-004, CMP-007

## 13. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: Head of Security Engineering | | | |
| Approver: ISSC Chair (CISO), on behalf of the ISSC | | | |
