# 🎯 **Remote Desktop Manager**
### `File Name: RemoteDesktopManager.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** ogmini  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
A Target to collect files that are related to Remote Desktop Manager from Devolutions

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Remote Desktop Manager to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Remote Desktop Manager events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Remote Desktop Manager storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: A Target to collect files that are related to Remote Desktop Manager from Devolutions
Author: ogmini
Version: 1.0
Id: a529546a-971e-4b19-83cf-5ed24e3b67ae
RecreateDirectories: true
Targets:
    -
        Name: SQLite Data Sources
        Category: Configuration
        Path: C:\Users\%user%\AppData\Local\Devolutions\RemoteDesktopManager
        Recursive: false
        FileMask: "*.db"
        Comment: "SQLite database of connections and settings. Connections.db is the default. There can be others in different locations. This will only pick up db files in the default location."
    -
        Name: XML Data Sources
        Category: Configuration
        Path: C:\Users\%user%\AppData\Local\Devolutions\RemoteDesktopManager
        Recursive: false
        FileMask: "*.xml"
        Comment: XML of connections and settings. Connections.xml is the default. There can be others in different locations. This will only pick up XML files in the default location."
    -
        Name: Connections.log
        Category: Logs
        Path: C:\Users\%user%\AppData\Local\Devolutions\RemoteDesktopManager
        Recursive: false
        FileMask: "Connections.log"
        Comment: "Log file for connections."
    -
        Name: RemoteDesktopManager.cfg
        Category: Configuration
        Path: C:\Users\%user%\AppData\Local\Devolutions\RemoteDesktopManager
        Recursive: false
        FileMask: "RemoteDesktopManager.cfg"
        Comment: "Configuration settings."
    -
        Name: Most Recently Used XML
        Category: XML
        Path: C:\Users\%user%\AppData\Local\Devolutions\RemoteDesktopManager\*\
        FileMask: "Mru.xml"
        Comment: "XML file of most recently used connections."
    -
        Name: Favorites XML
        Category: XML
        Path: C:\Users\%user%\AppData\Local\Devolutions\RemoteDesktopManager\*\
        FileMask: "Favorites.xml"
        Comment: "XML file of Favorited connections."

# Documentation
# This target is for Remote Desktop Manager from Devolutions. https://devolutions.net/remote-desktop-manager/
# https://ogmini.github.io/research#remote-desktop-manager
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
