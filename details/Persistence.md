# ⚙️ **Persistence**
### `File Name: Persistence.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Max Zabuty  
**Version:** 1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Parsing all Persistence category

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Persistence to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Persistence logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Persistence timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parsing all Persistence category
Category: Persistence
Author: Max Zabuty
Version: 1
Id: 65f33b7e-aba8-4e1e-85f1-8c40e1f23083
ExportFormat: json
Processors:
    -
        Executable: Windows_schtasks.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: SysInternals_Autoruns.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_WMIProviders.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_AccessibilityFeatures.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation:
# N/A
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
