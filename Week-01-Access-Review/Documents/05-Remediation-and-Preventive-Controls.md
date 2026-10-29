# 05: Remediation and Preventive Controls

**Project:** Northwind Health | IAM User Access Review  
**Scenario date:** 5 October 2026  

## 1. Remediation Approach

Remediation prioritises access after employment or contract end dates, privileged accounts, and shared credentials.

Selected changes were implemented in Microsoft Entra ID using Microsoft Graph PowerShell. Account states and directory role membership were checked after remediation.

**Lab assumptions:** Tom had no contract extension, Lisa did not require access during leave, and Dan did not require the Entra ID User Administrator role.

## 2. Corrective Actions

| Account | Assessment Priority | Implemented in Entra ID | Follow-up |
|---|---|---|---|
| `skim` | High | Account disabled and state verified | Investigate the recorded post-termination activity |
| `treyes` | Critical, pending authorisation check | Account disabled and state verified | Resolve the contract-extension question and investigate activity |
| `testadmin` | High | Account disabled and state verified | Establish ownership and continued business need before considering reactivation |
| `support-shared` | High | Account disabled and state verified | Rotate the exposed password, remove it from the wiki, and replace shared access with named accounts |
| `lgrant` | Requires confirmation | Account disabled under the stated lab assumption | Confirm access requirements during leave |
| `pnair` | No finding identified | Account remained enabled | Include in routine access reviews |
| `dholt` | Requires confirmation | Entra ID User Administrator role removed; account remained enabled | Confirm the required portal permissions and document privileged-access justification |

## 3. Preventive Control Recommendations

| Control Area | Recommended Control | Intended Outcome |
|---|---|---|
| Employee Offboarding | Trigger access removal from recorded HR termination events | Remove access promptly when employment ends |
| Contractor Access | Track contract end dates and trigger access removal unless an approved extension is recorded | Prevent access continuing beyond its authorised period |
| Account Ownership and Inactivity | Assign an accountable owner and review inactive accounts against their business purpose | Identify unmanaged or unnecessary access |
| Shared Accounts | Use named accounts and prohibit credential storage in team wikis | Improve accountability and credential protection |
| Privileged Access | Record business justification and conduct quarterly reviews with the relevant owner | Maintain appropriate administrative access |
| Extended Leave | Define when access should be retained, suspended, and restored during leave | Apply consistent access decisions based on business need |

## 4. Implementation and Validation

| Check | Observed Result |
|---|---|
| Account-state verification | Sarah, Tom, Lisa, `support-shared`, and `testadmin` returned `AccountEnabled: False` |
| Retained-account verification | Dan and Priya remained enabled |
| Directory role verification | Dan no longer held the Entra ID User Administrator role |
| Post-remediation reconciliation | Two observations remained: shared-account accountability and `testadmin` ownership |

The remaining observations require credential governance and ownership decisions.

[View the implementation walkthrough, scripts, and test evidence](../Lab-and-Testing/README.md)

---

[Back to Week 01 Overview](../README.md)
