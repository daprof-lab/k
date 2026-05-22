# 🎯 **Windows Copilot Recall**
### `File Name: WindowsCopilotRecall.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Zach Stanford/Phill Moore  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows Copilot+ Recall

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Windows Copilot Recall to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Windows Copilot Recall events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Windows Copilot Recall storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Windows Copilot+ Recall
Author: Zach Stanford/Phill Moore
Version: 1.0
Id: 333b716c-468e-48e7-960b-248526029dda
RecreateDirectories: true
Targets:
    -
        Name: Recall folder
        Category: FileKnowledge
        Path: C:\Users\*\AppData\Local\CoreAIPlatform.00\UKP\
        Recursive: true

# Documentation
# Files and folder related to Copilot+ Recall
# https://doublepulsar.com/recall-stealing-everything-youve-ever-typed-or-viewed-on-your-own-windows-pc-is-now-possible-da3e12e9465e
# https://cybercx.com.au/blog/forensic-applications-of-microsoft-recall/
# https://github.com/xaitax/TotalRecall
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
