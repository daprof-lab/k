# 🎯 **Windows Routing Tables**
### `File Name: Windows_RoutingTable.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Mike Cary  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Gathers the local OS networking routing table, identifying active default gateways.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Windows Routing Tables to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Windows Routing Tables events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Windows Routing Tables storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: RoutingTable
Category: LiveResponse
Author: Mike Cary
Version: 1.0
Id: 8aaad838-be9e-43d4-8643-145ceaa4208b
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\route.exe
        CommandLine: print
        ExportFormat: txt
        ExportFile: routing_table.txt

# Documentation
# https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/route_ws2008
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
