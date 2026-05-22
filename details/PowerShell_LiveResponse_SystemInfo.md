# ⚙️ **Power Shell Live Response System Info**
### `File Name: PowerShell_LiveResponse_SystemInfo.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Vito Alfano & piesecurity  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Gathers Basic System Information Using PowerShell (Replacing the command net)

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Live Response System Info to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Live Response System Info logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Live Response System Info timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Gathers Basic System Information Using PowerShell (Replacing the command net)
Category: LiveResponse
Author: Vito Alfano & piesecurity
Version: 1.1
Id: 0b43fe8e-a9aa-42ae-8de6-5ccfb772bdc9
ExportFormat: csv
Processors:
    -
        Executable: PowerShell_User_List.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_Local_Group_List.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_LocalAdmin.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Windows_Net_Accounts.mkape
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
        Executable: PowerShell_SMBMapping.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_Services_List.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation:
# N/A
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
