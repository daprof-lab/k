# 🎯 **Group Policy**
### `File Name: GroupPolicy.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** piesecurity  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Current Group Policy Enforcement

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Group Policy to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Group Policy events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Group Policy storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Current Group Policy Enforcement
Author: piesecurity
Version: 1.1
Id: e5595e9c-ebab-41db-a688-fdffe91f6fcb
RecreateDirectories: true
Targets:
    -
        Name: Group Policy Files
        Category: Communications
        Path: C:\Windows\System32\grouppolicy\
        Recursive: true
    -
        Name: Computer Group Policy files
        Category: Communications
        Path: C:\ProgramData\Microsoft\Group Policy\History\
        Recursive: true
    -
        Name: User Group Policy files
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Group Policy\History
        Recursive: true
    -
        Name: Local Group Policy INI Files
        Category: Communications
        Path: C:\Windows.old\Windows\System32\grouppolicy\
        FileMask: '*.ini'
    -
        Name: Local Group Policy Files - Registry Policy Files
        Category: Communications
        Path: C:\Windows\System32\grouppolicy\
        FileMask: '*.pol'
    -
        Name: Local Group Policy Files - Registry Policy Files
        Category: Communications
        Path: C:\Windows.old\Windows\System32\grouppolicy\
        FileMask: '*.pol'
    -
        Name: Local Group Policy Files - Startup/Shutdown Scripts
        Category: Communications
        Path: C:\Windows\System32\grouppolicy\*\Scripts\
        Recursive: true
    -
        Name: Local Group Policy Files - Startup/Shutdown Scripts
        Category: Communications
        Path: C:\Windows.old\Windows\System32\grouppolicy\*\Scripts\
        Recursive: true

# Documentation
# https://medium.com/@grzegorztworek/gpo-group-policy-object-is-one-of-the-most-useful-features-of-the-windows-ecosystem-73b6eeab812
# https://learn.microsoft.com/en-us/troubleshoot/windows-server/group-policy/remove-this-item-if-it-is-no-longer-applied-option
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
