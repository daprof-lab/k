# 🎯 **Keepass XC**
### `File Name: KeepassXC.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
KeepassXC

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Keepass XC to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Keepass XC events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Keepass XC storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: KeepassXC
Author: Vito Alfano
Version: 1.0
Id: 314f0d04-f238-4058-aa7f-e470c7c28d9b
RecreateDirectories: true
Targets:
   -
      Name: Keepass Local Ini
      Category: Apps
      Path: C:\Users\%user%\AppData\Local\KeePassXC\
      FileMask: "*.ini"
   -
      Name: Keepass Roaming Ini
      Category: Apps
      Path: C:\Users\%user%\AppData\Roaming\KeePassXC\
      FileMask: "*.ini"

# Documentation
# https://keepassxc.org/project/
# KeePassXC is a free open source password manager, considered the best variant the well known KeePass.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
