# **⚙️ Core OS & File System - Modules**

{% hint style="success" %}

**Module Execution Info:** These modules process data collected under the Core OS & File System category using specialized analytical tools. Click on any **Short Name** to view a dedicated detail page including use-cases and KAPE module definitions.

{% endhint %}

[⬅️ Back to Core OS & File System](core_os_artifacts.md)

---

## **Available Modules (.mkape)**

| Short Name | Description | File Name | Author | Version |
| :--- | :--- | :--- | :--- | :--- |
| **[MFTECmd Parser](details/MFTECmd.md)** | Executes Eric Zimmerman's MFTECmd tool to process raw `$MFT`, `$Boot`, `$LogFile`, and `$J` files into structured, timeline-friendly CSV tables. | **MFTECmd.mkape** | Eric Zimmerman | 1.0 |
| **[PECmd Prefetch Parser](details/PECmd.md)** | Runs PECmd to process Windows Prefetch files (.pf), mapping process execution times, loaded DLL lists, and launching directories. | **PECmd.mkape** | Eric Zimmerman / Andrew Rathbun | 1.1 |
| **[LECmd Link File Parser](details/LECmd.md)** | Runs LECmd to parse Windows LNK shortcut files, revealing target file specs, network paths, volume serial numbers, and MAC addresses. | **LECmd.mkape** | Eric Zimmerman | 1.1 |
| **[JLECmd Jump List Parser](details/JLECmd.md)** | Runs JLECmd to process taskbar Jump Lists, recovering pinned applications and recent user document browsing habits. | **JLECmd.mkape** | Eric Zimmerman | 1.1 |
| **[RBCmd Recycle Bin Parser](details/RBCmd.md)** | Runs RBCmd to parse Windows Recycle Bin metadata files, resolving raw deleted files to original paths, file sizes, and deletion times. | **RBCmd.mkape** | Eric Zimmerman | 1.0 |
| **[SrumECmd SRUM Parser](details/SrumECmd.md)** | Runs SrumECmd to parse srudb.dat databases, detailing historic application network uploads, downloads, battery usage, and CPU times. | **SrumECmd.mkape** | Andrew Rathbun | 1.1 |
| **[AmcacheParser](details/AmcacheParser.md)** | Runs AmcacheParser to parse Amcache.hve hives, extracting executable execution paths, hashes, compiler times, and installation statuses. | **AmcacheParser.mkape** | Eric Zimmerman | 1.1 |
| **[AppCompatCacheParser (Shimcache)](details/AppCompatCacheParser.md)** | Runs AppCompatCacheParser to extract execution records from the SYSTEM registry hive, locating file paths and execution status. | **AppCompatCacheParser.mkape** | Eric Zimmerman | 1.1 |
| **[RecentFileCache Parser](details/RecentFileCacheParser.md)** | Parses legacy RecentFileCache.bcf files to recover application execution histories from older versions of Windows. | **RecentFileCacheParser.mkape** | Eric Zimmerman | 1.0 |
| **[RegRipper Hive Parser](details/RegRipper.md)** | Runs the RegRipper framework to parse user, system, software, and sam hives using targeted forensic plugins. | **RegRipper.mkape** | ZeArioch / Phill Moore | 1.1 |
| **[Reghunter Core Suite](details/Reghunter.md)** | Executes advanced Reghunter registry parsers to audit system configs, identifying unauthorized configuration shifts or persistent items. | **Reghunter.mkape** | Georg Lauenstein | 1.0 |
| **[WxTCmd Timeline Parser](details/WxTCmd.md)** | Runs WxTCmd to parse Windows Timeline SQLite databases (ActivitiesCache.db), timelines user application focuses, opened documents, and clipboard logs. | **WxTCmd.mkape** | Mike Cary | 1.0 |
| **[PowerShell Recycle Bin Parser](details/PowerShell_RecycleBinParsing.md)** | Parses Windows Recycle Bin directory states using lightweight PowerShell scripts, outputting mapped paths and file sizes to structured files. | **PowerShell_RecycleBinParsing.mkape** | Max Zabuty | 1.0 |

---

[⬅️ Back to Core OS & File System](core_os_artifacts.md)
