# ⚙️ **Tzworks Cafae64 Userassist**
### `File Name: TZWorks_cafae64_Userassist.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse Userassist from NTUSER.DAT. Userassist tracks execution of GUI based executables and links opened in Explorer 

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 Userassist to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 Userassist logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 Userassist timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse Userassist from NTUSER.DAT. Userassist tracks execution of GUI based executables and links opened in Explorer '
Category: ProgramExecution
Author: Ajith Ravindran
Version: 0.1
Id: b904f46a-25b4-42d9-bfd0-13680ee335bf
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: NTUSER.DAT
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -userassist -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: Userassist_Parser.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
