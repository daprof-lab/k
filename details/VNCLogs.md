# 🎯 **Vnclogs**
### `File Name: VNCLogs.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Phill Moore, Evangelos Dragonas  
**Version:** 1.3
{% endhint %}

---

## 📖 **Forensic Description & Value**
VNC Logs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Vnclogs to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Vnclogs events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Vnclogs storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: VNC Logs
Author: Phill Moore, Evangelos Dragonas
Version: 1.3
Id: b98dab2e-81f3-472e-a22a-05269ad16270
RecreateDirectories: true
Targets:
    -
        Name: RealVNC Log
        Category: ApplicationLogs
        Path: C:\Users\%user%\AppData\Local\RealVNC\
        FileMask: vncserver.log
        Comment: "https://www.realvnc.com/en/connect/docs/logging.html#logging"
    -
        Name: RealVNC Viewer Log
        Category: ApplicationLogs
        Path: C:\Users\*\AppData\Local\RealVNC\
        FileMask: vncviewer.log
        Comment: "https://help.realvnc.com/hc/en-us/articles/360002254238-All-About-Logging#realvnc-server-0-1"
    -
        Name: RealVNC Log
        Category: ApplicationLogs
        Path: C:\ProgramData\RealVNC-Service
        FileMask: vncserver.log
        Comment: "https://help.realvnc.com/hc/en-us/articles/360002254238-All-About-Logging-"
    -
        Name: RealVNC Application Logs
        Category: EventLogs
        Path: ApplicationEvents.tkape
        Comment: "Contains RealVNC entries, event source: VNC Server"
    -
        Name: TightVNC Application Logs
        Category: ApplicationLogs
        Path: C:\ProgramData\TightVNC\Server\Logs
        Comment: "https://ro.ecu.edu.au/cgi/viewcontent.cgi?article=1160&context=adf"


# Documentation
# https://www.semanticscholar.org/paper/Tracing-VNC-And-RDP-Protocol-Artefacts-on-Windows-Kerai/20467cee88102cffcc2b856b93fc0bb7a58fd499
# https://www.hackingarticles.in/capture-vnc-session-remote-pc-using-settoolkit/
# https://help.realvnc.com/hc/en-us/articles/360002254238-All-About-Logging#realvnc-server-0-1
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
