# ⚙️ **Zircolite Update**
### `File Name: Zircolite_Update.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
zircolite - Update Zircolite rules

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Zircolite Update to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Zircolite Update logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Zircolite Update timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: zircolite - Update Zircolite rules
Category: EventLogs
Author: Andrew Rathbun
Version: 1.0
Id: 19461b7a-a558-4662-93e6-63e6a126dca9
BinaryUrl: https://github.com/wagga40/Zircolite/releases/download/2.9.7/zircolite_win10_x64_2.9.7.7z
ExportFormat: json
Processors:
    -
        Executable: zircolite\zircolite_win10.exe
        CommandLine: -U
        ExportFormat: json

# Documentation
# https://github.com/wagga40/Zircolite/tree/master/docs
# See Zircolite_Scan Module for more installation instructions
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
