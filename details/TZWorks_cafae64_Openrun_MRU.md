# ⚙️ **Tzworks Cafae64 Openrun MRU**
### `File Name: TZWorks_cafae64_Openrun_MRU.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse Last Visited MRU from NTUSER.DAT

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 Openrun MRU to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 Openrun MRU logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 Openrun MRU timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse Last Visited MRU from NTUSER.DAT'
Category: Registry_Artifacts
Author: Ajith Ravindran
Version: 0.1
Id: 11aab96d-8bdd-46c0-93a1-0a61e7148363
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: NTUSER.DAT
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -openrun_mru -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: Openrun_MRU.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
