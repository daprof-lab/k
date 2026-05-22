# ⚙️ **Tzworks Cafae64 Devices**
### `File Name: TZWorks_cafae64_Devices.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using cafae64.exe to parse information about the devices on the system from SYSTEM registry hive (HKLM\SYSTEM\CurrentControlSet\Enum)

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Cafae64 Devices to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Cafae64 Devices logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Cafae64 Devices timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using cafae64.exe to parse information about the devices on the system from SYSTEM registry hive (HKLM\SYSTEM\CurrentControlSet\Enum)'
Category: Registry_Artifacts
Author: Ajith Ravindran
Version: 0.1
Id: d71417fd-d876-43e1-a6de-f5f0da38d81c
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: SYSTEM
ExportFormat: csv
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -devices -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: Devices_Parsed.csv

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
