# 🎯 **Cloud Storage One Drive Explorer**
### `File Name: CloudStorage_OneDriveExplorer.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Brian Maloney  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
OneDrive and other files used with OneDriveExplorer

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Cloud Storage One Drive Explorer to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Cloud Storage One Drive Explorer events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Cloud Storage One Drive Explorer storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: OneDrive and other files used with OneDriveExplorer
Author: Brian Maloney
Version: 1.0
Id: 9783ccfe-42c2-440b-82c6-428afc5d9a61
RecreateDirectories: true
Targets:
    -
        Name: OneDrive Metadata
        Category: Apps
        Path: OneDrive_Metadata.tkape
    -
        Name: User Related Registry hives
        Category: Registry
        Path: RegistryHivesUser.tkape
    -
        Name: Recycle Bin DataAndInfo
        Category: FileDeletion
        Path: RecycleBin.tkape

# Documentation
# N/A
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
