# ⚙️ **Power Shell Srum Ecmd SRUM Repair And Parse**
### `File Name: PowerShell_SrumECmd_SRUM-RepairAndParse.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Matthew Arbaugh  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Extract SRUM data and repair with SrumECmd

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Srum Ecmd SRUM Repair And Parse to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Srum Ecmd SRUM Repair And Parse logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Srum Ecmd SRUM Repair And Parse timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Extract SRUM data and repair with SrumECmd
Category: SRUM
Author: Matthew Arbaugh
Version: 1.0
Id: a03a3be0-0101-42cc-a639-484ab24e0018
BinaryUrl: https://github.com/AndrewRathbun/DFIRPowerShellScripts/blob/main/KAPE/SRUM-Repair.ps1
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: "& '%kapeDirectory%\\Modules\\bin\\SRUM-Repair.ps1' -TargetPath %sourceDirectory% -OutputPath %destinationDirectory% -Kape"
        ExportFormat: csv

# Documentation
# Use this to make a copy of the SRUM DB with PowerShell, repair with esentutl.exe, and extract SUM data with SrumECmd
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
