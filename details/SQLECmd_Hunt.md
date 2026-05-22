# ⚙️ **Sqlecmd Hunt**
### `File Name: SQLECmd_Hunt.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
SQLECmd: process SQLite databases with Hunt mode

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Sqlecmd Hunt to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Sqlecmd Hunt logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Sqlecmd Hunt timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'SQLECmd: process SQLite databases with Hunt mode'
Category: SQLDatabases
Author: Andrew Rathbun
Version: 1.0
Id: 74343dd0-47bf-406d-9173-fb626e38cc50
BinaryUrl: https://download.ericzimmermanstools.com/SQLECmd.zip
ExportFormat: csv
Processors:
    -
        Executable: SQLECmd\SQLECmd.exe
        CommandLine: -d %sourceDirectory% --hunt --csv %destinationDirectory%
        ExportFormat: csv
        ExportFile: SQLECmdHuntResults.txt
    -
        Executable: SQLECmd\SQLECmd.exe
        CommandLine: -d %sourceDirectory% --hunt --json %destinationDirectory%
        ExportFormat: json
        ExportFile: SQLECmdHuntResults.txt

# Documentation
# https://github.com/EricZimmerman/SQLECmd
# https://leanpub.com/eztoolsmanuals
# Hunt mode should be used to help identify SQLite databases within a dataset (check console window to see which SQLite databases don't have a Map)
# Hunt mode should also be used to parse SQLite databases which do not follow a strict naming convention, i.e. %timestamp%.SQLite
# An example of a SQLECmd Map that will require Hunt mode every time is Windows_TeraCopy_History.smap
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
