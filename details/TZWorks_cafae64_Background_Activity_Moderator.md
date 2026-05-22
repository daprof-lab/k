# ⚙️ **Tzworks Cafae64 Background Activity Moderator**
### `File Name: TZWorks_cafae64_Background_Activity_Moderator.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse Background/Desktop Activity Moderator keys from the host

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 Background Activity Moderator to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 Background Activity Moderator logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 Background Activity Moderator timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse Background/Desktop Activity Moderator keys from the host'
Category: ProgramExecution
Author: Ajith Ravindran
Version: 0.1
Id: a64c09d5-9f5c-41c1-9ca2-219ac3211c88
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: SYSTEM
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -bam -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: Background_Activity_Moderator_Parsed.csv

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
