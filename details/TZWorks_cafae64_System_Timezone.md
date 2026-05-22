# ⚙️ **Tzworks Cafae64 System Timezone**
### `File Name: TZWorks_cafae64_System_Timezone.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse SYSTEM hive and extract the timezone information of the host

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 System Timezone to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 System Timezone logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 System Timezone timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse SYSTEM hive and extract the timezone information of the host'
Category: ProgramExecution
Author: Ajith Ravindran
Version: 0.1
Id: 2c08affe-abd9-4c0c-b089-66367aeea667
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: SYSTEM
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -timezone -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: System_Timezone.csv

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
