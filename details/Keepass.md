# 🎯 **Keepass**
### `File Name: Keepass.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Keepass

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Keepass to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Keepass events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Keepass storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Keepass
Author: Vito Alfano
Version: 1.0
Id: 7965e0a4-fc19-4b06-adc6-26d883449079
RecreateDirectories: true
Targets:
   -
      Name: Keepass User Config
      Category: Apps
      Path: C:\Users\%user%\AppData\Roaming\KeePass\
      FileMask: "*.xml"
      Comment: "Collecting Keepass User Configuration File"
   -
      Name: Keepass Config Xml
      Category: Apps
      Path: C:\Program Files\KeePass Password Safe*\
      FileMask: "*.xml"
      Comment: "Collecting Keepass Configuration File"
   -
      Name: Keepass Application Details
      Category: Apps
      Path: C:\Program Files\KeePass Password Safe*\
      FileMask: "*.config"
      Comment: "Collecting Keepass Application Details"

# Documentation
# http://fir.ferris.edu:8080/xmlui/bitstream/handle/2323/6381/Middleton2017E2.pdf?sequence=1&isAllowed=y
# https://cqureacademy.com/blog/hacks/safe-store-password-keepass-browser
# https://github.com/GhostPack/KeeThief
# https://github.com/Orange-Cyberdefense/KeePwn
# KeePass is a free open source password manager, which helps you to manage your passwords in a secure way. You can store all your passwords in one database, which is locked with a master key. So you only have to remember one single master key to unlock the whole database. Database files are encrypted using the best and most secure encryption algorithms currently known (AES-256, ChaCha20 and Twofish)
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
