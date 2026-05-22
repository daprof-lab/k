# 🎯 **Q Bittorrent**
### `File Name: qBittorrent.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Banaanhangwagen  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
qBittorrent

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Q Bittorrent to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Q Bittorrent events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Q Bittorrent storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: qBittorrent
Author: Banaanhangwagen
Version: 1.0
Id: 17956359-4d7b-4428-8207-2d745d7f6267
RecreateDirectories: true
Targets:
    -
        Name: TorrentClients - qBittorrent
        Category: FileDownload
        Path: C:\Users\%user%\AppData\Roaming\qBittorrent\
        FileMask: '*.ini'
    -
        Name: TorrentClients - qBittorrent
        Category: FileDownload
        Path: C:\Users\%user%\AppData\Local\qBittorrent\logs\
    -
        Name: TorrentClients - qBittorrent
        Category: FileDownload
        Path: C:\Users\%user%\AppData\Local\qBittorrent\GeoDB\
        Comment: "Locate .mmdb file for network peer connection analysis."
    -
        Name: TorrentClients - qBittorrent
        Category: FileDownload
        Path: C:\Users\%user%\AppData\Local\qBittorrent\BT_backup\
        Comment: "Locate active (in-progress) torrent files."

# Documentation
# https://troy4n6.blogspot.com/2019/02/text-based-treasure-qbittorent-log-file.html
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
