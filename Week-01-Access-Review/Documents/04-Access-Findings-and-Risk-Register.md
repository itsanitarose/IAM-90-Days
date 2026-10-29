# 04: Access Findings and Risk Register

**Project:** Northwind Health | IAM User Access Review  
**Scenario date:** 5 October 2026

## 1. Findings Overview

The review covers seven portal accounts. Four present access risks; two require further confirmation, and one has no identified discrepancy.

Findings are assessed using the [Access Risk Methodology](03-Access-Risk-Methodology.md). Ratings reflect the supplied evidence and potential business impact.

## 2. Access Risk Register

| ID | Account | Finding | Risk | Severity | Recommended Action |
|---|---|---|---|---|---|
| IAM-01 | `skim` | Terminated 15 August; portal login recorded on 2 September | Potential unauthorised access after employment ended | High | Disable if still active, revoke sessions, and investigate the recorded activity |
| IAM-02 | `treyes` | Recorded contract end of 31 July; Admin login on 28 September | Potential unauthorised use of administrative privileges | Critical, pending authorisation check | Confirm any contract extension immediately; suspend access if valid authorisation cannot be established and investigate activity |
| IAM-03 | `testadmin` | Admin account last used on 20 November 2025; its creator has departed | Stale privileged access with no current owner or purpose established in the records | High | Confirm ownership, purpose, and dependencies; disable if no longer required |
| IAM-04 | `support-shared` | Shared login with its password stored in a team wiki | Credential exposure and limited ability to attribute actions to individuals | High | Rotate the password, remove it from the wiki, and replace shared access with named accounts |

## 3. Access Requiring Confirmation

| Account | Observation | Required Check |
|---|---|---|
| `dholt` | Active Engineering employee with Admin access | Confirm the tasks requiring Admin privileges and whether a narrower role would meet the need |
| `lgrant` | Active employee on leave since May; last login on 11 May | Confirm leave arrangements and whether portal access remains necessary |
| `pnair` | Active Finance employee with read-only access | No discrepancy identified from the supplied records; retain in routine access reviews |

These accounts have no finding severity assigned at this stage. Record a finding if further checks establish inappropriate access.

## 4. Risk Prioritisation

**First priority: IAM-02, `treyes`.**

The account combines Admin privileges with a login after its recorded contract end date. This creates greater potential impact than the other accounts reviewed.

Confirm the contract and access authorisation immediately. If valid authorisation cannot be established, suspend access, revoke sessions, and investigate the activity.

If an extension is confirmed, update the records and verify that Admin access remains justified.

`skim` also requires urgent attention because its recorded login follows an explicit termination date.

The exports do not establish whether patient information was accessed or compromised.

## 5. Risk Distribution

| Severity | Findings |
|---|---|
| Critical, pending authorisation check | 1 |
| High | 3 |
| Medium | 0 |
| Low | 0 |
| **Total risk findings** | **4** |

Two accounts require confirmation. One has no identified discrepancy.

---

[Back to Week 01 Overview](../README.md)
