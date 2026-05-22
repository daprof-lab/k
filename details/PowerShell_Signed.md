# ⚙️ **Power Shell Signed**
### `File Name: PowerShell_Signed.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
PowerShell_Signing

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Signed to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Signed logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Signed timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'PowerShell_Signing'
Category: LiveResponse
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: 2fec6f40-c36f-4faa-8b42-c997e494d92b
BinaryUrl: https://raw.githubusercontent.com/conexioninversa/Forensics/master/PowerShell_Signed.ps1
ExportFormat: json
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -ep bypass -Command %kapedirectory%\Modules\bin\PowerShell_Signed.ps1 | Out-File -FilePath %destinationDirectory%\FilesNot_Signed.json
        ExportFormat: json

# Documentation
# Checks the digital signature of the DLL and EXE files in the folders c:\windows\system32 and C:\Windows\SysWOW64\ Unsigned files in these folders could be an indication of lateral movement, which is used by attackers for lateral movement between machines
# https://github.com/conexioninversa/Forensics/blob/master/README.md
# In order for this module to work, place the powershell script on the modules bin folder
# Expected Results:
# It will save the result in the destination folder "LiveResponse" and this contains the DLL and EXE files that are not signed.
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
