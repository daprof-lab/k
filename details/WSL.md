# 🎯 **WSL Filesystems**
### `File Name: WSL.tkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Matt Dawson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
WSL configuration states and raw ext4 file containers representing virtualized Linux environments.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from WSL Filesystems to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate WSL Filesystems events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit WSL Filesystems storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: All Windows Subsystem for Linux targets
Author: Matt Dawson
Version: 1.0
Id: 6f1d49c3-e558-4d59-bf33-5ce8bb611102
RecreateDirectories: true
Targets:
    -
        Name: Debian
        Category: WSL
        Path: Debian.tkape
    -
        Name: Ubuntu
        Category: WSL
        Path: Ubuntu.tkape
    -
        Name: Kali
        Category: WSL
        Path: Kali.tkape
    -
        Name: openSUSE
        Category: WSL
        Path: openSUSE.tkape
    -
        Name: SUSE Linux Enterprise Server
        Category: WSL
        Path: SUSELinuxEnterpriseServer.tkape

# Documentation
# N/A
```
---

[⬅️ Back to Memory & Virtualization Targets](../memory_virtualization_targets.md)
