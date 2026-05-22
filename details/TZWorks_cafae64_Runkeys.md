# ⚙️ **Tzworks Cafae64 Runkeys**
### `File Name: TZWorks_cafae64_Runkeys.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse out Run keys found in SOFTWARE Hives. Run keys are usually used by malicious applications to achieve persistence on hosts.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 Runkeys to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 Runkeys logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 Runkeys timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse out Run keys found in SOFTWARE Hives. Run keys are usually used by malicious applications to achieve persistence on hosts.'
Category: Registry_Artifacts
Author: Ajith Ravindran
Version: 0.1
Id: f08a4f58-230b-4ad5-a364-8a5093bf0898
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: SOFTWARE
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -runkeys -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: Runkeys_Parsed.csv

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
