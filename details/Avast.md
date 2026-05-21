# 🎯 **Avast Antivirus**
### `File Name: Avast.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Drew Ervin / Dhiral Panjwani  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Collects threat databases, active scan logs, and quarantine records from Avast systems.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Avast Antivirus to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Avast Antivirus events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Avast Antivirus storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Avast Antivirus Data
Author: Drew Ervin and Dhiral Panjwani
Version: 1.1
Id: 8b625ea2-fafa-46be-8ba1-15efd1de2a53
RecreateDirectories: true
Targets:
    -
        Name: Avast AV Logs (XP)
        Category: Antivirus
        Path: C:\Documents And Settings\All Users\Application Data\Avast Software\Avast\Log\
        Recursive: true
    -
        Name: Avast AV Logs
        Category: Antivirus
        Path: C:\ProgramData\Avast Software\Avast\Log\
        Recursive: true
    -
        Name: Avast AV User Logs
        Category: Antivirus
        Path: C:\Users\%user%\Avast Software\Avast\Log\
        Recursive: true
    -
        Name: Avast AV Index
        Category: Antivirus
        Path: C:\ProgramData\Avast Software\Avast\Chest\
        FileMask: index.xml
    -
        Name: Avast Persistent Data Logs
        Category: Antivirus
        Path: C:\ProgramData\Avast Software\Persistent Data\Avast\Logs
        Recursive: true
    -
        Name: Avast Icarus Logs
        Category: Antivirus
        Path: C:\ProgramData\Avast Software\Icarus\Logs
        Recursive: true

# Documentation
# https://businesshelp.avast.com/Content/Products/General_Help/LogLocations/BaseAntivirusLogs.htm
# https://forensafe.com/blogs/windows_avast.html
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
