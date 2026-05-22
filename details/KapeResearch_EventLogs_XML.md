# ⚙️ **Kape Research Event Logs XML**
### `File Name: KapeResearch_EventLogs_XML.mkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
EvtxECmd: Convert Windows Event Log files (.evtx) to XML for research

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Kape Research Event Logs XML to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Kape Research Event Logs XML logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Kape Research Event Logs XML timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'EvtxECmd: Convert Windows Event Log files (.evtx) to XML for research'
Category: KapeResearch
Author: Andrew Rathbun
Version: 1.0
Id: 09b93d8e-c417-4e79-aaef-a2af3f46fd08
BinaryUrl: https://f001.backblazeb2.com/file/EricZimmermanTools/EvtxExplorer.zip
ExportFormat: xml
Processors:
    -
        Executable: EvtxECmd\EvtxECmd.exe
        CommandLine: -d %sourceDirectory% --xml %destinationDirectory%
        ExportFormat: xml

# Documentation
# https://github.com/EricZimmerman/evtx
# https://binaryforay.blogspot.com/2019/04/introducing-evtxecmd.html
# https://www.youtube.com/watch?v=YvMg3p7O6ro
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# Be sure to run evtxecmd.exe --sync within your .\KAPE\Modules\bin\EvtxECmd directory to ensure you have the latest maps!
# This Module will convert any Event Logs into XML, which is helpful for viewing all of the data stored within the various Event Logs on a system
```
---

[⬅️ Back to Threat Hunting, AV & Logs Modules](../threat_hunting_modules.md)
