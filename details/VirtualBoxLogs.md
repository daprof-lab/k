# 🎯 **VirtualBox Logs**
### `File Name: VirtualBoxLogs.tkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Matt Dawson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Diagnostics logs tracking virtualization setups, connected devices, and machine shutdowns.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from VirtualBox Logs to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate VirtualBox Logs events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit VirtualBox Logs storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Collects VirtualBox log files
Author: Matt Dawson
Version: 1.0
Id: 3d5398fc-5774-4329-a268-29ed1a6d4d9e
RecreateDirectories: true
Targets:
    -
        Name: VirtualBox Logs
        Category: Apps
        Path: C:\
        Recursive: true
        FileMask: "VBox.log"
        Comment: "Locates all VBox.log files on disk"
    -
        Name: VirtualBox Backup Logs
        Category: Apps
        Path: C:\
        Recursive: true
        FileMask: "VBox.log.*"
        Comment: "Locates all backup VBox.log files on disk - these can show historic VM usage"
    -
        Name: VirtualBox Hardening Logs
        Category: Apps
        Path: C:\
        Recursive: true
        FileMask: "VBoxHardening.log"
        Comment: "Locates all VBoxHardening.log files on disk"

# Documentation
# N/A
```
---

[⬅️ Back to Memory & Virtualization Targets](../memory_virtualization_targets.md)
