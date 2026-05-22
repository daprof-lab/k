# 🎯 **Newsleecher**
### `File Name: Newsleecher.tkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Newsleecher

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Newsleecher to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Newsleecher events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Newsleecher storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Newsleecher
Author: Andrew Rathbun
Version: 1.0
Id: 82920bd3-68bf-42c5-ba3c-55d59af35f64
RecreateDirectories: true
Targets:
    -
        Name: Usenet Clients - Newsleecher
        Category: FileDownload
        Path: C:\Users\%user%\AppData\Roaming\NewsLeecher\
        FileMask: 'downloaded.dat'
        Comment: "Locates Newsleecher download .dat file"

# Documentation
# C:\Users\%user%\AppData\Roaming\NewsLeecher\downloaded.dat is where the download log file resides. I haven't been able to test Newsleecher yet so I haven't been able to populate this file.
```
---

[⬅️ Back to Memory & Virtualization Targets](../memory_virtualization_targets.md)
