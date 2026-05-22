# ⚙️ **Windows Nbtstat Net Bioscache**
### `File Name: Windows_nbtstat_NetBIOSCache.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Mike Cary, Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
NBTStat_NETBIOS_Cache

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Nbtstat Net Bioscache to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Nbtstat Net Bioscache logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Nbtstat Net Bioscache timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: NBTStat_NETBIOS_Cache
Category: Network Activity
Author: Mike Cary, Max Zabuty
Version: 1.0
Id: d0309794-03b1-40bf-bbdd-12fe77f5e0a6
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\nbtstat.exe
        CommandLine: -c
        ExportFormat: txt
        ExportFile: NetBIOS Cache.txt

# Documentation
# https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/nbtstat
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
