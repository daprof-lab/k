# 🎯 **Directory Traversal Wild Card Example**
### `File Name: DirectoryTraversal_WildCardExample.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Find zip archives

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Directory Traversal Wild Card Example to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Directory Traversal Wild Card Example events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Directory Traversal Wild Card Example storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Find zip archives
Author: Eric Zimmerman
Version: 1.0
Id: 9878f1fc-5e22-46a0-8cfd-c921ac9c4b13
RecreateDirectories: true
Targets:
    -
        Name: Zips
        Category: Archives
        Path: C:\
        # Values starting with * need to be enclosed in single quotes because * denotes a reference in yaml
        # You can also do regex:<regex pattern> if more control is needed. i.e. FileMask: regex:(2019|DSC|Log).+\.(jpg|txt)
        FileMask: '*.zip'
        Recursive: true
        Comment: This is an example of how to walk a drive for a file mask. Probably do not want to use this one as is
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
