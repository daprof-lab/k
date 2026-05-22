# ⚙️ **Tzworks Cafae64 Explorer**
### `File Name: TZWorks_cafae64_Explorer.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse Desktop related keys (Explorer) related information from SOFTWARE registry hive

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 Explorer to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 Explorer logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 Explorer timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse Desktop related keys (Explorer) related information from SOFTWARE registry hive'
Category: Registry_Artifacts
Author: Ajith Ravindran
Version: 0.1
Id: 69c174c5-3593-4e3f-a5b4-d7d4c80762ed
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: SOFTWARE
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -explorer -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: Explorer_Parsed.csv

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
