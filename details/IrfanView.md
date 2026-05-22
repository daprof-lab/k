# 🎯 **Irfan View**
### `File Name: IrfanView.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
IrfanView

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Irfan View to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Irfan View events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Irfan View storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: IrfanView
Author: Andrew Rathbun
Version: 1.0
Id: 20c9d7ae-4efc-4eb0-b1c5-99504e1f6aac
RecreateDirectories: true
Targets:
    -
        Name: IrfanView Configuration File
        Category: FileKnowledge
        Path: C:\Users\%user%\AppData\Roaming\IrfanView\
        FileMask: i_view32.ini

# Documentation
# N/A
#
# This .ini file appears to contain record of the last 15 files opened by the user
# Additionally, this .ini file appears to contain the folder path the user will be presented with upon clicking on File -> Open within IrfanView
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
