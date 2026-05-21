# 🎯 **Apache Web Server Logs**
### `File Name: ApacheAccessLog.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Hadar Yudovich  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Apache access and error log tables documenting remote HTTP traffic.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Apache Web Server Logs to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Apache Web Server Logs events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Apache Web Server Logs storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Apache Access Log
Author: Hadar Yudovich
Version: 1.0
Id: 6ad85ab3-701a-409c-98b8-ea4ef806cdf0
RecreateDirectories: true
Targets:
    -
        Name: Apache Access Log
        Category: Webservers
        Path: C:\
        FileMask: 'access.log'
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
