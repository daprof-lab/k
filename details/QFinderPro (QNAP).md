# 🎯 **Qfinder Pro (QNAP)**
### `File Name: QFinderPro (QNAP).tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
QFinderPro (QNAP)

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Qfinder Pro (QNAP) to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Qfinder Pro (QNAP) events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Qfinder Pro (QNAP) storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: QFinderPro (QNAP)
Author: Andrew Rathbun
Version: 1.0
Id: 7323637e-de45-47c4-8f2f-6b11a4f82919
RecreateDirectories: true
Targets:
    -
        Name: QFinderPro
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\QNAP\QfinderPro
        Comment: "Locates a JSON file that provides network location information for any QNAP connected devices."

# Documentation
# QFinderPro is the GUI Windows application used to manage a QNAP device outside of the NAS itself.
# A .json file resides in the above location which will lay out the following: Firmware Version, IP Address, MAC Address, Device Model, Name of Device, and Timestamp (likely date of last firmware update).
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
