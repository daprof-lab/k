# ⚙️ **Power Shell Mftecmd J Mftparsing**
### `File Name: PowerShell_MFTECmd_J-MFTParsing.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Andrew Rathbun  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
MFTECmd - Parse $J and $MFT together to produce CSV output with ParentPath populated in $J CSV

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Mftecmd J Mftparsing to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Mftecmd J Mftparsing logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Mftecmd J Mftparsing timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: MFTECmd - Parse $J and $MFT together to produce CSV output with ParentPath populated in $J CSV
Category: FileSystem
Author: Andrew Rathbun
Version: 1.1
Id: ac0660c3-4eb2-4dee-ad90-5ef782b94750
BinaryUrl: https://github.com/AndrewRathbun/DFIRPowerShellScripts/blob/main/KAPE/MFTECmd%24J%24MFTParser.ps1
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: "& '%kapeDirectory%\\Modules\\bin\\MFTECmd$J$MFTParser.ps1' -TargetsFolder %sourceDirectory% -OutputFolder %destinationDirectory% -KAPE"
        ExportFormat: csv

# Documentation
# https://github.com/AndrewRathbun/DFIRPowerShellScripts/blob/main/MFTECmd%24J%24MFTParser.ps1
# Use this when there's a $J and $MFT present. This script will search for the $J and $MFT and parse them with the MFTECmd executable that resides in .\KAPE\Modules\bin
# The main reason for this script's existence is because a KAPE Module cannot have 2 file masks (one for $J and another for $MFT) so this script serves as the workaround for that scenario
# To use this properly, point to a parent folder where somewhere in a child folder there exists a $J and $MFT, ideally from the same system!
# v1.1, add KAPE switch so it searches for MFTECmd.exe in .\KAPE\Modules\bin and uses that to parse $J and $MFT together
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
