# 🎯 **Xeox**
### `File Name: Xeox.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Skatoff @DFIR_TNT  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Xeox Application Logs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Xeox to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Xeox events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Xeox storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Xeox Application Logs
Author: Andrew Skatoff @DFIR_TNT
Version: 1.0
Id: 5e2c322f-616c-42e4-9cd7-4546cf2412e6
RecreateDirectories: true
Targets:
    -
        Name: Xeox RMM Client Application logs
        Category: ApplicationLogs
        Path: C:\Program Files\Xeox
        FileMask: '*.log'
        Comment: "Contains Application Log entries such as service start and incomming connections."

# Documentation
# https://dfirtnt.wordpress.com/2023/08/01/rmm-xeox-client-side-evidence/
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
