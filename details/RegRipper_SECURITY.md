# ⚙️ **Reg Ripper SECURITY**
### `File Name: RegRipper_SECURITY.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** ZeArioch <https://{github,twitter}.com/ZeArioch>, Phill Moore  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
RegRipper: parse SECURITY hive

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Reg Ripper SECURITY to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Reg Ripper SECURITY logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Reg Ripper SECURITY timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'RegRipper: parse SECURITY hive'
Category: Registry
Author: ZeArioch <https://{github,twitter}.com/ZeArioch>, Phill Moore
Version: 1.1
Id: a0011605-10ac-4e7b-b422-8d1afeebfd5c
BinaryUrl: https://github.com/keydet89/RegRipper3.0/archive/master.zip
ExportFormat: txt
FileMask: SECURITY
Processors:
    -
        Executable: regripper\rip.exe
        CommandLine: -r %sourceFile% -f security
        ExportFormat: txt
        ExportFile: regripper-security.txt

# Documentation
# https://github.com/keydet89/RegRipper3.0
# Create a folder "regripper" within the "Modules\bin" KAPE folder
# Place "rip.exe", "p2x5124.dll" and the "plugins" folder into "Modules\bin\regripper"
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
