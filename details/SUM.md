# 🎯 **SUM**
### `File Name: SUM.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun, Yogesh Khatri  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
SUM Database

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from SUM to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate SUM events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit SUM storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: SUM Database
Author: Andrew Rathbun, Yogesh Khatri
Version: 1.1
Id: f548fd75-def3-4129-bd50-4933c98fe65a
RecreateDirectories: true
Targets:
    -
        Name: SUM Database (.mdb files)
        Category: Logs
        Path: C:\Windows\System32\LogFiles\SUM\
        Recursive: true
        Comment: "Grabs Current.mdb, SystemIdentity.mdb, [GUID].mdb and associated ESE db log files"

# Documentation
# https://advisory.kpmg.us/blog/2021/digital-forensics-incident-response.html
# https://svch0st.medium.com/windows-user-access-logs-ual-9580f1100635
# https://github.com/EricZimmerman/Sum - be sure to follow the guide here for repairing the DB prior to parsing
# https://github.com/brimorlabs/KStrike
# https://docs.microsoft.com/en-us/windows-server/administration/user-access-logging/manage-user-access-logging
# https://www.thedfirspot.com/post/sum-ual-investigating-server-access-with-user-access-logging
# LogFiles.tkape Target acquires this as well, but this is a more specific Target in that it ONLY grabs the SUM Database artifacts and nothing else, unlike LogFiles.tkape
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
