# 🎯 **Cisco Jabber**
### `File Name: CiscoJabber.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Bannon  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Jabber

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Cisco Jabber to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Cisco Jabber events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Cisco Jabber storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Jabber
Author: Andrew Bannon
Version: 1.0
Id: 69249cc7-2b04-47c4-8ba9-d8055fadc950
RecreateDirectories: true
Targets:
    -
        Name: Cisco Jabber Database
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Cisco\Unified Communications\Jabber\CSF\History\
        FileMask: '*.db'
        Comment: "The Cisco Jabber process needs to be killed before database can be copied."

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
