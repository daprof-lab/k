# 🎯 **RDP Bitmap Cache**
### `File Name: RDPCache.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Hadar Yudovich  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Cached display tiles from Remote Desktop sessions. Reconstructs screens viewed by remote attackers.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from RDP Bitmap Cache to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate RDP Bitmap Cache events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit RDP Bitmap Cache storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: RDP Cache Files
Author: Hadar Yudovich
Version: 1.1
Id: 527a5de1-fb71-4efd-9701-89a30ea908e3
RecreateDirectories: true
Targets:
    -
        Name: RDP Cache Files
        Category: FileSystem
        Path: C:\Users\%user%\AppData\Local\Microsoft\Terminal Server Client\Cache\
    -
        Name: Windows.old RDP Cache Files
        Category: FileSystem
        Path: C:\Windows.old\Users\%user%\AppData\Local\Microsoft\Terminal Server Client\Cache\
    -
        Name: RDP Cache Files
        Category: FileSystem
        Path: C:\Documents and Settings\%user%\Local Settings\Application Data\Microsoft\Terminal Server Client\Cache\

# Documentation
# https://www.youtube.com/watch?v=NnEOk5-Dstw
# https://cbtgeeks.com/2018/05/22/digital-forensics-on-rdp-cache/
# https://github.com/BSI-Bund/RdpCacheStitcher
# https://www.thedfirspot.com/post/rdp-bitmap-cache-piece-s-of-the-puzzle
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
