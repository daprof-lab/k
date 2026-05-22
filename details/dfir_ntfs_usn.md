# ⚙️ **Dfir Ntfs Usn**
### `File Name: dfir_ntfs_usn.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Nick Polosukhin  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
dfir_ntfs: process $J file

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Dfir Ntfs Usn to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Dfir Ntfs Usn logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Dfir Ntfs Usn timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'dfir_ntfs: process $J file'
Category: FileSystem
Author: Nick Polosukhin
Version: 1.0
Id: 415bccbe-1317-4b88-b476-4e230725f5ea
BinaryUrl: https://github.com/msuhanov/dfir_ntfs/archive/refs/tags/1.1.19.zip
ExportFormat: csv
FileMask: $MFT
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine:  -c "$J_Path = Get-ChildItem -Path "%sourceDirectory%" -Recurse -Force -ErrorAction SilentlyContinue | Where-Object { $_.Name -eq '$J' } | Select-Object -ExpandProperty FullName;python.exe %kapeDirectory%\\Modules\\bin\\dfir_ntfs\\ntfs_parser --usn '%sourceFile%' $J_Path %destinationDirectory%\\dfir_ntfs_usn.csv"
        ExportFormat: csv

# Documentation
# https://github.com/msuhanov/dfir_ntfs
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
