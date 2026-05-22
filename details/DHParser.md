# ⚙️ **Dhparser**
### `File Name: DHParser.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Jordan Klepser  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Retrieve Defender DetectionHistory threat data into JSON

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Dhparser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Dhparser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Dhparser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Retrieve Defender DetectionHistory threat data into JSON
Category: Antivirus
Author: Jordan Klepser
Version: 1.1
Id: 0256a455-1248-4e30-8175-727679189ddd
BinaryUrl: https://github.com/jklepsercyber/defender-detectionhistory-parser/blob/main/dhparser.exe
ExportFormat: json
Processors:
    -
        Executable: dhparser.exe
        CommandLine: -rgf %sourceDirectory% -o %destinationDirectory%
        ExportFormat: json

# Documentation
# https://github.com/jklepsercyber/defender-detectionhistory-parser/blob/main/README.md
# https://www.sans.org/blog/uncovering-windows-defender-real-time-protection-history-with-dhparser/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
