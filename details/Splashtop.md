# 🎯 **Splashtop Remote**
### `File Name: Splashtop.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Andrew Rathbun / Yogesh Khatri  
**Version:** 2.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Splashtop local log structures, active sessions, and client credentials databases.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Splashtop Remote to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Splashtop Remote events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Splashtop Remote storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Splashtop
Author: Andrew Rathbun, Yogesh Khatri, Evangelos Dragonas
Version: 2.0
Id: 940c768b-b32c-4b4b-82d7-68385ff470c8

RecreateDirectories: true
Targets:
    -
        Name: Splashtop Log Files
        Category: Software
        Path: C:\Program Files*\Splashtop\Splashtop Remote\Server\log
        Recursive: true
        Comment: "Collects logs for Splashtop"
    -
        Name: Splashtop Log Files in ProgramData
        Category: Software
        Path: C:\ProgramData\Splashtop\Temp\log
        Recursive: true
        Comment: "Collects logs for Splashtop"
    -
        Name: Splashtop Gateway Log Files
        Category: Software
        Path: C:\Program Files*\Splashtop\Splashtop Remote\Splashtop Gateway\log
        Recursive: true
        Comment: "Collects logs for Splashtop Gateway"
    -
        Name: Splashtop Enterprise/Business(legacy) Log Files in ProgramData
        Category: Software
        Path: C:\ProgramData\Splashtop\Splashtop Remote Client for ST*\*\log
        Recursive: true
        Comment: "Collects logs for Splashtop Enterprise/Business(legacy)"

# Documentation
# https://jsac.jpcert.or.jp/archive/2023/pdf/JSAC2023_1_1_yamashige-nakatani-tanaka_en.pdf
# https://www.synacktiv.com/en/publications/legitimate-rats-a-comprehensive-forensic-analysis-of-the-usual-suspects
# https://support-splashtoponprem.splashtop.com/hc/en-us/articles/900000385223-Log-files
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
