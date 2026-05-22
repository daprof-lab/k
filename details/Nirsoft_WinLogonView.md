# ⚙️ **Nirsoft Win Logon View**
### `File Name: Nirsoft_WinLogonView.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
NirSoft_winlogonview - Nirsoft

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nirsoft Win Logon View to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nirsoft Win Logon View logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nirsoft Win Logon View timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'NirSoft_winlogonview - Nirsoft'
Category: EventLogs
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: 8bbe88c3-1dd5-4262-af4e-fcd349cca472
BinaryUrl: https://www.nirsoft.net/utils/winlogonview.zip
ExportFormat: csv
Processors:
    -
        Executable: winlogonview.exe
        CommandLine: /scomma %destinationDirectory%\Nirsoft_winlogonview.csv  /sort "User Name" /sort "Logon Time"
        ExportFormat: csv

# Documentation
# https://www.nirsoft.net/utils/windows_log_on_times_view.html
# WinLogOnView is a simple tool for Windows 10/8/7/Vista/2008 that analyses the security event log of Windows operating system, and detects the date/time that users logged on and logged off. For every time that a user log on/log off to your system, the following information is displayed: Logon ID, User Name, Domain, Computer, Logon Time, Logoff Time, Duration, and network address.
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
