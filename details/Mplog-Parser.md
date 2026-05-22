# ⚙️ **Mplog Parser**
### `File Name: Mplog-Parser.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Thomas DIOT (Qazeer)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Mplog-Parser: parses Microsoft Protection log files into CSV files

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Mplog Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Mplog Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Mplog Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Mplog-Parser: parses Microsoft Protection log files into CSV files'
Category: Antivirus
Author: Thomas DIOT (Qazeer)
Version: 1.0
Id: 6084c8ab-2059-41a4-89f4-dba2cfdb4bb4
BinaryUrl: https://github.com/Qazeer/mplog_parser-compiled/releases/download/v1.0/mplog_parser.exe
ExportFormat: csv
Processors:
    -
        Executable: mplog_parser.exe
        CommandLine: -d "%SourceDirectory%\ProgramData\Microsoft\Windows Defender\Support" -o "%destinationDirectory%"
        ExportFormat: csv

# Documentation
# Mplog-Parser parses Microsoft Protection log files into a number of CSV files.
# mplog_parser source: https://github.com/Intrinsec/mplog_parser
# Compiled version: https://github.com/Qazeer/mplog_parser-compiled
# Information on Windows Defender MPLog:
# https://www.crowdstrike.com/blog/how-to-use-microsoft-protection-logging-for-forensic-investigations/
# https://www.intrinsec.com/hunt-mplogs/
# https://artefacts.help/windows_defender_support_logs.html
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
