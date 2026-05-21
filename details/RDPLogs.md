# 🎯 **RDP Event Logs**
### `File Name: RDPLogs.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Drew Ervin  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows Event Logs mapping Terminal Services connections, logins, and session timeouts.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from RDP Event Logs to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate RDP Event Logs events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit RDP Event Logs storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: RDP Logs
Author: Drew Ervin
Version: 1.0
Id: 6fa6ac8c-d940-4658-9c61-fdad4cf6416b
RecreateDirectories: true
Targets:
    -
        Name: RemoteConnectionManager Event Logs
        Category: EventLogs
        Path: C:\Windows\System32\winevt\logs\
        FileMask: Microsoft-Windows-TerminalServices-RemoteConnectionManager*
    -
        Name: RemoteConnectionManager Event Logs
        Category: EventLogs
        Path: C:\Windows.old\Windows\System32\winevt\logs\
        FileMask: Microsoft-Windows-TerminalServices-RemoteConnectionManager*
    -
        Name: LocalSessionManager Event Logs
        Category: EventLogs
        Path: C:\Windows\System32\winevt\logs\
        FileMask: Microsoft-Windows-TerminalServices-LocalSessionManager*
    -
        Name: LocalSessionManager Event Logs
        Category: EventLogs
        Path: C:\Windows.old\Windows\System32\winevt\logs\
        FileMask: Microsoft-Windows-TerminalServices-LocalSessionManager*
    -
        Name: RDPClient Event Logs
        Category: EventLogs
        Path: C:\Windows\System32\winevt\logs\
        FileMask: Microsoft-Windows-TerminalServices-RDPClient*
    -
        Name: RDPClient Event Logs
        Category: EventLogs
        Path: C:\Windows.old\Windows\System32\winevt\logs\
        FileMask: Microsoft-Windows-TerminalServices-RDPClient*
    -
        Name: RDPCoreTS Event Logs
        Category: EventLogs
        Path: C:\Windows\System32\winevt\logs\
        FileMask: Microsoft-Windows-RemoteDesktopServices-RdpCoreTS*
        Comment: "Can be used to correlate RDP logon failures by originating IP"
    -
        Name: RDPCoreTS Event Logs
        Category: EventLogs
        Path: C:\Windows.old\Windows\System32\winevt\logs\
        FileMask: Microsoft-Windows-RemoteDesktopServices-RdpCoreTS*
        Comment: "Can be used to correlate RDP logon failures by originating IP"

# Documentation
# https://www.andreafortuna.org/2020/06/04/windows-forensic-analysis-some-thoughts-on-rdp-related-event-ids/
# https://ponderthebits.com/2018/02/windows-rdp-related-event-logs-identification-tracking-and-investigation/
# https://www.13cubed.com/downloads/rdp_flowchart.pdf
# https://www.youtube.com/watch?v=myzG11BP3Sk
# https://www.thedfirspot.com/post/lateral-movement-remote-desktop-protocol-rdp-event-logs
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
