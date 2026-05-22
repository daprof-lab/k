# ⚙️ **Ntfslog Tracker $log File C0966e7a 1cc6 4bf7 Be28 871caa8de3da**
### `File Name: NTFSLogTracker_$LogFile_c0966e7a-1cc6-4bf7-be28-871caa8de3da.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Hyun Yi @hyuunnn  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
NTFS Log Tracker: process $LogFile files

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Ntfslog Tracker $log File C0966e7a 1cc6 4bf7 Be28 871caa8de3da to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Ntfslog Tracker $log File C0966e7a 1cc6 4bf7 Be28 871caa8de3da logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Ntfslog Tracker $log File C0966e7a 1cc6 4bf7 Be28 871caa8de3da timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'NTFS Log Tracker: process $LogFile files'
Category: FileSystem
Author: Hyun Yi @hyuunnn
Version: 1.0
Id: 03939a50-0325-49f0-8cad-1f35c083f44b
BinaryUrl: https://sites.google.com/site/forensicnote/ntfs-log-tracker/NTFS Log Tracker v1.6 CMD.zip
ExportFormat: sqlite3
FileMask: $LogFile
Processors:
    -
        Executable: NTFS Log Tracker v1.6 CMD\NTFS_Log_Tracker_CMD_V1.6.exe
        CommandLine: -l %sourceFile% -o %destinationDirectory%
        ExportFormat: sqlite3
    -
        Executable: NTFS Log Tracker v1.6 CMD\NTFS_Log_Tracker_CMD_V1.6.exe
        CommandLine: -l %sourceFile% -o %destinationDirectory% -c
        ExportFormat: csv

# Documentation
# https://sites.google.com/site/forensicnote/ntfs-log-tracker
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
