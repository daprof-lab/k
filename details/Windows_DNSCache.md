# 🎯 **Windows DNS Cache Logs**
### `File Name: Windows_DNSCache.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Mike Cary  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Collects active system DNS lookup records, mapping queried domains to resolving IPs.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Windows DNS Cache Logs to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Windows DNS Cache Logs events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Windows DNS Cache Logs storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

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

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
