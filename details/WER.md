# 🎯 **Windows Error Reporting**
### `File Name: WER.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Troy Larson  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows Error Reporting files (.wer) and system crash logs. These contain program crash crashdumps, crash times, faulting module names, and command-line arguments.

---

## 🔍 **Investigative Use-Cases**
* **Exploit Loop Discovery**: Audit repetitive application crashes in core system processes, indicating active buffer overflow exploit attempts.
* **Malware Execution Verification**: Identify crash logs of custom malware binaries that failed or raised runtime exceptions during run attempts.
* **User Crash Profiling**: Trace when application failures occurred to coordinate with other indicators of compromise.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Windows Error Reporting
Author: Troy Larson
Version: 1.1
Id: 03106a1c-e1f8-4075-abdb-f9c83078347d
RecreateDirectories: true
Targets:
    -
        Name: WER Files
        Category: Executables
        Path: C:\ProgramData\Microsoft\Windows\WER\
        Recursive: true
    -
        Name: WER Files
        Category: Executables
        Path: C:\Users\%user%\AppData\Local\Microsoft\Windows\WER\
        Recursive: true
    -
        Name: Crash Dumps
        Category: SQL Exploitation
        Path: C:\Users\%user%\AppData\Local\CrashDumps\
        FileMask: '*.dmp'
    -
        Name: Crash Dumps
        Category: SQL Exploitation
        Path: C:\Windows\
        FileMask: '*.dmp'
    -
        Name: Crash Dumps
        Category: SQL Exploitation
        Path: C:\Windows.old\Windows\
        FileMask: '*.dmp'

# Documentation
# https://isc.sans.edu/forums/diary/Windows+Error+Reporting+DFIR+Benefits+and+Privacy+Concerns/22536/
# https://medium.com/dfir-dudes/amcache-is-not-alone-using-wer-files-to-hunt-evil-86bdfdb216d7
# https://nasbench.medium.com/windows-forensics-analysis-windows-artifacts-part-i-c7ad81ada16c
# https://www.sans.org/reading-room/whitepapers/forensics/windows-crash-dumps-remote-incident-identification-36012
# http://journeyintoir.blogspot.com/2014/02/exploring-windows-error-reporting.html
# https://www.secjuice.com/windows-forensics-artifacts-2/
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
