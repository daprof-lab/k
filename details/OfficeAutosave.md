# 🎯 **Office Autosave**
### `File Name: OfficeAutosave.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Russ Taylor  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Office Autosave

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Office Autosave to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Office Autosave events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Office Autosave storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Office Autosave
Author: Russ Taylor
Version: 1.0
Id: 71f1efe7-37be-4285-9896-11f0f6be2770
RecreateDirectories: true
Targets:
    -
        Name: Word Autosave Location
        Category: FileKnowledge
        Path: C:\Users\%user%\AppData\Roaming\Microsoft\Word\
        Recursive: true
    -
        Name: Excel Autosave Location
        Category: ApplicationCompatibility
        Path: C:\Users\%user%\AppData\Roaming\Microsoft\Excel\
        Recursive: true
    -
        Name: Powerpoint Autosave Location
        Category: FileKnowledge
        Path: C:\Users\%user%\AppData\Roaming\Microsoft\Powerpoint\
        Recursive: true
    -
        Name: Publisher Autosave Location
        Category: FileKnowledge
        Path: C:\Users\%user%\AppData\Roaming\Microsoft\Publisher\
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
