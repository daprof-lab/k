# 🎯 **Share X**
### `File Name: ShareX.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
ShareX

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Share X to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Share X events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Share X storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: ShareX
Author: Andrew Rathbun
Version: 1.0
Id: a8409b28-70ac-4961-a1d0-94bdf1b3e7e2
RecreateDirectories: true
Targets:
    -
        Name: ShareX
        Category: Apps
        Path: C:\Users\%user%\Documents\ShareX
        Recursive: true
        Comment: "Locates and captures all files within the default ShareX folder path"

# Documentation
# ShareX is an amazing, free, and open-source alternative to Snipping Tool, Snagit, etc.
# By default, a user's captures are stored in the above location.
# The user can change their default folder path for screenshots by navigating to Application Settings -> Paths -> ShareX Personal Folder, hitting Apply, and restarting the program. Please note this target will be ineffective if the user changes the default folder path.
# C:\Users\%user%\Documents\ShareX\PersonalPath.cfg will list where the user currently saves all screenshots, application configuration files, backups, and logs, to name a few. This file should persist even after the user changes the default ShareX folder path.
# I changed the default folder location for where my screenshots, settings, etc were stored but C:\Users\%user%\Documents\ShareX\PersonalPath.cfg still existed and pointed to the location I moved everything over to.
# Screenshots folder will contain logical copies of all captures by the user typically separated by folder in YYYY-MM format with the logical files residing inside.
# Within the application's storage folder, there will be a Logs folder with files with a naming convention of ShareX-Log-YYYY-MM.txt. These files are important as they give a literal play-by-play of the user's actions with ShareX.
# This Target captures the contents of everything within the default folder path upon ShareX's installation. Modify the target as needed if. Contact me if you need help with that.
# UploadersConfig.json will have information regarding FTP/Cloud Storage accounts set up by the user.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
