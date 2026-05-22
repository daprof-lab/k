# 🎯 **Supremo Remote Desktop**
### `File Name: SupremoRemoteDesktop.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** epoxigen  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Supremo Remote Desktop Control Logs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Supremo Remote Desktop to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Supremo Remote Desktop events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Supremo Remote Desktop storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Supremo Remote Desktop Control Logs
Author: epoxigen
Version: 1.1
Id: 0d88cf87-bbc5-4bcf-bb4f-2bc9a3e300f0
RecreateDirectories: true
Targets:
    -
        Name: Supremo Connection Logs
        Category: Communications
        Path: C:\ProgramData\SupremoRemoteDesktop\Log
        FileMask: '*.log'
        Comment: "Includes Supremo.00.Client.log and Supremo.00.Incoming.log"
    -
        Name: Supremo File Transfer Inbox
        Category: Communications
        Path: C:\ProgramData\SupremoRemoteDesktop\Inbox
        Comment: "Includes files transferred to the inbox folder during a remote session. See Supremo.00.FileTransfer.log"

# Documentation
# https://www.supremocontrol.com/
# Supremo Remote Desktop is a Remote Access Tool similar to TeamViewer.
# Supremo.00.Incoming.log is logging the incoming remote sessions.
# Supremo.00.ReportsQueue.log is logging device related information of remote sessions.
# Supremo.00.Client.log is logging application events such as program start/exit and the client-server-connections to the Supremo servers.
# Supremo.00.FileTransfer.log is logging file transfers between remote sessions.
# Keep in mind: Files can be transferred to any location on the remote client, not only into the Inbox folder.
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
