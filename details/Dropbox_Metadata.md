# 🎯 **Dropbox Sync Metadata**
### `File Name: Dropbox_Metadata.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Chad Tilbury / Andrew Rathbun  
**Version:** 1.5
{% endhint %}

---

## 📖 **Forensic Description & Value**
SQL databases detailing Dropbox file synchronization timelines, file ids, and hashes.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Dropbox Sync Metadata to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Dropbox Sync Metadata events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Dropbox Sync Metadata storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Dropbox Cloud Storage Metadata
Author: Chad Tilbury and Andrew Rathbun
Version: 1.5
Id: bc2be151-1ecb-4cba-8c74-11b411fcc7ef
RecreateDirectories: true
Targets:
    -
        Name: Dropbox Metadata
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\Dropbox\
        FileMask: info.json
        Comment: "Getting individual files because folder may contain very large extraneous files. Info.json contains user's Dropbox folder location"
    -
        Name: Dropbox Metadata
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\Dropbox\
        FileMask: host.db
        Comment: "SQLite database which contains the local path of the user's Dropbox folder encoded in BASE64."
    -
        Name: Dropbox Metadata
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\Dropbox\machine_storage
        FileMask: tray-thumbnails.db
        Comment: "SQLite database containing references to image files at one time present in a user’s Dropbox instance."
    -
        Name: Dropbox Metadata
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\Dropbox\
        FileMask: host.dbx
        Comment: "SQLite database which contains the local path of the user's Dropbox folder encoded in BASE64. Decode each line separately, not together."
    -
        Name: Windows Protect Folder
        Category: FileSystem
        Path: C:\Users\%user%\AppData\Roaming\Microsoft\Protect\*\
        Recursive: true
        Comment: "Required for offline decryption of Dropbox databases"
    -
        Name: Dropbox Metadata
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\Dropbox\instance*\
        Recursive: true
        Comment: "instance folder holds multiple SQLite databases related to Dropbox activity and contents"

# Documentation
# home.db: SQlite database tracking some of a user's recent Dropbox activity
# icon.db: SQLite database tracking of icons in the user's Dropbox sync history which can give an indication as to which files and folders are present
# sync_history.db: SQLite database containing recent synchronization events including usage activity
# nucleus.sqlite3: SQLite database tracking names of local and cloud-only files
# aggregation.dbx: SQLite database that can contain a snapshot table of the user's Dropbox contents in JSON with timestamps in UNIX Epoch
# avatarcache.db: SQLite database which appears to contain the ID's of account(s) on the user's system where Dropbox is installed
# tray-thumbnails.db: SQLite database containing references to image files at one time present in a user’s Dropbox instance.  Can include references to deleted files no longer present in Dropbox.
# The SQLite database(s) this Target collects can be parsed with SQLECmd using the following map(s): https://github.com/EricZimmerman/SQLECmd/blob/master/SQLMap/Maps/Windows_Dropbox_Configurations.smap, https://github.com/EricZimmerman/SQLECmd/blob/master/SQLMap/Maps/Windows_Dropbox_FileCache.smap, and https://github.com/EricZimmerman/SQLECmd/blob/master/SQLMap/Maps/Windows_Dropbox_InstanceDB.smap
# https://www.marshall.edu/forensics/files/Treleven-Dropbox-Paper-FINAL.pdf
# https://arxiv.org/pdf/1709.10395
# https://www.sans.org/blog/digital-forensics-dropbox/
# https://www.researchgate.net/publication/342991973_Forensic_Analysis_of_Dropbox_Data_Remnants_on_Windows_10
# https://www.atropos4n6.com/cloud-forensics/windows-10-artifacts-of-dropboxs-native-app-usage/
# https://www.atropos4n6.com/cloud-forensics/artifacts-of-dropbox-usage-on-windows-10-part-2/
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
