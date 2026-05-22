# 🎯 **Rdcman**
### `File Name: RDCMan.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** ogmini  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
A Target to collect files that are related to RDCMan

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Rdcman to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Rdcman events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Rdcman storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: A Target to collect files that are related to RDCMan
Author: ogmini
Version: 1.0
Id: 29301648-40da-46a6-a33b-cfdde51d01d6
RecreateDirectories: true
Targets:
    -
        Name: RDG Files
        Category: Configuration
        Path: C:\
        Recursive: true
        FileMask: "*.rdg"
        Comment: "These files store the information about Remote Desktop Groups."
    -
        Name: Old RDG Files
        Category: Configuration
        Path: C:\
        Recursive: true
        FileMask: "*.rdg.old"
        Comment: "These files store the information about Remote Desktop Groups. They are backups created when upgrading to a newer version of RDCMan."
    -
        Name: RDCMan Settings File
        Category: Configuration
        Path: C:\Users\%user%\AppData\Local\Microsoft\Remote Desktop Connection Manager\
        Recursive: true
        FileMask: "*.settings"
        Comment: "Stores settings information for RDCMan."
    -
        Name: RDCMan Personal Certificate
        Category: Certificate
        Path: C:\Users%user%\AppData\Roaming\Microsoft\SystemCertificates\My\Certificates
        Comment: "Encryption Certificate for stored passwords"

# Documentation
# https://ogmini.github.io/2025/05/06/Researching-RDCMan.html
# https://ogmini.github.io/2025/05/07/Researching-RDCMan-Part-2.html
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
