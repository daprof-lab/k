# ⚙️ **Tzworks Cafae64 Muicache**
### `File Name: TZWorks_cafae64_MUIcache.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse MUICache from USRCLASS.DAT

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 Muicache to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 Muicache logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 Muicache timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse MUICache from USRCLASS.DAT'
Category: Registry_Artifacts
Author: Ajith Ravindran
Version: 0.1
Id: 5721a241-43fb-433f-92f1-be7d21d43da2
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: USRCLASS.DAT
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -muicache -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: MUIcache_Parser.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
