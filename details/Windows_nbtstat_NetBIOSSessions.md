# ⚙️ **Windows Nbtstat Net Biossessions**
### `File Name: Windows_nbtstat_NetBIOSSessions.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Mike Cary, Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
NBTStat_NETBIOS_Sessions

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Nbtstat Net Biossessions to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Nbtstat Net Biossessions logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Nbtstat Net Biossessions timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: NBTStat_NETBIOS_Sessions
Category: Network Activity
Author: Mike Cary, Max Zabuty
Version: 1.0
Id: 340d77a6-a9bd-400b-b3b6-bdd5a2085e3c
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\nbtstat.exe
        CommandLine: -s
        ExportFormat: txt
        ExportFile: NetBIOS Session.txt

# Documentation
# https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/nbtstat
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
