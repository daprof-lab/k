# ⚙️ **Nir Soft Full Event Log View Security**
### `File Name: NirSoft_FullEventLogView_Security.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Barrie Hill  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Parses Security event log using Nirsoft FullEventLogView.exe

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nir Soft Full Event Log View Security to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nir Soft Full Event Log View Security logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nir Soft Full Event Log View Security timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parses Security event log using Nirsoft FullEventLogView.exe
Category: EventLogs
Author: Barrie Hill
Version: 1.0
Id: 6f9da2e0-0c7c-4147-9a02-58622e4c1b34
BinaryUrl: https://www.nirsoft.net/utils/fulleventlogview-x64.zip
ExportFormat: csv
FileMask: Security.evtx
Processors:
    -
        Executable: FullEventLogView.exe
        CommandLine: /TimeFilter 0 /DataSource 3 /LogFolder %sourceDirectory%\Windows\System32\winevt\Logs\ /LogFolderWildcard Security.evtx /scomma %destinationDirectory%\full_security_event_log.csv
        ExportFormat: csv

# Documentation
# Uses Nirsoft's FullEventLogView to export event logs to csv
# https://www.nirsoft.net/utils/full_event_log_view.html
# FullEventLogView.exe should be in the Modules\bin folder
# Assumes the msource will include the drive letter. e.g. D:\kape\C
# Example: .\kape.exe --msource D:\kape\C --mdest D:\kape\out --module SecurityFullEventLogView
# Example: .\kape.exe --msource C:\Windows\System32\winevt\Logs\ --mdest D:\kape\out --module SecurityFullEventLogView
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
