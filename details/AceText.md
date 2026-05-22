# 🎯 **Ace Text**
### `File Name: AceText.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
AceText

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Ace Text to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Ace Text events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Ace Text storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: AceText
Author: Andrew Rathbun
Version: 1.0
Id: 0b7b9e23-5653-4075-9862-48cbdf1dda8a
RecreateDirectories: true
Targets:
    -
        Name: AceText - Clipboard History
        Category: Apps
        Path: C:\Users\%user%\Documents
        FileMask: '*.atc'
        Comment: "Locates the Clipboard history for AceText"

# Documentation
# AceText is made by the same people who make Edit Pad Pro, PowerGREP, etc. It's a cool program that serves as a Clipboard extension tool.
# From a forensic perspective, the entirety of a user's clipboard history is available for our perusal!
# Once you have the .atc file, you can open with any text editor and see the entire history of a user's clipboard contents.
# The copied text will be found between the <text> and </text> parameters.
# If content is copied from a webpage, copied text will be the same as above but there will also be a <url> and </url> parameter which will display the URL from which the contents were copied from.
# In addition to the above, the kind= parameter will provide clues as to where the contents were copied from.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
