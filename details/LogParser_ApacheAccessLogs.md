# ⚙️ **Apache Log Parser**
### `File Name: LogParser_ApacheAccessLogs.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Hadar Yudovich  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Parses Apache server access and error logs to identify malicious web scans and queries.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Apache Log Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Apache Log Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Apache Log Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: LogParser Apache Access Log
Category: Webservers
Author: Hadar Yudovich
Version: 1.0
Id: 631ac549-9ddf-48ea-b95b-ca4678230df6
BinaryUrl: https://www.microsoft.com/en-us/download/confirmation.aspx?id=24659
ExportFormat: csv
FileMask: access.log
Processors:
    -
        Executable: LogParser.exe
        CommandLine: -i:ncsa -o:csv "select * into '%destinationDirectory%\access_log.csv' from '%sourceDirectory%\access.log'"
        ExportFormat: csv

# Documentation
# https://www.microsoft.com/en-us/download/details.aspx?id=24659
# https://www.stevebunting.org/udpd4n6/forensics/logparser.htm
# Uses Microsoft Log Parser
# Point msource (Module Source) to the Apache logs folder
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
