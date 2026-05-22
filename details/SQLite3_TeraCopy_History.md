# ⚙️ **Sqlite3 Tera Copy History**
### `File Name: SQLite3_TeraCopy_History.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Kevin Pagano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Parses the history file databases for TeraCopy history

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Sqlite3 Tera Copy History to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Sqlite3 Tera Copy History logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Sqlite3 Tera Copy History timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parses the history file databases for TeraCopy history
Category: FileKnowledge
Author: Kevin Pagano
Version: 1.0
Id: d77856a2-b657-4be7-88a8-5dffc32e8983
BinaryUrl: https://sqlite.org/2019/sqlite-tools-win32-x86-3270200.zip
ExportFormat: csv
FileMask: "*.db"
Processors:
    -
        Executable: sqlite3.exe
        CommandLine: -header -separator "," %sourceFile% "SELECT Source as \"File Path\", CASE State WHEN 0 THEN 'Added' WHEN 1 THEN 'OK' WHEN 2 THEN 'Verified' WHEN 3 THEN 'Error' WHEN 4 THEN 'Skipped' WHEN 5 THEN 'Deleted' WHEN 6 THEN 'Moved' END as \"Operation State\", Size as \"Size (Bytes)\", Attributes, Case IsFolder WHEN 0 THEN '' WHEN 1 THEN 'Yes' END as \"Folder\", datetime(julianday(Creation)) as \"Created Date-Time\", datetime(julianday(Access)) as \"Accessed Date-Time\", datetime(julianday(Write)) as \"Modified Date-Time\", SourceCRC as \"Source Hash\", TargetCRC as \"Target Hash\", Message FROM Files"
        ExportFormat: csv
        ExportFile: TeraCopy-history_%fileName%.csv

# Documentation
# https://www.codesector.com/teracopy
# Uses sqlite3.exe to parse the history files from TeraCopy and export them in the proper format
# Note: preferred to point msource to the TeraCopy history folder, as other DB's could be pulled using the FileMask
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
