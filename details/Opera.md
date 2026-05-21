# 🎯 **Opera Browser**
### `File Name: Opera.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
History records, user downloads, and active session configurations for Opera.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Opera Browser to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Opera Browser events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Opera Browser storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Opera
Author: Andrew Rathbun
Version: 1.0
Id: 29e3154b-7d33-4f74-8d0c-c4b8980cf989
RecreateDirectories: true
Targets:
    -
        Name: Opera - Local Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Opera Software\Opera Stable
        Recursive: true
        Comment: Grabs entire contents of the Opera AppData\Local folder
    -
        Name: Opera - Roaming Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Opera Software\Opera Stable
        Recursive: true
        Comment: Grabs entire contents of the Opera AppData\Roaming folder

# Documentation
# https://kb.digital-detective.net/display/BF/Opera
# https://www.digitalforensics.com/blog/an-overview-of-web-browser-forensics/
# https://davidkoepi.wordpress.com/2012/12/16/opera-forensics/
# https://www.forensafe.com/blogs/opera.html
# Opera is a third-party web browser that has a small market share compared to the bigger names.
# The Local folder is mostly going to contain cache files that are not readable in a text editor.
# The Roaming folder is where one can find the most useful information.
# Within Roaming, IndexedDB folder will have folders named after URLs the user navigates to.
# Within Roaming, Session Storage will have logs with the naming convention of XXXXXX.log that increment as they are rolled over. Within these files are URLs the user navigated to in a given session.
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
