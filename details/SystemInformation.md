# ⚙️ **System Information**
### `File Name: SystemInformation.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Max Zabuty  
**Version:** 1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Parsing all information for System Information Category

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run System Information to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw System Information logs to index file anomalies.
* **Incident Impact Assessment**: Leverage System Information timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parsing all information for System Information Category
Category: System Information
Author: Max Zabuty
Version: 1
Id: 223ac60b-b5be-4f79-8e16-4f16b1597f3c
ExportFormat: json
Processors:
    -
        Executable: PowerShell_SystemInformation.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_Processes.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_ProcessesIncludingServices.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_Drivers.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_NetworkShares.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_ActiveDrives.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_LocalUsers.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_LocalGroups.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Windows_klist.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Windows_nltest.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_Defender_Exclusions.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation:
# N/A
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
