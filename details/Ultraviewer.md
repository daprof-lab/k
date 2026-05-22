# 🎯 **Ultraviewer**
### `File Name: Ultraviewer.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ryan McVicar, Sam Smoker  
**Version:** 2.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
UltraViewer

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Ultraviewer to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Ultraviewer events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Ultraviewer storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: UltraViewer
Author: Ryan McVicar, Sam Smoker
Version: 2.0
Id: 992869b7-f262-4058-98d4-623ca2383a66
RecreateDirectories: true
Targets:
    -
        Name: UltraViewer User Logs
        Category: Remote Access
        Path: C:\Users\%user%\AppData\Roaming\UltraViewer
        Recursive: true
        Comment: "Includes all files related to UltraViewer chat, connections, and recordings"
    -
        Name: UltraViewer System Logs
        Category: Remote Access
        Path: C:\Windows\SysWOW64\config\systemprofile\AppData\Roaming\UltraViewer
        Recursive: true
        Comment: "Includes all files related to UltraViewer chat, connections, and recordings"
    -
        Name: UltraViewer Service Log
        Category: Remote Access
        Path: C:\Program Files*\UltraViewer
        FileMask: UltraViewerService_log.txt
        Comment: "UltraViewer Service log file"
    -
        Name: UltraViewer Connection Log
        Category: Remote Access
        Path: C:\Program Files*\UltraViewer
        FileMask: ConnectionLog.Log
        Comment: "UltraViewer Service level connection log"
# Documentation
# Information on UltraViewer logs can be found here: https://www.ultraviewer.net/en/200000026-summary-of-ultraviewer-s-security-information.html granted it is sparse.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
