# ⚙️ **Live Response Network Details**
### `File Name: LiveResponse_NetworkDetails.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Mike Cary  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Network Details

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Live Response Network Details to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Live Response Network Details logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Live Response Network Details timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Network Details
Category: LiveResponse
Author: Mike Cary
Version: 1.0
Id: 77b87364-39b1-46ff-b355-3d6fa8da9560
ExportFormat: txt
FileMask: ""
Processors:
    -
        Executable: Windows_IPConfig.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Windows_DNSCache.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Windows_ARPCache.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Windows_RoutingTable.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Windows_NetStat.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Windows_nbtstat_NetBIOSSessions.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Windows_nbtstat_NetBIOSCache.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation
# As this processes live data off the sytem any directory can be set as "msource"
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
