# 🎯 **Windows Prefetch**
### `File Name: Prefetch.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
System-generated files (.pf) designed to optimize application launch times. They store program execution metadata, run counts, timestamps, and files loaded during launch.

---

## 🔍 **Investigative Use-Cases**
* **Evidence of Process Execution**: Prove that a specific program (e.g. malware or hacktool) was actually executed on the system.
* **Application Timeline Analysis**: Extract the last 8 execution timestamps (on Windows 8+) to establish program execution patterns.
* **Staged Payload Detection**: Discover files loaded by an executable, mapping out DLL dependencies and staged payload folders.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Prefetch files
Author: Eric Zimmerman
Version: 1.0
Id: f6715d3f-b8ca-4cc2-9e5e-4ed18e88abbe
RecreateDirectories: true
Targets:
    -
        Name: Prefetch
        Category: Prefetch
        Path: C:\Windows\prefetch\
        FileMask: '*.pf'
    -
        Name: Prefetch
        Category: Prefetch
        Path: C:\Windows.old\Windows\prefetch\
        FileMask: '*.pf'

# Documentation
# https://forensicswiki.xyz/wiki/index.php?title=Prefetch
# https://www.youtube.com/watch?v=f4RAtR_3zcs
# https://nasbench.medium.com/windows-forensics-analysis-windows-artifacts-part-ii-71b8fa68d8a1
# https://www.sans.org/blog/device-profiling-with-windows-prefetch
# https://www.youtube.com/watch?v=prEghfj3bPI
# https://www.sans.org/security-resources/posters/windows-forensic-analysis/170/download
# https://www.forensafe.com/blogs/prefetch.html
# https://www.thedfirspot.com/post/artifacts-of-execution-i-know-what-you-did-last-incident
# https://y0sh1mitsu.github.io/posts/how-are-prefetch-created
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
