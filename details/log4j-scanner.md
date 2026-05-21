# ⚙️ **Log4j Vulnerability Scanner**
### `File Name: log4j-scanner.mkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Georg Lauenstein  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Checks local storage for vulnerable Log4j libraries, helping secure internal systems.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Log4j Vulnerability Scanner to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Log4j Vulnerability Scanner logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Log4j Vulnerability Scanner timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Vulnerability scanner and mitigation patch for Log4j2 CVE-2021-44228
Category: LiveResponse
Author: Georg Lauenstein
Version: 1.0
Id: 625db471-45bd-4b3b-a60f-97a376168a94
BinaryUrl: https://github.com/logpresso/CVE-2021-44228-Scanner
ExportFormat: csv
Processors:
    -
        Executable: log4j2-scan.exe
        CommandLine: "--all-drives --scan-log4j1 --scan-logback --report-dir %destinationDirectory%"
        ExportFormat: csv

# Documentation
# Check GitHub for additional options during scan
```
---

[⬅️ Back to Threat Hunting, AV & Logs Modules](../threat_hunting_modules.md)
