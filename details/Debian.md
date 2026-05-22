# 🎯 **Debian**
### `File Name: Debian.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Matt Dawson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Debian on Windows Subsystem for Linux

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Debian to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Debian events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Debian storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Debian on Windows Subsystem for Linux
Author: Matt Dawson
Version: 1.0
Id: 3629bafb-16b5-41de-988f-6961c6d3b6e1
RecreateDirectories: true
Targets:
    -
        Name: Debian WSL /etc/debian_version
        Category: Windows Subsystem for Linux
        Path: C:\Users\%user%\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\
        FileMask: "debian_version"
    -
        Name: Debian WSL /etc/fstab
        Category: Windows Subsystem for Linux
        Path: C:\Users\%user%\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\
        FileMask: "fstab"
    -
        Name: Debian WSL /etc/os-release
        Category: Windows Subsystem for Linux
        Path: C:\Users\%user%\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\
        FileMask: "os-release"
    -
        Name: Debian WSL /etc/passwd
        Category: Windows Subsystem for Linux
        Path: C:\Users\%user%\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\
        FileMask: "passwd"
    -
        Name: Debian WSL /etc/group
        Category: Windows Subsystem for Linux
        Path: C:\Users\%user%\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\
        FileMask: "group"
    -
        Name: Debian WSL /etc/shadow
        Category: Windows Subsystem for Linux
        Path: C:\Users\%user%\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\
        FileMask: "shadow"
    -
        Name: Debian WSL /etc/timezone
        Category: Windows Subsystem for Linux
        Path: C:\Users\%user%\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\
        FileMask: "timezone"
    -
        Name: Debian WSL /etc/hostname
        Category: Windows Subsystem for Linux
        Path: C:\Users\%user%\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\
        FileMask: "hostname"
    -
        Name: Debian WSL /etc/hosts
        Category: Windows Subsystem for Linux
        Path: C:\Users\%user%\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\
        FileMask: "hosts"
    -
        Name: Debian WSL /etc/crontab
        Category: Windows Subsystem for Linux
        Path: C:\Users\%user%\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\
        FileMask: "crontab"
    -
        Name: Debian WSL /etc/bash.bashrc
        Category: Windows Subsystem for Linux
        Path: C:\Users\%user%\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\
        FileMask: "bash.bashrc"
    -
        Name: Debian WSL /etc/profile
        Category: Windows Subsystem for Linux
        Path: C:\Users\%user%\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\etc\
        FileMask: "profile"
    -
        Name: Debian WSL .bash_history
        Category: Windows Subsystem for Linux
        Path: C:\Users\%user%\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\
        Recursive: true
        FileMask: ".bash_history"
    -
        Name: Debian WSL .bashrc
        Category: Windows Subsystem for Linux
        Path: C:\Users\%user%\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\
        Recursive: true
        FileMask: ".bashrc"
    -
        Name: Debian WSL .profile
        Category: Windows Subsystem for Linux
        Path: C:\Users\%user%\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\
        Recursive: true
        FileMask: ".profile"
    -
        Name: Debian WSL User Crontabs
        Category: Windows Subsystem for Linux
        Path: C:\Users\%user%\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\var\spool\cron\crontabs\
        Recursive: true
    -
        Name: Debian WSL Apt Logs
        Category: Windows Subsystem for Linux
        Path: C:\Users\%user%\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\rootfs\var\log\apt\
        Recursive: true
        FileMask: "*.log"
    -
        Name: Debian WSL ext4.vhdx
        Category: Windows Subsystem for Linux
        Path: C:\Users\%user%\AppData\Local\Packages\TheDebianProject.DebianGNULinux_*\LocalState\
        FileMask: "ext4.vhdx"

# Documentation
# https://blog.1234n6.com/2017/10/further-forensicating-of-windows.html
# https://medium.com/@tho.le/linux-forensics-some-useful-artifacts-74497dca1ab2
# https://christopherkibble.com/posts/wsl-vhdx-recovery/
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
