# **📱 Application Execution & Data**

{% hint style="info" %}

**Investigator Note:** Find tools here related to end-user applications, chat clients, productivity software, and peer-to-peer (P2P) filesharing. Essential for mapping user behavior, communications, and data exfiltration.

{% endhint %}

---

## **Explore Category Contents**

Select a sub-page below to browse the full forensic components in this category.

### 🎯 [Browse Targets (.tkape)](applications_targets.md)
> Collect raw forensic artifacts from user applications, chat clients, and productivity software.
> * **16 Targets Available** (e.g., `Slack.tkape`, `Discord.tkape`, `Notepad.tkape`)
> * [View All Targets &rarr;](applications_targets.md)

### ⚙️ [Browse Modules (.mkape)](applications_modules.md)
> Process the collected application artifacts to reconstruct history, chats, and active states.
> * **5 Modules Available** (e.g., `TeamsParser.mkape`, `WindowsNotepadParser.mkape`, `SQLite3_TeraCopy_Main.mkape`)
> * [View All Modules &rarr;](applications_modules.md)

---

## 📊 **Category Quick Stats**

| Metric | Details |
| :--- | :--- |
| **📁 Focus Area** | End-user applications, chat messengers, IDEs, torrent clients, and recent media history |
| **🎯 Total Targets** | **16** configuration files |
| **⚙️ Total Modules** | **5** parser plugins |

---

## 💡 **Key Highlighted Artifacts**

* **Chat Applications (Slack, Teams, Discord, WhatsApp)**: Crucial for determining corporate communications, lateral exfiltration, or social engineering attacks.
* **Text Editors (Notepad++, Notepad, VS Code)**: Recover unsaved notes, recently accessed source files, and development artifacts.
* **P2P & Media (uTorrent, VLC)**: Track media consumption and file exfiltration via peer-to-peer clients.
* **Snipping Tool & Snip and Sketch**: Collect cached screenshots to find high-value visible data cached on disk.