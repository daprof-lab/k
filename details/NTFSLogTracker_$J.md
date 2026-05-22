# ⚙️ **Ntfslog Tracker $J**
### `File Name: NTFSLogTracker_$J.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Hyun Yi @hyuunnn and Vito Alfano  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
NTFS Log Tracker: process $J files

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Ntfslog Tracker $J to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Ntfslog Tracker $J logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Ntfslog Tracker $J timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'NTFS Log Tracker: process $J files'
Category: FileSystem
Author: Hyun Yi @hyuunnn and Vito Alfano
Version: 1.2
Id: 74ee5d04-2fb2-11ee-be56-0242ac120002
BinaryUrl: https://sites.google.com/site/forensicnote/ntfs-log-tracker/
ExportFormat: sqlite3
FileMask: '$UsnJrnl%3A$J|$J|UsnJrnl-J|$UsnJrnl_*.bin'
Processors:
    -
        Executable: NTFS Log Tracker CMD v1.8\NTFS_Log_Tracker_CMD.exe
        CommandLine: -u %sourceFile% -o %destinationDirectory%
        ExportFormat: sqlite3
    -
        Executable: NTFS Log Tracker CMD v1.8\NTFS_Log_Tracker_CMD.exe
        CommandLine: -u %sourceFile% -o %destinationDirectory% -c
        ExportFormat: csv

# Documentation
# https://sites.google.com/site/forensicnote/ntfs-log-tracker
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
