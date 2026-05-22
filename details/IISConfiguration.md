# 🎯 **Iisconfiguration**
### `File Name: IISConfiguration.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** NVISO (@NVISOsecurity)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
IIS

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Iisconfiguration to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Iisconfiguration events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Iisconfiguration storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: IIS
Author: NVISO (@NVISOsecurity)
Version: 1.0
Id: 08378263-dd33-4a38-9abb-bf02004a4cf3
RecreateDirectories: true
Targets:
    -
        Name: IIS applicationHost.config
        Category: Apps
        Path: C:\Windows\System32\inetsrv\config\
        FileMask: "applicationHost.config"
        Comment: "This configuration file stores the settings for all your Web sites and applications."
    -
        Name: IIS administration.config
        Category: Apps
        Path: C:\Windows\System32\inetsrv\config\
        FileMask: "administration.config"
        Comment: "This configuration file stores the settings for IIS management."
    -
        Name: IIS redirection.config
        Category: Apps
        Path: C:\Windows\System32\inetsrv\config\
        FileMask: "redirection.config"
        Comment: "This configuration file contains the settings that indicate the location where the centralized configuration files are stored."
    -
        Name: web.config
        Category: Apps
        Path: C:\inetpub\wwwroot
        Recursive: true
        FileMask: "web.config"
        Comment: "The web.config is a file that is read by IIS and the ASP.NET Core Module to configure an app hosted with IIS."

# Documentation
# https://docs.microsoft.com/en-us/iis/configuration/
# https://www.microsoft.com/en-us/security/blog/2022/07/26/malicious-iis-extensions-quietly-open-persistent-backdoors-into-servers
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
