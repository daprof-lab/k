# 🎯 **VLC Media Player**
### `File Name: VLC Media Player.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Matt Dawson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Recovers VLC logs, playing playlists, and recently viewed media histories.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from VLC Media Player to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate VLC Media Player events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit VLC Media Player storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: VLC Media Player
Author: Matt Dawson
Version: 1.0
Id: f7187e39-0410-41cb-b7e0-243d92090c9c
RecreateDirectories: true
Targets:
    -
        Name: VLC Recently Opened Files
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\vlc\
        FileMask: "vlc-qt-interface.ini"
        Comment: "Configuration file for VLC. Holds [RecentsMRL] key which lists recently opened files as well as sometimes retaining timestamps for file opening"
    -
        Name: VLC Recorded Files
        Category: Apps
        Path: C:\Users\%user%\Videos\
        FileMask: "vlc-*.avi"
        Comment: "Recorded files in VLC. Sometimes the Record button may be pressed instead of Play by suspects, which can record them watching content with VLC"

# Documentation
# https://www.forensicfocus.com/forums/general/vlc-recent-files/
# https://superuser.com/questions/287137/does-vlc-media-player-store-the-files-or-its-history-in-a-hidden-location/1206411
# https://www.forensafe.com/blogs/vlc.html
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
