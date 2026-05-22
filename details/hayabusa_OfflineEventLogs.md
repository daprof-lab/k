# ⚙️ **Hayabusa Offline Event Logs**
### `File Name: hayabusa_OfflineEventLogs.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Georg Lauenstein (sure[secure])  
**Version:** 1.5
{% endhint %}

---

## 📖 **Forensic Description & Value**
Hayabusa a timeline generator for Windows event logs - Offline

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Hayabusa Offline Event Logs to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Hayabusa Offline Event Logs logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Hayabusa Offline Event Logs timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Hayabusa a timeline generator for Windows event logs - Offline
Category: EventLogs
Author: Georg Lauenstein (sure[secure])
Version: 1.5
Id: 49f9cd2d-3da5-4349-a9aa-c2b450582ccc
BinaryUrl: https://github.com/Yamato-Security/hayabusa/releases
ExportFormat: csv
Processors:
    -
        Executable: hayabusa\hayabusa.exe
        CommandLine: csv-timeline -d %sourceDirectory% --profile standard -w --quiet --UTC -o %destinationDirectory%\hayabusa_events_offline.csv
        ExportFormat: csv
    -
        Executable: hayabusa\hayabusa.exe
        CommandLine: json-timeline -d %sourceDirectory% --profile standard -w --quiet --UTC -o %destinationDirectory%\hayabusa_events_offline.jsonl -L
        ExportFormat: json

# Documentation
# Create a folder "hayabusa" within the "Modules\bin" KAPE folder
# Place "zip archive" file into "Modules\bin\hayabusa" and unpack
# rename the hayabusa executable to hayabusa.exe
# You can delete all except: "config"; "rules" and the "hayabusa.exe"
# For more options use: hayabusa.exe help
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
