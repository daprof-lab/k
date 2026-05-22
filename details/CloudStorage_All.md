# 🎯 **Cloud Storage All**
### `File Name: CloudStorage_All.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Chad Tilbury and Andrew Rathbun  
**Version:** 1.4
{% endhint %}

---

## 📖 **Forensic Description & Value**
Cloud Storage Contents and Metadata

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Cloud Storage All to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Cloud Storage All events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Cloud Storage All storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Cloud Storage Contents and Metadata
Author: Chad Tilbury and Andrew Rathbun
Version: 1.4
Id: 63c7ff1e-0fcb-45ae-9d72-29bf8458b6db
RecreateDirectories: true
Targets:
    -
        Name: Box User Files
        Category: Apps
        Path: BoxDrive_UserFiles.tkape
    -
        Name: Dropbox User Files
        Category: Apps
        Path: Dropbox_UserFiles.tkape
    -
        Name: Google Drive Backup and Sync User Files
        Category: Apps
        Path: GoogleDriveBackupSync_UserFiles.tkape
    -
        Name: OneDrive User Files
        Category: Apps
        Path: OneDrive_UserFiles.tkape
    -
        Name: pCloudDatabase
        Category: Apps
        Path: pCloudDatabase.tkape
    -
        Name: SugarSync
        Category: Apps
        Path: SugarSync.tkape
    -
        Name: CloudStorage Metadata
        Category: Apps
        Path: CloudStorage_Metadata.tkape
    -
        Name: Idrive Backup
        Category: Apps
        Path: Idrive.tkape

# Documentation
# For those looking to contribute to this list, check here for ideas: https://en.wikipedia.org/wiki/Comparison_of_online_backup_services.
# Install one of the applications not covered above and find where useful information is stored. If useful information can be located, make an individual Target for it and place in the appropriate folder. Then, include that Target in the appropriate Compound Target.
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
