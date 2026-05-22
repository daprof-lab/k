# ⚙️ **Power Shell Netscan**
### `File Name: PowerShell_Netscan.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** nov3mb3r  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Network scan of process connections

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Netscan to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Netscan logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Netscan timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Network scan of process connections
Category: LiveResponse
Author: nov3mb3r
Version: 1.0
Id: c1847d86-3fa9-492b-ae09-8c90173ec222
BinaryUrl: https://github.com/nov3mb3r/Get-Netscan/blob/main/Get-Netscan.ps1
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: "& '%kapeDirectory%\\Modules\\bin\\Get-Netscan.ps1'"
        ExportFormat: txt
        ExportFile: netscan.txt

# Documentation
# https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/netstat
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
