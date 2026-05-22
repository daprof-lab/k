# 🎯 **Steam Gaming Platform**
### `File Name: Steam.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Nisarg Suthar, SolitudePy  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Collects local Steam configurations, installed gaming logs, active users, and chat databases.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Steam Gaming Platform to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Steam Gaming Platform events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Steam Gaming Platform storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Steam
Author: Nisarg Suthar, SolitudePy
Version: 1.1
Id: 945e447d-7fd0-4458-99a0-898f8ce63267
RecreateDirectories: true
Targets:
    -
        Name: Steam Game Image files
        Category: Apps
        Path: C:\Program Files\Steam\appcache\librarycache\
        Recursive: true
        Comment: "Locates the directory containing image resources of installed/uninstalled games."
    -
        Name: Steam Login Metadata file
        Category: Apps
        Path: C:\Program Files\Steam\config\
        Recursive: true
        FileMask: loginusers.vdf
        Comment: "Locates file containing Steam username and persona name."
    -
        Name: Steam Friend List and Username History file
        Category: Apps
        Path: C:\Program Files\Steam\userdata\*\config\
        Recursive: true
        FileMask: localconfig.vdf
        Comment: "Locates file containing Steam Friend List and Username History."
    -
        Name: Steam User Avatar files
        Category: Apps
        Path: C:\Program Files\Steam\config\avatarcache\
        Recursive: true
        Comment: "Locates the directory containing avatar cache."
    -
        Name: Steam Game Tray Icon files
        Category: Apps
        Path: C:\Program Files\Steam\steam\games\
        Recursive: true
        Comment: "Locates the directory containing game icons appearing from tray menu."
    -
        Name: Steam Startup Times Log file
        Category: Apps
        Path: C:\Program Files\Steam\logs\
        Recursive: true
        FileMask: bootstrap_log.txt
        Comment: "Locates the directory containing log for Steam startup times."
    -
        Name: Steam Game Image files
        Category: Apps
        Path: C:\Program Files (x86)\Steam\appcache\librarycache\
        Recursive: true
        Comment: "Locates the directory containing image resources of installed/uninstalled games."
    -
        Name: Steam Login Metadata file
        Category: Apps
        Path: C:\Program Files (x86)\Steam\config\
        Recursive: true
        FileMask: loginusers.vdf
        Comment: "Locates file containing Steam username and persona name."
    -
        Name: Steam Friend List and Username History file
        Category: Apps
        Path: C:\Program Files (x86)\Steam\userdata\*\config\
        Recursive: true
        FileMask: localconfig.vdf
        Comment: "Locates file containing Steam Friend List and Username History."
    -
        Name: Steam User Avatar files
        Category: Apps
        Path: C:\Program Files (x86)\Steam\config\avatarcache\
        Recursive: true
        Comment: "Locates the directory containing avatar cache."
    -
        Name: Steam Game Tray Icon files
        Category: Apps
        Path: C:\Program Files (x86)\Steam\steam\games\
        Recursive: true
        Comment: "Locates the directory containing game icons appearing from tray menu."
    -
        Name: Steam Startup Times Log file
        Category: Apps
        Path: C:\Program Files (x86)\Steam\logs\
        Recursive: true
        FileMask: bootstrap_log.txt
        Comment: "Locates the directory containing log for Steam startup times."

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
