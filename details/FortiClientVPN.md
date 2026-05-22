# 🎯 **Forti Client VPN**
### `File Name: FortiClientVPN.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Paul CABON - CERT Cwatch Almond  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Forti Client VPN

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Forti Client VPN to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Forti Client VPN events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Forti Client VPN storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Forti Client VPN
Author: Paul CABON - CERT Cwatch Almond
Version: 1.0
Id: 3364b046-fd5e-4da9-9bae-b7ea9583e4b4
RecreateDirectories: true
Targets:
    -
        Name: FortiClient trace logs in AppData
        Category: Apps
        Path: C:\Users\*\AppData\Local\FortiClient\logs\trace
        Recursive: true
        FileMask: '*'
        Comment: "Trace Logs for Forti Client VPN"
    -
        Name: FortiClient trace logs in Program Files
        Category: Apps
        Path: C:\Program Files\Fortinet\FortiClient\logs\trace
        Recursive: true
        FileMask: '*'
        Comment: "Trace Logs for Forti Client VPN"


# Documentation
# https://community.fortinet.com/t5/FortiClient/Troubleshooting-Tip-Collecting-logs-for-addressing-VPN/ta-p/362101
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
