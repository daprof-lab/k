# ⚙️ **Tzworks Evtwalk64 Event Logs Startstop**
### `File Name: TZWorks_evtwalk64_EventLogs_Startstop.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using evtwalk64.exe to parse Windows Event Logs from C:\Windows\System32\winevt\logs\ folder to extract system start/stop times

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Evtwalk64 Event Logs Startstop to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Evtwalk64 Event Logs Startstop logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Evtwalk64 Event Logs Startstop timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using evtwalk64.exe to parse Windows Event Logs from C:\Windows\System32\winevt\logs\ folder to extract system start/stop times'
Category: Win_EventLogs
Author: Ajith Ravindran
Version: 0.1
Id: 01c0a7dc-47af-4631-8553-71822afe0590
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=25
FileMask: System.evtx
ExportFormat: csv
Processors:
    -
        Executable: evtwalk64.exe
        CommandLine: -log %sourceFile% -startstop -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: EventLogs_Parsed_Startstop.csv

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
