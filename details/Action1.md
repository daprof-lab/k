# 🎯 **Action1**
### `File Name: Action1.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Skatoff @DFIR_TNT  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Action1 Application Logs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Action1 to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Action1 events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Action1 storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Action1 Application Logs
Author: Andrew Skatoff @DFIR_TNT
Version: 1.0
Id: 9cdf145a-c67e-45cd-bdec-1bcfeb2d50b1
RecreateDirectories: true
Targets:
    -
        Name: Action1 Client Application logs
        Category: ApplicationLogs
        Path: C:\Windows\Action1\logs
        FileMask: '*.log'
        Comment: "Contains Application Log entries such as service start and incomming connections, and deployed scripts/jobs."

# Documentation
# https://dfirtnt.wordpress.com/2023/08/23/rmm-action1-client-side-evidence/
# https://www.bleepingcomputer.com/news/security/hackers-start-abusing-action1-rmm-in-ransomware-attacks/
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
