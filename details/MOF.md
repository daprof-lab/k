# 🎯 **MOF**
### `File Name: MOF.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
MOF files (WMI)

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from MOF to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate MOF events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit MOF storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: MOF files (WMI)
Author: Eric Zimmerman
Version: 1.0
Id: 4fc9820c-3d30-4a38-2e48-5e0b745a4b0c
RecreateDirectories: true
Targets:
    -
        Name: MOF files
        Category: WMI
        Path: C:\
        Recursive: true
        FileMask: '*.MOF'

# Documentation
# https://digital-forensics.sans.org/media/DFPS_FOR508_v4.4_1-19.pdf
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
