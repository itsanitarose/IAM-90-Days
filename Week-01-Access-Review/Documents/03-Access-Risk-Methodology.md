# 03: Access Risk Assessment Methodology

**Project:** Northwind Health | IAM User Access Review  
**Scenario date:** 5 October 2026

## 1. Risk Assessment Approach

Findings are assessed using the supplied HR records and patient administration portal export.

Severity reflects the access involved, evidence of activity, and potential business impact. Response priority considers how urgently the exposure needs to be investigated or contained.

## 2. Risk Assessment Criteria

| Factor | What I Assess |
|---|---|
| Employment Status | Whether recorded login activity aligns with employment or contract dates |
| Privilege Level | The assigned role and the actions it could permit |
| Account Accountability | Whether an individual user or accountable owner can be identified |
| Business Justification | Whether the available records support a continued need for access |
| Potential Impact | Possible consequences for patient information, account security, and business operations |

## 3. Risk Severity Classification

| Severity | Definition | Response |
|---|---|---|
| **Critical** | Severe exposure requiring immediate attention, particularly where privileged access and evidence of unauthorised use coincide | Investigate immediately and contain the exposure |
| **High** | Significant access control or accountability weakness with substantial potential impact | Investigate promptly and prioritise corrective action |
| **Medium** | An identified weakness with moderate exposure or impact | Schedule corrective action and track it to completion |
| **Low** | A minor weakness with limited exposure or impact | Address through routine access maintenance |

An account with no identified issue receives no finding rating. Where the records are insufficient, mark the observation **Requires confirmation** and state what needs checking.

A login after a recorded end date warrants investigation. It does not, by itself, establish a breach.

When findings have the same severity, prioritise those with greater privileges, more recent activity, and wider potential impact.

---

[Back to Week 01 Overview](../README.md)
