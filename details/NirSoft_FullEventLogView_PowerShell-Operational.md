# ⚙️ **Nir Soft Full Event Log View Power Shell Operational**
### `File Name: NirSoft_FullEventLogView_PowerShell-Operational.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Barrie Hill  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Parses PowerShell-Operational event log using Nirsoft FullEventLogView.exe

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nir Soft Full Event Log View Power Shell Operational to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nir Soft Full Event Log View Power Shell Operational logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nir Soft Full Event Log View Power Shell Operational timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parses PowerShell-Operational event log using Nirsoft FullEventLogView.exe
Category: EventLogs
Author: Barrie Hill
Version: 1.0
Id: 3189c1e4-a76d-4bd6-a16b-a7e7fb821635
BinaryUrl: https://www.nirsoft.net/utils/fulleventlogview-x64.zip
ExportFormat: csv
FileMask: Microsoft-Windows-PowerShell%4Operational.evtx
Processors:
    -
        Executable: FullEventLogView.exe
        CommandLine: /TimeFilter 0 /DataSource 3 /LogFolder %sourceDirectory%\Windows\System32\winevt\Logs\ /LogFolderWildcard Microsoft-Windows-PowerShell%4Operational.evtx /scomma %destinationDirectory%\full_powershell_operational_event_log.csv
        ExportFormat: csv

# Documentation
# Uses Nirsoft's FullEventLogView to export event logs to csv
# https://www.nirsoft.net/utils/full_event_log_view.html
# FullEventLogView.exe should be in the Modules\bin folder
# Assumes the msource will include the drive letter. e.g. D:\kape\C
# Example: .\kape.exe --msource D:\kape\C --mdest D:\kape\out --module PowerShellOperationalFullEventLogView
# Example: .\kape.exe --msource C:\Windows\System32\winevt\Logs\ --mdest D:\kape\out --module PowerShellOperationalFullEventLogView
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
