# ⚙️ **Mmdbcmd**
### `File Name: MMDBCmd.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Nisarg Suthar  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
MMDBCmd

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Mmdbcmd to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Mmdbcmd logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Mmdbcmd timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: MMDBCmd
Category: Databases
Author: Nisarg Suthar
Version: 1.0
Id: fe7483e7-725b-4b90-bd41-cd3d3630b91d
BinaryUrl: https://github.com/nisargsuthar/MMDBCmd/releases/download/v1.1/MMDBCmd.exe
ExportFormat: csv
FileMask: "*.mmdb"
Processors:
    -
        Executable: MMDBCmd.exe
        CommandLine: "-d %sourceDirectory% --csv %destinationDirectory%"
        ExportFormat: csv

# Documentation
# https://github.com/ovimihai/MaxMind-python-mmdb-to-csv-converter/tree/main
# https://maxmind.github.io/MaxMind-DB/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
