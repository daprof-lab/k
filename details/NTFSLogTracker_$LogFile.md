# ⚙️ **Ntfslog Tracker $log File**
### `File Name: NTFSLogTracker_$LogFile.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Hyun Yi @hyuunnn and Vito Alfano  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
NTFS Log Tracker: process $LogFile files

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Ntfslog Tracker $log File to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Ntfslog Tracker $log File logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Ntfslog Tracker $log File timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'NTFS Log Tracker: process $LogFile files'
Category: FileSystem
Author: Hyun Yi @hyuunnn and Vito Alfano
Version: 1.2
Id: 74ee60a6-2fb2-11ee-be56-0242ac120002
BinaryUrl: https://sites.google.com/site/forensicnote/ntfs-log-tracker/
ExportFormat: sqlite3
FileMask: $LogFile
Processors:
    -
        Executable: NTFS Log Tracker CMD v1.8\NTFS_Log_Tracker_CMD.exe
        CommandLine: -l %sourceFile% -o %destinationDirectory%
        ExportFormat: sqlite3
    -
        Executable: NTFS Log Tracker CMD v1.8\NTFS_Log_Tracker_CMD.exe
        CommandLine: -l %sourceFile% -o %destinationDirectory% -c
        ExportFormat: csv

# Documentation
# https://sites.google.com/site/forensicnote/ntfs-log-tracker
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
