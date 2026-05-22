# 🎯 **Ircclients**
### `File Name: IRCClients.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
IRC Clients

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Ircclients to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Ircclients events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Ircclients storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: IRC Clients
Author: Andrew Rathbun
Version: 1.0
Id: 295e5eeb-a836-4ff8-88b7-1caf47c95701
RecreateDirectories: true
Targets:
    -
        Name: HexChat
        Category: Communications
        Path: HexChat.tkape
    -
        Name: IceChat
        Category: Communications
        Path: IceChat.tkape
    -
        Name: mIRC
        Category: Communications
        Path: mIRC.tkape

# Documentation
# For those looking to contribute to this list, check here for ideas: https://en.wikipedia.org/wiki/Comparison_of_Internet_Relay_Chat_clients.
# Install one of the applications not covered above and find where useful information is stored. If useful information can be located, make an individual Target for it and place in the appropriate folder. Then, include that Target in the appropriate Compound Target.
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
