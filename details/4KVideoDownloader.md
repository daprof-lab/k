# 🎯 **4kvideo Downloader**
### `File Name: 4KVideoDownloader.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
4K Video Downloader

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from 4kvideo Downloader to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate 4kvideo Downloader events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit 4kvideo Downloader storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: 4K Video Downloader
Author: Andrew Rathbun
Version: 1.1
Id: e33d4392-459b-459e-82e0-d9c624adbfbc
RecreateDirectories: true
Targets:
    -
        Name: 4K Video Downloader
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\4kdownload.com\4K Video Downloader\4K Video Downloader
        FileMask: "*.sqlite"
        Comment: "Grabs database(s) that stores user download history"
    -
        Name: 4K Video Downloader+
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\4kdownload.com\4K Video Downloader+\4K Video Downloader+
        FileMask: "*.sqlite"
        Comment: "Grabs database(s) that stores user download history"

# Documentation
# https://www.4kdownload.com/products/product-videodownloader
# The SQLite database(s) this Target collects can be parsed with SQLECmd using the following map(s):
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
