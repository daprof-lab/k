# 🎯 **Bitdefender Antivirus**
### `File Name: Bitdefender.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Drew Ervin, Ahmed Elshaer  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Antivirus detection logs, file scanning logs, and quarantine configurations.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Bitdefender Antivirus to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Bitdefender Antivirus events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Bitdefender Antivirus storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Bitdefender Antivirus Data
Author: Drew Ervin, Ahmed Elshaer
Version: 1.1
Id: e48c32bf-4069-4f79-acac-4ed181fa84c9
RecreateDirectories: true
Targets:
    -
        Name: Bitdefender Endpoint Security Logs
        Category: Antivirus
        Path: C:\ProgramData\Bitdefender\Endpoint Security\Logs\
        Recursive: true
    -
        Name: Bitdefender Internet Security Logs
        Category: Antivirus
        Path: C:\ProgramData\Bitdefender\Desktop\Profiles\Logs\
        Recursive: true
    -
        Name: Bitdefender SQLite DB Files
        Category: Antivirus
        Path: C:\Program Files*\Bitdefender*\
        Recursive: true
        FileMask: regex:*.+\.(db|db-wal|db-shm)
        Comment: "Bitdefender SQLite databases"

# Documentation
# https://anelshaer.medium.com/browsing-history-in-bitdefender-dbs-2d63ba940f92
# https://forensafe.com/blogs/windows_bitdefender.html
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
