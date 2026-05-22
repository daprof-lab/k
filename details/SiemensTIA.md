# 🎯 **Siemens TIA**
### `File Name: SiemensTIA.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Olaf Schwarz (@b00010111)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Copy Siemens TIA Settings

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Siemens TIA to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Siemens TIA events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Siemens TIA storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Copy Siemens TIA Settings
Author: Olaf Schwarz (@b00010111)
Version: 1.0
Id: 0e43ebe5-cd5b-4487-ab41-66f46ebfc5c9
RecreateDirectories: true
Targets:
    -
        Name: Siemens TIA Settings
        Category: ICS
        Path: C:\Users\%user%\AppData\Roaming\Siemens\Automation\Portal*\Settings\
        Recursive: true

# Documentation
# The Settings.xml file contains information about opened project files, last storge location used and so on.
# You can find more info on the Settings.xml file in part 2 of this blog post series: https://blog.nviso.eu/series/investigating-an-engineering-workstation/
# There is a tool available to parse the Settings.xml file: https://github.com/00010111/parse_tSettings The verbose output also provides information on the content of the Settings.xml file
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
