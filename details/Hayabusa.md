# ⚙️ **Hayabusa Event Parser**
### `File Name: Hayabusa.mkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Andrew Rathbun, Georg Lauenstein (sure[secure])  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Fast Event Log (EVTX) timeline generator applying Sigma detection rules to locate lateral movement.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Hayabusa Event Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Hayabusa Event Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Hayabusa Event Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Hayabusa a timeline generator for Windows event logs
Category: EventLogs
Author: Andrew Rathbun, Georg Lauenstein (sure[secure])
Version: 1.1
Id: 0976ccf9-b7f8-4e5d-9bf7-96ba3b051db8
BinaryUrl: https://github.com/Yamato-Security/hayabusa/releases
ExportFormat: csv
Processors:
    -
        Executable: hayabusa_EventStatistics.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: hayabusa_LiveResponse.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: hayabusa_LogonSummary.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation
# Create a folder "hayabusa" within the "Modules\bin" KAPE folder
# Place "zip archive" file into "Modules\bin\hayabusa" and unpack
# rename hayabusa-x.x.x.exe to hayabusa.exe
# You can delete all except: "config"; "rules" and the "hayabusa.exe"
# Update Rules with: hayabusa.exe update-rules
# Setup for European Time format. Check options for more: hayabusa.exe -h
```
---

[⬅️ Back to Threat Hunting, AV & Logs Modules](../threat_hunting_modules.md)
