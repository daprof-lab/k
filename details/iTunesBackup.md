# 🎯 **I Tunes Backup**
### `File Name: iTunesBackup.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Tony Knutson  
**Version:** 2.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
iTunes Backups

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from I Tunes Backup to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate I Tunes Backup events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit I Tunes Backup storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: iTunes Backups
Author: Tony Knutson
Version: 2.0
Id: 7b4a98d9-b36a-40be-bacc-ad0102b0a8c3
RecreateDirectories: true
Targets:
    -
        Name: iTunes Backup Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Apple\Mobilesync\Backup\
        Recursive: true
    -
        Name: iTunes Backup Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Apple Computer\Mobilesync\Backup\
        Recursive: true
    -
        Name: iTunes Backup Folder - iOS13
        Category: Communications
        Path: C:\Users\%user%\Apple\Mobilesync\Backup\
        Recursive: true

# Documentation
# https://cyberforensicator.com/2017/03/01/how-to-find-passwords-for-encrypted-itunes-backups/
# https://farleyforensics.com/2019/04/14/forensic-analysis-of-itunes-backups/
# https://www.digitalforensics.com/blog/itunes-backup-forensic-analysis/
# https://forensafe.com/blogs/itunes.html
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
