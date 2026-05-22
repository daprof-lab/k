# 🎯 **Microsoft Azure Copy**
### `File Name: MicrosoftAzureCopy.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Chuck Whitson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Microsoft Azure Copy

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Microsoft Azure Copy to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Microsoft Azure Copy events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Microsoft Azure Copy storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Microsoft Azure Copy
Author: Chuck Whitson
Version: 1.0
Id: 57a25748-2828-4a7f-bda5-1b4f793716d2
RecreateDirectories: true
Targets:
    -
        Name: Azure Copy - User Profile - *.log
        Category: Apps
        Path: C:\Users\%user%\.azcopy\
        FileMask: '*.log'
        Comment: "Collects session and transfer logs for Microsoft Azure Copy from a user profile"
    -
        Name: Azure Copy - Plans - *.ste*
        Category: Apps
        Path: C:\Users\%user%\.azcopy\plans\
        FileMask: '*.ste*'
        Comment: "Collects the plans for Microsoft Azure Copy from a user profile"

# Documentation
# https://learn.microsoft.com/en-us/azure/storage/common/storage-use-azcopy-configure#log-and-plan-files
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
