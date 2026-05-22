# ⚙️ **Winlogbeat ALL**
### `File Name: Winlogbeat_ALL.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Thomas DIOT (Qazeer)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Winlogbeat - Parse all EVTX files (and all their events) to JSON.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Winlogbeat ALL to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Winlogbeat ALL logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Winlogbeat ALL timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Winlogbeat - Parse all EVTX files (and all their events) to JSON.
Category: EventLogs
Author: Thomas DIOT (Qazeer)
Version: 1.0
Id: a059c70b-2615-47ce-a45c-75a377eb4fc7
BinaryUrl: https://www.elastic.co/fr/downloads/beats/winlogbeat
ExportFormat: json
FileMask: "*.evtx"
Processors:
    -
        Executable: Winlogbeat\winlogbeat.exe
        CommandLine: -e -c "%kapeDirectory%\Modules\bin\Winlogbeat\Winlogbeat_Windows_single_EVTX_to_JSON.yml" -E EVTX_FILE=%sourceFile% -E OUTPUT_FOLDER="%destinationDirectory%"
        ExportFormat: json

# Documentation
# Uses Winlogbeat to parse EVTX to JSON: https://www.elastic.co/guide/en/beats/winlogbeat/current/index.html
# Parses EVTX file one by one, due to limitation in the way files can be specified to Winlogbeat
# The "Winlogbeat_Windows_single_EVTX_to_JSON.yml" configuration file can be retrieved from: https://gist.github.com/Qazeer/48e5895a958b32c223e6d0e92e2182ac
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
