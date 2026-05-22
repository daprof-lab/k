# ⚙️ **Events Ripper Event File**
### `File Name: Events-Ripper_eventFile.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Brian Maloney  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Events-Ripper: Events File

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Events Ripper Event File to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Events Ripper Event File logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Events Ripper Event File timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Events-Ripper: Events File'
Category: EventLogs
Author: Brian Maloney
Version: 1.0
Id: c05546e4-0caa-487e-8a65-cc52116d9b8c
BinaryUrl: https://github.com/keydet89/Events-Ripper/archive/master.zip
ExportFormat: txt
FileMask: "*.evtx"
Processors:
    -
        Executable: Events-Ripper\wevtx.bat
        CommandLine: '%sourceFile% %destinationDirectory%\events.txt'
        ExportFormat: txt

# Documentation
# https://github.com/keydet89/Events-Ripper
# Create a folder "Events-Ripper" within the "Modules\bin" KAPE folder
# unpack "zip archive" file into "Modules\bin\Events-Ripper"
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
