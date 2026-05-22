# 🎯 **Free File Sync**
### `File Name: FreeFileSync.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
FreeFileSync

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Free File Sync to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Free File Sync events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Free File Sync storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: FreeFileSync
Author: Andrew Rathbun
Version: 1.0
Id: 1525ef00-abe5-4fdf-8c3c-7c1f291c8866
RecreateDirectories: true
Targets:
    -
        Name: FreeFileSync
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\FreeFileSync\Logs
        Comment: "Copies out all log files"

# Documentation
# FreeFileSync is an awesome program for making copies of the logical contents of a drive, volume, folder, etc.
# By default, the logs for each use of this program is stored in an HTML file at the above location.
# HTML logs are plain text readable and easy to interpret.
# You will find that each file copied is timestamped. Please note this time is recorded as the system time at the time of file copy.
# Full file paths are provided in these logs so if files were deleted at the time of seizure of these logs, this will help prove the files existed at a certain date/time.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
