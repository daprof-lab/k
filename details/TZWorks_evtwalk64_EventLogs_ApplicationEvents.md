# ⚙️ **Tzworks Evtwalk64 Event Logs Application Events**
### `File Name: TZWorks_evtwalk64_EventLogs_ApplicationEvents.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Justin Price  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Parses Application event log using TZWorks evtwalk64

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Evtwalk64 Event Logs Application Events to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Evtwalk64 Event Logs Application Events logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Evtwalk64 Event Logs Application Events timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parses Application event log using TZWorks evtwalk64
Category: ProgramExecution
Author: Justin Price
Version: 1.0
Id: 64cda4d2-8fa0-4948-a994-6b60bc1a50b7
BinaryUrl: https://tzworks.net/download_links.php
ExportFormat: csv
FileMask: Application.evtx
Processors:
    -
        Executable: evtwalk64.exe
        CommandLine: -log %sourceFile% -pair_datetime -csv -no_whitespace
        ExportFormat: csv
        ExportFile: application_event_log.csv

# Documentation
# https://tzworks.net/prototype_page.php?proto_id=25
# This is an example of how to use a tool that cant write out to a destination file. It is not recommended to use evtwalk since it will silently drop logs it doesnt know how to deal with as of testing in August 2019
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
