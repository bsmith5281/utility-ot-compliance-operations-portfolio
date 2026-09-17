# OT Access Review & Evidence Tracker

## Quarterly User Access Review Checklist (TMS / EMS Support Systems)

| User ID | User Role | System | Manager Approval | Review Date | Access Decision | Remediation Status | Evidence Reference |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **USR-8821** | System Engineer | EMS-PROD | Approved | 2026-09-15 | Retain Access | Completed | AR-2026-Q3-001 |
| **USR-4102** | OT Administrator | TMS-PROD | Approved | 2026-09-15 | Retain Access | Completed | AR-2026-Q3-002 |
| **USR-1923** | Database Specialist | EMS-DB-01 | Approved | 2026-09-16 | Modify Access | In Progress | AR-2026-Q3-003 |
| **USR-7734** | Contract Operator | TMS-STAGE | Denied | 2026-09-16 | Revoke Access | Revoked (2026-09-16) | AR-2026-Q3-004 |
| **USR-3391** | Network Technician | EMS-GW-01 | Approved | 2026-09-17 | Retain Access | Completed | AR-2026-Q3-005 |

---

## Executive Summary: Q3 Access Review Exceptions & Recommendations

**Prepared By:** Compliance & Operations Review Team  
**Review Period:** Q3 2026  
**Target Environment:** TMS/EMS Operational Support Systems  

### Summary of Exceptions Identified
1. **Contractor Over-Privilege (`USR-1923`):** Identified elevated database administration privileges no longer required for active contract tasks. Request submitted to downgrade to read-only analyst access.
2. **Terminated Contractor Stale Account (`USR-7734`):** Account retained active access post-contract termination date. Access was immediately revoked upon discovery during the review cycle.

### Root Cause & Risk Analysis
* Account revocation delays occurred due to a gap in cross-departmental offboarding notifications between HR and OT IT operations.
* Unnecessary administrative rights pose an elevated operational risk to high-availability EMS databases.

### Recommended Follow-Up Actions
* **Immediate:** Re-audit all active contractor accounts associated with TMS/EMS production environments against active HR contracts.
* **Process Enhancement:** Integrate automated offboarding webhook notifications between HR system and OT Directory Services to auto-disable accounts upon contract end dates.
* **Audit Trail:** Archive signed manager approvals and tickets `AR-2026-Q3-001` through `005` in the central compliance repository for upcoming regulatory reviews.
