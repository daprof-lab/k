# ⚙️ **Dfir Ntfs Logfile**
### `File Name: dfir_ntfs_logfile.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Nick Polosukhin  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
dfir_ntfs: process $LogFile file

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Dfir Ntfs Logfile to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Dfir Ntfs Logfile logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Dfir Ntfs Logfile timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'dfir_ntfs: process $LogFile file'
Category: FileSystem
Author: Nick Polosukhin
Version: 1.0
Id: 2df90ab9-b8b9-49ba-89ee-28b8b3c8e4e6
BinaryUrl: https://github.com/msuhanov/dfir_ntfs/archive/refs/tags/1.1.19.zip
ExportFormat: txt
FileMask: $MFT
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine:  -c "$LogFile_Path = Get-ChildItem -Path "%sourceDirectory%" -Recurse -Force -ErrorAction SilentlyContinue | Where-Object { $_.Name -eq '$LogFile' } | Select-Object -ExpandProperty FullName;python.exe %kapeDirectory%\\Modules\\bin\\dfir_ntfs\\ntfs_parser --log '%sourceFile%' $LogFile_Path %destinationDirectory%\\dfir_ntfs_logfile.txt"
        ExportFormat: txt

# Documentation
# https://github.com/msuhanov/dfir_ntfs
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
