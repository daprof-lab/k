# ⚙️ **Live Response Process Details**
### `File Name: LiveResponse_ProcessDetails.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** piesecurity  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Combination Module for LiveResponse. Gathering Running Process Details

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Live Response Process Details to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Live Response Process Details logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Live Response Process Details timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Combination Module for LiveResponse. Gathering Running Process Details
Category: LiveResponse
Author: piesecurity
Version: 1.0
Id: 337a4733-5549-4d3e-818e-8c4c6b0381de
ExportFormat: txt
FileMask: ""
Processors:
    -
        Executable: PowerShell_Get-InjectedThread.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_ProcessList_WMI.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: SysInternals_PsList.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: SysInternals_PsTree.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: SysInternals_PsService.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: SysInternals_Handle.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation
# As this processes live data off the sytem any directory can be set as "msource"
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
