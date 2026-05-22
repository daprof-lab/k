# 🎯 **Messaging Clients**
### `File Name: MessagingClients.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Gregor Wegberg  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Messaging and communication apps

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Messaging Clients to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Messaging Clients events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Messaging Clients storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Messaging and communication apps
Author: Gregor Wegberg
Version: 1.0
Id: c6d3b238-0be7-4764-afa7-9224e46097c0
RecreateDirectories: true
Targets:
    -
        Name: IRC Clients
        Category: Compound
        Path: IRCClients.tkape
    -
        Name: Cisco Jabber
        Category: Apps
        Path: CiscoJabber.tkape
    -
        Name: Discord
        Category: Apps
        Path: Discord.tkape
    -
        Name: Mattermost
        Category: Apps
        Path: Mattermost.tkape
    -
        Name: Microsoft Teams
        Category: Apps
        Path: MicrosoftTeams.tkape
    -
        Name: Signal
        Category: Apps
        Path: Signal.tkape
    -
        Name: Skype
        Category: Apps
        Path: Skype.tkape
    -
        Name: Slack
        Category: Apps
        Path: Slack.tkape
    -
        Name: Telegram
        Category: Apps
        Path: Telegram.tkape
    -
        Name: Viber
        Category: Apps
        Path: Viber.tkape
    -
        Name: WhatsApp
        Category: Apps
        Path: WhatsApp.tkape

# Documentation
# For those looking to contribute to this list, check here for ideas:
# - https://en.wikipedia.org/wiki/Comparison_of_cross-platform_instant_messaging_clients
# - https://en.wikipedia.org/wiki/Comparison_of_user_features_of_messaging_platforms
# Install one of the applications not covered above and find where useful information is stored. If useful information can be located, make an individual Target for it and place in the appropriate folder. Then, include that Target in the appropriate Compound Target.
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
