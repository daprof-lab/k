# 🎯 **Active Directory NTDS**
### `File Name: ActiveDirectoryNTDS.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Zawadi Done  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Active Directory NTDS

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Active Directory NTDS to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Active Directory NTDS events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Active Directory NTDS storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Active Directory NTDS
Author: Zawadi Done
Version: 1.1
Id: 18335b99-64bb-4888-8c24-c895b6cd239d
RecreateDirectories: true
Targets:
    -
        Name: NTDS
        Category: Active Directory
        Path: C:\Windows\NTDS
        Recursive: true

# Documentation
# https://www.thehacker.recipes/ad/movement/credentials/dumping/ntds
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
