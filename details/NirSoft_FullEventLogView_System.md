# ⚙️ **Nir Soft Full Event Log View System**
### `File Name: NirSoft_FullEventLogView_System.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Barrie Hill  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Parses System event log using Nirsoft FullEventLogView.exe

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nir Soft Full Event Log View System to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nir Soft Full Event Log View System logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nir Soft Full Event Log View System timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parses System event log using Nirsoft FullEventLogView.exe
Category: EventLogs
Author: Barrie Hill
Version: 1.0
Id: bb628207-56cc-4293-aa6a-2073d406c8cb
BinaryUrl: https://www.nirsoft.net/utils/fulleventlogview-x64.zip
ExportFormat: csv
FileMask: System.evtx
Processors:
    -
        Executable: FullEventLogView.exe
        CommandLine: /TimeFilter 0 /DataSource 3 /LogFolder %sourceDirectory%\Windows\System32\winevt\Logs\ /LogFolderWildcard System.evtx /scomma %destinationDirectory%\full_system_event_log.csv
        ExportFormat: csv

# Documentation
# https://www.nirsoft.net/utils/full_event_log_view.html
# Uses Nirsoft's FullEventLogView to export event logs to csv
# FullEventLogView.exe should be in the Modules\bin folder
# Assumes the msource will include the drive letter. e.g. D:\kape\C
# Example: .\kape.exe --msource D:\kape\C --mdest D:\kape\out --module SystemFullEventLogView
# Example: .\kape.exe --msource C:\Windows\System32\winevt\Logs\ --mdest D:\kape\out --module SystemFullEventLogView
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
