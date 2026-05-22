# 🎯 **Google Earth**
### `File Name: GoogleEarth.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Guus Beckers  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Google Earth

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Google Earth to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Google Earth events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Google Earth storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Google Earth
Author: Guus Beckers
Version: 1.0
Id: 1ad35449-19a6-4e90-855e-elb4bfb2748b
RecreateDirectories: true
Targets:
    -
        Name: Google Earth My Places file
        Category: Apps
        Path: C:\Users\%user%\AppData\LocalLow\Google\GoogleEarth
        FileMask: 'myplaces.kml'
        Comment: "File which holds favorited locations"
    -
        Name: Google Earth My Places Backup file
        Category: Apps
        Path: C:\Users\%user%\AppData\LocalLow\Google\GoogleEarth
        FileMask: 'myplaces.backup.kml'
        Comment: "Backup file which holds favorited locations"
    -
        Name: Google Earth My Places file (XP)
        Category: Apps
        Path: C:\Documents and Settings\%user%\Application Data\Google\GoogleEarth
        FileMask: 'myplaces.kml'
        Comment: "File which holds favorited locations"
    -
        Name: Google Earth My Places Backup file (XP)
        Category: Apps
        Path: C:\Documents and Settings\%user%\Application Data\Google\GoogleEarth
        FileMask: 'myplaces.backup.kml'
        Comment: "Backup file which holds favorited locations"

# Documentation
# https://support.google.com/earth/answer/166438?hl=en
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
