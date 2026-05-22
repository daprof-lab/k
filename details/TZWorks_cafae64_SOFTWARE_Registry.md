# ⚙️ **Tzworks Cafae64 SOFTWARE Registry**
### `File Name: TZWorks_cafae64_SOFTWARE_Registry.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse all available artifacts from SOFTWARE registry hive

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 SOFTWARE Registry to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 SOFTWARE Registry logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 SOFTWARE Registry timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse all available artifacts from SOFTWARE registry hive'
Category: Registry_Artifacts
Author: Ajith Ravindran
Version: 0.1
Id: f9aa63d4-8058-4e58-aae8-073ce621fab8
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: SOFTWARE
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -all_software -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: SOFTWARE_Registry_Parsed.csv

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
