# ⚙️ **Tzworks Cafae64 Volume Info**
### `File Name: TZWorks_cafae64_Volume_Info.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse out Volume Related Artifacts found in User Hives and SOFTWARE Hives

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 Volume Info to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 Volume Info logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 Volume Info timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse out Volume Related Artifacts found in User Hives and SOFTWARE Hives'
Category: Registry_Artifacts
Author: Ajith Ravindran
Version: 0.1
Id: 1448a9a2-ae40-4e5f-9ead-87339f455806
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: (NTUSER.DAT|SOFTWARE)
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -volumes -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: Volume_Info_Parsed.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
