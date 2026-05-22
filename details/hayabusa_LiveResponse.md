# ⚙️ **Hayabusa Live Response**
### `File Name: hayabusa_LiveResponse.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Georg Lauenstein (sure[secure])  
**Version:** 1.5
{% endhint %}

---

## 📖 **Forensic Description & Value**
Hayabusa a timeline generator for Windows event logs - Live

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Hayabusa Live Response to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Hayabusa Live Response logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Hayabusa Live Response timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Hayabusa a timeline generator for Windows event logs - Live
Category: EventLogs
Author: Georg Lauenstein (sure[secure])
Version: 1.5
Id: 9696412c-c973-4fd4-a426-06318011b8ba
BinaryUrl: https://github.com/Yamato-Security/hayabusa/releases
ExportFormat: csv
Processors:
    -
        Executable: hayabusa\hayabusa.exe
        CommandLine: csv-timeline --live-analysis --profile standard -w --min-level medium --quiet --UTC -o %destinationDirectory%\hayabusa_events_live_system.csv
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
