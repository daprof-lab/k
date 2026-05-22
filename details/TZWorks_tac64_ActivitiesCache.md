# ⚙️ **Tzworks Tac64 Activities Cache**
### `File Name: TZWorks_tac64_ActivitiesCache.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using tac64.exe to parse Windows Timeline ActivitiesCache files from C:\Users\<useracct>\AppData\Local\ConnectedDevicesPlatform\L.<useracct>\ActivitiesCache.db folder. The parsed output lists a history from the most recent tasks to a few weeks ago (up to 30 days) showing a chronology of actions taken by the user

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Tac64 Activities Cache to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Tac64 Activities Cache logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Tac64 Activities Cache timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using tac64.exe to parse Windows Timeline ActivitiesCache files from C:\Users\<useracct>\AppData\Local\ConnectedDevicesPlatform\L.<useracct>\ActivitiesCache.db folder. The parsed output lists a history from the most recent tasks to a few weeks ago (up to 30 days) showing a chronology of actions taken by the user'
Category: ProgramExecution
Author: Ajith Ravindran
Version: 0.1
Id: e48e85b4-f3e2-4941-9a9e-79299cf57647
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=41
ExportFormat: csv
FileMask: ActivitiesCache.db
Processors:
    -
        Executable: tac64.exe
        CommandLine: -db %sourceFile% -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: ActivitiesCache_Parsed.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
