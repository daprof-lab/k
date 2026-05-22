# ⚙️ **Tzworks Cafae64 System Restore**
### `File Name: TZWorks_cafae64_System_Restore.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse out System Restore Related Artifacts found in SOFTWARE and SYSTEM Hives

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 System Restore to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 System Restore logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 System Restore timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse out System Restore Related Artifacts found in SOFTWARE and SYSTEM Hives'
Category: Registry_Artifacts
Author: Ajith Ravindran
Version: 0.1
Id: a5530924-7ddb-4a50-b5b4-2496093ceac7
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: (SYSTEM|SOFTWARE)
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -restore -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: System_Restore_Parsed.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
