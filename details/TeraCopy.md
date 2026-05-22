# 🎯 **Tera Copy**
### `File Name: TeraCopy.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Kevin Pagano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
TeraCopy log history

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Tera Copy to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Tera Copy events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Tera Copy storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: 'TeraCopy log history'
Author: Kevin Pagano
Version: 1.0
Id: 111ee9ac-f8b3-4026-a3c9-90f76b6b2cb4
RecreateDirectories: true
Targets:
    -
        Name: TeraCopy
        Category: TeraCopy
        Path: C:\Users\%user%\AppData\Roaming\TeraCopy\
        Recursive: true

# Documentation
# https://www.kraftkennedy.com/teracopy-forensics-finding-elusive-copy-log/
# https://www.stark4n6.com/2018/11/teracopy-forensic-analysis-part-1.html
# https://www.stark4n6.com/2018/11/teracopy-forensic-analysis-part-2.html
# # The SQLite database(s) this Target collects can be parsed with SQLECmd using the following map(s): https://github.com/EricZimmerman/SQLECmd/blob/master/SQLMap/Maps/Windows_TeraCopy_History.smap and https://github.com/EricZimmerman/SQLECmd/blob/master/SQLMap/Maps/Windows_TeraCopy_MainDB.smap
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
