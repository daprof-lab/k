# 🎯 **OneDrive Sync Metadata**
### `File Name: OneDrive_Metadata.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Chad Tilbury, Brian Maloney  
**Version:** 2.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
System databases (e.g., .dat, .previous.dat) documenting file states and shared OneDrive folders.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from OneDrive Sync Metadata to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate OneDrive Sync Metadata events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit OneDrive Sync Metadata storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Microsoft OneDrive Storage Metadata
Author: Chad Tilbury, Brian Maloney
Version: 2.0
Id: 726ca098-6c5b-40e3-ade8-60730c5ec4f8
RecreateDirectories: true
Targets:
    -
        Name: OneDrive User Profile
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\Microsoft\OneDrive\
        Recursive: true

# Documentation
# https://www.sans.org/blog/cloud-storage-acquisition-from-endpoint-devices/
# https://www.forensicfocus.com/forums/general/onedrive-files-on-demand-windows-10-storage-sense-settings/
# https://www.forensafe.com/blogs/onedrive.html
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
