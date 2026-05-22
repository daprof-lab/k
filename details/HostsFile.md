# 🎯 **Hosts File**
### `File Name: HostsFile.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Hosts file

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Hosts File to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Hosts File events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Hosts File storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Hosts file
Author: Max Zabuty
Version: 1.0
Id: 6f045c9b-5d0c-42ec-ab09-050b9853a5e9
RecreateDirectories: true
Targets:
    -
        Name: HostsFile
        Category: HostsFile
        Path: C:\Windows\System32\drivers\etc\
        FileMask: 'Hosts'

# Documentation
# N/A
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
