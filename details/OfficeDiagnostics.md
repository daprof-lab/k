# 🎯 **Office Diagnostics**
### `File Name: OfficeDiagnostics.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** teddy-ROxPin  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Office Diagnostics

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Office Diagnostics to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Office Diagnostics events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Office Diagnostics storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Office Diagnostics
Author: teddy-ROxPin
Version: 1.0
Id: 5ef604c2-e76b-40a0-9150-6b6715f2ebd7
RecreateDirectories: true
Targets:
    -
        Name: Office Diagnostics
        Category: Execution
        Path: C:\Users\%user%\AppData\Local\Diagnostics\
        FileMask: "PCW.debugreport.xml"
        Comment: "Payloads for CVE-2022-30190 ('Follina') will be in this log"
    -
        Name: Office Elevated Diagnostics
        Category: Execution
        Path: C:\Users\%user%\AppData\Local\ElevatedDiagnostics\
        FileMask: "PCW.debugreport.xml"
        Comment: "Payloads for CVE-2022-30190 ('Follina') will be in this log"

# Documentation
# https://twitter.com/nas_bench/status/1531718490494844928?cxt=HHwWgIC-ncH24MEqAAAA
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
