# 🎯 **Google Drive Metadata**
### `File Name: GoogleDrive_Metadata.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Chad Tilbury  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Sync databases (cloud_graph.db) tracking local folder configurations and Google Drive storage sync timelines.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Google Drive Metadata to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Google Drive Metadata events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Google Drive Metadata storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Google Drive Metadata
Author: Chad Tilbury
Version: 1.1
Id: 2bfd54a5-175f-48ad-a1bc-7be1dc0465e7
RecreateDirectories: true
Targets:
    -
        Name: Google Drive Backup and Sync Metadata
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\Google\Drive\
        Recursive: true
        Comment: "Older version of Google Drive"
    -
        Name: Google Drive for Desktop Metadata
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\Google\DriveFS\
        Recursive: true
        Comment: "Metadata folder the same for both newer Google Drive for Desktop and older Google File Stream application"

# Documentation
# Log files from the DriveFS directory can be parsed using https://toolbox.googleapps.com/apps/loggershark/
# https://www.researchgate.net/publication/330319091_Cloud_Drives_Forensic_Artifacts_A_Google_Drive_Case
# https://cyberforensicator.com/2018/10/19/cloud-forensics-google-drive/
# https://www.atropos4n6.com/cloud-artifacts/google-drive-forensics/
# https://www.atropos4n6.com/cloud-artifacts/google-drive-forensics-2/
# https://www.forensafe.com/blogs/googledrive.html
# https://forensafe.com/blogs/windows_google_drive.html
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
