# ⚙️ **Hayabusa Csv Timeline To Timesketch**
### `File Name: hayabusa_CsvTimeline_To_Timesketch.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pietro Sammartano (z3f1r0)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Hayabusa a timeline CSV format compatible to import into Timesketch

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Hayabusa Csv Timeline To Timesketch to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Hayabusa Csv Timeline To Timesketch logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Hayabusa Csv Timeline To Timesketch timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Hayabusa a timeline CSV format compatible to import into Timesketch
Category: EventLogs
Author: Pietro Sammartano (z3f1r0)
Version: 1.0
Id: 9dc3c167-ebf2-4f42-b951-355e35253163
BinaryUrl: https://github.com/Yamato-Security/hayabusa/releases
ExportFormat: csv
Processors:
    -
        Executable: hayabusa\hayabusa.exe
        CommandLine: csv-timeline -d %sourceDirectory% --RFC-3339 -w -o %destinationDirectory%\hayabusa_timesketch_import.csv -p timesketch-verbose -U
        ExportFormat: csv

# Documentation
# Create a folder "hayabusa" within the "Modules\bin" KAPE folder
# Place "zip archive" file into "Modules\bin\hayabusa" and unpack
# rename the hayabusa executable to hayabusa.exe
# You can delete all except: "config"; "rules" and the "hayabusa.exe"
# For more options use: hayabusa.exe help
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
