# ⚙️ **Sepparser**
### `File Name: SEPparser.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Brian Maloney  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Symantec Logs

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Sepparser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Sepparser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Sepparser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Symantec Logs
Category: Antivirus
Author: Brian Maloney
Version: 1.1
Id: 073300a3-2d16-4bf5-b332-b038b571e95f
BinaryUrl: https://github.com/Beercow/SEPparser/raw/master/bin/SEPparser.exe
ExportFormat: csv
FileMask: ""
Processors:
    -
        Executable: SEPparser.exe
        CommandLine: -d  %sourceDirectory% -o %destinationDirectory% -k -l -hf -eb
        ExportFormat: csv

# Documentation
# https://github.com/Beercow/SEPparser
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
