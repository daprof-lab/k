# ⚙️ **Power Shell Sum Ecmd SUM Repair And Parse**
### `File Name: PowerShell_SumECmd_SUM-RepairAndParse.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Matthew Arbaugh  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Extract SUM data and repair with SumECmd

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Sum Ecmd SUM Repair And Parse to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Sum Ecmd SUM Repair And Parse logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Sum Ecmd SUM Repair And Parse timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Extract SUM data and repair with SumECmd
Category: SUM
Author: Matthew Arbaugh
Version: 1.0
Id: 92cc0f6c-4e41-4b1f-b250-4b016724f1c8
BinaryUrl: https://github.com/AndrewRathbun/DFIRPowerShellScripts/blob/main/KAPE/SUM-Repair.ps1
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: "& '%kapeDirectory%\\Modules\\bin\\SUM-Repair.ps1' -TargetPath %sourceDirectory% -OutputPath %destinationDirectory% -Kape"
        ExportFormat: csv

# Documentation
# Use this to make a copy of the SUM DB with PowerShell, repair with esentutl.exe, and extract SUM data with SumECmd
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
