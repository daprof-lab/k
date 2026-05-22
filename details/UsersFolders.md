# 🎯 **Users Folders**
### `File Name: UsersFolders.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Users folders Dump

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Users Folders to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Users Folders events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Users Folders storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Users folders Dump
Author: Vito Alfano
Version: 1.0
Id: 0eb51e6a-1286-42fe-bfdc-401356003395
RecreateDirectories: true
Targets:
    -
        Name: Users
        Category: Application
        Path: C:\Users\%user%\
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
