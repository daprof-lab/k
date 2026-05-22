# 🎯 **Registry Hives Msixapps**
### `File Name: RegistryHivesMSIXApps.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Zach Stanford, Mari DeGrazia, Reece394  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
MSIX/APPX App Hives

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Registry Hives Msixapps to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Registry Hives Msixapps events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Registry Hives Msixapps storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: MSIX/APPX App Hives
Author: Zach Stanford, Mari DeGrazia, Reece394
Version: 1.2
Id: 932a7d2b-3cb7-4e35-ab89-60dfa1e55c8e
RecreateDirectories: true
Targets:
    -
        Name: Registry.dat MSIX Hive
        Category: Registry
        Path: C:\Users\%user%\AppData\Local\Packages\*\SystemAppData\Helium\
        FileMask: Registry.dat*
    -
        Name: Registry.dat MSIX Hive
        Category: Registry
        Path: C:\Program Files\WindowsApps\*\
        FileMask: Registry.dat*
    -
        Name: Registry.dat MSIX Hive
        Category: Registry
        Path: C:\Windows\SystemApps\*\
        FileMask: Registry.dat*
    -
        Name: settings.dat MSIX Hive
        Category: Registry
        Path: C:\Users\%user%\AppData\Local\Packages\*\Settings\
        FileMask: settings.dat*
    -
        Name: User.dat MSIX Hive
        Category: Registry
        Path: C:\Users\%user%\AppData\Local\Packages\*\SystemAppData\Helium\
        FileMask: User.dat*
    -
        Name: UserClasses.dat MSIX Hive
        Category: Registry
        Path: C:\Users\%user%\AppData\Local\Packages\*\SystemAppData\Helium\
        FileMask: UserClasses.dat*

# Documentation
# https://www.zerofox.com/blog/the-registry-hives-you-may-be-msix-ing-registry-redirection-with-ms-msix/
# https://github.com/ydkhatri/Appx-Analysis/blob/master/winapps_appx_mus_2019.pdf
# https://learn.microsoft.com/en-us/windows/msix/desktop/desktop-to-uwp-behind-the-scenes
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
