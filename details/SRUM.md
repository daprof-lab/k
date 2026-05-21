# 🎯 **System Resource Usage Monitor**
### `File Name: SRUM.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Mark Hallman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
System database (srudb.dat) documenting long-term system resource utilization including network traffic, CPU times, application energy usage, and active background pushes.

---

## 🔍 **Investigative Use-Cases**
* **Exfiltration Analysis**: Audit long-term network usage (bytes uploaded/downloaded) per application executable to detect large data flows.
* **Process Execution Validation**: Detect historic process execution timelines (CPU cycles consumed) for programs that have been deleted.
* **System Activity Profiling**: Reconstruct general active hours, network interfaces used, and device battery status over a 30-day window.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: System Resource Usage Monitor (SRUM) Data
Author: Mark Hallman
Version: 1.0
Id: 9858f1fc-5e22-46a0-8bfd-c821ac9b4a13
RecreateDirectories: true
Targets:
    -
        Name: SRUM
        Category: Execution
        Path: C:\Windows\System32\SRU\
        Recursive: true
    -
        Name: SRUM
        Category: Execution
        Path: C:\Windows.old\Windows\System32\SRU\
        Recursive: true
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
        Name: SOFTWARE registry transaction files
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: SOFTWARE.LOG*
    -
        Name: SOFTWARE registry transaction files
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\
        FileMask: SOFTWARE.LOG*

# Documentation
# https://medium.com/@esmyl/srum-forensics-dfir-aa9522a925c5
# https://medium.com/velociraptor-ir/digging-into-the-system-resource-usage-monitor-srum-afbadb1a375
# https://www.youtube.com/watch?v=l6-83WU95Sw
# https://www.youtube.com/watch?v=Uw8n4_o-ETM
# https://digital-forensics.sans.org/summit-archives/file/summit_archive_1492184583.pdf
# https://frsecure.com/blog/windows-forensics-execution/
# https://isc.sans.edu/forums/diary/System+Resource+Utilization+Monitor/21927/
# https://medium.com/velociraptor-ir/digging-into-the-system-resource-usage-monitor-srum-afbadb1a375
# https://coek.info/pdf-forensic-implications-of-system-resource-usage-monitor-srum-data-in-windows-8-.html
# https://digitalforensicsdotblog.wordpress.com/2021/10/06/swimming-in-the-srum/
# https://www.forensafe.com/blogs/srudb.html
# https://twitter.com/purp1ew0lf/status/1504491533487296517?s=21
# https://github.com/WithSecureLabs/slide-decks/blob/main/2023-SANS_DFIR_Summit_Europe/Exploring_the_depths_of_SRUM_for_incident_response.pdf
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
