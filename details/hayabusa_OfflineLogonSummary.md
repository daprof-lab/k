# ⚙️ **Hayabusa Offline Logon Summary**
### `File Name: hayabusa_OfflineLogonSummary.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Georg Lauenstein (sure[secure]) & angry-bender  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Hayabusa a timeline generator for Windows event logs - Offline Logon Summary

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Hayabusa Offline Logon Summary to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Hayabusa Offline Logon Summary logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Hayabusa Offline Logon Summary timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Hayabusa a timeline generator for Windows event logs - Offline Logon Summary
Category: EventLogs
Author: Georg Lauenstein (sure[secure]) & angry-bender
Version: 1.1
Id: 05e743ea-8149-4adf-8979-73b957a3139e
BinaryUrl: https://github.com/Yamato-Security/hayabusa/releases
ExportFormat: csv
Processors:
    -
        Executable: hayabusa\hayabusa.exe
        CommandLine: logon-summary -d %sourceDirectory% --UTC -o %destinationDirectory%\hayabusa_logon_summary_offline.csv
        ExportFormat: csv

# Documentation
# Create a folder "hayabusa" within the "Modules\bin" KAPE folder
# Place "zip archive" file into "Modules\bin\hayabusa" and unpack
# rename the hayabusa executable to hayabusa.exe
# You can delete all except: "config"; "rules" and the "hayabusa.exe"
# For more options use: hayabusa.exe help
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
