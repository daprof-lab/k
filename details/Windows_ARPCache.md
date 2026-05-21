# 🎯 **Windows ARP Cache Logs**
### `File Name: Windows_ARPCache.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Mike Cary  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Pulls local Address Resolution Protocol (ARP) tables linking local IPs to MAC addresses.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Windows ARP Cache Logs to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Windows ARP Cache Logs events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Windows ARP Cache Logs storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

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

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
