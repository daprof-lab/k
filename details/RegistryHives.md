# 🎯 **Master Registry Package**
### `File Name: RegistryHives.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Eric Zimmerman  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
Collects all user-level profiles and system registry hives simultaneously.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Master Registry Package to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Master Registry Package events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Master Registry Package storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: System and user related Registry hives
Author: Eric Zimmerman
Version: 1.2
Id: 76af6086-bd0b-429f-bfd7-4a8e8ff8138f
RecreateDirectories: true
Targets:
    -
        Name: System Registry Files
        Category: Registry
        Path: RegistryHivesSystem.tkape
    -
        Name: User Level Registry Files
        Category: Registry
        Path: RegistryHivesUser.tkape
    -
        Name: MSIX Application Registry Files
        Category: Registry
        Path: RegistryHivesMSIXApps.tkape

# Documentation
# Please note, this Compound Target does NOT include the RegistryHivesOther Target on purpose. While they are technically Registry hives, they are not currently identified as being forensically significant.
# However, for the purpose of KapeResearch_Registry Modules that will dump hives from the ROOT key to JSON for the purpose of (hopefully) finding forensically relevant data in one of these Registry hives, RegistryHivesOther exists for that very reason.
# If you want to pull every single Registry hive possible, combine this Compound Target along with the RegistryHivesOther Target.
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
