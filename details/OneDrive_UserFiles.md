# 🎯 **OneDrive User Files**
### `File Name: OneDrive_UserFiles.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Chad Tilbury  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Local folder trees and offline files synchronized via Microsoft OneDrive.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from OneDrive User Files to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate OneDrive User Files events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit OneDrive User Files storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Microsoft OneDrive Storage Files
Author: Chad Tilbury
Version: 1.0
Id: e222254a-518d-4ded-8566-60a4d3654a65
RecreateDirectories: true
Targets:
    -
        Name: OneDrive User Files
        Category: Apps
        Path: C:\Users\%user%\OneDrive*\
        Recursive: true
        Comment: "Caution -- This target will collect OneDrive contents from the local drive AND on-demand cloud files. Ensure your scope of authority permits cloud collections before use or isolate system from network."

# Documentation
# https://www.sans.org/blog/cloud-storage-acquisition-from-endpoint-devices/
# https://www.forensicfocus.com/forums/general/onedrive-files-on-demand-windows-10-storage-sense-settings/
# This target collects user OneDrive files from the default folders of OneDrive Personal and Business, but folders can be user-defined.  Check NTUSER.DAT\Software\Microsoft\OneDrive\Accounts\<Personal|Business> to see if locations have been changed.
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
