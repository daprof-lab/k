# 🎯 **Windows Your Phone**
### `File Name: WindowsYourPhone.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows Your Phone

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Windows Your Phone to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Windows Your Phone events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Windows Your Phone storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Windows Your Phone
Author: Andrew Rathbun
Version: 1.0
Id: 2151d28a-3b2b-4784-a91f-72622a97a17b
RecreateDirectories: true
Targets:
    -
        Name: Windows Your Phone - All Databases
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\Packages\Microsoft.YourPhone_8wekyb3d8bbwe\LocalCache\Indexed
        Recursive: true
        Comment: "Locates all Your Phone database files"

# Documentation
# https://iconline.ipleiria.pt/bitstream/10400.8/4179/1/Digital_forensic_artifacts_YourPhone_W10.pdf
# This has only been tested with Android at this time. I don't own an Apple device but if someone else does, feel free to edit this target file with iOS related information.
# This target will recursively grab folders with a complete file path similar to this one: .\AppData\Local\Packages\Microsoft.YourPhone_8wekyb3d8bbwe\LocalCache\Indexed\GUID\System\Database\.
# Inside this directory on my system were the following files:
#    calling.db
#    calling.db-shm
#    calling.db-wal
#    contacts.db
#    contacts.db-shm
#    contacts.db-wal
#    deviceData.db-shm
#    deviceData.db-wal
#    notifications.db
#    notifications.db-shm
#    notifications.db-wal
#    phone.db
#    phone.db-shm
#    phone.db-wal
#    photos.db
#    photos.db-shm
#    photos.db-wal
#    settings.db
#    settings.db-shm
#    settings.db-wal
# Throw any of these files into a SQLite viewer such as SQLite Expert Pro or DB Browser for SQLite to view the contents.
# A quick rundown:
#    Photos.db will have filenames and blob files.
#    Phone.db will contain all text messages on the device, including RCS chats, conversations, and file transfers, MMS messages, etc.
#    Contacts.db will contain all contact names, numbers, addresses, email addresses, etc.
#    Settings.db will contain an enumerated list of installed apps on the device.
#    Calling.db will contain call history.
#    Notifications.db will show the active notifications from the device.
#    DeviceData.db will have the current wallpaper that's displayed on the device.
# There are now SQLECmd maps for this databases:
#    https://github.com/EricZimmerman/SQLECmd/blob/master/SQLMap/Maps/Windows_YourPhone_NotificationsDB.smap
#    https://github.com/EricZimmerman/SQLECmd/blob/master/SQLMap/Maps/Windows_YourPhone_PhoneDB-SMSMessages.smap
#    https://github.com/EricZimmerman/SQLECmd/blob/master/SQLMap/Maps/Windows_YourPhone_PhotosDB.smap
#    https://github.com/EricZimmerman/SQLECmd/blob/master/SQLMap/Maps/Windows_YourPhone_SettingsDB.smap
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
