# ⚙️ **Reg Ripper Ntuser Variable**
### `File Name: RegRipper_NTUser-Variable.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andreas Hunkeler (@Karneades)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
RegRipper: parse NTUSER hives using provided plugin name

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Reg Ripper Ntuser Variable to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Reg Ripper Ntuser Variable logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Reg Ripper Ntuser Variable timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'RegRipper: parse NTUSER hives using provided plugin name'
Category: Registry
Author: Andreas Hunkeler (@Karneades)
Version: 1.0
Id: b1c7a758-664a-459d-82d5-3165772f21fc
BinaryUrl: https://github.com/keydet89/RegRipper3.0/archive/master.zip
ExportFormat: txt
FileMask: ntuser.dat
Processors:
    -
        Executable: regripper\rip.exe
        CommandLine: -r %sourceFile% -p %ntuserPlugin%
        ExportFormat: txt
        ExportFile: regripper-ntuser-%ntuserPlugin%.txt
        Append: true

# Documentation
# https://github.com/keydet89/RegRipper3.0
# Create a folder "regripper" within the "Modules\bin" KAPE folder
# Place "rip.exe", "p2x5124.dll" and the "plugins" folder into "Modules\bin\regripper"
# Provide a module variable called ntuserPlugin using --mvars
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
