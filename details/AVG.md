# 🎯 **AVG**
### `File Name: AVG.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Kirtan Shah and Dhiral Panjwani  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
AVG Antivirus Data

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from AVG to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate AVG events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit AVG storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: AVG Antivirus Data
Author: Kirtan Shah and Dhiral Panjwani
Version: 1.1
Id: b0a4112d-e7f6-4e47-a186-7459cf8b3ab4
RecreateDirectories: true
Targets:
    -
        Name: AVG AV Logs (XP)
        Category: Antivirus
        Path: C:\Documents and Settings\All Users\Application Data\AVG\Antivirus\log
        Recursive: true
    -
        Name: AVG AV Report Logs (XP)
        Category: Antivirus
        Path: C:\Documents and Settings\All Users\Application Data\AVG\Antivirus\report
        Recursive: true
    -
        Name: AVG AV Logs
        Category: Antivirus
        Path: C:\ProgramData\AVG\Antivirus\log
        Recursive: true
    -
        Name: AVG Report Logs
        Category: Antivirus
        Path: C:\ProgramData\AVG\Antivirus\report
        Recursive: true
    -
        Name: AVG Persistent Logs
        Category: Antivirus
        Path: C:\ProgramData\AVG\Persistent Data\Antivirus\Logs
        Recursive: true
    -
        Name: AVG FileInfo DB
        Category: Antivirus
        Path: C:\ProgramData\AVG\Antivirus
        FileMask: FileInfo2.db
        Recursive: true
    -
        Name: AVG lsdbj2 JSON
        Category: Antivirus
        Path: C:\ProgramData\AVG\Antivirus
        FileMask: lsdb2.json

# Documentation
# https://businesshelp.avast.com/Content/Products/General_Help/LogLocations/BaseAntivirusLogs.htm
# https://forensafe.com/blogs/windows_avg.html
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
