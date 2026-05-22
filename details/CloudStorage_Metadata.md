# 🎯 **Cloud Storage Metadata**
### `File Name: CloudStorage_Metadata.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Chad Tilbury and Andrew Rathbun, Eric Capuano  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
Cloud Storage Metadata

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Cloud Storage Metadata to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Cloud Storage Metadata events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Cloud Storage Metadata storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Cloud Storage Metadata
Author: Chad Tilbury and Andrew Rathbun, Eric Capuano
Version: 1.2
Id: 136ca523-2f99-4203-bd66-6aa50fe8d3a8
RecreateDirectories: true
Targets:
    -
        Name: Box Metadata
        Category: Apps
        Path: BoxDrive_Metadata.tkape
    -
        Name: Dropbox Metadata
        Category: Apps
        Path: Dropbox_Metadata.tkape
    -
        Name: Google Drive Metadata
        Category: Apps
        Path: GoogleDrive_Metadata.tkape
    -
        Name: MegaSync Data Collection
        Category: Apps
        Path: Megasync.tkape
    -
        Name: OneDrive Metadata
        Category: Apps
        Path: OneDrive_Metadata.tkape
    -
        Name: Rclone Conf File
        Category: Apps
        Path: RcloneConf.tkape
    -
        Name: FreeFileSync
        Category: Apps
        Path: FreeFileSync.tkape

# Documentation
# For those looking to contribute to this list, check here for ideas: https://en.wikipedia.org/wiki/Comparison_of_online_backup_services.
# Install one of the applications not covered above and find where useful information is stored. If useful information can be located, make an individual Target for it and place in the appropriate folder. Then, include that Target in the appropriate Compound Target.
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
