# ⚙️ **Loki Live Response**
### `File Name: Loki_LiveResponse.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Georg Lauenstein  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Loki - Simple IOC and Incident Response Scanner - Live Response

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Loki Live Response to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Loki Live Response logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Loki Live Response timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Loki - Simple IOC and Incident Response Scanner - Live Response
Category: LiveResponse
Author: Georg Lauenstein
Version: 1.0
Id: e93f1052-4d8f-4b63-b680-2af845e95a98
BinaryUrl: https://github.com/Neo23x0/Loki/releases/download/v0.44.2/loki_0.44.2.zip
ExportFormat: log
Processors:
    -
        Executable: Loki\loki.exe
        CommandLine: "-p %sourceDirectory% --logfolder %destinationDirectory% --debug"
        ExportFormat: log

# Documentation
# HOW TO PLACE THE BINARY
# 1. Download loki using the link above. It's a free tool
# 2. Unzip loki.zip into '<KAPE_working_directory>/Modules'
# 3. Update the yara signatures -> 'loki.exe --update'
# 4. KAPE should now be able to find the executable in '<KAPE_working_directory>/Modules/bin/loki/loki.exe'
# 5. Use 'loki.exe --help' for options
# 6. More info here: https://www.nextron-systems.com/loki/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
