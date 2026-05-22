# 🎯 **Perf Logs**
### `File Name: PerfLogs.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Perflogs Folder Copy

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Perf Logs to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Perf Logs events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Perf Logs storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Perflogs Folder Copy
Author: Vito Alfano
Version: 1.0
Id: b87302c9-fe0e-4d07-9f9f-64c5b73c80a2
RecreateDirectories: true
Targets:
    -
        Name: Perflogs
        Category: Application
        Path: C:\PerfLogs\
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
