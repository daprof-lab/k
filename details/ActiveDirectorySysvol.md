# 🎯 **Active Directory Sysvol**
### `File Name: ActiveDirectorySysvol.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Zawadi Done  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Active Directory Sysvol

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Active Directory Sysvol to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Active Directory Sysvol events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Active Directory Sysvol storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Active Directory Sysvol
Author: Zawadi Done
Version: 1.0
Id: fa98e781-d828-4076-9721-dfbfde4d7739
RecreateDirectories: true
Targets:
    -
        Name: SYSVOL
        Category: Active Directory
        Path: C:\Windows\SYSVOL
        Recursive: true

# Documentation
# https://www.thehacker.recipes/ad/movement/credentials/dumping/ntds
# https://www.minitool.com/lib/sysvol.html
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
