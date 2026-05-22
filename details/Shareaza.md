# 🎯 **Shareaza**
### `File Name: Shareaza.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Shareaza

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Shareaza to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Shareaza events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Shareaza storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Shareaza
Author: Andrew Rathbun
Version: 1.0
Id: 3d3203ae-e753-4c37-ac82-d67735972d44
RecreateDirectories: true
Targets:
    -
        Name: Shareaza Logs
        Category: FileDownload
        Path: C:\Users\%user%\AppData\Roaming\Shareaza\
        Recursive: true
        Comment: "Locates Shareaza logs and copies them."

# Documentation
# https://www.researchgate.net/publication/222404106_Forensic_Investigation_of_Peer-to-Peer_File-Sharing_Networks
# Shareaza is a file-sharing client which supports the gnutella, Gnutella2 (G2), eDonkey, BitTorrent, FTP, HTTP and HTTPS.
# Logs are stored in .dat format and have to be viewed in a hex editor.
# Searches.dat within the Data folder will contain information on searches conducted by the user as well as results displayed.
# TKape was created for version 2.7.10.2.
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
