# TPL-006 — Incident Report Template

## 1. Document control

| Field | Value |
|---|---|
| Document ID | TPL-006 |
| Title | Incident Report Template |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | T — Template |
| Classification | Internal (a completed form is classified Confidential, or Restricted where it contains Restricted data, under SEC-002) |
| Owner | SOC Manager |
| Approver | Chief Information Security Officer (CISO) |
| Effective date | [DECISION REQUIRED: Date of CISO approval] |
| Next review date | Effective date + 12 months |
| Parent document | RES-002 Incident Response Plan |
| Related documents | RES-001, RES-002, RES-003, TPL-007, CMP-004, SEC-002, SEC-012, TPL-001 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | SOC Manager | Initial release |

## 3. Purpose

This template is the single record of a Security Incident from first report to closure. It
captures the facts, Severity Level, actions, decisions, evidence and notifications required by
RES-001 and RES-002, and provides the inputs for breach determination under RES-003 and for
the Post-Incident Review recorded in TPL-007.

## 4. Instructions

| Item | Instruction |
|---|---|
| Who completes it | The Scribe assigned under RES-002 completes and maintains the form, under the direction of the Incident Commander. Where no Scribe is assigned (Sev-3 and Sev-4), the Incident Commander completes it. |
| When | Opened when a Security Event is declared a Security Incident under RES-002. Updated at each phase transition, at each Severity Level change, and at each status update cadence in RES-002. Closed when the Incident Commander confirms the closure criteria in section 5.10. |
| Record identifier | One form per Security Incident, numbered `INC-YYYY-NNNN` (calendar year, then a four-digit sequence restarting each year). Related incidents are cross-referenced in section 5.1, not merged. |
| Where it is stored | In the incident record system designated by the SOC Manager, with access restricted to the IR team, the CISO, the GC and roles granted access by the Incident Commander. Where the Legal Lead directs that the record is prepared under Legal Privilege, the form is labelled accordingly and stored as the Legal Lead instructs. |
| Classification | Confidential at minimum; Restricted where the form contains Restricted data, indicators that would enable attack, or privileged legal analysis (SEC-002). Do not paste Restricted data (e.g. PAN, PHI, Secrets) into the form; reference the evidence item ID instead. |
| Retention | Retained as an incident record for the period in CMP-004. Legal Hold, where issued by the GC, overrides deletion. |
| Breach determination | Sections 5.6 and 5.7 record facts only. The breach determination itself is made and documented under RES-003. |
| Post-Incident Review | Where RES-002 requires a Post-Incident Review, the completed form is the primary input to TPL-007. |
| Completeness | Every field is completed or marked "N/A" with a reason. Times are recorded in UTC in the format `YYYY-MM-DD hh:mm UTC`. |

## 5. Form

### 5.1 Incident identification

| Field | Value |
|---|---|
| Incident ID (INC-YYYY-NNNN) | |
| Incident title (short, no Restricted data) | |
| Related incident IDs | |
| Related alert / ticket IDs (SEC-012) | |
| Date/time first Security Event observed (UTC) | |
| Date/time reported to the SOC (UTC) | |
| Date/time declared a Security Incident (UTC) | |
| Reported by (name, role, contact) | |
| Reporting channel | ☐ Security reporting channel (RES-001) ☐ SIEM / detection alert ☐ Third Party ☐ Customer ☐ Law enforcement or regulator ☐ Vulnerability Disclosure Program ☐ Other: |
| Legal Privilege applied (directed by Legal Lead) | ☐ Yes ☐ No |

### 5.2 Classification

| Field | Value |
|---|---|
| Incident category | ☐ Ransomware ☐ Business Email Compromise ☐ Credential Compromise ☐ Data Exfiltration ☐ Insider Threat ☐ DDoS ☐ Cloud Account Compromise ☐ `[PCI]` Card Data Compromise ☐ Lost or Stolen Device ☐ Third-Party Breach ☐ AI System Misuse ☐ Malware (non-ransomware) ☐ Unauthorized Access ☐ Policy Violation ☐ Other: |
| Playbook invoked (RES-002) | ☐ PB-01 ☐ PB-02 ☐ PB-03 ☐ PB-04 ☐ PB-05 ☐ PB-06 ☐ PB-07 ☐ PB-08 `[PCI]` ☐ PB-09 ☐ PB-10 ☐ PB-11 ☐ None (reason): |
| Initial Severity Level (criteria in RES-002) | ☐ Sev-1 Critical ☐ Sev-2 High ☐ Sev-3 Medium ☐ Sev-4 Low |
| Severity rationale (criteria met, by reference to RES-002) | |
| Severity assigned by / date-time (UTC) | |
| Current phase | ☐ Detection & Analysis ☐ Containment ☐ Eradication ☐ Recovery ☐ Post-Incident Activity ☐ Closed |
| Potential Personal Data Breach (refer to RES-003) | ☐ Yes ☐ No ☐ Unknown |
| Potential Material Cybersecurity Incident `[SOX]` (refer to RES-003) | ☐ Yes ☐ No ☐ Unknown |
| CMT activation requested (RES-004) | ☐ Yes ☐ No |
| DR declaration requested (RES-005) | ☐ Yes ☐ No |

#### Severity change log

| # | Date/time (UTC) | From | To | Reason (RES-002 criterion) | Approved by (Incident Commander) |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

### 5.3 IR team

| IR team role (RES-002) | Name | Business role | Assigned date/time (UTC) |
|---|---|---|---|
| Incident Commander | | | |
| Scribe | | | |
| Communications Lead | | | |
| Legal Lead (GC or delegate) | | | |
| Technical Lead(s) | | | |
| Executive sponsor (CISO) | | | |
| External IR retainer engaged (RES-001) — firm, engagement reference | | | |
| Other participants (Data Owner, System Owner, CPO, DPO, HIPAA Security Officer, Third Party) | | | |

### 5.4 Description and scope

| Field | Value |
|---|---|
| Summary of what happened (facts only, no speculation) | |
| How the incident was detected | |
| Attack vector or cause (known / suspected) | |
| MITRE ATT&CK technique(s) observed (RSK-005.5.7.5) | |
| Threat actor (if known): ☐ External ☐ Insider ☐ Third Party ☐ Unknown | |
| Indicators of compromise (reference evidence item IDs; do not paste live Secrets) | |
| Business processes affected and Recovery Tier (RSK-004) | |

#### Affected assets

| # | Asset / system (Asset Inventory ID, SEC-001) | System Owner | Recovery Tier (RSK-004) | Environment (prod / non-prod / CDE `[PCI]`) | Impact (C / I / A) | Status |
|---|---|---|---|---|---|---|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |

#### Affected accounts

| # | Account / identity | Type (User / Privileged Account / Service Account) | Action taken (disabled, reset, revoked) | Date/time (UTC) |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |

### 5.5 Data involved

| Field | Value |
|---|---|
| Highest Classification Level involved (SEC-002) | ☐ Public ☐ Internal ☐ Confidential ☐ Restricted |
| Data types involved | ☐ Personal Data ☐ Sensitive Personal Information ☐ `[HIPAA]` PHI / ePHI ☐ `[PCI]` CHD ☐ `[PCI]` SAD ☐ Secrets ☐ `[SOX]` Financially Significant System data ☐ Intellectual property ☐ Other: |
| Data encrypted at time of incident (SEC-006) and key not compromised | ☐ Yes ☐ No ☐ Partially ☐ Unknown |
| Approximate number of records | |
| Approximate number of individuals affected | |
| Jurisdictions of affected individuals (countries; US states) | |
| Data Owner(s) notified (name, date/time UTC) | |
| Customers whose data is involved (names held by Legal Lead; enter count here) | |
| Organization role for the data `[GDPR]` `[HIPAA]` | ☐ Controller ☐ Processor ☐ Covered Entity ☐ Business Associate ☐ N/A |

### 5.6 Response actions log

Record every material action in time order. The Scribe maintains this log during the incident.

| # | Date/time (UTC) | Phase | Action taken / decision made | By (name, IR role) | Evidence item ID |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |
| 6 | | | | | |
| 7 | | | | | |
| 8 | | | | | |

#### Containment, eradication and recovery summary

| Phase | Actions completed | Completed date/time (UTC) | Verified by |
|---|---|---|---|
| Containment (incl. system isolation authorized under RES-001) | | | |
| Eradication | | | |
| Recovery (incl. restore from Backup, SEC-018; DR, RES-005) | | | |
| Emergency Changes raised (SEC-013 change IDs) | | | |

### 5.7 Evidence register

Chain of Custody is maintained under RES-001 for each item.

| Evidence item ID | Description | Source system | Collected by | Date/time collected (UTC) | Hash (SHA-256) | Storage location | Chain-of-custody record ref. |
|---|---|---|---|---|---|---|---|
| | | | | | | | |
| | | | | | | | |
| | | | | | | | |

| Field | Value |
|---|---|
| Legal Hold issued by GC | ☐ Yes (date) ☐ No |
| Law enforcement involved (authorized under RES-001) | ☐ Yes — agency and case reference: ☐ No |

### 5.8 Escalations and notifications

#### Internal escalations

| Recipient | Required by | Date/time notified (UTC) | Notified by | Within RES-002 / RES-003 time limit? |
|---|---|---|---|---|
| CISO | RES-002 | | | ☐ Yes ☐ No |
| Executive notification (Sev-1) | RES-002 | | | ☐ Yes ☐ No ☐ N/A |
| GC and CPO (suspected Personal Data Breach) | RES-003 | | | ☐ Yes ☐ No ☐ N/A |
| ISSC extraordinary meeting (Sev-1) | GOV-001 | | | ☐ Yes ☐ No ☐ N/A |
| Crisis Management Team | RES-004 | | | ☐ Yes ☐ No ☐ N/A |
| HIPAA Security Officer / HIPAA Privacy Officer `[HIPAA]` | RES-003 | | | ☐ Yes ☐ No ☐ N/A |
| DPO `[GDPR]` | RES-003 | | | ☐ Yes ☐ No ☐ N/A |
| CFO (`[SOX]` Financially Significant System or potential materiality) | RES-003 | | | ☐ Yes ☐ No ☐ N/A |

#### Status updates issued

| # | Date/time (UTC) | Audience | Issued by (Communications Lead) | Summary |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

#### External notifications

Notifications are decided and made under RES-003. Record each one here.

| Recipient | Regulation / contract | Decision ref. (RES-003) | Date/time sent (UTC) | Sent by (role) | Reference / acknowledgement |
|---|---|---|---|---|---|
| `[GDPR]` Supervisory Authority | GDPR Art. 33 | | | | |
| `[GDPR]` Data Subjects | GDPR Art. 34 | | | | |
| `[GDPR]` Controller (where the Organization is Processor) | GDPR Art. 33(2) | | | | |
| `[HIPAA]` Covered Entity / individuals / HHS / media | 45 CFR §§164.404–164.410 | | | | |
| `[PCI]` Acquirer and payment brands | Brand rules; PCI DSS 12.10.1 | | | | |
| `[SOX]` Form 8-K Item 1.05 filing | 17 CFR 229.106 | | | | |
| US state regulators / residents | State breach laws | | | | |
| Customers (contractual) | Contract | | | | |
| Cyber insurer | Insurance policy | | | | |
| Law enforcement | RES-001 | | | | |
| Other: | | | | | |

### 5.9 Impact assessment

| Field | Value |
|---|---|
| Service downtime (start, end, duration) | |
| Recovery within RTO (RSK-004) | ☐ Yes ☐ No ☐ N/A |
| Data loss within RPO (RSK-004) | ☐ Yes ☐ No ☐ N/A |
| Estimated direct cost (response, recovery, third-party fees) | |
| Customer impact (count, description) | |
| Regulatory / contractual impact | |
| Reputational impact | ☐ None ☐ Limited ☐ Public media coverage |

### 5.10 Closure

| Closure criterion | Confirmed | Date | By |
|---|---|---|---|
| Threat eradicated and no further malicious activity observed | ☐ | | |
| Affected systems restored and validated by System Owner | ☐ | | |
| Breach determination recorded under RES-003 (or marked N/A) | ☐ | | |
| All required notifications made and logged in 5.8 | ☐ | | |
| Evidence register complete and evidence stored per RES-001 and CMP-004 | ☐ | | |
| Post-Incident Review required under RES-002 | ☐ Yes — TPL-007 ref.: ☐ No | | |
| Residual Risks raised in the Risk Register (TPL-001) — Risk IDs | ☐ | | |
| Incident closed in the incident record system | ☐ | | |

| Field | Value |
|---|---|
| Final Severity Level | ☐ Sev-1 ☐ Sev-2 ☐ Sev-3 ☐ Sev-4 |
| Final category | |
| Root Cause (summary; detail in TPL-007 where required) | |
| Date/time closed (UTC) | |

## 6. Approval signatures

| Role | Name | Signature | Date |
|---|---|---|---|
| Incident Commander (form complete and accurate) | | | |
| SOC Manager (closure accepted) | | | |
| CISO (required for Sev-1 and Sev-2) | | | |
| Legal Lead (required where a notification was made or a breach determination recorded under RES-003) | | | |

### Template approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: SOC Manager | | | |
| Approver: CISO | | | |
