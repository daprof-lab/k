# ⚙️ **Tzworks Cafae64 Recent Docs**
### `File Name: TZWorks_cafae64_Recent_Docs.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse RecentDocs from NTUSER.DAT

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 Recent Docs to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 Recent Docs logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 Recent Docs timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse RecentDocs from NTUSER.DAT'
Category: Registry_Artifacts
Author: Ajith Ravindran
Version: 0.1
Id: 08507dbb-7a81-4097-aca2-06e76e116496
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: NTUSER.DAT
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -recent_docs -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: Recent_Docs_Parsed.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
