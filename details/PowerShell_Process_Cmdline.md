# ⚙️ **Power Shell Process Cmdline**
### `File Name: PowerShell_Process_Cmdline.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** nov3mb3r  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Process Commandline

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Process Cmdline to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Process Cmdline logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Process Cmdline timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Process Commandline
Category: LiveResponse
Author: nov3mb3r
Version: 1.0
Id: 92039073-8cb7-4b82-86de-1911fd8e317a
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-WmiObject Win32_Process | Select-Object Name,  ProcessId, CommandLine | Sort Name | Format-Table -Wrap"
        ExportFormat: txt
        ExportFile: processcmdline.txt

# Documentation
# https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
