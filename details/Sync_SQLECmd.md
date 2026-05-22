# ⚙️ **Sync Sqlecmd**
### `File Name: Sync_SQLECmd.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Andrew Rathbun  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
SQLECmd: Sync for new Maps

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Sync Sqlecmd to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Sync Sqlecmd logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Sync Sqlecmd timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'SQLECmd: Sync for new Maps'
Category: KAPESync
Author: Andrew Rathbun
Version: 1.1
Id: 6da27d9b-b3e2-4a21-9762-ce7058f5aac2
BinaryUrl: https://f001.backblazeb2.com/file/EricZimmermanTools/SQLECmd.zip
ExportFormat: ""
Processors:
    -
        Executable: SQLECmd\SQLECmd.exe
        CommandLine: --sync --debug
        ExportFormat: ""
        ExportFile: Sync_SQLECMD.txt

# Documentation
# https://github.com/EricZimmerman/SQLECmd
# This Module ensures you have the latest Maps for SQLECmd prior to running SQLECmd
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
