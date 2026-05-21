# 🎯 **uTorrent Client**
### `File Name: uTorrent.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Banaanhangwagen  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Active downloads database, custom folder paths, and torrent hash caches for uTorrent.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from uTorrent Client to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate uTorrent Client events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit uTorrent Client storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: uTorrent
Author: Banaanhangwagen
Version: 1.0
Id: df8ed278-cd5e-4345-bb30-9b25182bf2d4
RecreateDirectories: true
Targets:
    -
        Name: TorrentClients - uTorrent
        Category: FileDownload
        Path: C:\Users\%user%\AppData\Roaming\uTorrent\
        FileMask: '*.dat'

# Documentation
# https://robertpearsonblog.wordpress.com/2016/11/11/utorrent-and-windows-10-forensic-nuggets-of-info/
# https://www.forensicfocus.com/articles/forensic-analysis-of-the-%CE%BCtorrent-peer-to-peer-client-in-windows/
# https://forensafe.com/blogs/android_utorrent.html
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
