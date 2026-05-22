# 🎯 **Power Shell7config**
### `File Name: PowerShell7Config.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
PowerShell 7 Runtime Config

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Power Shell7config to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Power Shell7config events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Power Shell7config storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: PowerShell 7 Runtime Config
Author: Andrew Rathbun
Version: 1.0
Id: 41963eda-a586-464f-aee3-1473e38ddd85
RecreateDirectories: true
Targets:
    -
        Name: PowerShell 7 Config JSON
        Category: PowerShell
        Path: C:\Program Files\PowerShell\7
        FileMask: 'powershell.config.json'

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_powershell_config?view=powershell-7.3
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
