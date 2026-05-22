# ⚙️ **Wifipass View**
### `File Name: WIFIPassView.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
WIFIPassView - allows you to obtain the list of WIFI connected to the equipment and their stored passwords

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Wifipass View to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Wifipass View logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Wifipass View timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'WIFIPassView - allows you to obtain the list of WIFI connected to the equipment and their stored passwords'
Category: LiveResponse
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: 4c04b8f0-26b8-4342-b58a-06939fe48d5f
BinaryUrl: https://raw.githubusercontent.com/conexioninversa/Forensics/master/WIFIPassView.ps1
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -ep bypass -Command %kapedirectory%\Modules\bin\WIFIPassView.ps1 | Out-File -FilePath %destinationDirectory%\WIFIPassView.csv
        ExportFormat: csv

# Documentation
# This script allows you to obtain the list of WIFI connected to the equipment and their stored passwords.
# The result is written to the WIFIPassView.csv file
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
