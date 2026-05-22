# ⚙️ **Windows System Info**
### `File Name: Windows_SystemInfo.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** piesecurity  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Gathers Basic System Information

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows System Info to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows System Info logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows System Info timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Gathers Basic System Information
Category: LiveResponse
Author: piesecurity
Version: 1.0
Id: e4263b9f-cc93-434a-b56f-d3d7cc205e4b
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\systeminfo.exe
        CommandLine: /FO CSV
        ExportFormat: csv
        ExportFile: SystemInfo.csv

# Documentation
# https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/systeminfo
# https://en.wikipedia.org/wiki/Systeminfo.exe
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
