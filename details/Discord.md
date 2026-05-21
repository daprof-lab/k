# 🎯 **Discord App**
### `File Name: Discord.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Christian Johansen / Matt Dawson  
**Version:** 2.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Discord LevelDB databases, application cache, and web assets cache containing user messaging states.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Discord App to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Discord App events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Discord App storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Discord Cache and LevelDB Files
Author: Christian Johansen and Matt Dawson
Version: 2.0
Id: 5a44a0ef-db56-4103-8748-797432487028
RecreateDirectories: true
Targets:
    -
        Name: Discord Cache Files
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\discord\cache\
        Recursive: true
        Comment: "Gets cached data from Discord app"
    -
        Name: Discord Local Storage LevelDB Files
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\discord\local storage\leveldb\
        Recursive: true
        Comment: "Gets LevelDB database from Discord app"

# Documentation
# https://abrignoni.blogspot.com/2018/03/finding-discord-app-chats-in-windows.html
# https://abrignoni.blogspot.com/2020/08/update-on-discord-forensic-artifacts.html
# https://www.champlain.edu/Documents/LCDI/ApplicationAnalysis_S17.pdf
# https://www.forensafe.com/blogs/discord.html
# Discord is a free voice, video, and text chat app that's used by tens of millions of people ages 13+ to talk and hang out with their communities and friends.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
