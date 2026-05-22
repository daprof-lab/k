# ⚙️ **Nirsoft App Resources Usage View**
### `File Name: Nirsoft_AppResourcesUsageView.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Nirsoft_AppResourcesUsageView Nirsoft

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nirsoft App Resources Usage View to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nirsoft App Resources Usage View logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nirsoft App Resources Usage View timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Nirsoft_AppResourcesUsageView Nirsoft
Category: Databases
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: 917b36bd-ad2b-4910-a9ab-3b95aa2436a7
BinaryUrl: https://www.nirsoft.net/utils/appresourcesusageview.zip
ExportFormat: csv
Processors:
    -
        Executable: AppResourcesUsageView.exe
        CommandLine: \%sourceDirectory%\C\Windows\System32\SRU\SRUDB.dat /scomma %destinationDirectory%\Nirsoft_SRUDB_Results.csv
        ExportFormat: csv

# Documentation
# extracts and displays the application resources usage information stored in the SRUDB.dat database of Windows 10 and Windows 11.
# The application resources usage data is automatically collected by Windows operating systems and includes the following information: Record ID, Timestamp, Application, User, Cycle Time (Foreground/Background), Face Time, Context Switches (Foreground/Background), Bytes Read/Written (Foreground/Background), Read/Write Operations Count (Foreground/Background)
# https://www.nirsoft.net/utils/app_resources_usage_view.html
# Must set msource to users directory of triage to be parsed
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
