# ⚙️ **Thor Upgrade**
### `File Name: Thor_Upgrade.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Thor, an IOC and YARA scanner written in Golang - Upgrade

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Thor Upgrade to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Thor Upgrade logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Thor Upgrade timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Thor, an IOC and YARA scanner written in Golang - Upgrade
Category: IOCs
Author: Andrew Rathbun
Version: 1.0
Id: aaff8e82-a5c1-42e0-b3f0-1c35c6932e12
BinaryUrl: https://www.nextron-systems.com/thor/
ExportFormat: ""
Processors:
    -
        Executable: thor\thor-util.exe
        CommandLine: "upgrade --techpreview"
        ExportFormat: ""

# Documentation
# https://thor-manual.nextron-systems.com/en/latest/usage/beforeyoubegin.html?highlight=upgrade#upgrade-thor-and-update-the-signatures
# This Module is specifically for those with a Lab license, which is meant for running against mounted images, offline files, etc
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
