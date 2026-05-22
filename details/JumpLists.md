# 🎯 **Jump Lists**
### `File Name: JumpLists.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Max Zabuty  
**Version:** 1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Jump lists

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Jump Lists to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Jump Lists events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Jump Lists storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Jump lists
Author: Max Zabuty
Version: 1
Id: 2e354bdc-e418-438e-8439-c21c83c64e11
RecreateDirectories: true
Targets:
    -
        Name: JumpLists from CustomDestinations
        Category: JumpLists
        Path: C:\Users\%user%\AppData\Roaming\Microsoft\Windows\Recent\AutomaticDestinations\
        Recursive: true
    -
        Name: JumpLists from CustomDestinations
        Category: JumpLists
        Path: C:\Users\%user%\AppData\Roaming\Microsoft\Windows\Recent\CustomDestinations\
        Recursive: true

# Documentation
# https://www.forensafe.com/blogs/jumplist.html
# https://dfir.pubpub.org/pub/wfuxlu9v/release/1
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
