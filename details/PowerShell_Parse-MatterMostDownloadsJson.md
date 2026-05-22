# ⚙️ **Power Shell Parse Matter Most Downloads Json**
### `File Name: PowerShell_Parse-MatterMostDownloadsJson.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Parse-MatterMostDownloadsJson.ps1 - Parses Downloads.json artifact for MatterMost

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Parse Matter Most Downloads Json to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Parse Matter Most Downloads Json logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Parse Matter Most Downloads Json timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parse-MatterMostDownloadsJson.ps1 - Parses Downloads.json artifact for MatterMost
Category: Downloads
Author: Andrew Rathbun
Version: 1.0
Id: cb794d78-a91a-4119-95b5-3a3b844d3fbe
BinaryUrl: https://github.com/AndrewRathbun/DFIRPowerShellScripts/blob/main/KAPE/Parse-MatterMostDownloadsJson.ps1
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: "& '%kapeDirectory%\\Modules\\bin\\Parse-MatterMostDownloadsJson.ps1' -folderPath '%sourceDirectory%' -outputPath %destinationDirectory%"
        ExportFormat: csv

# Documentation
# https://github.com/AndrewRathbun/DFIRPowerShellScripts/blob/main/Parse-MatterMostDownloadsJson.ps1
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
