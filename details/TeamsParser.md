# ⚙️ **Teams LevelDB Parser**
### `File Name: TeamsParser.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Extracts and parses Microsoft Teams chat logs, status records, and database structures from LevelDB.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Teams LevelDB Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Teams LevelDB Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Teams LevelDB Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Forensic open-source parser that allows extracting the messages, comments, posts, contacts, calendar entries and reactions from a Microsoft Teams IndexedDB LevelDB database.
Category: Databases
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: a099aa6f-fbd7-48a2-a4cb-da41100d2755
BinaryUrl: https://github.com/lxndrblz/forensicsim/releases/download/v0.5.0/ms_teams_parser.exe
ExportFormat: json
Processors:
    -
        Executable: TeamsParser/ms_teams_parser.exe
        CommandLine: -f %sourceDirectory% -o %destinationDirectory%\Results.json
        ExportFormat: json

# Documentation
# https://github.com/lxndrblz/forensicsim/
# Example: CommandLine: -f "C:\Users\ConexionInversa\Downloads\harver\forensicsim-main\testdata\John Doe\IndexedDB\https_teams.microsoft.com_0.indexeddb.leveldb" -o "C:\Users\ConexionInversa\Downloads\harver\Results.json"
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
