# ⚙️ **Tzworks Evtwalk64 Event Logs Pwchange**
### `File Name: TZWorks_evtwalk64_EventLogs_PWChange.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using evtwalk64.exe to parse Windows Event Logs from C:\Windows\System32\winevt\logs\ folder to extract Password change related events

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Evtwalk64 Event Logs Pwchange to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Evtwalk64 Event Logs Pwchange logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Evtwalk64 Event Logs Pwchange timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using evtwalk64.exe to parse Windows Event Logs from C:\Windows\System32\winevt\logs\ folder to extract Password change related events'
Category: Win_EventLogs
Author: Ajith Ravindran
Version: 0.1
Id: 11340fd6-1fc2-4370-bb73-593fe6d0b82e
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=25
FileMask: Security.evtx
ExportFormat: csv
Processors:
    -
        Executable: evtwalk64.exe
        CommandLine: -log %sourceFile% -pw -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: EventLogs_Parsed_PWChange.csv

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
