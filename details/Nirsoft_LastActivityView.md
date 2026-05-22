# ⚙️ **Nirsoft Last Activity View**
### `File Name: Nirsoft_LastActivityView.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
NirSoft_LastActivityView - Nirsoft

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nirsoft Last Activity View to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nirsoft Last Activity View logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nirsoft Last Activity View timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'NirSoft_LastActivityView - Nirsoft'
Category: LiveResponse
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: 07ecd985-15ef-4c79-b15e-0cfd9610cc3a
BinaryUrl: https://www.nirsoft.net/utils/lastactivityview.zip
ExportFormat: csv
Processors:
    -
        Executable: LastActivityView.exe
        CommandLine: /scomma %destinationDirectory%\LastActivityView.csv
        ExportFormat: csv

# Documentation
#  https://www.nirsoft.net/utils/lastactivityview.zip
# LastActivityView is a tool for Windows operating system that collects information from various sources on a running system, and displays a log of actions made by the user and events occurred on this computer. The activity displayed by LastActivityView includes: Running .exe file, Opening open/save dialog-box, Opening file/folder from Explorer or other software, software installation, system shutdown/start, application or system crash, network connection/disconnection and more
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
