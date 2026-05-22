# ⚙️ **Ccmruafinder Recently Used Apps**
### `File Name: CCMRUAFinder_RecentlyUsedApps.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Brian Maloney  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Extracts SCCM software metering RecentlyUsedApplication logs from OBJECTS.DATA files

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Ccmruafinder Recently Used Apps to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Ccmruafinder Recently Used Apps logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Ccmruafinder Recently Used Apps timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Extracts SCCM software metering RecentlyUsedApplication logs from OBJECTS.DATA files'
Category: ProgramExecution
Author: Brian Maloney
Version: 1.0
Id: 591b2715-f4eb-47bd-9a6c-249b8c22aba1
BinaryUrl: https://github.com/esecrpm/WMI_Forensics/raw/master/CCM_RUA_Finder.exe
ExportFormat: tsv
FileMask: OBJECTS.DATA
Processors:
    -
        Executable: CCM_RUA_Finder.exe
        CommandLine: -i %sourceFile% -o %destinationDirectory%\SCCM_RecentlyUsedApplication.tsv
        ExportFormat: tsv

# Documentation
# https://github.com/davidpany/WMI_Forensics/blob/master/CCM_RUA_Finder.py
# Uses David Pany's CCM_RUA_finder.py to extract SCCM software metering RecentlyUsedApplication logs from OBJECTS.DATA files.
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
