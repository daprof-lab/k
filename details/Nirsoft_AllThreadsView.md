# ⚙️ **Nirsoft All Threads View**
### `File Name: Nirsoft_AllThreadsView.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
AllThreadsView is a simple tool for Windows that displays a list of all running threads from all processes on your system in one table. For every thread, the following information is displayed Thread ID, Creation Time, Kernel Time, User Time, Duration, Start Address, Priority, Base Priority, Context Switch Count, Context Switch Change (Since the last refresh), Wait Reason, Process ID, Process Path.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nirsoft All Threads View to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nirsoft All Threads View logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nirsoft All Threads View timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: AllThreadsView is a simple tool for Windows that displays a list of all running threads from all processes on your system in one table. For every thread, the following information is displayed Thread ID, Creation Time, Kernel Time, User Time, Duration, Start Address, Priority, Base Priority, Context Switch Count, Context Switch Change (Since the last refresh), Wait Reason, Process ID, Process Path.
Category: LiveResponse
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: 612d92e7-c80f-41c4-b47d-ca7a1456117a
BinaryUrl: https://www.nirsoft.net/utils/allthreadsview-x64.zip
ExportFormat: csv
Processors:
    -
        Executable: AllThreadsView.exe
        CommandLine: /scomma %destinationDirectory%\Nirsoft_AllThreadsView.csv
        ExportFormat: csv

# Documentation
# https://www.nirsoft.net/utils/all_threads_view.html
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
