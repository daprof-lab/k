# ⚙️ **Live Response Net System Info**
### `File Name: LiveResponse_NetSystemInfo.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** piesecurity, Andreas Hunkeler (@Karneades)  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Gathers Basic System Information Using the Net Command

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Live Response Net System Info to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Live Response Net System Info logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Live Response Net System Info timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Gathers Basic System Information Using the Net Command
Category: LiveResponse
Author: piesecurity, Andreas Hunkeler (@Karneades)
Version: 1.1
Id: be86ac26-4eea-4bcb-b5ae-9686ad0557c4
ExportFormat: txt
Processors:
    -
        Executable: Windows_Net_User.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Windows_Net_LocalGroup.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_NetUserAdministrators.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Windows_Net_Accounts.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Windows_Net_File.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Windows_Net_Session.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Windows_Net_Use.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Windows_Net_Start.mkape
        CommandLine: ""
        ExportFormat: ""
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
