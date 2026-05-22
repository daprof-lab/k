# 🎯 **Usenet Clients**
### `File Name: UsenetClients.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Usenet Clients

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Usenet Clients to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Usenet Clients events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Usenet Clients storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Usenet Clients
Author: Andrew Rathbun
Version: 1.0
Id: 2aef5440-16f8-4720-ae40-c2cad380da8d
RecreateDirectories: true
Targets:
    -
        Name: NewsbinPro
        Category: FileDownload
        Path: NewsbinPro.tkape
    -
        Name: Newsleecher
        Category: FileDownload
        Path: Newsleecher.tkape
    -
        Name: NZBGet
        Category: FileDownload
        Path: NZBGet.tkape
    -
        Name: SABnbzd
        Category: FileDownload
        Path: SABnbzd.tkape

# Documentation
# For those looking to contribute to this list, check here for ideas: https://en.wikipedia.org/wiki/Comparison_of_Usenet_newsreaders.
# Install one of the applications not covered above and find where useful information is stored. If useful information can be located, make an individual Target for it and place in the appropriate folder. Then, include that Target in the appropriate Compound Target.
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
