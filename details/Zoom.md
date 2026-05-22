# 🎯 **Zoom**
### `File Name: Zoom.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ryan McVicar  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Zoom client artifacts

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Zoom to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Zoom events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Zoom storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Zoom client artifacts
Author: Ryan McVicar
Version: 1.0
Id: 420ce1b0-bfc0-40de-a0fe-f154bbc5eec8
RecreateDirectories: true
Targets:
    -
        Name: Zoom client logs
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Zoom\logs
        Recursive: true
        FileMask: "*"
        Comment: "Zoom client artifacts"
    -
        Name: Zoom client logs (Windows XP)
        Category: Apps
        Path: C:\Documents and Settings\%user%\Application Data\Zoom\
        Recursive: true
        FileMask: "*"
        Comment: "Zoom client artifacts (Windows XP)"
    -
        Name: Zoom client recordings
        Category: Apps
        Path: C:\Users\%user%\Documents\Zoom\
        Recursive: true
        FileMask: "*"
        Comment: "Zoom recording artifacts"
    -
        Name: Zoom plugin (Outlook)
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Zoom Plugin
        FileMask: "*.json"
        Comment: "Zoom plugin artifacts"

# Documentation
# https://support.zoom.us/hc/en-us/articles/201512326-Troubleshooting-log-for-Windows
# https://www.sans.org/posters/windows-third-party-apps-forensics-poster/
# https://www.sciencedirect.com/science/article/pii/S2666281721000019
# https://www.forensafe.com/blogs/zoom.html
# This target includes some "irrelevant" artifacts like DLLs, and exes
# We collect everything to hopefully avoid missing crucial artifacts
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
