# ⚙️ **Hayabusa Update Rules**
### `File Name: hayabusa_UpdateRules.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
Hayabusa a timeline generator for Windows event logs - Update Rules

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Hayabusa Update Rules to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Hayabusa Update Rules logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Hayabusa Update Rules timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Hayabusa a timeline generator for Windows event logs - Update Rules
Category: EventLogs
Author: Andrew Rathbun
Version: 1.2
Id: cd547400-e8cb-4339-9a50-818327fe059b
BinaryUrl: https://github.com/Yamato-Security/hayabusa/releases
ExportFormat: ""
Processors:
    -
        Executable: hayabusa\hayabusa.exe
        CommandLine: update-rules
        ExportFormat: ""

# Documentation
# Create a folder "hayabusa" within the "Modules\bin" KAPE folder
# Place "zip archive" file into "Modules\bin\hayabusa" and unpack
# rename the hayabusa executable to hayabusa.exe
# You can delete all except: "config"; "rules" and the "hayabusa.exe"
# For more options use: hayabusa.exe help
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
