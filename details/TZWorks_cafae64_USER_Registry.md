# ⚙️ **Tzworks Cafae64 USER Registry**
### `File Name: TZWorks_cafae64_USER_Registry.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse all available artifacts from NTUSER.DAT and USRCLASS.DAT registry hive

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 USER Registry to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 USER Registry logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 USER Registry timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse all available artifacts from NTUSER.DAT and USRCLASS.DAT registry hive'
Category: Registry_Artifacts
Author: Ajith Ravindran
Version: 0.1
Id: 59e955a4-360c-43f4-ba86-fc611b5bc03c
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: (NTUSER.DAT|USRCLASS.DAT)
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -all_user -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: USER_Registry_Parsed.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
