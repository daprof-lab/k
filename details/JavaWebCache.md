# 🎯 **Java Web Cache**
### `File Name: JavaWebCache.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** piesecurity  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Java WebStart Cache - (IDX Files)

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Java Web Cache to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Java Web Cache events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Java Web Cache storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Java WebStart Cache - (IDX Files)
Author: piesecurity
Version: 1.0
Id: 4dc2e35c-fc20-45f6-89a6-5d729596c522
RecreateDirectories: true
Targets:
    -
        Name: Java WebStart Cache User Level - Default
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Sun\Java\Deployment\cache\*\*\
        FileMask: '*.idx'
    -
        Name: Java WebStart Cache User Level - IE Protected Mode
        Category: Communications
        Path: C:\Users\%user%\AppData\LocalLow\Sun\Java\Deployment\cache\*\*\
        FileMask: '*.idx'
    -
        Name: Java WebStart Cache System level
        Category: Communications
        Path: C:\Windows\System32\config\systemprofile\AppData\Local\Sun\Java\Deployment\cache\*\*\
        FileMask: '*.idx'
    -
        Name: Java WebStart Cache System level
        Category: Communications
        Path: C:\Windows.old\Windows\System32\config\systemprofile\AppData\Local\Sun\Java\Deployment\cache\*\*\
        FileMask: '*.idx'
    -
        Name: Java WebStart Cache System level - IE Protected Mode
        Category: Communications
        Path: C:\Windows\System32\config\systemprofile\AppData\LocalLow\Sun\Java\Deployment\cache\*\*\
        FileMask: '*.idx'
    -
        Name: Java WebStart Cache System level - IE Protected Mode
        Category: Communications
        Path: C:\Windows.old\Windows\System32\config\systemprofile\AppData\LocalLow\Sun\Java\Deployment\cache\*\*\
        FileMask: '*.idx'
    -
        Name: Java WebStart Cache System level (SysWow64)
        Category: Communications
        Path: C:\Windows\SysWOW64\config\systemprofile\AppData\Local\Sun\Java\Deployment\cache\*\*\
        FileMask: '*.idx'
    -
        Name: Java WebStart Cache System level (SysWow64)
        Category: Communications
        Path: C:\Windows.old\Windows\SysWOW64\config\systemprofile\AppData\Local\Sun\Java\Deployment\cache\*\*\
        FileMask: '*.idx'
    -
        Name: Java WebStart Cache System level (SysWow64) - IE Protected Mode
        Category: Communications
        Path: C:\Windows\SysWOW64\config\systemprofile\AppData\LocalLow\Sun\Java\Deployment\cache\*\*\
        FileMask: '*.idx'
    -
        Name: Java WebStart Cache System level (SysWow64) - IE Protected Mode
        Category: Communications
        Path: C:\Windows.old\Windows\SysWOW64\config\systemprofile\AppData\LocalLow\Sun\Java\Deployment\cache\*\*\
        FileMask: '*.idx'
    -
        Name: Java WebStart Cache User Level - XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Application Data\Sun\Java\Deployment\cache\*\*\
        FileMask: '*.idx'

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
