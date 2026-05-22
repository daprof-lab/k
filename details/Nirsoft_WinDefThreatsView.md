# ⚙️ **Nirsoft Win Def Threats View**
### `File Name: Nirsoft_WinDefThreatsView.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
WinDefThreatsView is a tool for Windows 10 that displays the list of all threats detected by Windows Defender Antivirus and allows you to set the default action easily (Allow, Quarantine, Clean, Remove, Block, or No Action) for multiple threats at once

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nirsoft Win Def Threats View to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nirsoft Win Def Threats View logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nirsoft Win Def Threats View timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: WinDefThreatsView is a tool for Windows 10 that displays the list of all threats detected by Windows Defender Antivirus and allows you to set the default action easily (Allow, Quarantine, Clean, Remove, Block, or No Action) for multiple threats at once
Category: EventLogs
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: e28c4400-ff01-4d23-8253-4375de7172ec
BinaryUrl: https://www.nirsoft.net/utils/windefthreatsview-x64.zip
ExportFormat: csv
Processors:
    -
        Executable: windefthreatsview.exe
        CommandLine: /scomma %destinationDirectory%\Nirsoft_Windefthreatsview.csv
        ExportFormat: csv

# Documentation
# https://www.nirsoft.net/utils/windows_defender_threats_view.html
# information is displayed: Filename, Threat Name, Severity, Process Name, Initial Detect Time, Status Change Time, Remediation Time, Threat ID, Threat Status, Default Threat Action, and more...
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
