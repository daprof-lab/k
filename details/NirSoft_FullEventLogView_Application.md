# ⚙️ **Nir Soft Full Event Log View Application**
### `File Name: NirSoft_FullEventLogView_Application.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Barrie Hill  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Parses Application event log using Nirsoft FullEventLogView.exe

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nir Soft Full Event Log View Application to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nir Soft Full Event Log View Application logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nir Soft Full Event Log View Application timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parses Application event log using Nirsoft FullEventLogView.exe
Category: EventLogs
Author: Barrie Hill
Version: 1.0
Id: 505019ce-2fae-4a87-bcf5-cc663c60b030
BinaryUrl: https://www.nirsoft.net/utils/fulleventlogview-x64.zip
ExportFormat: csv
FileMask: Application.evtx
Processors:
    -
        Executable: FullEventLogView.exe
        CommandLine: /TimeFilter 0 /DataSource 3 /LogFolder %sourceDirectory%\Windows\System32\winevt\Logs\ /LogFolderWildcard Application.evtx /scomma %destinationDirectory%\full_application_event_log.csv
        ExportFormat: csv

# Documentation
# Uses Nirsoft's FullEventLogView to export event logs to CSV
# https://www.nirsoft.net/utils/full_event_log_view.html
# FullEventLogView.exe should be in the Modules\bin folder
# Assumes the msource will include the drive letter. e.g. D:\kape\C
# Example: .\kape.exe --msource D:\kape\C --mdest D:\kape\out --module ApplicationFullEventLogView
# Example: .\kape.exe --msource C:\Windows\System32\winevt\Logs --mdest D:\kape\out --module ApplicationFullEventLogView
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
