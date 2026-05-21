# ⚙️ **LogParser Compound Module**
### `File Name: LogParser.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Orchestrates LogParser scripts to analyze IIS, RDP, and system logs concurrently.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run LogParser Compound Module to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw LogParser Compound Module logs to index file anomalies.
* **Incident Impact Assessment**: Leverage LogParser Compound Module timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: LogParser Compound Module
Category: Modules
Author: Andrew Rathbun
Version: 1.0
Id: 60643e70-1f3d-4aa6-a08a-c907f69faaa5
BinaryUrl: https://www.microsoft.com/en-us/download/confirmation.aspx?id=24659
ExportFormat: csv
Processors:
    -
        Executable: LogParser_ApacheAccessLogs.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: LogParser_DetailedNetworkShareAccess.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: LogParser_LogonLogoffEvents.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: LogParser_RDPUsageEvents.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: LogParser_SMBServerAnonymousLogons.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation
# N/A
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
