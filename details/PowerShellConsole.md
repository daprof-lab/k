# 🎯 **Power Shell Console**
### `File Name: PowerShellConsole.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Mike Cary, 2thewes, Vikas Singh  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
PowerShell Console Log File

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Power Shell Console to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Power Shell Console events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Power Shell Console storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: PowerShell Console Log File
Author: Mike Cary, 2thewes, Vikas Singh
Version: 1.2
Id: efa4332a-89eb-430c-ab61-006a9e6620d7
RecreateDirectories: true
Targets:
    -
        Name: PowerShell Console Log
        Category: PowerShellConsoleLog
        Path: C:\Users\%user%\AppData\Roaming\Microsoft\Windows\PowerShell\PSReadline\
        FileMask: '*_history.txt'
    -
        Name: PowerShell Console Log Systemprofile
        Category: PowerShellConsoleLog
        Path: C:\Windows\System32\config\systemprofile\AppData\Roaming\Microsoft\Windows\PowerShell\PSReadLine\
        FileMask: '*_history.txt'
    -
        Name: PowerShell Console Log WOW64 Systemprofile
        Category: PowerShellConsoleLog
        Path: C:\Windows\SysWOW64\config\systemprofile\AppData\Roaming\Microsoft\Windows\PowerShell\PSReadLine\
        FileMask: '*_history.txt'
    -
        Name: PowerShell ISE - AutoSave Files
        Category: PowerShellConsoleLog
        Path: C:\Users\%user%\AppData\Local\Microsoft_Corporation\powershell_ise.exe_StrongName*\*\AutoSaveFiles\
        FileMask: '*.ps1'
    -
        Name: PowerShell ISE - User Config
        Category: PowerShellConsoleLog
        Path: C:\Users\%user%\AppData\Local\Microsoft_Corporation\powershell_ise.exe_StrongName*\*\
        FileMask: '*.config'

# Documentation
# https://vikas-singh.notion.site/PowerShell-Command-History-Forensics-81a35c4f0b824c2b95c28f98134d49a4?pvs=4
# https://community.sophos.com/malware/b/blog/posts/powershell-command-history-forensics
# https://darizotas.blogspot.com/2018/10/forensics-powershell-artifacts.html
# https://digital-forensics.sans.org/media/DFPS_FOR508_v4.4_1-19.pdf
# https://www.forensafe.com/blogs/powershell.html
# https://learn.microsoft.com/en-us/powershell/module/psreadline/about/about_psreadline?view=powershell-7.3#command-history
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
