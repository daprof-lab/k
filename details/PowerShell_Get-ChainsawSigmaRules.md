# ⚙️ **Power Shell Get Chainsaw Sigma Rules**
### `File Name: PowerShell_Get-ChainsawSigmaRules.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Get-ChainsawSigmaRules.ps1 - Update Sigma Rules that Chainsaw relies on

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Get Chainsaw Sigma Rules to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Get Chainsaw Sigma Rules logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Get Chainsaw Sigma Rules timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Get-ChainsawSigmaRules.ps1 - Update Sigma Rules that Chainsaw relies on
Category: ChainsawSync
Author: Andrew Rathbun
Version: 1.0
Id: b3fc53a5-4f10-431d-903a-65700bf16e2f
BinaryUrl: https://github.com/AndrewRathbun/DFIRPowerShellScripts/blob/main/KAPE/Get-ChainsawSigmaRules.ps1
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: "& '%kapeDirectory%\\Modules\\bin\\Get-ChainsawSigmaRules.ps1'"
        ExportFormat: txt

# Documentation
# https://github.com/AndrewRathbun/DFIRPowerShellScripts/blob/main/Get-ChainsawSigmaRules.ps1
# Use this to ensure Chainsaw is working with the most updated Sigma Rules!
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
