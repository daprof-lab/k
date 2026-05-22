# ⚙️ **Reg Ripper Ntuser**
### `File Name: RegRipper_NTUser.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** ZeArioch <https://{github,twitter}.com/ZeArioch>, Phill Moore  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
RegRipper: parse NTUSER hives

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Reg Ripper Ntuser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Reg Ripper Ntuser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Reg Ripper Ntuser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'RegRipper: parse NTUSER hives'
Category: Registry
Author: ZeArioch <https://{github,twitter}.com/ZeArioch>, Phill Moore
Version: 1.1
Id: ce3bf979-0d4d-4a31-8240-6be6f95610b7
BinaryUrl: https://github.com/keydet89/RegRipper3.0/archive/master.zip
ExportFormat: txt
FileMask: ntuser.dat
Processors:
    -
        Executable: regripper\rip.exe
        CommandLine: -r %sourceFile% -f ntuser
        ExportFormat: txt
        ExportFile: regripper-ntuser.txt

# Documentation
# https://github.com/keydet89/RegRipper3.0
# Create a folder "regripper" within the "Modules\bin" KAPE folder
# Place "rip.exe", "p2x5124.dll" and the "plugins" folder into "Modules\bin\regripper"
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
