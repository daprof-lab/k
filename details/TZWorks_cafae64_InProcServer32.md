# ⚙️ **Tzworks Cafae64 In Proc Server32**
### `File Name: TZWorks_cafae64_InProcServer32.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse InProcServer32 related information from SOFTWARE registry hive. Malicious actors are known to modify InProcServer32 registry values to load their malicious DLLs while perform COM Hijacking.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 In Proc Server32 to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 In Proc Server32 logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 In Proc Server32 timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse InProcServer32 related information from SOFTWARE registry hive. Malicious actors are known to modify InProcServer32 registry values to load their malicious DLLs while perform COM Hijacking.'
Category: Registry_Artifacts
Author: Ajith Ravindran
Version: 0.1
Id: bfc7de28-faf1-4380-a5f1-d379cd9b4f18
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: SOFTWARE
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -inprocservers -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: InProcServer32_Parsed.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
