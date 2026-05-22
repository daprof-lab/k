# ⚙️ **Tzworks CAFAE Registry System**
### `File Name: TZWorks_CAFAE_Registry_System.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Scott Downie  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
CAFAE: extract registry information

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks CAFAE Registry System to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks CAFAE Registry System logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks CAFAE Registry System timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'CAFAE: extract registry information'
Category: Registry
Author: Scott Downie
Version: 1.0
Id: 5405e8ff-e40f-407c-9c73-224b09ef57ba
BinaryUrl: https://tzworks.net/download_links.php
ExportFormat: txt
FileMask: SYSTEM
Processors:
    -
        Executable: cafae64.exe
        CommandLine: -hive %sourceFile% -csv -devices -no_regkey_hdr
        ExportFormat: txt
        ExportFile: devices.txt

# Documentation
# https://tzworks.net/prototype_page.php?proto_id=19
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
