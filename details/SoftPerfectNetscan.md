# 🎯 **Soft Perfect Netscan**
### `File Name: SoftPerfectNetscan.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** CERT CWATCH - ALMOND  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Soft Perfect Network Scanner Output

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Soft Perfect Netscan to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Soft Perfect Netscan events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Soft Perfect Netscan storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Soft Perfect Network Scanner Output
Author: CERT CWATCH - ALMOND
Version: 1.0
Id: 0b5e2e0e-c5d7-4fa8-8ae7-6a257291bb57
RecreateDirectories: true
Targets:
    -
        Name: Netscan XML default output
        Category: Apps
        Path: C:\
        FileMask: 'netscan.xml'
        Recursive: true

# Documentation
# SoftPerfect Network Scanner 'Netscan' is a lightweight scanning tool commonly leveraged by threat actors.
# By default, it creates an XML file named 'netscan.xml'.
# This file stores credentials in use and a cache of previously scanned machines.
# Retrieving this file from compromised systems can provide a quick advantage during incident response by swiftly identifying the affected scope.
# https://almond.eu/wp-content/uploads/Almond-x-Amossys-8Base.pdf
# https://www.softperfect.com/products/networkscanner/
# https://www.protect.airbus.com/blog/uncovering-cyber-intruders-netscan/
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
