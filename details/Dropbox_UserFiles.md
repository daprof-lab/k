# 🎯 **Dropbox User Files**
### `File Name: Dropbox_UserFiles.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Chad Tilbury  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Local Dropbox synchronization directories and cached operational databases.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Dropbox User Files to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Dropbox User Files events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Dropbox User Files storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Dropbox Cloud Storage Files
Author: Chad Tilbury
Version: 1.0
Id: 6ed5ecbe-af8c-46fd-b827-58228824ea34
RecreateDirectories: true
Targets:
    -
        Name: Dropbox User Files
        Category: Apps
        Path: C:\Users\%user%\Dropbox*\
        Recursive: true
        Comment: "Default storage location for Dropbox Personal and Business (when using wildcard), but can be user-defined. Check info.json file in user Dropbox metadata files to identify default folder."

# Documentation
# This target will also collect the ".dropbox.cache" folder located in the storage location
# https://www.marshall.edu/forensics/files/Treleven-Dropbox-Paper-FINAL.pdf
# https://arxiv.org/pdf/1709.10395
# https://www.sans.org/blog/digital-forensics-dropbox/
# https://www.researchgate.net/publication/342991973_Forensic_Analysis_of_Dropbox_Data_Remnants_on_Windows_10
# https://www.atropos4n6.com/cloud-forensics/windows-10-artifacts-of-dropboxs-native-app-usage/
# https://www.atropos4n6.com/cloud-forensics/artifacts-of-dropbox-usage-on-windows-10-part-2/
# https://www.forensafe.com/blogs/dropbox.html
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
