# ⚙️ **Block Parser Zipped**
### `File Name: block-parser-zipped.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Phill Moore, Reece394  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Block Parser Zipped

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Block Parser Zipped to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Block Parser Zipped logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Block Parser Zipped timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Block Parser Zipped
Category: EventLogs
Author: Phill Moore, Reece394
Version: 1.1
Id: cb817a29-bab0-4051-ac7d-7019d6e2ac65
BinaryUrl: https://github.com/randomaccess3/block-parser
FileMask: "Microsoft-Windows-PowerShell%4Operational.evtx"
ExportFormat: zip
Processors:
    -
        Executable: block-parser.exe
        CommandLine: -o %destinationDirectory% -z %sourceFile%
        ExportFormat: zip

# Documentation
# https://www.fireeye.com/blog/threat-research/2016/02/greater_visibilityt.html
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
