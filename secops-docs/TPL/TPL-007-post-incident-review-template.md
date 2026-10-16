# TPL-007 — Post-Incident Review Template

## 1. Document control

| Field | Value |
|---|---|
| Document ID | TPL-007 |
| Title | Post-Incident Review Template |
| Version | 1.0 |
| Status | Draft — pending approval |
| Tier | T — Template |
| Classification | Internal (a completed form is classified Confidential, or Restricted where it contains Restricted data, under SEC-002) |
| Owner | SOC Manager |
| Approver | Chief Information Security Officer (CISO) |
| Effective date | [DECISION REQUIRED: Date of CISO approval] |
| Next review date | Effective date + 12 months |
| Parent document | RES-002 Incident Response Plan |
| Related documents | RES-001, RES-002, RES-003, TPL-006, TPL-001, RSK-001, GOV-002, CMP-003, CMP-004 |

## 2. Version history

| Version | Date | Author (role) | Change summary |
|---|---|---|---|
| 1.0 | [Effective date] | SOC Manager | Initial release |

## 3. Purpose

This template records the Post-Incident Review required by RES-002. It establishes what
happened, why it happened, how well the Organization detected and responded, and which
corrective actions and Control, policy and plan updates will prevent recurrence. It supports
continual improvement of incident response (NIST SP 800-61 Rev. 3; NIST CSF 2.0 ID.IM;
ISO/IEC 27001:2022 A.5.27; PCI DSS v4.0.1 12.10.6).

## 4. Instructions

| Item | Instruction |
|---|---|
| When it is required | For every Security Incident for which RES-002 requires a Post-Incident Review, completed within the time set in RES-002. The Incident Commander or SOC Manager MAY also require it for any other Security Incident, and the CISO MAY require it for any Security Event. |
| Who completes it | A facilitator appointed by the SOC Manager who was not the Incident Commander for the incident, with the Incident Commander, Scribe, Technical Lead(s), Communications Lead, Legal Lead and the affected System Owners and Data Owners as participants. |
| Blameless format | The review examines systems, processes and conditions, not individual fault. Record actions and decisions by IR role or team, not by individual name, in sections 5.3 to 5.6. Participants are told at the start that statements made in the review are not used as the basis for disciplinary action. This does not override CMP-007 where the incident record shows deliberate misconduct, which is handled separately and outside this review. |
| Inputs | The completed incident report (TPL-006), evidence register, SIEM and detection records (SEC-012), communications log, and any breach determination recorded under RES-003. |
| Legal Privilege | The Legal Lead decides before the review meeting whether the review is conducted under Legal Privilege and, if so, how the record is labelled and distributed. |
| Corrective actions | Every corrective action has a single owner and a due date. Actions that leave a Residual Risk above Risk Appetite are entered in the Risk Register (TPL-001) under RSK-001. Actions that cannot be met by the due date require an Exception under CMP-003 or a Risk Acceptance under RSK-001. |
| Policy updates | A Root Cause related to a suite document triggers the event-triggered review in GOV-002; record the request in section 5.8. |
| Where it is stored | With the incident record, under the same Incident ID, in the incident record system designated by the SOC Manager. |
| Retention | Retained as a Post-Incident Review for the period in CMP-004. |
| Distribution | Final review to the CISO; summary of findings and corrective actions to the ISSC in the next monthly metrics report (GOV-003). |
| Times | Recorded in UTC, format `YYYY-MM-DD hh:mm UTC`. |

## 5. Form

### 5.1 Review identification

| Field | Value |
|---|---|
| Incident ID (INC-YYYY-NNNN) | |
| Incident title | |
| Final Severity Level (RES-002) | ☐ Sev-1 Critical ☐ Sev-2 High ☐ Sev-3 Medium ☐ Sev-4 Low |
| Incident category / playbook invoked | |
| Incident closure date (TPL-006 section 5.10) | |
| Review due date (per RES-002) | |
| Review meeting date | |
| Review completed date | |
| Completed within RES-002 time limit | ☐ Yes ☐ No — reason: |
| Facilitator (role) | |
| Conducted under Legal Privilege | ☐ Yes ☐ No |

#### Participants

| IR team role / business role | Team or function | Attended |
|---|---|---|
| Incident Commander | | ☐ |
| Scribe | | ☐ |
| Technical Lead(s) | | ☐ |
| Communications Lead | | ☐ |
| Legal Lead | | ☐ |
| System Owner(s) / Data Owner(s) | | ☐ |
| CPO / DPO / HIPAA Security Officer (where data was involved) | | ☐ |
| Third Party representative (where involved) | | ☐ |

### 5.2 Blameless review acknowledgement

| Statement | Confirmed |
|---|---|
| The facilitator stated the blameless principle at the start of the review | ☐ |
| The record describes actions by role or team, not by named individual | ☐ |
| Findings focus on conditions, Controls and processes that allowed the incident | ☐ |

### 5.3 Executive summary

| Field | Value |
|---|---|
| What happened (3–5 sentences, no Restricted data) | |
| Business impact (systems, data, customers, downtime, cost) | |
| Root Cause (one sentence) | |
| Most important corrective actions (top 3, by ID from 5.7) | |
| Notifications made under RES-003 (yes/no and recipients) | |

### 5.4 Timeline

Build from the TPL-006 response actions log and system records. Include the earliest known
attacker or failure activity, even where it was discovered later.

| # | Date/time (UTC) | Event / action | Source (log, alert, person-by-role) | Phase |
|---|---|---|---|---|
| 1 | | Earliest known malicious or failure activity | | |
| 2 | | First Security Event generated | | |
| 3 | | Alert triaged (SEC-012) | | |
| 4 | | Declared Security Incident; Severity Level assigned | | |
| 5 | | Incident Commander assigned | | |
| 6 | | Containment achieved | | |
| 7 | | Eradication completed | | |
| 8 | | Recovery completed; service restored | | |
| 9 | | Incident closed | | |
| 10 | | | | |
| 11 | | | | |
| 12 | | | | |

### 5.5 Response metrics

| Metric | Calculation | Result (hours/minutes) | Met target in RES-002 / SEC-012 / RSK-004? |
|---|---|---|---|
| Dwell Time | First Security Event observed − earliest malicious activity | | N/A |
| Time to detect | Alert generated or report received − earliest malicious activity | | N/A |
| Time to triage | Alert triaged − alert generated (target in SEC-012) | | ☐ Yes ☐ No |
| Time to assign Incident Commander | Commander assigned − incident declared (target in RES-002) | | ☐ Yes ☐ No |
| Time to contain | Containment achieved − incident declared | | ☐ Yes ☐ No ☐ No target |
| Time to eradicate | Eradication completed − incident declared | | ☐ Yes ☐ No ☐ No target |
| Time to recover | Service restored − disruption start (RTO in RSK-004) | | ☐ Yes ☐ No ☐ N/A |
| Data loss window | Disruption start − last good restore point (RPO in RSK-004) | | ☐ Yes ☐ No ☐ N/A |
| Executive notification time | Executive notified − incident declared (target in RES-002) | | ☐ Yes ☐ No ☐ N/A |
| Notification timeliness | Each notification sent vs. deadline in RES-003 | | ☐ Yes ☐ No ☐ N/A |
| Status update cadence | Updates issued vs. cadence in RES-002 | | ☐ Yes ☐ No |

### 5.6 What went well and what did not

| Area | What worked | What did not work |
|---|---|---|
| Detection (monitoring, alerting, reporting by Workforce Members) | | |
| Analysis and Severity classification | | |
| Containment and eradication | | |
| Recovery (Backup, DR, restore validation) | | |
| Communication (internal, executive, external) | | |
| Coordination with Third Parties and the external IR retainer | | |
| Playbook and tooling | | |
| Evidence handling and Chain of Custody | | |

### 5.7 Root Cause analysis

#### 5.7.1 Problem statement

| Field | Value |
|---|---|
| Problem statement (the undesired outcome, stated as a fact) | |

#### 5.7.2 5 Whys

Continue until the answer identifies a Control, process or design condition the Organization
can change. Add rows if more than five levels are needed; record branches separately.

| Level | Why? | Answer | Evidence |
|---|---|---|---|
| 1 | Why did the problem occur? | | |
| 2 | Why? | | |
| 3 | Why? | | |
| 4 | Why? | | |
| 5 | Why? | | |

| Field | Value |
|---|---|
| Root Cause | |
| MITRE ATT&CK technique(s) confirmed (RSK-005.5.7.5; SOC Manager updates the coverage map) | |
| Root Cause category | ☐ Control absent ☐ Control designed ineffectively ☐ Control not operating ☐ Process gap ☐ Configuration error ☐ Unpatched Vulnerability ☐ Third-Party failure ☐ Human error enabled by a process or design gap ☐ Other: |
| Related suite document(s) whose requirement failed or was missing | |
| Other analysis method used (e.g. fishbone, fault tree), if any | |

#### 5.7.3 Contributing factors

| Category | Contributing factor | Effect on incident (cause, spread, delay in detection or response) |
|---|---|---|
| People (training, staffing, availability, awareness) | | |
| Process (procedures, playbooks, handoffs, approvals) | | |
| Technology (tools, configuration, monitoring coverage, architecture) | | |
| Third Party (vendor controls, contract terms, notification) | | |
| Environment / external (threat actor capability, timing) | | |

### 5.8 Corrective and preventive actions

Each action has one owner (role and name) and a due date. Priority: High = due within 30 days;
Medium = within 90 days; Low = within 180 days. [DECISION REQUIRED: Confirm corrective action
due-date bands. Recommended default: High 30 days, Medium 90 days, Low 180 days.]

| Action ID | Action | Addresses (Root Cause / contributing factor ref.) | Priority | Owner (role, name) | Due date | Tracking ref. (ticket, Risk ID) | Status |
|---|---|---|---|---|---|---|---|
| CA-01 | | | ☐ H ☐ M ☐ L | | | | ☐ Open ☐ Done |
| CA-02 | | | ☐ H ☐ M ☐ L | | | | ☐ Open ☐ Done |
| CA-03 | | | ☐ H ☐ M ☐ L | | | | ☐ Open ☐ Done |
| CA-04 | | | ☐ H ☐ M ☐ L | | | | ☐ Open ☐ Done |
| CA-05 | | | ☐ H ☐ M ☐ L | | | | ☐ Open ☐ Done |
| CA-06 | | | ☐ H ☐ M ☐ L | | | | ☐ Open ☐ Done |

| Field | Value |
|---|---|
| Residual Risks entered in the Risk Register (TPL-001) — Risk IDs | |
| Exceptions (CMP-003) or Risk Acceptances (RSK-001) requested — IDs | |

### 5.9 Control, policy and plan updates

| # | Document or Control | Update required | Mechanism | Owner (role) | Due date | Request ref. |
|---|---|---|---|---|---|---|
| 1 | RES-002 (plan or playbook) | | ☐ Plan revision | | | |
| 2 | Suite policy or standard (ID): | | ☐ GOV-002 event-triggered review | | | |
| 3 | Control in REF-001 (ID): | | ☐ Control redesign ☐ New Control | | | |
| 4 | Detection rule / monitoring use case (SEC-012) | | ☐ New or tuned detection | | | |
| 5 | Training content (PPL-002) | | ☐ Awareness ☐ Role-based | | | |
| 6 | Third-Party contract or assessment (RSK-003) | | ☐ Contract change ☐ Reassessment | | | |
| 7 | Other: | | | | | |

| Field | Value |
|---|---|
| Does the Root Cause relate to a suite document (GOV-002 event-triggered review required)? | ☐ Yes ☐ No |
| Does this incident change the enterprise risk assessment (RSK-002 trigger)? | ☐ Yes ☐ No |
| `[PCI]` IR plan modified per lessons learned (PCI DSS 12.10.6) | ☐ Yes ☐ No ☐ N/A |

### 5.10 Follow-up verification

| Field | Value |
|---|---|
| Date corrective actions reviewed for completion | |
| All corrective actions closed | ☐ Yes ☐ No — open action IDs: |
| Effectiveness verified (e.g. retest, tabletop, control test) | ☐ Yes ☐ No — method: |
| Verified by (role) | |

## 6. Approval signatures

| Role | Name | Signature | Date |
|---|---|---|---|
| Facilitator (review complete and accurate) | | | |
| Incident Commander | | | |
| SOC Manager (findings and corrective actions accepted) | | | |
| CISO (required for Sev-1 and Sev-2) | | | |
| Legal Lead (where conducted under privilege or notifications were made) | | | |

### Template approval

| Role | Name | Signature | Date |
|---|---|---|---|
| Owner: SOC Manager | | | |
| Approver: CISO | | | |
