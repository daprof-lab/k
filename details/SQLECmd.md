# ⚙️ **Sqlecmd**
### `File Name: SQLECmd.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
SQLECmd: process SQLite databases

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Sqlecmd to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Sqlecmd logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Sqlecmd timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'SQLECmd: process SQLite databases'
Category: SQLDatabases
Author: Andrew Rathbun
Version: 1.0
Id: f9198051-4899-465d-aa5a-8291525d82b1
BinaryUrl: https://download.ericzimmermanstools.com/SQLECmd.zip
ExportFormat: csv
Processors:
    -
        Executable: SQLECmd\SQLECmd.exe
        CommandLine: -d %sourceDirectory% --csv %destinationDirectory%
        ExportFormat: csv
    -
        Executable: SQLECmd\SQLECmd.exe
        CommandLine: -d %sourceDirectory% --json %destinationDirectory%
        ExportFormat: json

# Documentation
# https://github.com/EricZimmerman/SQLECmd
# https://leanpub.com/eztoolsmanuals
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
