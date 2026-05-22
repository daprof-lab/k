# 🎯 **Windows Server Dnsand DHCP**
### `File Name: WindowsServerDNSAndDHCP.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Zawadi Done  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows Server DNS and DHCP log files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Windows Server Dnsand DHCP to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Windows Server Dnsand DHCP events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Windows Server Dnsand DHCP storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Windows Server DNS and DHCP log files
Author: Zawadi Done
Version: 1.1
Id: 2f6dc2b4-cbdf-4a11-807d-da2f885daafd
RecreateDirectories: true
Targets:
    -
        Name: DNS Netlogon files
        Category: DNS
        Path: C:\Windows\System32\config\
        FileMask: 'netlogon.*'
        Recursive: true
    -
        Name: DNS files
        Category: DNS
        Path: C:\Windows\System32\dns\
        Recursive: true
    -
        Name: DHCP files
        Category: DHCP
        Path: C:\Windows\System32\dhcp
        Recursive: true

# Documentation
# https://windowstechno.com/what-is-netlogon/
# https://learn.microsoft.com/en-us/troubleshoot/windows-server/networking/verify-srv-dns-records-have-been-created
# https://www.oreilly.com/library/view/windows-server-2008/9780735624375/ch19s06.html
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
