# ⚙️ **Power Shell Startup Commands**
### `File Name: PowerShell_Startup_Commands.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** nov3mb3r  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Commands on Startup

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Startup Commands to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Startup Commands logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Startup Commands timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Commands on Startup
Category: LiveResponse
Author: nov3mb3r
Version: 1.0
Id: 67733d63-8052-4abf-b85e-450bbd368e36
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-CimInstance -Class Win32_StartupCommand | Format-Table -Property Name, Command, User, Location -Wrap"
        ExportFormat: txt
        ExportFile: startup.txt

# Documentation
# N/A
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
