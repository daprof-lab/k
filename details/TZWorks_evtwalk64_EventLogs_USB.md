# ⚙️ **Tzworks Evtwalk64 Event Logs USB**
### `File Name: TZWorks_evtwalk64_EventLogs_USB.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using evtwalk64.exe to parse Windows Event Logs from C:\Windows\System32\winevt\logs\ folder to extract the USB insertions and removals events

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Evtwalk64 Event Logs USB to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Evtwalk64 Event Logs USB logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Evtwalk64 Event Logs USB timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using evtwalk64.exe to parse Windows Event Logs from C:\Windows\System32\winevt\logs\ folder to extract the USB insertions and removals events'
Category: Win_EventLogs
Author: Ajith Ravindran
Version: 0.1
Id: 6a2109b9-3106-4b03-8e4e-1670261da697
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=25
FileMask: (System.evtx|Microsoft-Windows-DriverFrameworks-UserMode%4Operational.evtx|Microsoft-Windows-Kernel-PnP*.evtx|Microsoft-Windows-Partition%4Diagnostic.evtx)
ExportFormat: csv
Processors:
    -
        Executable: evtwalk64.exe
        CommandLine: -log %sourceFile% -usb -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: EventLogs_Parsed_USB.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
