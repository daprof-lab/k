# ⚙️ **Evtx Hussar**
### `File Name: EvtxHussar.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
EvtxHussar

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Evtx Hussar to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Evtx Hussar logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Evtx Hussar timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: EvtxHussar
Category: EventLogs
Author: Andrew Rathbun
Version: 1.0
Id: baeb5700-a62f-4b8f-b47a-3a9c8545cbe3
BinaryUrl: https://github.com/yarox24/EvtxHussar/releases
ExportFormat: csv
Processors:
    -
        Executable: EvtxHussar\EvtxHussar.exe
        CommandLine: -r %sourceDirectory% -f CSV -o %destinationDirectory% -d
        ExportFormat: csv
    -
        Executable: EvtxHussar\EvtxHussar.exe
        CommandLine: -r %sourceDirectory% -f JSON -o %destinationDirectory% -d
        ExportFormat: json

# Documentation
# https://github.com/yarox24/EvtxHussar
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
