# ⚙️ **Nir Soft Turned On Times View**
### `File Name: NirSoft_TurnedOnTimesView.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Thomas DIOT  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Uses Nirsoft TurnedOnTimesViewtime to determine time ranges the system was turned on

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nir Soft Turned On Times View to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nir Soft Turned On Times View logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nir Soft Turned On Times View timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Uses Nirsoft TurnedOnTimesViewtime to determine time ranges the system was turned on'
Category: EventLogs
Author: Thomas DIOT
Version: 1.0
Id: 95549abe-f13a-4c8c-bccb-8dbb7fdbe83a
BinaryUrl: https://www.nirsoft.net/utils/turnedontimesview.zip
ExportFormat: csv
Processors:
    -
        Executable: turnedontimesview\TurnedOnTimesView.exe
        CommandLine: /RunAsAdmin /Source 3 /ExternalFolder %sourceDirectory%\Windows\System32\winevt\Logs /scomma %destinationDirectory%\TurnedOnTimes.csv
        ExportFormat: csv

# Documentation
# https://www.nirsoft.net/utils/computer_turned_on_times.html
# TurnedOnTimesViewtime execution may produce an empty CSV output.
# In such case, the "New Event Log API" should be turned off ("UseNewEventLogAPI=0" in the "TurnedOnTimesView.cfg" config file).
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
