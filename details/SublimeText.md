# 🎯 **Sublime Text**
### `File Name: SublimeText.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Mathias Frank and Nisarg Suthar  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Sublime Text 2/3/4 Auto Save Session

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Sublime Text to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Sublime Text events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Sublime Text storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Sublime Text 2/3/4 Auto Save Session
Author: Mathias Frank and Nisarg Suthar
Version: 1.1
Id: c1a64d12-bdf3-4ebe-a715-719bd6f2ddad
RecreateDirectories: true
Targets:
    -
        Name: SublimeText 2/3 Auto Save Session
        Category: Text Editor
        Path: C:\Users\%user%\AppData\Roaming\Sublime Text*\Settings\
        FileMask: Session.sublime_session
        Comment: "Sublime Text 2/3 stores unsaved (temporary) files and its content in its Session.sublime_session file"
    -
        Name: SublimeText 4 Auto Save Session
        Category: Text Editor
        Path: C:\Users\%user%\AppData\Roaming\Sublime Text*\Local\
        FileMask: '*.sublime_session'
        Comment: "Sublime Text 4 stores unsaved (temporary) files and its content in its .sublime_session files"

# Documentation
# https://superuser.com/questions/894021/where-does-sublime-text-store-its-un-saved-windows
# https://forum.sublimetext.com/t/restoring-files-saved-in-auto-save-session-sublime-session/25654/2
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
