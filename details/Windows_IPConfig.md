# ⚙️ **Windows Ipconfig**
### `File Name: Windows_IPConfig.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Mike Cary  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
IPConfig

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Ipconfig to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Ipconfig logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Ipconfig timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: IPConfig
Category: LiveResponse
Author: Mike Cary
Version: 1.0
Id: 5afdfd6b-5ebb-4545-9980-88e6f421e508
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\ipconfig.exe
        CommandLine: /all
        ExportFormat: txt
        ExportFile: ipconfig.txt

# Documentation
# https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/ipconfig
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
