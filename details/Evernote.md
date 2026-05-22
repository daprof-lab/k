# 🎯 **Evernote**
### `File Name: Evernote.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Matt Dawson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Evernote

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Evernote to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Evernote events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Evernote storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Evernote
Author: Matt Dawson
Version: 1.0
Id: acea0975-6610-4813-8a27-8e78186c87d5
RecreateDirectories: true
Targets:
   -
      Name: Evernote Accounts
      Category: Apps
      Path: C:\Users\%user%\AppData\Local\Evernote\Evernote\Databases\
      Recursive: true
      FileMask: ".accounts"
      Comment: "Holds username and email of accounts"
   -
      Name: Evernote Notebooks
      Category: Apps
      Path: C:\Users\%user%\AppData\Local\Evernote\Evernote\Databases\
      Recursive: true
      FileMask: "*.exb"
      Comment: "SQLite Database of the notes"
   -
      Name: Evernote Notebook Snippets
      Category: Apps
      Path: C:\Users\%user%\AppData\Local\Evernote\Evernote\Databases\
      Recursive: true
      FileMask: "*.exb.snippets"
      Comment: "Note 'Snippets'"

# Documentation
# https://arxiv.org/pdf/1709.10395
# https://www.forensicfocus.com/articles/evernote-introduction/
# https://www.carpeindicium.com/blog/quick-dirty-recover-local-evernote/
# https://www.forensafe.com/blogs/evernote.html
# Evernote is a powerful tool that can help executives, entrepreneurs and creative people capture and arrange their ideas. All you have to do is use it.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
