# ⚙️ **Reg Ripper SAM**
### `File Name: RegRipper_SAM.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** ZeArioch <https://{github,twitter}.com/ZeArioch>, Phill Moore  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
RegRipper: parse SAM hive

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Reg Ripper SAM to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Reg Ripper SAM logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Reg Ripper SAM timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'RegRipper: parse SAM hive'
Category: Registry
Author: ZeArioch <https://{github,twitter}.com/ZeArioch>, Phill Moore
Version: 1.1
Id: 4b1babd2-c7e1-4f1f-a34f-1968d3672752
BinaryUrl: https://github.com/keydet89/RegRipper3.0/archive/master.zip
ExportFormat: txt
FileMask: SAM
Processors:
    -
        Executable: regripper\rip.exe
        CommandLine: -r %sourceFile% -f sam
        ExportFormat: txt
        ExportFile: regripper-sam.txt

# Documentation
# https://github.com/keydet89/RegRipper3.0
# Create a folder "regripper" within the "Modules\bin" KAPE folder
# Place "rip.exe", "p2x5124.dll" and the "plugins" folder into "Modules\bin\regripper"
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
