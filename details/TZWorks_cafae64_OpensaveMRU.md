# ⚙️ **Tzworks Cafae64 Opensave MRU**
### `File Name: TZWorks_cafae64_OpensaveMRU.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse NTUSER.DAT hive to rather the recently opened or saved files from an "Open/Save As" shell dialog box

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 Opensave MRU to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 Opensave MRU logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 Opensave MRU timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse NTUSER.DAT hive to rather the recently opened or saved files from an "Open/Save As" shell dialog box'
Category: File_Accessed
Author: Ajith Ravindran
Version: 0.1
Id: 3c2ce769-ed17-4551-b234-7dd458269f37
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: NTUSER.DAT
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -opensave_mru -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: OpensaveMRU_Parsed.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
