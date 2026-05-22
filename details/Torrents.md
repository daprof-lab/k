# 🎯 **Torrents**
### `File Name: Torrents.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Tony Knutson  
**Version:** 2.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Torrent Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Torrents to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Torrents events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Torrents storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Torrent Files
Author: Tony Knutson
Version: 2.0
Id: 082de7fa-17b4-4e10-a4e8-94ef2fb27ec2
RecreateDirectories: true
Targets:
    -
        Name: Torrents
        Category: FileDownload
        Path: C:\
        FileMask: '*.torrent'
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
