# ⚙️ **Tzworks Cafae64 Other Apps Run**
### `File Name: TZWorks_cafae64_OtherAppsRun.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse and list recently executed applications from Users NTUSER.DAT registry hive

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 Other Apps Run to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 Other Apps Run logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 Other Apps Run timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse and list recently executed applications from Users NTUSER.DAT registry hive'
Category: ProgramExecution
Author: Ajith Ravindran
Version: 0.1
Id: 990d2bc9-1282-4f93-b303-655905851a8d
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: NTUSER.DAT
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -otherapps_run -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: OtherAppsRun.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
