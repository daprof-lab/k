# ⚙️ **Reg Ripper Usr Class**
### `File Name: RegRipper_UsrClass.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andreas Hunkeler (@Karneades)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
RegRipper: parse UsrClass hives

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Reg Ripper Usr Class to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Reg Ripper Usr Class logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Reg Ripper Usr Class timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'RegRipper: parse UsrClass hives'
Category: Registry
Author: Andreas Hunkeler (@Karneades)
Version: 1.0
Id: 253acccb-86c0-49dd-9b6d-b9c228a49a55
BinaryUrl: https://github.com/keydet89/RegRipper3.0/archive/master.zip
ExportFormat: txt
FileMask: UsrClass.dat
Processors:
    -
        Executable: regripper\rip.exe
        CommandLine: -r %sourceFile% -f UsrClass
        ExportFormat: txt
        ExportFile: regripper-usrclass.txt

# Documentation
# https://github.com/keydet89/RegRipper3.0
# Create a folder "regripper" within the "Modules\bin" KAPE folder
# Place "rip.exe", "p2x5124.dll" and the "plugins" folder into "Modules\bin\regripper"
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
