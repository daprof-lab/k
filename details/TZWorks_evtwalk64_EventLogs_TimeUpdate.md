# ⚙️ **Tzworks Evtwalk64 Event Logs Time Update**
### `File Name: TZWorks_evtwalk64_EventLogs_TimeUpdate.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using evtwalk64.exe to parse Windows Event Logs from C:\Windows\System32\winevt\logs\ folder to extract Clock changes/time update related events

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Evtwalk64 Event Logs Time Update to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Evtwalk64 Event Logs Time Update logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Evtwalk64 Event Logs Time Update timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using evtwalk64.exe to parse Windows Event Logs from C:\Windows\System32\winevt\logs\ folder to extract Clock changes/time update related events'
Category: Win_EventLogs
Author: Ajith Ravindran
Version: 0.1
Id: b2d3e22e-9ce9-4dae-851a-59ed1281606d
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=25
FileMask: Security.evtx
ExportFormat: csv
Processors:
    -
        Executable: evtwalk64.exe
        CommandLine: -log %sourceFile% -time -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: EventLogs_Parsed_TimeUpdate.csv

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
