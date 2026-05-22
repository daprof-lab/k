# 🎯 **Sshtunnel Command Artifacts**
### `File Name: SSHTunnelCommandArtifacts.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Aashiq Ahmed  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Collect command history, scripts, and SSH client artifacts useful for identifying SSH tunneling and pivoting commands

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Sshtunnel Command Artifacts to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Sshtunnel Command Artifacts events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Sshtunnel Command Artifacts storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Collect command history, scripts, and SSH client artifacts useful for identifying SSH tunneling and pivoting commands
Author: Aashiq Ahmed
Version: 1.0
Id: 4d7c1c5b-7b9d-4c8c-a8dd-2f7d51b29011
RecreateDirectories: true
Targets:
  -
    Name: PowerShell ConsoleHost history
    Category: CommandHistory
    Path: C:\Users\%user%\AppData\Roaming\Microsoft\Windows\PowerShell\PSReadLine
    FileMask: ConsoleHost_history.txt
    Recursive: true
    Comment: PowerShell command history may contain ssh, plink, and pivot tool commands

  -
    Name: Bash history in user profiles
    Category: CommandHistory
    Path: C:\Users\%user%
    FileMask: .bash_history
    Recursive: true
    Comment: Bash history may contain ssh tunneling and pivot commands

  -
    Name: Zsh history in user profiles
    Category: CommandHistory
    Path: C:\Users\%user%
    FileMask: .zsh_history
    Recursive: true
    Comment: Zsh history may contain ssh tunneling and pivot commands

  -
    Name: User PowerShell scripts
    Category: Scripts
    Path: C:\Users\%user%
    FileMask: "*.ps1"
    Recursive: true
    Comment: User-created PowerShell scripts may contain pivoting commands

  -
    Name: User batch scripts
    Category: Scripts
    Path: C:\Users\%user%
    FileMask: "*.bat"
    Recursive: true
    Comment: Batch scripts may contain ssh, plink, or netsh portproxy commands

  -
    Name: User command scripts
    Category: Scripts
    Path: C:\Users\%user%
    FileMask: "*.cmd"
    Recursive: true
    Comment: CMD scripts may contain ssh, plink, or netsh portproxy commands

  -
    Name: User shell scripts
    Category: Scripts
    Path: C:\Users\%user%
    FileMask: "*.sh"
    Recursive: true
    Comment: Shell scripts may contain ssh tunneling and proxy commands

  -
    Name: SSH known_hosts
    Category: SSH
    Path: C:\Users\%user%\.ssh
    FileMask: known_hosts
    Recursive: false
    Comment: known_hosts records SSH servers previously connected to

  -
    Name: SSH config
    Category: SSH
    Path: C:\Users\%user%\.ssh
    FileMask: config
    Recursive: false
    Comment: SSH config may contain port forwarding or tunneling settings

  -
    Name: SSH directory artifacts
    Category: SSH
    Path: C:\Users\%user%\.ssh
    FileMask: "*"
    Recursive: true
    Comment: SSH directory may contain keys, configs, and other connection artifacts

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
