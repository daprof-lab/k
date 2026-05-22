# 🎯 **Google Drive Backup Sync User Files**
### `File Name: GoogleDriveBackupSync_UserFiles.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Chad Tilbury  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Google Backup and Sync Storage Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Google Drive Backup Sync User Files to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Google Drive Backup Sync User Files events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Google Drive Backup Sync User Files storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Google Backup and Sync Storage Files
Author: Chad Tilbury
Version: 1.0
Id: 6ebae21e-2323-4605-b258-38ea3a43b283
RecreateDirectories: true
Targets:
    -
        Name: Google Drive Backup and Sync User Files
        Category: Apps
        Path: C:\Users\%user%\Google Drive*\
        Recursive: true
        Comment: "Older Google Drive Backup and Sync application only"

# Documentation
# Google Drive for Desktop (originally Google File Stream) stores user files in a virtualized "G:\My Drive" folder by default. This target will not collect files from those versions of Google Drive.
# https://www.researchgate.net/publication/330319091_Cloud_Drives_Forensic_Artifacts_A_Google_Drive_Case
# https://cyberforensicator.com/2018/10/19/cloud-forensics-google-drive/
# https://www.atropos4n6.com/cloud-artifacts/google-drive-forensics/
# https://www.atropos4n6.com/cloud-artifacts/google-drive-forensics-2/
# https://forensafe.com/blogs/windows_google_drive.html
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
