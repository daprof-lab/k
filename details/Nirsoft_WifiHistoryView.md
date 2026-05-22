# ⚙️ **Nirsoft Wifi History View**
### `File Name: Nirsoft_WifiHistoryView.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
NirSoft_WifiHistoryView - Nirsoft

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nirsoft Wifi History View to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nirsoft Wifi History View logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nirsoft Wifi History View timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'NirSoft_WifiHistoryView - Nirsoft'
Category: LiveResponse
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: 816c1e88-419e-421e-b117-9c4112c2232f
BinaryUrl: https://www.nirsoft.net/utils/wifi_history_view.zip
ExportFormat: csv
Processors:
    -
        Executable: WifiHistoryView.exe
        CommandLine: /scomma %destinationDirectory%\Nirsoft_WifiHistoryView.csv
        ExportFormat: txt

# Documentation
# https://www.nirsoft.net/utils/wifi_history_view.html
# WifiHistoryView is a simple tool for Windows 11/10/8/7/Vista that displays the history of connections to wireless networks on your computer.
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
