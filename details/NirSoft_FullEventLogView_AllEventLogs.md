# ⚙️ **Nir Soft Full Event Log View All Event Logs**
### `File Name: NirSoft_FullEventLogView_AllEventLogs.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Parses all event logs using Nirsoft FullEventLogView.exe

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nir Soft Full Event Log View All Event Logs to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nir Soft Full Event Log View All Event Logs logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nir Soft Full Event Log View All Event Logs timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parses all event logs using Nirsoft FullEventLogView.exe
Category: EventLogs
Author: Andrew Rathbun
Version: 1.1
Id: 123e00c7-b7d0-4e48-9a93-6c49c29d6e82
BinaryUrl: https://www.nirsoft.net/utils/fulleventlogview-x64.zip
ExportFormat: csv
Processors:
    -
        Executable: FullEventLogView.exe
        CommandLine: /TimeFilter 0 /DataSource 3 /LogFolder %sourceDirectory%\Windows\System32\winevt\Logs\ /scomma %destinationDirectory%\all_event_logs.csv
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
