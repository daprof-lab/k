# ⚙️ **Power Shell Execute Winlogbeat**
### `File Name: PowerShell_Execute-Winlogbeat.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Thomas DIOT (Qazeer)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Execute-Winlogbeat.ps1 - Recursively process the source directory to execute Winlogbeat once on all EVTX files found.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Execute Winlogbeat to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Execute Winlogbeat logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Execute Winlogbeat timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Execute-Winlogbeat.ps1 - Recursively process the source directory to execute Winlogbeat once on all EVTX files found.
Category: EventLogs
Author: Thomas DIOT (Qazeer)
Version: 1.0
Id: e4ff9d06-2548-43b4-b037-7d7f1d37cfea
BinaryUrl: https://gist.github.com/Qazeer/4936ec6c9fa511500f9496d0ceacab22
ExportFormat: JSON
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: "& '%kapeDirectory%\\Modules\\bin\\Execute-Winlogbeat.ps1' -WinlogbeatBinary '%kapeDirectory%\\Modules\\bin\\Winlogbeat\\winlogbeat.exe' -InputDir '%sourceDirectory%' -OutputDir '%destinationDirectory%'"
        ExportFormat: JSON

# Documentation
# Recursively process the source directory to execute Winlogbeat once on all EVTX files found.
# Execute-Winlogbeat.ps1 is basically a wrapper to make Winlogbeat recursive, with out a predefined set of EVTX files to look for.
# https://gist.github.com/Qazeer/4936ec6c9fa511500f9496d0ceacab22
# Winlogbeat (https://www.elastic.co/fr/downloads/beats/winlogbeat) full folder must be placed under "%kapeDirectory%\Modules\bin\Winlogbeat".
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
