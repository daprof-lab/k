# 🎯 **Recent Folders**
### `File Name: RecentFolders.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Max Zabuty  
**Version:** 1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Recent Folders LNK files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Recent Folders to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Recent Folders events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Recent Folders storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Recent Folders LNK files
Author: Max Zabuty
Version: 1
Id: 103c8de7-3303-41ea-98d5-35ea1a3ae1ae
RecreateDirectories: true
Targets:
    -
        Name: LNK Files from Recent
        Category: File and Folder Usage
        Path: C:\Users\%user%\AppData\Roaming\Microsoft\Windows\Recent\
        Recursive: true
    -
        Name: LNK Files from Microsoft Office Recent
        Category: File and Folder Usage
        Path: C:\Users\%user%\AppData\Roaming\Microsoft\Office\Recent\
        Recursive: true

# Documentation
# https://www.cybertriage.com/artifact/windows-recents-folder-artifact/
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
