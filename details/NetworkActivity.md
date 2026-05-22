# ⚙️ **Network Activity**
### `File Name: NetworkActivity.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Max Zabuty  
**Version:** 1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Parsing all information for Network Activity Category

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Network Activity to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Network Activity logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Network Activity timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parsing all information for Network Activity Category
Category: Network Activity
Author: Max Zabuty
Version: 1
Id: 8da4a739-5367-47ca-ab84-12f4a0f8e0de
ExportFormat: json
Processors:
    -
        Executable: PowerShell_SMBMapping.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_SMBOpenFile.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_SMBSession.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_NetNeighbor.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_TCPConnections.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_NetworkAdapters.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_NetworkIPAddresses.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_NetworkIPConfiguration.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_DnsClientCache.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Windows_nbtstat_NetBIOSCache.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Windows_nbtstat_NetBIOSSessions.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Powershell_Wireless_Network_Connections.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_NamedPipes.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_NetRoute.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation:
# N/A
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
