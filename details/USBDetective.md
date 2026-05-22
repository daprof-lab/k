# 🎯 **Usbdetective**
### `File Name: USBDetective.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Kevin Pagano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Collects files that can be input into USB Detective for parsing

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Usbdetective to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Usbdetective events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Usbdetective storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Collects files that can be input into USB Detective for parsing
Author: Kevin Pagano
Version: 1.0
Id: 6c3f8a69-f529-4201-a00e-067f6db7be8e
RecreateDirectories: true
Targets:
    -
        Name: USBDevicesLogs
        Category: USB
        Path: USBDevicesLogs.tkape
    -
        Name: RegistryHives
        Category: Registry Hives
        Path: RegistryHives.tkape
    -
        Name: Event Logs
        Category: EventLogs
        Path: EventLogs.tkape
    -
        Name: LNKFilesAndJumplists
        Category: File Access
        Path: LNKFilesAndJumplists.tkape
    -
        Name: Amcache
        Category: ApplicationCompatibility
        Path: Amcache.tkape

# Documentation
# For more information on USB Detective go here: https://usbdetective.com/features/
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
