# 🎯 **Internet Explorer**
### `File Name: InternetExplorer.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Internet Explorer

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Internet Explorer to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Internet Explorer events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Internet Explorer storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Internet Explorer
Author: Eric Zimmerman
Version: 1.0
Id: b1e1d79b-324d-4587-a002-cc81144588ff
RecreateDirectories: true
Targets:
    -
        Name: Index.dat History
        Category: Communications
        Path: C:\Documents and Settings\%user%\Local Settings\History\History.IE5\
        FileMask: index.dat
    -
        Name: Index.dat History subdirectory
        Category: Communications
        Path: C:\Documents and Settings\%user%\Local Settings\History\History.IE5\*\
        FileMask: index.dat
    -
        Name: Index.dat cookies
        Category: Communications
        Path: C:\Documents and Settings\%user%\Cookies\
        FileMask: index.dat
    -
        Name: Index.dat UserData
        Category: Communications
        Path: C:\Documents and Settings\%user%\Application Data\Microsoft\Internet Explorer\UserData\
        FileMask: index.dat
    -
        Name: Index.dat Office XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Application Data\Microsoft\Office\Recent\
        FileMask: index.dat
    -
        Name: Index.dat Office
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Microsoft\Office\Recent\
        FileMask: index.dat
    -
        Name: Local Internet Explorer folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Internet Explorer\
        Recursive: true
    -
        Name: Roaming Internet Explorer folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Microsoft\Internet Explorer\
        Recursive: true
    -
        Name: IE 9/10 History
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Windows\History\
        Recursive: true
    -
        Name: IE 9/10 Cookies
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Windows\Cookies\
        Recursive: true
    -
        Name: IE 9/10 Download History
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Windows\IEDownloadHistory\
        Recursive: true
    -
        Name: IE 11 Metadata
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Windows\WebCache\
    -
        Name: IE 11 Cookies
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Windows\INetCookies\
        Recursive: true

# Documentation
# https://www.sans.org/security-resources/posters/windows-forensic-analysis/170/download
# https://www.digitalforensics.com/blog/an-overview-of-web-browser-forensics/
# https://www.dataforensics.org/internet-explorer-forensics/
# https://www.xploreforensics.com/blog/internet-explorer-forensic-artifacts-analysis.html
# https://cyberforensicator.com/2017/02/07/windows-10-forensics/
# https://www.forensafe.com/blogs/internetexplorer.html
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
