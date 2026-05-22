# 🎯 **Quick Assist**
### `File Name: QuickAssist.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Microsoft Quick Assist/Remote Help

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Quick Assist to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Quick Assist events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Quick Assist storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Microsoft Quick Assist/Remote Help
Author: Andrew Rathbun
Version: 1.1
Id: 553b355d-8279-46ec-abd1-d43147583c6e
RecreateDirectories: true
Targets:
    -
        Name: Microsoft Quick Assist
        Category: RemoteAdmin
        Path: C:\Users\%user%\AppData\Local\Temp\QuickAssist
        Recursive: true
    -
        Name: Microsoft Remote Help
        Category: RemoteAdmin
        Path: C:\Users\%user%\AppData\Local\Temp\RemoteHelp
        Recursive: true

# Documentation
# https://support.microsoft.com/en-us/windows/solve-pc-problems-remotely-using-quick-assist-b077e31a-16f4-2529-1a47-21f6a9040bf3
# https://learn.microsoft.com/en-us/mem/intune/fundamentals/remote-help
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
