# ⚙️ **Tzworks Mala64 Logfile**
### `File Name: TZWorks_mala64_Logfile.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using mala64.exe to parse the Windows NTFS file systems transactional log $LogFile from the host.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Mala64 Logfile to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Mala64 Logfile logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Mala64 Logfile timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using mala64.exe to parse the Windows NTFS file systems transactional log $LogFile from the host.'
Category: File_Accessed
Author: Ajith Ravindran
Version: 0.1
Id: 23b0b934-b01e-4b73-83cb-3eea74dc5e91
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=46
ExportFormat: csv
FileMask: $MFT
Processors:
    -
        Executable: mala64.exe
        CommandLine: -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace -log %sourceDirectory%\\$LogFile  -mftfile %sourceFile%
        ExportFormat: csv
        ExportFile: Logfile_Parsed.csv

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
