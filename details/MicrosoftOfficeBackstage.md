# 🎯 **Microsoft Office Backstage**
### `File Name: MicrosoftOfficeBackstage.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Brian Maloney  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Microsoft Office Backstage

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Microsoft Office Backstage to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Microsoft Office Backstage events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Microsoft Office Backstage storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Microsoft Office Backstage
Author: Brian Maloney
Version: 1.0
Id: 43e3486e-1a21-4f8f-a493-499d6fdc9eb7
RecreateDirectories: true
Targets:
    -
        Name: Microsoft Office Backstage
        Category: FileKnowledge
        Path: C:\Users\%user%\AppData\Local\Microsoft\Office\*\BackstageinAppNavCache\
        Recursive: true

# Documentation
# https://www.hecfblog.com/2018/10/daily-blog-510-office-2016-backstage.html
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
