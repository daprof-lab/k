# ⚙️ **Windows Arpcache**
### `File Name: Windows_ARPCache.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Mike Cary  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
ARPCache

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Arpcache to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Arpcache logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Arpcache timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: ARPCache
Category: LiveResponse
Author: Mike Cary
Version: 1.0
Id: 6d4ea3be-f634-4809-b7d8-db0d22800737
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\arp.exe
        CommandLine: -a
        ExportFormat: txt
        ExportFile: arp_cache.txt

# Documentation
# https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/arp
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
