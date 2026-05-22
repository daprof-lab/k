# ⚙️ **Forensic Timeliner**
### `File Name: ForensicTimeliner.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Reece394  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Forensic Timeliner: Quickly consolidate CSV output from top-tier triage tools into a unified mini timeline

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Forensic Timeliner to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Forensic Timeliner logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Forensic Timeliner timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Forensic Timeliner: Quickly consolidate CSV output from top-tier triage tools into a unified mini timeline'
Category: ForensicTimeliner
Author: Reece394
Version: 1.0
Id: eea7a5c5-d0ed-4c56-88d7-0c2230104b4f
BinaryUrl: https://github.com/acquiredsecurity/forensic-timeliner/releases/download/v2.2/ForensicTimeliner2.2.zip
ExportFormat: csv
Processors:
    -
        Executable: ForensicTimeliner\ForensicTimeliner.exe
        CommandLine: --BaseDir %destinationDirectory%\.. --ALL --OutputFile %destinationDirectory%\ForensicTimeliner.csv --EnableTagger --NoBanner --NoPrompt
        ExportFormat: csv
    -
        Executable: ForensicTimeliner\ForensicTimeliner.exe
        CommandLine: --BaseDir %destinationDirectory%\.. --ALL --OutputFile %destinationDirectory%\ForensicTimeliner.json --ExportFormat jsonl --NoBanner --NoPrompt
        ExportFormat: json

# Documentation
# https://github.com/acquiredsecurity/forensic-timeliner
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
