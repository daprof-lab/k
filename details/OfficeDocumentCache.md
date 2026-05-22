# 🎯 **Office Document Cache**
### `File Name: OfficeDocumentCache.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Banaanhangwagen  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Office Document Cache

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Office Document Cache to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Office Document Cache events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Office Document Cache storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Office Document Cache
Author: Banaanhangwagen
Version: 1.0
Id: 15e92d9c-b02d-4cdf-a86e-bafb3d25af5c
RecreateDirectories: true
Targets:
    -
        Name: Office Document Cache
        Category: FileKnowledge
        Path: C:\Users\%user%\AppData\Local\Microsoft\Office\*\OfficeFileCache\
        Recursive: true

# Documentation
# https://arsenalrecon.com/2019/10/the-office-document-cache-and-introducing-odc-recon-part-i/
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
