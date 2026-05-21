# 🎯 **BitTorrent Client**
### `File Name: BitTorrent.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Banaanhangwagen  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Downloads list, active configurations, RSS feeds, and torrent cache logs for BitTorrent.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from BitTorrent Client to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate BitTorrent Client events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit BitTorrent Client storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: BitTorrent
Author: Banaanhangwagen
Version: 1.0
Id: ea203900-3f49-4ebf-a213-21d82ccae5db
RecreateDirectories: true
Targets:
    -
        Name: TorrentClients - BitTorrent
        Category: FileDownload
        Path: C:\Users\%user%\AppData\Roaming\BitTorrent\
        FileMask: '*.dat'

# Documentation
# https://www.researchgate.net/publication/288858418_Investigation_of_Artifacts_Left_by_BitTorrent_Client_on_the_Local_Computer_Operating_under_Windows_81
# https://www.sans.org/reading-room/whitepapers/legal/bittorrent-digital-contraband-36887
# https://www.sciencedirect.com/science/article/abs/pii/S1742287610000770
# https://www.sciencedirect.com/science/article/pii/S1742287614000152
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
