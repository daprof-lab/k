# ⚙️ **Dfir Ntfs Mft**
### `File Name: dfir_ntfs_mft.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Nick Polosukhin  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
dfir_ntfs: process $MFT file

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Dfir Ntfs Mft to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Dfir Ntfs Mft logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Dfir Ntfs Mft timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'dfir_ntfs: process $MFT file'
Category: FileSystem
Author: Nick Polosukhin
Version: 1.0
Id: e86455d0-b1b8-4386-9f2e-d557c7fbe533
BinaryUrl: https://github.com/msuhanov/dfir_ntfs/archive/refs/tags/1.1.19.zip
ExportFormat: csv
FileMask: $MFT
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine:  -c "python.exe %kapeDirectory%\\Modules\\bin\\dfir_ntfs\\ntfs_parser --mft '%sourceFile%' %destinationDirectory%\\dfir_ntfs_mft.csv"
        ExportFormat: csv

# Documentation
# https://github.com/msuhanov/dfir_ntfs
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
