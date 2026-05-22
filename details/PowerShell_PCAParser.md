# ⚙️ **Power Shell Pcaparser**
### `File Name: PowerShell_PCAParser.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
PCAParser.ps1 - Parses Windows 11 artifacts related to Program Compatability Assistant

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Pcaparser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Pcaparser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Pcaparser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: PCAParser.ps1 - Parses Windows 11 artifacts related to Program Compatability Assistant
Category: ProgramExecution
Author: Andrew Rathbun
Version: 1.0
Id: e817f4f2-5daa-42b2-bde8-0c532c99b1d9
BinaryUrl: https://github.com/AndrewRathbun/PCAParser/blob/main/PCAParser.ps1
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: "& '%kapeDirectory%\\Modules\\bin\\PCAParser.ps1' -inputPath '%sourceDirectory%' -outputPath %destinationDirectory%"
        ExportFormat: csv

# Documentation
# https://github.com/AndrewRathbun/PCAParser
# https://aboutdfir.com/new-windows-11-pro-22h2-evidence-of-execution-artifact/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
