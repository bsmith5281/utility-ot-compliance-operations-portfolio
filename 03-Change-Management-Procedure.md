# Secure Change-Management Procedure

**Document ID:** OT-PROC-CM-004  
**Version:** 2.1  
**Target System:** Transmission Management System (TMS) & Energy Management System (EMS)  
**Classification:** Internal Operational Procedure  

---

## 1. Request Intake
All proposed hardware, software, network, or configuration changes affecting TMS/EMS environments must be initiated via an official Change Request (CR) ticket.
* **Required Fields:** Change description, business driver, affected assets, requester, target execution date, and preliminary risk level.

## 2. Operational & Security Impact Review
Every CR undergoes mandatory joint review by OT Operations and OT Security.
* Assess operational impact on grid control and telemetry.
* Evaluate cybersecurity posture (e.g., port changes, firewall modifications, software updates).
* Identify required outage windows or dual-redundancy requirements.

## 3. Risk Rating Matrix
Changes are categorized into three distinct operational risk tiers:

| Tier | Definition | Examples | Approval Level Required |
| :--- | :--- | :--- | :--- |
| **Low / Standard** | Pre-approved, low-risk routine updates. | Standard database backups, routine rule tuning. | OT Supervisor |
| **Medium** | Systems updates with redundancy or minimal operational risk. | Secondary application server patch, switch reboot. | Change Advisory Board (CAB) |
| **High / Critical** | Direct impact on active production EMS/TMS or primary gateways. | Gateway firmware update, core SCADA failover. | CAB + Director of Grid Ops |

## 4. Required Approvals
* **Formal Sign-off:** No Medium or High change may proceed without documented CAB approval.
* **Emergency Changes:** Must be verbally authorized by the Grid Operations Director and documented within 24 hours post-event.

## 5. Pre-Implementation Testing
* Changes must be executed and validated in a non-production (staging) environment prior to production deployment.
* Test logs and validation check results must be attached to the CR ticket.

## 6. Rollback Plan
Every CR must contain an explicit, step-by-step rollback procedure:
* Estimated time to restore prior operational state.
* Defined execution trigger (e.g., "If system fails health check within 15 minutes post-change, execute rollback").
* Backup files or baseline system configurations stored locally prior to change start.

## 7. Scheduled Maintenance Window
* All production changes must occur during approved low-impact operational windows (typically Tuesdays/Thursdays between 01:00 and 04:00 local time).
* Continuous communication must be maintained with Control Room Operators throughout the maintenance window.

## 8. Implementation Validation
Post-change verification must be conducted prior to closing the maintenance window:
* Telemetry status checks, signal verification, and application health confirmation.
* Formal operator sign-off that systems are stable and performing as expected.

## 9. Evidence Retention
* All documentation (CR ticket, pre-test logs, approvals, post-check results, operator sign-offs) must be archived in the compliance vault.
* **Retention Requirement:** Retain all change artifacts for a minimum of 3 years to ensure audit readiness.
