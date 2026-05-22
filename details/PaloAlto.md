# 🎯 **Palo Alto**
### `File Name: PaloAlto.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Evangelos Dragonas  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Palo Alto Networks GlobalProtect VPN logs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Palo Alto to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Palo Alto events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Palo Alto storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Palo Alto Networks GlobalProtect VPN logs
Author: Evangelos Dragonas
Version: 1.0
Id: 69e25afa-05b2-4311-aa42-db2e20b6c07a
RecreateDirectories: true
Targets:
    -
        Name: Palo Alto GlobalProtect VPN
        Category: Apps
        Path: C:\Users\*\AppData\Local\Palo Alto Networks\GlobalProtect
        Recursive: true
        FileMask: 'PanGP*.log*'
        Comment: "Authentication, portal/gateway connection, and user-side events (login/logout attempts)"
    -
        Name: Palo Alto GlobalProtect VPN
        Category: Apps
        Path: C:\Program Files*\Palo Alto Networks\GlobalProtect
        Recursive: true
        FileMask: '*.log*'
        Comment: "Multiple logs like PanGPS.log that stores authentication, portal/gateway connection, and user-side events (login/logout attempts)"

# Documentation
# https://knowledgebase.paloaltonetworks.com/kcSArticleDetail?id=kA10g000000ClUk
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
