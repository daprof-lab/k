# ⚙️ **Windows Dnscache**
### `File Name: Windows_DNSCache.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Mike Cary  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
DNSCache

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Dnscache to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Dnscache logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Dnscache timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: DNSCache
Category: LiveResponse
Author: Mike Cary
Version: 1.0
Id: b5df17b0-29d2-448f-bdaa-ec221bee29b6
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\ipconfig.exe
        CommandLine: /DISPLAYDNS
        ExportFormat: txt
        ExportFile: dns_cache.txt

# Documentation
# https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/ipconfig
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
