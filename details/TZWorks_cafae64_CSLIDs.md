# ⚙️ **Tzworks Cafae64 Cslids**
### `File Name: TZWorks_cafae64_CSLIDs.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse Class Identifiers (CSLIDs) from SOFTWARE registry hive

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 Cslids to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 Cslids logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 Cslids timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse Class Identifiers (CSLIDs) from SOFTWARE registry hive'
Category: Registry_Artifacts
Author: Ajith Ravindran
Version: 0.1
Id: 58287d3d-c6a4-451c-8dab-38e5c926ae5e
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: SOFTWARE
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -clsid -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: CSLIDs_Parsed.csv

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
