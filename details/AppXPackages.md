# 🎯 **App Xpackages**
### `File Name: AppXPackages.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Nisarg Suthar  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
AppXPackages

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from App Xpackages to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate App Xpackages events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit App Xpackages storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: AppXPackages
Author: Nisarg Suthar
Version: 1.0
Id: cda2c952-8d98-456b-8572-019b1c71359e
RecreateDirectories: true
Targets:
    -
        Name: WindowsApps for AppX
        Category: Apps
        Path: C:\Program Files\WindowsApps\Deleted*\
        Recursive: true
        Comment: "Locates all the user AppX package directories which were installed through Microsoft Store and updated/uninstalled by the user."
    -
        Name: SystemApps for AppX
        Category: Apps
        Path: C:\Windows\SystemApps\
        Recursive: true
        Comment: "Locates all the system AppX package directories which were installed by the system."
    -
        Name: UserSpecificPackages for AppX
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\Packages\
        Recursive: true
        Comment: "Locates all the user and system AppX package directories which are user specific on the system."
    -
        Name: AppRepository for AppX
        Category: Apps
        Path: C:\ProgramData\Microsoft\Windows\AppRepository\Packages\
        Recursive: true
        FileMask: StateRepository-*.srd
        Comment: "Locates the StateRepository .srd databases."
    -
        Name: ProgramData Packages for AppX
        Category: Apps
        Path: C:\ProgramData\Packages\
        Recursive: true
        Comment: "Locates the ProgramData AppX package directories."

# Documentation
# https://www.tenforums.com/software-apps/163591-windowsapps-deleted-other-subfolders.html
# https://github.com/ydkhatri/Appx-Analysis
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
