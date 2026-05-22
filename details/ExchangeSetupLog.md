# 🎯 **Exchange Setup Log**
### `File Name: ExchangeSetupLog.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** 2thewes  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Exchange Setup Log

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Exchange Setup Log to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Exchange Setup Log events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Exchange Setup Log storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Exchange Setup Log
Author: 2thewes
Version: 1.0
Id: 8becbf27-06bf-460c-a582-868db54359bf
RecreateDirectories: true
Targets:
    -
        Name: Exchange Setup Log file
        Category: Logs
        Path: C:\ExchangeSetupLogs\
        FileMask: "ExchangeSetup.log"
        Comment: "The Exchange Setup log tracks the progress of every task during the Exchange installation and configuration."

# Documentation
# https://learn.microsoft.com/en-us/exchange/plan-and-deploy/post-installation-tasks/verify-installation#review-the-windows-application-log-and-the-exchange-setup-log
# https://m365internals.com/2022/10/07/hunting-in-on-premises-exchange-server-logs/
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
