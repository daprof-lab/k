# 🎯 **Torrent Clients**
### `File Name: TorrentClients.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Torrent Clients

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Torrent Clients to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Torrent Clients events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Torrent Clients storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Torrent Clients
Author: Andrew Rathbun
Version: 1.0
Id: c409301a-0147-41e1-bb01-ffb8ec49a67a
RecreateDirectories: true
Targets:
    -
        Name: BitTorrent
        Category: FileDownload
        Path: BitTorrent.tkape
    -
        Name: qBittorrent
        Category: FileDownload
        Path: qBittorrent.tkape
    -
        Name: uTorrent
        Category: FileDownload
        Path: uTorrent.tkape

# Documentation
# For those looking to contribute to this list, check here for ideas: https://en.wikipedia.org/wiki/Comparison_of_BitTorrent_clients.
# Install one of the applications not covered above and find where useful information is stored. If useful information can be located, make an individual Target for it and place in the appropriate folder. Then, include that Target in the appropriate Compound Target.
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
