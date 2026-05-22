# ⚙️ **Backstage Parser**
### `File Name: BackstageParser.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Brian Maloney  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
BackstageParser

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Backstage Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Backstage Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Backstage Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: BackstageParser
Category: FileKnowledge
Author: Brian Maloney
Version: 1.0
Id: 5bc7c7b9-36c2-4eb9-8e1e-376962496765
BinaryUrl: https://github.com/Beercow/BackstageParser/releases/latest
ExportFormat: csv
Processors:
    -
        Executable: BackstageParser.exe
        CommandLine: -d %sourceDirectory%\C\Users\ -oc -o %destinationDirectory%\Backstage.csv
        ExportFormat: csv
    -
        Executable: BackstageParser.exe
        CommandLine: -d %sourceDirectory%\C\Users\ -oj -o %destinationDirectory%\Backstage.json
        ExportFormat: json

# Documentation
# https://github.com/ArsenalRecon/BackstageParser
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
