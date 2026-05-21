# ⚙️ **EvtxECmd Event Parser**
### `File Name: EvtxECmd.mkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Extracts and parses EVTX logs into highly detailed structured CSV/JSON forensic timelines.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run EvtxECmd Event Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw EvtxECmd Event Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage EvtxECmd Event Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'EvtxECmd: process event log files'
Category: EventLogs
Author: Eric Zimmerman
Version: 1.0
Id: 1b66f0e2-2ccf-467d-ae15-a2b3dc59df08
BinaryUrl: https://download.ericzimmermanstools.com/EvtxECmd.zip
ExportFormat: csv
Processors:
    -
        Executable: EvtxECmd\EvtxECmd.exe
        CommandLine: -d %sourceDirectory% --csv %destinationDirectory%
        ExportFormat: csv
    -
        Executable: EvtxECmd\EvtxECmd.exe
        CommandLine: -d %sourceDirectory% --xml %destinationDirectory%
        ExportFormat: xml
    -
        Executable: EvtxECmd\EvtxECmd.exe
        CommandLine: -d %sourceDirectory% --json %destinationDirectory%
        ExportFormat: json

# Documentation
# https://github.com/EricZimmerman/evtx
# https://binaryforay.blogspot.com/2019/04/introducing-evtxecmd.html
# https://www.youtube.com/watch?v=YvMg3p7O6ro
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# https://leanpub.com/eztoolsmanuals
# Be sure to run evtxecmd.exe --sync within your .\KAPE\Modules\bin\EvtxECmd directory to ensure you have the latest maps!
# Alternatively, run the !!ToolSync Module to keep all your Maps, Batch Files, and Targets/Modules updated!
```
---

[⬅️ Back to Threat Hunting, AV & Logs Modules](../threat_hunting_modules.md)
