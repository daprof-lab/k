# 🎯 **Log Files**
### `File Name: LogFiles.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Fabian Murer  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
LogFiles (includes SUM)

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Log Files to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Log Files events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Log Files storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: LogFiles (includes SUM)
Author: Fabian Murer
Version: 1.1
Id: 67c9bb8d-342b-4380-a110-565317fce014
RecreateDirectories: true
Targets:
    -
        Name: LogFiles
        Category: Logs
        Path: C:\Windows\System32\LogFiles\
        Recursive: true
    -
        Name: LogFiles
        Category: Logs
        Path: C:\Windows.old\Windows\System32\LogFiles\
        Recursive: true
    -
        Name: Error logging
        Category: Misc
        Path: C:\windows\
        FileMask: PFRO.log

# Documentation
# https://digital-forensics.sans.org/community/papers/gcfa/forensic-analysis-windows-2000-server-iis-oracle_112
# https://advisory.kpmg.us/blog/2021/digital-forensics-incident-response.html
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
