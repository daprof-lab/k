# 🎯 **Atera Agent**
### `File Name: AteraAgent.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
AteraAgent

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Atera Agent to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Atera Agent events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Atera Agent storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: AteraAgent
Author: Andrew Rathbun
Version: 1.0
Id: ca980fbe-fe64-490c-ac94-0bcdd8e8bce1
RecreateDirectories: true
Targets:
    -
        Name: AteraAgent .ini files
        Category: Software
        Path: C:\Program Files\ATERA Networks\AteraAgent
        FileMask: '*.ini'
        Recursive: true
        Comment: "Collects logs for AteraAgent"
    -
        Name: AteraAgent Logs
        Category: Software
        Path: C:\Program Files\ATERA Networks\AteraAgent
        FileMask: '*.txt'
        Recursive: true
        Comment: "Collects logs for AteraAgent"
    -
        Name: AteraAgent Logs
        Category: Software
        Path: C:\Program Files\ATERA Networks\AteraAgent
        FileMask: '*.db'
        Recursive: true
        Comment: "Collects logs for AteraAgent"
    -
        Name: AteraAgent Logs
        Category: Software
        Path: C:\Program Files\ATERA Networks\AteraAgent
        FileMask: '*.config'
        Recursive: true
        Comment: "Collects logs for AteraAgent"
    -
        Name: AteraAgent Logs
        Category: Software
        Path: C:\Program Files\ATERA Networks\AteraAgent
        FileMask: '*.cfg'
        Recursive: true
        Comment: "Collects logs for AteraAgent"

# Documentation
# https://www.advintel.io/post/secret-backdoor-behind-conti-ransomware-operation-introducing-atera-agent
# https://www.pcrisk.com/internet-threat-news/21576-conti-ransomwares-secret-backdoor-discovered
# https://news.sophos.com/en-us/2021/09/03/conti-affiliates-use-proxyshell-exchange-exploit-in-ransomware-attacks/
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
