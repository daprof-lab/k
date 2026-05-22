# 🎯 **Nzbget**
### `File Name: NZBGet.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
NZBGet

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Nzbget to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Nzbget events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Nzbget storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: NZBGet
Author: Andrew Rathbun
Version: 1.0
Id: 2c6ffe1d-f884-4065-a4e7-f81dd0d50ea7
RecreateDirectories: true
Targets:
    -
        Name: Usenet Clients - NZBGet Log File
        Category: FileDownload
        Path: C:\ProgramData\NZBGet\
        FileMask: 'nzbget.log'
        Comment: "Locates NZBGet download log file"
    -
        Name: Usenet Clients - NZBGet NZBs
        Category: FileDownload
        Path: C:\ProgramData\NZBGet\nzb\
        Comment: "Locates NZBGet NZB files that were used by the user"

# Documentation
# C:\ProgramData\NZBGet\nzbget.log is where a verbose log file exists.
# C:\ProgramData\NZBGet\nzb\ is where a replication of any NZBs used by the user will reside, regardless of where the NZB was residing prior to its use. This behavior is similar to Newsbin Pro above.
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
