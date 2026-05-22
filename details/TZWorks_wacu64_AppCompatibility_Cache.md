# ⚙️ **Tzworks Wacu64 App Compatibility Cache**
### `File Name: TZWorks_wacu64_AppCompatibility_Cache.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using wacu64.exe to parse ShimCache/AppCompat Cache from the host. Application Compatibility Cache is used by the Windows to provide backward compatibility so that legacy applications can run on the newer version of the OS. Artifact confirms presence of an executable on the host, but it may or may not be executed.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Wacu64 App Compatibility Cache to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Wacu64 App Compatibility Cache logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Wacu64 App Compatibility Cache timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using wacu64.exe to parse ShimCache/AppCompat Cache from the host. Application Compatibility Cache is used by the Windows to provide backward compatibility so that legacy applications can run on the newer version of the OS. Artifact confirms presence of an executable on the host, but it may or may not be executed.'
Category: ProgramExecution
Author: Ajith Ravindran
Version: 0.1
Id: 96dfc2f5-8027-45eb-ac57-db5584b2d2fb
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=29
ExportFormat: csv
FileMask: SYSTEM
Processors:
    -
        Executable: wacu64.exe
        CommandLine: -hive %sourceFile% -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: AppCompatibility_Cache_Parsed.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
