# **☁️ Cloud Storage & Remote Access**

{% hint style="info" %}

**Investigator Note:** Look here for evidence of data exfiltration (Dropbox, OneDrive) and unauthorized lateral movement via Remote Desktop Protocol (RDP) or third-party remote management tools (AnyDesk, TeamViewer).

{% endhint %}

---

## **Explore Category Contents**

Select a sub-page below to browse the full forensic components in this category.

### 🎯 [Browse Targets (.tkape)](cloud_remote_targets.md)
> Collect raw forensic artifacts from remote desktop logs, management tools, and cloud storage folders.
> * **14 Targets Available** (e.g., `AnyDesk.tkape`, `RDPLogs.tkape`, `OneDrive_Metadata.tkape`)
> * [View All Targets &rarr;](cloud_remote_targets.md)

### ⚙️ [Browse Modules (.mkape)](cloud_remote_modules.md)
> Process cloud storage sync caches and remote access data files to reconstruct remote sessions or extract credentials.
> * **5 Modules Available** (e.g., `OneDriveExplorer.mkape`, `LogParser_RDPUsageEvents.mkape`, `WinSCP_Session.mkape`)
> * [View All Modules &rarr;](cloud_remote_modules.md)

---

## 📊 **Category Quick Stats**

| Metric | Details |
| :--- | :--- |
| **📁 Focus Area** | Remote access logs, remote monitoring & management (RMM) history, and cloud synchronization files |
| **🎯 Total Targets** | **14** configuration files |
| **⚙️ Total Modules** | **5** parser plugins |

---

## 💡 **Key Highlighted Artifacts**

* **RMM Tools (AnyDesk, TeamViewer, Splashtop, ScreenConnect, LogMeIn)**: Establish unauthorized connections, find incoming IP addresses, chat logs, session timings, and transferred file lists.
* **Remote Desktop Protocol (RDP Logs & Cache)**: Recover bitmap caches to visually reconstruct what a threat actor saw on screen during lateral movement, and audit terminal services events.
* **Cloud Storage Sync (OneDrive, Dropbox, Google Drive, MegaSync)**: Vital for auditing data exfiltration. Retrieve sync logs, folder structures, deleted files metadata, and local copy directories.
* **Credentials (MobaXterm, WinSCP)**: Determine if external administration profiles were parsed and compromised.