# ⚙️ **Sys Internals Tcpvcon**
### `File Name: SysInternals_Tcpvcon.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andy Furnas  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
TCPView provides a more informative and conveniently presented subset of the Netstat program that ships with Windows.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Sys Internals Tcpvcon to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Sys Internals Tcpvcon logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Sys Internals Tcpvcon timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: TCPView provides a more informative and conveniently presented subset of the Netstat program that ships with Windows.
Category: LiveResponse
Author: Andy Furnas
Version: 1.0
Id: 528beed4-5703-454b-a4e8-879b8daecfd5
BinaryUrl: https://download.sysinternals.com/files/TCPView.zip
ExportFormat: csv
Processors:
    -
        Executable: Tcpvcon.exe
        CommandLine: -a -n -c -accepteula
        ExportFormat: csv
        ExportFile: tcpvcon.csv

# Documentation
# https://docs.microsoft.com/en-us/sysinternals/downloads/tcpview
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
