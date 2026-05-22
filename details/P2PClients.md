# 🎯 **P2pclients**
### `File Name: P2PClients.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Andrew Rathbun  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
P2P Clients

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from P2pclients to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate P2pclients events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit P2pclients storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: P2P Clients
Author: Andrew Rathbun
Version: 1.1
Id: 4357b5ff-0bd4-41c0-a644-463ea0e14c48
RecreateDirectories: true
Targets:
    -
        Name: DC++
        Category: FileDownload
        Path: DC++.tkape
    -
        Name: eMule
        Category: FileDownload
        Path: eMule.tkape
    -
        Name: FrostWire
        Category: FileDownload
        Path: FrostWire.tkape
    -
        Name: Gigatribe
        Category: FileDownload
        Path: Gigatribe.tkape
    -
        Name: Shareaza
        Category: FileDownload
        Path: Shareaza.tkape
    -
        Name: Soulseek
        Category: FileDownload
        Path: Soulseek.tkape

# For those looking to contribute to this list, check here for ideas: https://en.wikipedia.org/wiki/Comparison_of_file-sharing_applications.
# Install one of the applications not covered above and find where useful information is stored. If useful information can be located, make an individual Target for it and place in the appropriate folder. Then, include that Target in the appropriate Compound Target.
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
