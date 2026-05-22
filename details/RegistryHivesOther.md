# 🎯 **Registry Hives Other**
### `File Name: RegistryHivesOther.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Other Registry Hives

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Registry Hives Other to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Registry Hives Other events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Registry Hives Other storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Other Registry Hives
Author: Andrew Rathbun
Version: 1.1
Id: ea765ae7-b932-41a3-bd84-41fcdf236754
RecreateDirectories: true
Targets:
    -
        Name: BBI registry hive
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: BBI
    -
        Name: BBI registry hive
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\
        FileMask: BBI
    -
        Name: BBI registry transaction files
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: BBI.LOG*
    -
        Name: BBI registry transaction files
        Category: Registry
        Path: C:\Windows.old\System32\config\
        FileMask: BBI.LOG*
    -
        Name: BCD-Template registry hive
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: BCD-Template
    -
        Name: BCD-Template registry hive
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\
        FileMask: BCD-Template
    -
        Name: BCD-Template registry transaction files
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: BCD-Template.LOG*
    -
        Name: BCD-Template registry transaction files
        Category: Registry
        Path: C:\Windows.old\System32\config\
        FileMask: BCD-Template.LOG*
    -
        Name: COMPONENTS registry hive
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: COMPONENTS
    -
        Name: COMPONENTS registry hive
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\
        FileMask: COMPONENTS
    -
        Name: COMPONENTS registry transaction files
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: COMPONENTS.LOG*
    -
        Name: COMPONENTS registry transaction files
        Category: Registry
        Path: C:\Windows.old\System32\config\
        FileMask: COMPONENTS.LOG*
    -
        Name: DRIVERS registry hive
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: DRIVERS
    -
        Name: DRIVERS registry hive
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\
        FileMask: DRIVERS
    -
        Name: DRIVERS registry transaction files
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: DRIVERS.LOG*
    -
        Name: DRIVERS registry transaction files
        Category: Registry
        Path: C:\Windows.old\System32\config\
        FileMask: DRIVERS.LOG*
    -
        Name: ELAM registry hive
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: ELAM
    -
        Name: ELAM registry hive
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\
        FileMask: ELAM
    -
        Name: ELAM registry transaction files
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: ELAM.LOG*
    -
        Name: ELAM registry transaction files
        Category: Registry
        Path: C:\Windows.old\System32\config\
        FileMask: ELAM.LOG*
    -
        Name: userdiff registry hive
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: userdiff
    -
        Name: userdiff registry hive
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\
        FileMask: userdiff
    -
        Name: userdiff registry transaction files
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: userdiff.LOG*
    -
        Name: userdiff registry transaction files
        Category: Registry
        Path: C:\Windows.old\System32\config\
        FileMask: userdiff.LOG*
    -
        Name: VSMIDK registry hive
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: VSMIDK
    -
        Name: VSMIDK registry hive
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\
        FileMask: VSMIDK
    -
        Name: VSMIDK registry transaction files
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: VSMIDK.LOG*
    -
        Name: VSMIDK registry transaction files
        Category: Registry
        Path: C:\Windows.old\System32\config\
        FileMask: VSMIDK.LOG*

# Documentation
# https://medium.com/@lucideus/windows-registry-forensic-analysis-part-1-windows-forensics-manual-2018-2cb4da210125
# https://www.fireeye.com/blog/threat-research/2019/01/digging-up-the-past-windows-registry-forensics-revisited.html
# https://www.sans.org/security-resources/posters/windows-forensic-analysis/170/download
# https://www.youtube.com/watch?v=VYROU-ZwZX8
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
