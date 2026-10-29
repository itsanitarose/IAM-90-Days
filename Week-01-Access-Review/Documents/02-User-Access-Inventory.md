# 02: User Access Inventory

**Project:** Northwind Health | IAM User Access Review  
**Scenario date:** 5 October 2026

## 1. Access Reconciliation Overview

The review compares Northwind Health’s HR export with its patient administration portal user list to identify discrepancies between workforce status and application access.

The reconciliation covers five named users and two additional application accounts.

## 2. HR Records

| Employee / Contractor | ID | Status | End Date | Department |
|---|---|---|---|---|
| Sarah Kim | E1021 | Terminated | 15 Aug 2026 | Customer Success |
| Tom Reyes | C3004 | Contractor | 31 Jul 2026 | Engineering |
| Priya Nair | E1033 | Active | Not provided | Finance |
| Dan Holt | E1040 | Active | Not provided | Engineering |
| Lisa Grant | E1052 | Active, on leave since May | Not provided | HR |

## 3. Patient Admin Portal Access Register

| Username | Assigned Role | Last Login | Account Notes |
|---|---|---|---|
| `skim` | Support Agent | 2 Sep 2026 | None provided |
| `treyes` | Admin | 28 Sep 2026 | None provided |
| `pnair` | Read-only | 1 Oct 2026 | None provided |
| `dholt` | Admin | 2 Oct 2026 | None provided |
| `lgrant` | Support Agent | 11 May 2026 | None provided |
| `support-shared` | Support Agent | 3 Oct 2026 | Shared login; password stored in team wiki |
| `testadmin` | Admin | 20 Nov 2025 | Created by an engineer who has since left |

## 4. Reconciliation Results

| Account | HR / Portal Comparison | Review Observation |
|---|---|---|
| `skim` | Terminated 15 Aug; portal login 2 Sep | Login recorded after termination |
| `treyes` | Contract end 31 Jul; Admin login 28 Sep | Privileged login after recorded contract end; confirm whether the contract was extended |
| `pnair` | Active Finance employee; read-only role | No discrepancy established; access remains subject to routine business-need validation |
| `dholt` | Active Engineering employee; Admin role | Business justification for privileged access requires confirmation |
| `lgrant` | Active employee on leave; last login 11 May | Confirm access requirements during extended leave |
| `support-shared` | Shared account with no named individual identified in the supplied records | Shared credentials and limited individual accountability |
| `testadmin` | Account creator has departed | Current ownership and continued business need require confirmation |

## 5. Inventory Summary

The reconciliation identifies concerns and follow-up checks involving:

- **Offboarding:** Login activity recorded after employment or contract end dates.
- **Privileged access:** Admin permissions requiring business justification.
- **Account accountability:** Shared credentials and an administrative account whose creator has departed.
- **Access reviews:** Confirmation of continued access needs, including during extended leave.

These observations form the evidence base for the access risk assessment and findings register.

---

[Back to Week 01 Overview](../README.md)
