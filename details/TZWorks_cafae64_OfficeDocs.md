# ⚙️ **Tzworks Cafae64 Office Docs**
### `File Name: TZWorks_cafae64_OfficeDocs.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse NTUSER.DAT hive and extract information from keys associated with Office Documents

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 Office Docs to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 Office Docs logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 Office Docs timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse NTUSER.DAT hive and extract information from keys associated with Office Documents'
Category: File_Accessed
Author: Ajith Ravindran
Version: 0.1
Id: d29e4ef5-900f-4cb5-a245-b4fe3cedf83d
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: NTUSER.DAT
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -office_docs  -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: OfficeDocs_Parsed.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
