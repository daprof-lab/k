# 🎯 **Msty Database**
### `File Name: MstyDatabase.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** DReneau  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Msty is a UI to interact with large language models (LLMs)

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Msty Database to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Msty Database events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Msty Database storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Msty is a UI to interact with large language models (LLMs)
Author: DReneau
Version: 1.0
Id: ee102f02-b8f3-4d4f-8a0c-b6b357405e64
RecreateDirectories: true
Targets:
    -
        Name: Msty Artificial Intelligence
        Category: FileKnowledge
        Path: C:\Users\%user%\AppData\Roaming\Msty\
        FileMask: '*.db'
        Comment: Msty database includes API keys, chat messages, chat sessions, knowledge stack, etc.

# Documentation
# https://msty.app/
# https://docs.msty.app/getting-started/onboarding
# https://github.com/cloudstack-llc/msty-docs
# Msty is a front-end UI used to host local language models. Msty is developed by Cloudstack, LLC.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
