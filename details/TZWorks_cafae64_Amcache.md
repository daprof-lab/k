# ⚙️ **Tzworks Cafae64 Amcache**
### `File Name: TZWorks_cafae64_Amcache.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse Amcache.hve file

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 Amcache to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 Amcache logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 Amcache timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse Amcache.hve file'
Category: Registry_Artifacts
Author: Ajith Ravindran
Version: 0.1
Id: 5b5ea20b-a7ec-4210-95e2-a451af907c6d
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: Amcache.hve
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -all_amcache -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: Amcache_Parsed.csv

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
