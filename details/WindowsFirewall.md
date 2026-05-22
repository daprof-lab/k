# 🎯 **Windows Firewall**
### `File Name: WindowsFirewall.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Mike Cary  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows Firewall Logs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Windows Firewall to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Windows Firewall events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Windows Firewall storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Windows Firewall Logs
Author: Mike Cary
Version: 1.0
Id: e1c2040e-c1b4-47ef-973f-73a54c5e87ca
RecreateDirectories: true
Targets:
    -
        Name: Windows Firewall Logs
        Category: WindowsFirewallLogs
        Path: C:\Windows\System32\LogFiles\Firewall\
        FileMask: pfirewall.*
    -
        Name: Windows Firewall Logs
        Category: WindowsFirewallLogs
        Path: C:\Windows.old\Windows\System32\LogFiles\Firewall\
        FileMask: pfirewall.*

# Documentation
# https://www.forensicfocus.com/articles/finding-and-interpreting-windows-firewall-rules/
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
