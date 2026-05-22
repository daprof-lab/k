# ⚙️ **Events Ripper**
### `File Name: Events-Ripper.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Brian Maloney  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Events-Ripper: parse all supported events

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Events Ripper to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Events Ripper logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Events Ripper timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Events-Ripper: parse all supported events'
Category: EventLogs
Author: Brian Maloney
Version: 1.0
Id: 710ebfee-8703-4e9c-8d60-40970f180264
BinaryUrl: https://github.com/keydet89/Events-Ripper/archive/master.zip
ExportFormat: txt
Processors:
    -
        Executable: Events-Ripper_eventFile.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Events-Ripper_All.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation
# https://github.com/keydet89/Events-Ripper
# Create a folder "Events-Ripper" within the "Modules\bin" KAPE folder
# unpack "zip archive" file into "Modules\bin\Events-Ripper"
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
