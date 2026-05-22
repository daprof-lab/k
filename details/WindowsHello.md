# 🎯 **Windows Hello**
### `File Name: WindowsHello.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Kevin Pagano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows Hello

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Windows Hello to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Windows Hello events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Windows Hello storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Windows Hello
Author: Kevin Pagano
Version: 1.0
Id: 4d41e991-989a-4163-954e-2f44bd55eb71
RecreateDirectories: true
Targets:
    -
        Name: Cryptokeys
        Category: Windows Hello
        Path: C:\Windows\ServiceProfiles\LocalService\AppData\Roaming\Microsoft\Crypto\Keys\
        Recursive: true
    -
        Name: Masterkey
        Category: Windows Hello
        Path: C:\Windows\System32\Microsoft\Protect\S-1-5-18\User\
        Recursive: true
    -
        Name: NGC
        Category: Windows Hello
        Path: C:\Windows\ServiceProfiles\LocalService\AppData\Local\Microsoft\Ngc\
        Recursive: true
    -
        Name: SECURITY registry transaction files
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: SECURITY.LOG*
    -
        Name: SECURITY registry transaction files
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\
        FileMask: SECURITY.LOG*
    -
        Name: SOFTWARE registry transaction files
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: SOFTWARE.LOG*
    -
        Name: SOFTWARE registry transaction files
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\
        FileMask: SOFTWARE.LOG*
    -
        Name: SYSTEM registry transaction files
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: SYSTEM.LOG*
    -
        Name: SYSTEM registry transaction files
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\
        FileMask: SYSTEM.LOG*
    -
        Name: SECURITY registry hive
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: SECURITY
    -
        Name: SECURITY registry hive
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\
        FileMask: SECURITY
    -
        Name: SOFTWARE registry hive
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: SOFTWARE
    -
        Name: SOFTWARE registry hive
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\
        FileMask: SOFTWARE
    -
        Name: SYSTEM registry hive
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: SYSTEM
    -
        Name: SYSTEM registry hive
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\
        FileMask: SYSTEM
    -
        Name: SECURITY registry hive (RegBack)
        Category: Registry
        Path: C:\Windows\System32\config\RegBack\
        FileMask: SECURITY
    -
        Name: SECURITY registry hive (RegBack)
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\RegBack\
        FileMask: SECURITY
    -
        Name: SOFTWARE registry hive (RegBack)
        Category: Registry
        Path: C:\Windows\System32\config\RegBack\
        FileMask: SOFTWARE
    -
        Name: SOFTWARE registry hive (RegBack)
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\RegBack\
        FileMask: SOFTWARE
    -
        Name: SYSTEM registry hive (RegBack)
        Category: Registry
        Path: C:\Windows\System32\config\RegBack\
        FileMask: SYSTEM
    -
        Name: SYSTEM registry hive (RegBack)
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\RegBack\
        FileMask: SYSTEM
    -
        Name: SYSTEM registry hive (RegBack)
        Category: Registry
        Path: C:\Windows\System32\config\RegBack\
        FileMask: SYSTEM1
    -
        Name: SYSTEM registry hive (RegBack)
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\RegBack\
        FileMask: SYSTEM1

# Documentation
# Files and folders to be used for cracking the Windows Hello PIN
# NOTE: You may need to uncheck the "Deduplicate" function in KAPE as it may filter out needed Cryptokey files
# https://github.com/Banaanhangwagen/WINHELLO2hashcat
# https://hashcat.net/forum/thread-10461.html
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
