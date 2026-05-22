# ⚙️ **Tzworks Evtwalk64 Event Logs Scheduled Tasks**
### `File Name: TZWorks_evtwalk64_EventLogs_ScheduledTasks.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Justin Price  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Parses TaskScheduler-Operational event log using TZWorks evtwalk64

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Evtwalk64 Event Logs Scheduled Tasks to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Evtwalk64 Event Logs Scheduled Tasks logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Evtwalk64 Event Logs Scheduled Tasks timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parses TaskScheduler-Operational event log using TZWorks evtwalk64
Category: SystemActivity
Author: Justin Price
Version: 1.0
Id: 5875f69b-4de1-418b-b306-db49b9fc0072
BinaryUrl: https://tzworks.net/download_links.php
ExportFormat: csv
FileMask: Microsoft-Windows-TaskScheduler%4Operational.evtx
Processors:
    -
        Executable: evtwalk64.exe
        CommandLine: -log %sourceFile% -pair_datetime -csv -no_whitespace
        ExportFormat: csv
        ExportFile: task_scheduler_event_log.csv

# Documentation
# https://tzworks.net/prototype_page.php?proto_id=25
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
