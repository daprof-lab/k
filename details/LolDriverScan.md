# ⚙️ **Lol Driver Scan**
### `File Name: LolDriverScan.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Tool to LolDriverScan is a GoLang tool that allows users to discover vulnerable drivers on their system. This tool fetches the loldrivers.io list from their APIs and scans the system for any vulnerable drivers This project is implemented in Go and does not require elevated privileges to run

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Lol Driver Scan to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Lol Driver Scan logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Lol Driver Scan timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Tool to LolDriverScan is a GoLang tool that allows users to discover vulnerable drivers on their system. This tool fetches the loldrivers.io list from their APIs and scans the system for any vulnerable drivers This project is implemented in Go and does not require elevated privileges to run
Category: GitHub
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: 3bbc7869-7eba-4b43-8bbe-9721f0034191
BinaryUrl: https://github.com/FourCoreLabs/LolDriverScan/releases/tag/v1.2
ExportFormat: json
Processors:
    -
        Executable: loldriverscan.exe
        CommandLine: -json %destinationDirectory%\loldriverscan_Results.json
        ExportFormat: json

# Documentation
# https://github.com/conexioninversa/LolDriverScan
# Scans the system for vulnerable drivers
# Provides verbose output for detailed information
# Supports JSON output for easy integration with other tools
# No elevated privileges are required
# If it does not find vulnerable drivers it will not store logs
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
