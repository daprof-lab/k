# **🎯 Core OS & File System - Targets**

{% hint style="success" %}

**Target Collection Info:** These targets guide KAPE to collect raw operating system and application forensic files relating to core os & file system. Click on any **Short Name** to view a dedicated detail page including forensics value and KAPE target definitions.

{% endhint %}

[⬅️ Back to Core OS & File System](core_os_artifacts.md)

---

## **Available Targets (.tkape)**

| Short Name | Description | File Name | Author | Version |
| :--- | :--- | :--- | :--- | :--- |
| **[Master File Table ($MFT)](details/$MFT.md)** | The primary NTFS file system database. It contains metadata for every file and directory on an NTFS volume, including timestamps, permissions, file size, and physical cluster mapping. | **$MFT.tkape** | Eric Zimmerman | 1.0 |
| **[USN Journal ($UsnJrnl:$J)](details/$J.md)** | The Update Sequence Number (USN) Change Journal. It records metadata changes to files and folders on an NTFS volume, providing a rolling history of disk operations. | **$J.tkape** | Eric Zimmerman / Andrew Rathbun | 1.1 |
| **[NTFS Transaction Log ($LogFile)](details/$LogFile.md)** | A transaction log used by NTFS to maintain file system integrity. It records transaction steps for metadata operations before they are committed to the MFT. | **$LogFile.tkape** | Eric Zimmerman | 1.0 |
| **[Volume Boot Record ($Boot)](details/$Boot.md)** | The boot sector of an NTFS partition. It contains crucial disk geometry configurations, cluster sizing, and bootstrap code used by the system bootloader. | **$Boot.tkape** | Eric Zimmerman | 1.0 |
| **[Windows Prefetch](details/Prefetch.md)** | System-generated files (.pf) designed to optimize application launch times. They store program execution metadata, run counts, timestamps, and files loaded during launch. | **Prefetch.tkape** | Eric Zimmerman | 1.0 |
| **[System Registry Hives](details/RegistryHivesSystem.md)** | System-wide registry database files (SYSTEM, SOFTWARE, SAM, SECURITY). These house core system configuration, hardware parameters, installed applications, and local accounts. | **RegistryHivesSystem.tkape** | Eric Zimmerman / Mark Hallman | 1.0 |
| **[User Registry Hives](details/RegistryHivesUser.md)** | User-level registry database files (NTUSER.DAT and UsrClass.dat). These store individual user workspace configurations, recent file usage, shellbags, and application habits. | **RegistryHivesUser.tkape** | Eric Zimmerman / Mark Hallman | 1.0 |
| **[LNK Files & Jump Lists](details/LNKFilesAndJumpLists.md)** | Windows shortcut files (.lnk) and taskbar Jump Lists (.automaticDestinations-ms, .customDestinations-ms). These document user file openings and system navigation. | **LNKFilesAndJumpLists.tkape** | Eric Zimmerman / Andrew Rathbun / Yogesh Khatri | 1.3 |
| **[Explorer Thumbnail Cache](details/ThumbCache.md)** | System-generated cached databases (thumbcache_*.db) storing visual previews of pictures, videos, documents, and folders rendered in Windows Explorer. | **ThumbCache.tkape** | Eric Zimmerman | 1.0 |
| **[System Resource Usage Monitor](details/SRUM.md)** | System database (srudb.dat) documenting long-term system resource utilization including network traffic, CPU times, application energy usage, and active background pushes. | **SRUM.tkape** | Mark Hallman | 1.0 |
| **[Amcache Database](details/Amcache.md)** | System database hive (Amcache.hve) logging metadata of newly installed applications, executable file paths, compiler compilation times, and SHA-1 file hashes. | **Amcache.tkape** | Eric Zimmerman | 1.0 |
| **[RecentFileCache](details/RecentFileCache.md)** | Precursor file to Amcache (RecentFileCache.bcf) on older versions of Windows. It records paths and filenames of recently run applications. | **RecentFileCache.tkape** | Eric Zimmerman | 1.0 |
| **[Windows Timeline Database](details/WindowsTimeline.md)** | SQLite database containing user activity logs (ActivitiesCache.db). It records opened files, clipboard copies, application focus histories, and connected external devices. | **WindowsTimeline.tkape** | Lee Whitfield / Thomas DIOT | 1.1 |
| **[Evidence of Execution Suite](details/EvidenceOfExecution.md)** | A comprehensive compound target collecting all execution artifacts (Prefetch, Amcache, RecentFileCache, Shimcache, and system execution databases) in a single instruction. | **EvidenceOfExecution.tkape** | Eric Zimmerman | 1.1 |
| **[Recycle Bin Metadata](details/RecycleBin.md)** | Deleted file metadata files ($I*) and raw deleted file contents ($R*) residing within the hidden `$Recycle.Bin` directory on all drives. | **RecycleBin.tkape** | Mark Hallman / Joshua Hickman | 2.0 |
| **[USB Device Logs](details/USBDevicesLogs.md)** | Collects setupapi.dev.log files, system setup logs, and hardware device logs detailing external storage connections and driver setups. | **USBDevicesLogs.tkape** | Eric Zimmerman / esecrpm | 1.1 |
| **[Windows Error Reporting](details/WER.md)** | Windows Error Reporting files (.wer) and system crash logs. These contain program crash crashdumps, crash times, faulting module names, and command-line arguments. | **WER.tkape** | Troy Larson | 1.1 |
| **[BITS Persistent Jobs](details/BITS.md)** | System database folder for the Background Intelligent Transfer Service (BITS). BITS is widely abused by threat actors to establish stealthy persistent file downloads. | **BITS.tkape** | Jos Clephas | 1.0 |

---

[⬅️ Back to Core OS & File System](core_os_artifacts.md)
