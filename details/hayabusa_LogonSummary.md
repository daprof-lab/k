# ⚙️ **Hayabusa Logon Summary**
### `File Name: hayabusa_LogonSummary.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Georg Lauenstein (sure[secure])  
**Version:** 1.3
{% endhint %}

---

## 📖 **Forensic Description & Value**
Hayabusa a timeline generator for Windows event logs - Logon Summary

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Hayabusa Logon Summary to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Hayabusa Logon Summary logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Hayabusa Logon Summary timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Hayabusa a timeline generator for Windows event logs - Logon Summary
Category: EventLogs
Author: Georg Lauenstein (sure[secure])
Version: 1.3
Id: 2dd36453-d175-4b54-b98f-9cdf492859ce
BinaryUrl: https://github.com/Yamato-Security/hayabusa/releases
ExportFormat: csv
Processors:
    -
        Executable: hayabusa\hayabusa.exe
        CommandLine: logon-summary --live-analysis --UTC -o %destinationDirectory%\hayabusa_logon_summary.csv
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
