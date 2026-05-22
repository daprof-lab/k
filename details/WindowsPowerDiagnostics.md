# 🎯 **Windows Power Diagnostics**
### `File Name: WindowsPowerDiagnostics.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows Power Diagnostics

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Windows Power Diagnostics to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Windows Power Diagnostics events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Windows Power Diagnostics storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Windows Power Diagnostics
Author: Andrew Rathbun
Version: 1.0
Id: eefa0401-8cae-4c65-84f4-c2bffd0805b7
RecreateDirectories: true
Targets:
    -
        Name: Windows Power Diagnostics
        Category: Diagnostics
        Path: C:\ProgramData\Microsoft\Windows\Power Efficiency Diagnostics
        Recursive: true

# Documentation
# https://www.tenforums.com/tutorials/5148-create-power-efficiency-diagnostics-report-windows-10-a.html
# https://github.com/Chuyu-Team/Dism-Multi-language/issues/730
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
