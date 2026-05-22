# 🎯 **Sumatra PDF**
### `File Name: SumatraPDF.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
SumatraPDF

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Sumatra PDF to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Sumatra PDF events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Sumatra PDF storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: SumatraPDF
Author: Andrew Rathbun
Version: 1.1
Id: c3a2d097-bca5-4ebe-83b2-db509c86883f
RecreateDirectories: true
Targets:
    -
        Name: SumatraPDF Settings - SessionData
        Category: FileKnowledge
        Path: C:\Users\%user%\AppData\Local\SumatraPDF
        FileMask: SumatraPDF-settings.txt
        Recursive: false
        Comment: Settings file which contains information about previous user session
    -
        Name: SumatraPDF Cache
        Category: FileKnowledge
        Path: C:\Users\%user%\AppData\Local\SumatraPDF\sumatrapdfcache
        Recursive: false
        Comment: Folder contains a PNG snapshot of each PDF file the user had open at the time of last application close

# Documentation
# https://www.sumatrapdfreader.org/settings/settings.html
# In the above link, search for SessionData to warp to the applicable information you can find for what documents the user had opened within SumatraPDF at the last time of program exit
# I've had 170+ PDFs opened at once with SumatraPDF and each of their full file paths were recorded within this file. Very useful!
# Here's an example of some information you'll see about PDFs that've been opened with SumatraPDF
# OpenCount = 1
# DecryptionKey = 8cfbabc34e8d846dffb53b90c9g2acb5es82d9c86f314cb5aa7a1adfc66f76e800000000000000000000000000000000
# DecryptionKey only exists if the user chooses to remember the password for a PDF that's password protected
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
