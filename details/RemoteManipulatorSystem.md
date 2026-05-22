# 🎯 **Remote Manipulator System**
### `File Name: RemoteManipulatorSystem.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** raggadhub based on RemoteUtilities_App.tkape by Ryan McVicar  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Remote Manipulator System (RMS)

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Remote Manipulator System to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Remote Manipulator System events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Remote Manipulator System storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Remote Manipulator System (RMS)
Author: raggadhub based on RemoteUtilities_App.tkape by Ryan McVicar
Version: 1.0
Id: 2a971058-b1c7-486a-ac8f-c4e0de9f5eac
RecreateDirectories: true
Targets:
    -
        Name: Remote Manipulator System Connection Logs
        Category: Remote Access
        Path: C:\Program Files*\Remote Manipulator System - Host\Logs
        FileMask: "rms_log_*.html"
        Comment: "Includes connection log files"
    -
        Name: Remote Manipulator System Connection Logs in ProgramData
        Category: Remote Access
        Path: C:\ProgramData\Remote Manipulator System\Logs
        FileMask: "rms_log_*.html"
        Comment: "Includes connection log files"
    -
        Name: Remote Manipulator System Install Log
        Category: Remote Access
        Path: C:\ProgramData\Remote Manipulator System
        FileMask: "install.log"
        Comment: "Includes Install log file"

# Documentation
# Information on RemoteManipulatorSystem logs can be found here: https://rmansys.ru/support/help/
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
