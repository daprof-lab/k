# ⚙️ **Reg Ripper SYSTEM Variable**
### `File Name: RegRipper_SYSTEM-Variable.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andreas Hunkeler (@Karneades)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
RegRipper: parse SYSTEM hive using provided plugin name

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Reg Ripper SYSTEM Variable to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Reg Ripper SYSTEM Variable logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Reg Ripper SYSTEM Variable timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'RegRipper: parse SYSTEM hive using provided plugin name'
Category: Registry
Author: Andreas Hunkeler (@Karneades)
Version: 1.0
Id: 2eda739f-6af9-4b53-8d63-2c1154701a7c
BinaryUrl: https://github.com/keydet89/RegRipper3.0/archive/master.zip
ExportFormat: txt
FileMask: SYSTEM
Processors:
    -
        Executable: regripper\rip.exe
        CommandLine: -r %sourceFile% -p %systemPlugin%
        ExportFormat: txt
        ExportFile: regripper-system-%systemPlugin%.txt
        Append: true

# Documentation
# https://github.com/keydet89/RegRipper3.0
# Create a folder "regripper" within the "Modules\bin" KAPE folder
# Place "rip.exe", "p2x5124.dll" and the "plugins" folder into "Modules\bin\regripper"
# Provide a module variable using --mvars systemPlugin:pluginname
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
