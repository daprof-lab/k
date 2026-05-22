# 🎯 **Netclrusage Logs**
### `File Name: NETCLRUsageLogs.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Matias Davaro, Thomas DIOT (Qazeer)  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
.NET CLR UsageLogs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Netclrusage Logs to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Netclrusage Logs events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Netclrusage Logs storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: .NET CLR UsageLogs
Author: Matias Davaro, Thomas DIOT (Qazeer)
Version: 1.1
Id: f127a2a3-d86f-4ede-96e7-52193db822ad
RecreateDirectories: true
Targets:
    -
        Name: .NET CLR UsageLogs (user-scoped)
        Category: .NET CLR UsageLogs
        Path: C:\Users\%user%\AppData\Local\Microsoft\CLR_*\
        Recursive: true
        FileMask: '*.log'
    -
        Name: .NET CLR UsageLogs (system-scoped)
        Category: .NET CLR UsageLogs
        Path: C:\Windows*\System32\config\systemprofile\AppData\Local\Microsoft\CLR_*\
        Recursive: true
        FileMask: '*.log'

# Documentation
# https://bohops.com/2021/03/16/investigating-net-clr-usage-log-tampering-techniques-for-edr-evasion/
# https://blog.menasec.net/2019/07/interesting-difr-traces-of-net-clr.html
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
