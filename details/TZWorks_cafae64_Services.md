# ⚙️ **Tzworks Cafae64 Services**
### `File Name: TZWorks_cafae64_Services.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse out information about each service on the system, stored in SOFTWARE and SYSTEM Hives

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 Services to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 Services logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 Services timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse out information about each service on the system, stored in SOFTWARE and SYSTEM Hives'
Category: Registry_Artifacts
Author: Ajith Ravindran
Version: 0.1
Id: 67f9b054-ed69-493b-906b-455d6efd8776
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: (SYSTEM|SOFTWARE)
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -services -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: Services_Parsed.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
