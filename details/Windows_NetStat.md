# ⚙️ **Windows Net Stat**
### `File Name: Windows_NetStat.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Mike Cary  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
NetStat

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Net Stat to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Net Stat logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Net Stat timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: NetStat
Category: LiveResponse
Author: Mike Cary
Version: 1.0
Id: ea773d1a-0a69-432d-ab3a-45a0d87374b8
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\netstat.exe
        CommandLine: -anob
        ExportFormat: txt
        ExportFile: network_connections.txt

# Documentation
# https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/netstat
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
