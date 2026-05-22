# 🎯 **Capability Access Manager**
### `File Name: CapabilityAccessManager.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** qmadev  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Capability Access Manager database

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Capability Access Manager to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Capability Access Manager events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Capability Access Manager storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Capability Access Manager database
Author: qmadev
Version: 1.0
Id: a1d82b93-47ac-49bb-89f2-35543c47c550
RecreateDirectories: true
Targets:
    -
        Name: Capability Access Manager database
        Category: Apps
        Path: C:\ProgramData\Microsoft\Windows\CapabilityAccessManager\
        FileMask: CapabilityAccessManager.db

# Documentation
# http://medium.com/@cyber.sundae.dfir/capability-access-manager-forensics-in-windows-11-f586ef8aac79
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
