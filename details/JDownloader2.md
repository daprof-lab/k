# 🎯 **Jdownloader2**
### `File Name: JDownloader2.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Matt Dawson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
JDownloader 2

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Jdownloader2 to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Jdownloader2 events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Jdownloader2 storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: JDownloader 2
Author: Matt Dawson
Version: 1.0
Id: 41b218bd-c886-442d-b3a6-7a18a1cd4091
RecreateDirectories: true
Targets:
    -
        Name: JDownloader 2.0 Download Lists
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\JDownloader 2.0\cfg
        Recursive: true
        FileMask: "downloadList*.zip"
        Comment: "Zip folder which contains several files (00,00_00 and extraInfo) which list the download folder, the time it was created, the name of the download, origin URL, referral URL and more"
    -
        Name: JDownloader 2.0 Link Collector
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\JDownloader 2.0\cfg
        Recursive: true
        FileMask: "linkcollector*.zip"
        Comment: "Zip folder which contains several files (0X,0X_00 and extraInfo) which list the websites crawled for links, the referral URLs, timestamps and more"
    -
        Name: JDownloader 2.0 General Settings
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\JDownloader 2.0\cfg
        Recursive: true
        FileMask: "org.jdownloader.settings.GeneralSettings.json"
        Comment: "General user config for JDownloader 2.0. Holds default download folder."
    -
        Name: JDownloader 2.0 Link Grabber Settings
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\JDownloader 2.0\cfg
        Recursive: true
        FileMask: "org.jdownloader.gui.views.linkgrabber.addlinksdialog.LinkgrabberSettings.json"
        Comment: "Linkgrabber Settings for JDownloader 2.0. Holds latest download destination folder."
    -
        Name: JDownloader 2.0 Proxy Settings
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\JDownloader 2.0\cfg
        Recursive: true
        FileMask: "org.jdownloader.settings.InternetConnectionSettings.customproxylist.json"
        Comment: "Proxy configuration for JDownloader 2.0"

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
