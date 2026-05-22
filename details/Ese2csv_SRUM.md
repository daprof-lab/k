# ⚙️ **Ese2csv SRUM**
### `File Name: Ese2csv_SRUM.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Max Ye  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Ese2csv: Parsing SRUM Database

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Ese2csv SRUM to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Ese2csv SRUM logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Ese2csv SRUM timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Ese2csv: Parsing SRUM Database'
Category: SRUMDatabase
Author: Max Ye
Version: 1.0
Id: 852b64c1-fd0e-47ec-8aa4-0994dbf5d8d1
BinaryUrl: https://github.com/MarkBaggett/ese-analyst/archive/master.zip
ExportFormat: csv
Processors:
    -
        Executable: ese-analyst\ese2csv.exe
        CommandLine: -o %destinationDirectory% -p srudb_plugin --plugin-args "%sourceDirectory%\Windows\System32\config\SOFTWARE" -- "%sourceDirectory%\Windows\System32\sru\SRUDB.dat"
        ExportFormat: csv

# Documentation
# https://github.com/MarkBaggett/ese-analyst
# Create a folder "ese-analyst" within the ".\KAPE\Modules\bin" folder
# Place both files "ese2csv.exe" and "srudb_plugin.py" into ".\KAPE\Modules\bin\ese-analyst"
# When using this Module, the Module source should be set to OS drive root directory (e.g. C:\), because parameters use absolute paths
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
