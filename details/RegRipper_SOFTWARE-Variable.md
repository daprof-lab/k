# ⚙️ **Reg Ripper SOFTWARE Variable**
### `File Name: RegRipper_SOFTWARE-Variable.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andreas Hunkeler (@Karneades)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
RegRipper: parse SOFTWARE hive using provided plugin name

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Reg Ripper SOFTWARE Variable to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Reg Ripper SOFTWARE Variable logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Reg Ripper SOFTWARE Variable timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'RegRipper: parse SOFTWARE hive using provided plugin name'
Category: Registry
Author: Andreas Hunkeler (@Karneades)
Version: 1.0
Id: c2e63e6f-4207-4bf4-b6af-d4a465009418
BinaryUrl: https://github.com/keydet89/RegRipper3.0/archive/master.zip
ExportFormat: txt
FileMask: SOFTWARE
Processors:
    -
        Executable: regripper\rip.exe
        CommandLine: -r %sourceFile% -p %softwarePlugin%
        ExportFormat: txt
        ExportFile: regripper-software-%softwarePlugin%.txt
        Append: true

# Documentation
# https://github.com/keydet89/RegRipper3.0
# Create a folder "regripper" within the "Modules\bin" KAPE folder
# Place "rip.exe", "p2x5124.dll" and the "plugins" folder into "Modules\bin\regripper"
# Provide a module variable using --mvars softwarePlugin:pluginname
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
