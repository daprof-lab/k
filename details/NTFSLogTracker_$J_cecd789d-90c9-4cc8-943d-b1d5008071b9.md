# ⚙️ **Ntfslog Tracker $J Cecd789d 90c9 4cc8 943d B1d5008071b9**
### `File Name: NTFSLogTracker_$J_cecd789d-90c9-4cc8-943d-b1d5008071b9.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Hyun Yi @hyuunnn  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
NTFS Log Tracker: process $J files

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Ntfslog Tracker $J Cecd789d 90c9 4cc8 943d B1d5008071b9 to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Ntfslog Tracker $J Cecd789d 90c9 4cc8 943d B1d5008071b9 logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Ntfslog Tracker $J Cecd789d 90c9 4cc8 943d B1d5008071b9 timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'NTFS Log Tracker: process $J files'
Category: FileSystem
Author: Hyun Yi @hyuunnn
Version: 1.0
Id: adcf94a7-dde8-4eaf-855e-8072d7df1e14
BinaryUrl: https://sites.google.com/site/forensicnote/ntfs-log-tracker/NTFS Log Tracker v1.6 CMD.zip
ExportFormat: sqlite3
FileMask: $J
Processors:
    -
        Executable: NTFS Log Tracker v1.6 CMD\NTFS_Log_Tracker_CMD_V1.6.exe
        CommandLine: -u %sourceFile% -o %destinationDirectory%
        ExportFormat: sqlite3
    -
        Executable: NTFS Log Tracker v1.6 CMD\NTFS_Log_Tracker_CMD_V1.6.exe
        CommandLine: -u %sourceFile% -o %destinationDirectory% -c
        ExportFormat: csv

# Documentation
# https://sites.google.com/site/forensicnote/ntfs-log-tracker
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
