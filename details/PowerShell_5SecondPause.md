# ⚙️ **Power Shell 5second Pause**
### `File Name: PowerShell_5SecondPause.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
PowerShell: 5 Second Pause

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell 5second Pause to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell 5second Pause logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell 5second Pause timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: "PowerShell: 5 Second Pause"
Category: PowerShell
Author: Andrew Rathbun
Version: 1.0
Id: 3b729407-6466-4623-869e-6c43f76c4716
BinaryUrl: https://github.com/PowerShell/PowerShell/releases
ExportFormat: ""
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: start-sleep 5
        ExportFormat: ""

# Documentation
# All this Module does is give the --sync functions for RECmd, EVTXECmd, and KAPE time to execute successfully prior to performing tasks by Modules that follow
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
