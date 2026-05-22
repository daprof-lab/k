# ⚙️ **Tzworks Cafae64 Shimcache**
### `File Name: TZWorks_cafae64_Shimcache.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse out Shimcache related artifacts from the SYSTEM Hives

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 Shimcache to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 Shimcache logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 Shimcache timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse out Shimcache related artifacts from the SYSTEM Hives'
Category: ProgramExecution
Author: Ajith Ravindran
Version: 0.1
Id: f1c2c8a8-8fe8-4a92-b668-125b3d06d804
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: SYSTEM
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -shimcache -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: Shimcache_Parsed.csv

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
