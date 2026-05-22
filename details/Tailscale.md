# 🎯 **Tailscale**
### `File Name: Tailscale.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** ogmini  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
A Target to collect files from Tailscale

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Tailscale to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Tailscale events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Tailscale storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: A Target to collect files from Tailscale
Author: ogmini
Version: 0.1
Id: b483f009-313f-434f-a7ad-5d9806a90ae4
RecreateDirectories: true
Targets:
    -
        Name: Temp Install Files
        Category: Network
        Path: C:\Users\%user%\AppData\Local\temp\
        FileMask: "Tailscale*.log"
        Comment: "Tailscale Installation Log Files"
    -
        Name: Local App Data Files
        Category: Network
        Path: C:\Users\%user%\AppData\Local\Tailscale\
        Recursive: true
        Comment: "Local App Data Files and Avatars"
    -
        Name: Tailscale Program Data
        Category: Network
        Path: C:\ProgramData\Tailscale\
        Recursive: true
        Comment: "Tailscale Configuration and Log files. Partial file transfers."

# Documentation
# In progress - https://ogmini.github.io/tags.html#Tailscale
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
