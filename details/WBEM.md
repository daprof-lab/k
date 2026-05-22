# 🎯 **WBEM**
### `File Name: WBEM.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Mark Hallman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Web-Based Enterprise Management (WBEM)

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from WBEM to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate WBEM events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit WBEM storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Web-Based Enterprise Management (WBEM)
Author: Mark Hallman
Version: 1.0
Id: e985f5e3-f951-4e13-8099-a2a6877355cb
RecreateDirectories: true
Targets:
    -
        Name: WBEM
        Category: WBEM
        Path: C:\Windows\System32\wbem\Repository\
        Recursive: true
    -
        Name: WBEM
        Category: WBEM
        Path: C:\Windows.old\Windows\System32\wbem\Repository\
        Recursive: true

# Documentation
# https://www.jaiminton.com/cheatsheet/DFIR/
# https://www.sans.org/blog/investigating-wmi-attacks
# https://www.fireeye.com/blog/threat-research/2016/12/do_you_see_what_icc.html
# https://cyberforensicator.com/2019/07/13/using-mitre-attck-for-forensics-wmi-event-subscription-t1084/
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
