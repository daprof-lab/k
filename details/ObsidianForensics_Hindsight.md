# ⚙️ **Obsidian Forensics Hindsight**
### `File Name: ObsidianForensics_Hindsight.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Mike Cary  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
Hindsight - Chrome browser parsing

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Obsidian Forensics Hindsight to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Obsidian Forensics Hindsight logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Obsidian Forensics Hindsight timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Hindsight - Chrome browser parsing'
Category: WebBrowsers
Author: Mike Cary
Version: 1.2
Id: d9661ea6-3369-41d0-8807-904f00edcbf4
BinaryUrl: https://github.com/obsidianforensics/hindsight/releases
ExportFormat: xlsx
Processors:
    -
        Executable: hindsight.exe
        CommandLine: -i %sourceDirectory% -o %destinationDirectory%\Hindsight_output -f xlsx
        ExportFormat: xlsx
    -
        Executable: hindsight.exe
        CommandLine: -i %sourceDirectory% -o %destinationDirectory%\Hindsight_output -f jsonl
        ExportFormat: json

# Documentation
# Hindsight - Internet history forensics for Google Chrome/Chromium
# https://github.com/obsidianforensics/hindsight/releases
# Use version 2.3 or later to enable parsing of all profiles
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
