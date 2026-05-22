# ⚙️ **Tzworks Cafae64 Persistence**
### `File Name: TZWorks_cafae64_Persistence.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse out Persistence Related Artifacts found in SOFTWARE, SYSTEM and User Hives from associated NTUSER.dat registry hive. The parser lists most of the key usually used by malicious applications to achieve persistence on hosts.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 Persistence to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 Persistence logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 Persistence timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse out Persistence Related Artifacts found in SOFTWARE, SYSTEM and User Hives from associated NTUSER.dat registry hive. The parser lists most of the key usually used by malicious applications to achieve persistence on hosts.'
Category: Registry_Artifacts
Author: Ajith Ravindran
Version: 0.1
Id: bb0ad10f-1b40-44fb-b8e0-324495fd5115
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: (NTUSER.DAT|SYSTEM|SOFTWARE)
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -persistence -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: Persistence_Parsed.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
