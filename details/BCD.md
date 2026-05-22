# 🎯 **BCD**
### `File Name: BCD.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Troy Larson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Boot Configuration Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from BCD to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate BCD events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit BCD storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Boot Configuration Files
Author: Troy Larson
Version: 1.0
Id: eedec61a-bae4-4e96-a2cd-b6b30aa5a786
RecreateDirectories: true
Targets:
    -
        Name: BCD
        Category: Registry
        Path: C:\Boot\
        FileMask: BCD
    -
        Name: BCD Logs
        Category: Registry
        Path: C:\Boot\
        FileMask: 'BCD.LOG*'

# Documentation
# https://www.champlain.edu/Documents/LCDI/archive/Volume-shadow-Report_Redux.pdf
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
