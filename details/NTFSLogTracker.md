# ⚙️ **Ntfslog Tracker**
### `File Name: NTFSLogTracker.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Hyun Yi @hyuunnn  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
NTFS Log Tracker: process all files

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Ntfslog Tracker to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Ntfslog Tracker logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Ntfslog Tracker timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'NTFS Log Tracker: process all files'
Category: FileSystem
Author: Hyun Yi @hyuunnn
Version: 1.0
Id: 094e8964-ea15-4be1-869d-7b8fa1b55ada
BinaryUrl: https://sites.google.com/site/forensicnote/ntfs-log-tracker/
ExportFormat: sqlite3
Processors:
    -
        Executable: NTFSLogTracker_$J.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: NTFSLogTracker_$LogFile.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation
# https://sites.google.com/site/forensicnote/ntfs-log-tracker
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
