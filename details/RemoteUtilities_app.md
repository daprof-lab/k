# 🎯 **Remote Utilities App**
### `File Name: RemoteUtilities_app.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Ryan McVicar  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Remote Utilities

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Remote Utilities App to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Remote Utilities App events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Remote Utilities App storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Remote Utilities
Author: Ryan McVicar
Version: 1.1
Id: 55733479-dd80-4958-a0a8-0d1c1392f494
RecreateDirectories: true
Targets:
    -
        Name: RemoteUtilities Connection Logs
        Category: Remote Access
        Path: C:\Program Files*\Remote Utilities - Host\Logs
        FileMask: "rut_log_*.html"
        Comment: "Includes connection log files"
    -
        Name: RemoteUtilities Connection Logs in ProgramData
        Category: Remote Access
        Path: C:\ProgramData\Remote Utilities\Logs
        FileMask: "rut_log_*.html"
        Comment: "Includes connection log files"
    -
        Name: RemoteUtilities Install Log
        Category: Remote Access
        Path: C:\ProgramData\Remote Utilities
        FileMask: "install.log"
        Comment: "Includes Install log file"

# Documentation
# Information on RemoteUtilities logs can be found here: https://www.remoteutilities.com/support/docs/host-log/
# Information on the different Connection Modes is available here: https://www.remoteutilities.com/support/docs/connection-modes/
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
