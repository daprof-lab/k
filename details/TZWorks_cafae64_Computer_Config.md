# ⚙️ **Tzworks Cafae64 Computer Config**
### `File Name: TZWorks_cafae64_Computer_Config.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse Computer configurations from SOFTWARE, SYSTEM and User (NTUSER.DAT and USRCLASS.DAT) registry hive

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 Computer Config to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 Computer Config logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 Computer Config timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse Computer configurations from SOFTWARE, SYSTEM and User (NTUSER.DAT and USRCLASS.DAT) registry hive'
Category: Registry_Artifacts
Author: Ajith Ravindran
Version: 0.1
Id: 6c3fc9c9-4c95-475d-b354-d7007f3910ae
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: (SOFTWARE|SYSTEM|NTUSER.DAT|USRCLASS.DAT)
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -computer -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: Computer_Config_Parsed.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
