# ⚙️ **Tzworks Cafae64 Installed SW**
### `File Name: TZWorks_cafae64_Installed_SW.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse list of applications installed on the host from SOFTWARE registry hive

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 Installed SW to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 Installed SW logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 Installed SW timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse list of applications installed on the host from SOFTWARE registry hive'
Category: ProgramExecution
Author: Ajith Ravindran
Version: 0.1
Id: e74f5e86-7d6b-4412-90c9-f667153108d8
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: SOFTWARE
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -installed_sw -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: Installed_SW_Parsed.csv

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
