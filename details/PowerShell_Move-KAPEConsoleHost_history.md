# ⚙️ **Power Shell Move Kapeconsole Host History**
### `File Name: PowerShell_Move-KAPEConsoleHost_history.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun and Matt Arbaugh  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Move-KAPEConsoleHost_history.ps1 - Moves the ConsoleHost_history.txt file into the Modules output for better visibility

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Move Kapeconsole Host History to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Move Kapeconsole Host History logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Move Kapeconsole Host History timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Move-KAPEConsoleHost_history.ps1 - Moves the ConsoleHost_history.txt file into the Modules output for better visibility
Category: PowerShellHistory
Author: Andrew Rathbun and Matt Arbaugh
Version: 1.0
Id: e57584ec-0c9a-49cf-9ac5-7d42c7570fae
BinaryUrl: https://github.com/AndrewRathbun/DFIRPowerShellScripts/blob/main/KAPE/Move-KAPEConsoleHost_history.ps1
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: "& '%kapeDirectory%\\Modules\\bin\\Move-KAPEConsoleHost_history.ps1' -InputDir '%sourceDirectory%' -Destination %destinationDirectory%"
        ExportFormat: txt

# Documentation
# https://github.com/AndrewRathbun/DFIRPowerShellScripts/blob/main/Move-KAPEConsoleHost_history.ps1
# Use this to ensure the ConsoleHost_history.txt file for each user doesn't get forgotten about!
# This script will copy all instances of ConsoleHost_history.txt from your specified Source Directory and place a copy in the following structure: %destinationDirectory%\PowerShellHistory\%User%\ConsoleHost_history.txt
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
