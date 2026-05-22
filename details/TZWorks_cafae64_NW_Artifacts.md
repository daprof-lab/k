# ⚙️ **Tzworks Cafae64 NW Artifacts**
### `File Name: TZWorks_cafae64_NW_Artifacts.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse out Network Related Artifacts found in SOFTWARE, SYSTEM and User Hives from associated NTUSER.dat registry hive

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 NW Artifacts to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 NW Artifacts logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 NW Artifacts timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse out Network Related Artifacts found in SOFTWARE, SYSTEM and User Hives from associated NTUSER.dat registry hive'
Category: Registry_Artifacts
Author: Ajith Ravindran
Version: 0.1
Id: dd584a52-396d-4b09-b57e-167c7261ce35
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: (NTUSER.DAT|SYSTEM|SOFTWARE)
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -network -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: NW_Artifacts_Parsed.csv
        Append: true


# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
