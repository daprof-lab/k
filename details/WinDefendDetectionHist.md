# 🎯 **Win Defend Detection Hist**
### `File Name: WinDefendDetectionHist.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Jordan Klepser  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows Defender Threat DetectionHistory files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Win Defend Detection Hist to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Win Defend Detection Hist events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Win Defend Detection Hist storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: 'Windows Defender Threat DetectionHistory files'
Author: Jordan Klepser
Version: 1.1
Id: a780af32-cb91-4e32-b946-0546cc123930
RecreateDirectories: false
Targets:
    -
        Name: DetectionHistory
        Category: Antivirus
        Path: C:\ProgramData\Microsoft\Windows Defender\Scans\History\Service\DetectionHistory\*\
        Recursive: true

# Documentation
# https://github.com/jklepsercyber/defender-detectionhistory-parser/blob/main/README.md
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
