# 🎯 **Rust Desk**
### `File Name: RustDesk.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
RustDesk

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Rust Desk to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Rust Desk events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Rust Desk storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: RustDesk
Author: Andrew Rathbun
Version: 1.1
Id: 849299a3-7d74-4006-bdfa-3525d7a2bd94
RecreateDirectories: true
Targets:
    -
        Name: RustDesk logs
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\RustDesk\
        Comment: "Collects all log files related to RustDesk"
    -
        Name: RustDesk logs
        Category: Communications
        Path: C:\Windows\ServiceProfiles\LocalService\AppData\Roaming\RustDesk\log\server
        Comment: "Collects all log files related to RustDesk"

# Documentation
# https://github.com/rustdesk/rustdesk/wiki/FAQ#access-logs
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
