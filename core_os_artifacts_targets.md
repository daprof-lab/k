# **🎯 Core OS & File System - Targets**

{% hint style="success" %}

**Target Collection Info:** These targets guide KAPE to collect raw operating system and application forensic files relating to core os & file system. Click on any **Short Name** to view a dedicated detail page including forensics value and KAPE target definitions.

{% endhint %}

[⬅️ Back to Core OS & File System](core_os_artifacts.md)

---

## **Available Targets (.tkape)**

| Short Name | Description | File Name | Author | Version |
| :--- | :--- | :--- | :--- | :--- |
| **[🎯 $bitmap](details/$Bitmap.md)** | $Bitmap | **$Bitmap.tkape** | Nisarg Suthar | 1.0 |
| **[🎯 $mftmirr](details/$MFTMirr.md)** | $MFTMirr | **$MFTMirr.tkape** | Teo Kia Meng | 1.0 |
| **[🎯 $SDS](details/$SDS.md)** | $SDS | **$SDS.tkape** | Eric Zimmerman and Andrew Rathbun | 1.1 |
| **[🎯 $T](details/$T.md)** | $T | **$T.tkape** | Eric Zimmerman and Andrew Rathbun | 1.1 |
| **[🎯 Active Directory NTDS](details/ActiveDirectoryNTDS.md)** | Active Directory NTDS | **ActiveDirectoryNTDS.tkape** | Zawadi Done | 1.1 |
| **[🎯 Active Directory Sysvol](details/ActiveDirectorySysvol.md)** | Active Directory Sysvol | **ActiveDirectorySysvol.tkape** | Zawadi Done | 1.0 |
| **[🎯 Amcache Database](details/Amcache.md)** | System database hive (Amcache.hve) logging metadata of newly installed applications, executable file paths, compiler compilation times, and SHA-1 file hashes. | **Amcache.tkape** | Eric Zimmerman | 1.0 |
| **[🎯 App Compat PCA](details/AppCompatPCA.md)** | AppCompat PCA Folder | **AppCompatPCA.tkape** | Andrew Rathbun | 1.0 |
| **[🎯 App Data](details/AppData.md)** | AppData | **AppData.tkape** | Phill Moore | 1.1 |
| **[🎯 App Xpackages](details/AppXPackages.md)** | AppXPackages | **AppXPackages.tkape** | Nisarg Suthar | 1.0 |
| **[🎯 Application Events](details/ApplicationEvents.md)** | Windows Application Event Log | **ApplicationEvents.tkape** | Drew Ervin | 1.0 |
| **[🎯 BCD](details/BCD.md)** | Boot Configuration Files | **BCD.tkape** | Troy Larson | 1.0 |
| **[🎯 BITS Persistent Jobs](details/BITS.md)** | System database folder for the Background Intelligent Transfer Service (BITS). BITS is widely abused by threat actors to establish stealthy persistent file downloads. | **BITS.tkape** | Jos Clephas | 1.0 |
| **[🎯 Capability Access Manager](details/CapabilityAccessManager.md)** | Capability Access Manager database | **CapabilityAccessManager.tkape** | qmadev | 1.0 |
| **[🎯 Cert Util](details/CertUtil.md)** | Certutil | **CertUtil.tkape** | NVISO (@NVISOsecurity), 2thewes | 1.1 |
| **[🎯 Debian](details/Debian.md)** | Debian on Windows Subsystem for Linux | **Debian.tkape** | Matt Dawson | 1.0 |
| **[🎯 Directory Traversal Audio Files](details/DirectoryTraversal_AudioFiles.md)** | Find audio files covering a multitude of formats | **DirectoryTraversal_AudioFiles.tkape** | Andrew Rathbun | 1.0 |
| **[🎯 Directory Traversal Excel Documents](details/DirectoryTraversal_ExcelDocuments.md)** | Find Excel and Excel alternative documents | **DirectoryTraversal_ExcelDocuments.tkape** | Andrew Rathbun | 1.0 |
| **[🎯 Directory Traversal Pdfdocuments](details/DirectoryTraversal_PDFDocuments.md)** | Find PDF and PDF alternative documents | **DirectoryTraversal_PDFDocuments.tkape** | Andrew Rathbun | 1.0 |
| **[🎯 Directory Traversal Picture Files](details/DirectoryTraversal_PictureFiles.md)** | Find picture files covering a multitude of formats | **DirectoryTraversal_PictureFiles.tkape** | Andrew Rathbun | 1.0 |
| **[🎯 Directory Traversal Sqlite Databases](details/DirectoryTraversal_SQLiteDatabases.md)** | Find files with common SQLite file extensions | **DirectoryTraversal_SQLiteDatabases.tkape** | Andrew Rathbun | 1.0 |
| **[🎯 Directory Traversal Video Files](details/DirectoryTraversal_VideoFiles.md)** | Find video files covering a multitude of formats | **DirectoryTraversal_VideoFiles.tkape** | Andrew Rathbun | 1.0 |
| **[🎯 Directory Traversal Wild Card Example](details/DirectoryTraversal_WildCardExample.md)** | Find zip archives | **DirectoryTraversal_WildCardExample.tkape** | Eric Zimmerman | 1.0 |
| **[🎯 Directory Traversal Word Documents](details/DirectoryTraversal_WordDocuments.md)** | Find Word and Word alternative documents | **DirectoryTraversal_WordDocuments.tkape** | Andrew Rathbun | 1.0 |
| **[🎯 Drivers](details/Drivers.md)** | Windows Drivers | **Drivers.tkape** | Zawadi Done | 1.0 |
| **[🎯 Encapsulation Logging](details/EncapsulationLogging.md)** | EncapsulationLogging | **EncapsulationLogging.tkape** | Troy Larson | 1.0 |
| **[🎯 Event Trace Logs](details/EventTraceLogs.md)** | Event Trace Logs | **EventTraceLogs.tkape** | Mark Hallman | 1.1 |
| **[🎯 Event Transcript DB](details/EventTranscriptDB.md)** | EventTranscript.db (and other files related to Telemetry and Diagnostic Data) | **EventTranscriptDB.tkape** | Andrew Rathbun and Josh Mitchell | 1.2 |
| **[🎯 Evidence of Execution Suite](details/EvidenceOfExecution.md)** | A comprehensive compound target collecting all execution artifacts (Prefetch, Amcache, RecentFileCache, Shimcache, and system execution databases) in a single instruction. | **EvidenceOfExecution.tkape** | Eric Zimmerman | 1.1 |
| **[🎯 Exchange Client Access](details/ExchangeClientAccess.md)** | Exchange Client Access Log Files | **ExchangeClientAccess.tkape** | Keith Twombley | 1.0 |
| **[🎯 Exchange Cve 2021 26855](details/ExchangeCve-2021-26855.md)** | Exchange Server Vulnerability *.Compiled Files | **ExchangeCve-2021-26855.tkape** | Dennis Reneau | 1.0 |
| **[🎯 Exchange Setup Log](details/ExchangeSetupLog.md)** | Exchange Setup Log | **ExchangeSetupLog.tkape** | 2thewes | 1.0 |
| **[🎯 Exchange Transport](details/ExchangeTransport.md)** | Exchange Transport Log Files | **ExchangeTransport.tkape** | Keith Twombley | 1.0 |
| **[🎯 Explorer Thumbnail Cache](details/ThumbCache.md)** | System-generated cached databases (thumbcache_*.db) storing visual previews of pictures, videos, documents, and folders rendered in Windows Explorer. | **ThumbCache.tkape** | Eric Zimmerman | 1.0 |
| **[🎯 Group Policy](details/GroupPolicy.md)** | Current Group Policy Enforcement | **GroupPolicy.tkape** | piesecurity | 1.1 |
| **[🎯 Hosts File](details/HostsFile.md)** | Hosts file | **HostsFile.tkape** | Max Zabuty | 1.0 |
| **[🎯 Icon Cache DB](details/IconCacheDB.md)** | IconCache.db files | **IconCacheDB.tkape** | Herbert Bärschneider @SEC Consult | 1.0 |
| **[🎯 Iisconfiguration](details/IISConfiguration.md)** | IIS | **IISConfiguration.tkape** | NVISO (@NVISOsecurity) | 1.0 |
| **[🎯 Jump Lists](details/JumpLists.md)** | Jump lists | **JumpLists.tkape** | Max Zabuty | 1 |
| **[🎯 Kape Triage](details/!KapeTriage.md)** | Calls Kape Triage | **!KapeTriage.tkape** | Phill Moore | 1.0 |
| **[🎯 Kape Triage 075d99ed 1237 4a2d 9540 5793d184aa44](details/KapeTriage_075d99ed-1237-4a2d-9540-5793d184aa44.md)** | Kape Triage collections that will collect most of the files needed for a DFIR Investigation.  This module pulls evidence from File System files, Registry Hives, Event Logs, Scheduled Tasks, Evidence of Execution, SRUM data, SUM data, Web Browser data (IE/Edge, Chrome, Mozilla history), LNK Files, Jump Lists, 3rd party remote access software logs, 3rd party antivirus software logs, Windows 10 Timeline database, and $I Recycle Bin data files. | **KapeTriage_075d99ed-1237-4a2d-9540-5793d184aa44.tkape** | Scott Downie | 4.0 |
| **[🎯 Linux On Windows Profile Files](details/LinuxOnWindowsProfileFiles.md)** | Linux on Windows Profile Files | **LinuxOnWindowsProfileFiles.tkape** | Troy Larson | 1.0 |
| **[🎯 Live User Files](details/LiveUserFiles.md)** | Live User Files | **LiveUserFiles.tkape** | Mark Hallman | 1.0 |
| **[🎯 LNK Files & Jump Lists](details/LNKFilesAndJumpLists.md)** | Windows shortcut files (.lnk) and taskbar Jump Lists (.automaticDestinations-ms, .customDestinations-ms). These document user file openings and system navigation. | **LNKFilesAndJumpLists.tkape** | Eric Zimmerman, Andrew Rathbun, Yogesh Khatri | 1.3 |
| **[🎯 Log Files](details/LogFiles.md)** | LogFiles (includes SUM) | **LogFiles.tkape** | Fabian Murer | 1.1 |
| **[🎯 Master File Table ($MFT)](details/$MFT.md)** | The primary NTFS file system database. It contains metadata for every file and directory on an NTFS volume, including timestamps, permissions, file size, and physical cluster mapping. | **$MFT.tkape** | Eric Zimmerman | 1.0 |
| **[🎯 Microsoft Office Backstage](details/MicrosoftOfficeBackstage.md)** | Microsoft Office Backstage | **MicrosoftOfficeBackstage.tkape** | Brian Maloney | 1.0 |
| **[🎯 MOF](details/MOF.md)** | MOF files (WMI) | **MOF.tkape** | Eric Zimmerman | 1.0 |
| **[🎯 Netclrusage Logs](details/NETCLRUsageLogs.md)** | .NET CLR UsageLogs | **NETCLRUsageLogs.tkape** | Matias Davaro, Thomas DIOT (Qazeer) | 1.1 |
| **[🎯 NTFS Transaction Log ($LogFile)](details/$LogFile.md)** | A transaction log used by NTFS to maintain file system integrity. It records transaction steps for metadata operations before they are committed to the MFT. | **$LogFile.tkape** | Eric Zimmerman | 1.0 |
| **[🎯 Office Autosave](details/OfficeAutosave.md)** | Office Autosave | **OfficeAutosave.tkape** | Russ Taylor | 1.0 |
| **[🎯 Office Diagnostics](details/OfficeDiagnostics.md)** | Office Diagnostics | **OfficeDiagnostics.tkape** | teddy-ROxPin | 1.0 |
| **[🎯 Office Document Cache](details/OfficeDocumentCache.md)** | Office Document Cache | **OfficeDocumentCache.tkape** | Banaanhangwagen | 1.0 |
| **[🎯 Open SUSE](details/openSUSE.md)** | openSUSE on Windows Subsystem for Linux | **openSUSE.tkape** | Matt Dawson | 1.0 |
| **[🎯 Perf Logs](details/PerfLogs.md)** | Perflogs Folder Copy | **PerfLogs.tkape** | Vito Alfano | 1.0 |
| **[🎯 Power Shell7config](details/PowerShell7Config.md)** | PowerShell 7 Runtime Config | **PowerShell7Config.tkape** | Andrew Rathbun | 1.0 |
| **[🎯 Push Notification](details/PushNotification.md)** | Windows Push Notification Service | **PushNotification.tkape** | Zawadi Done | 1.0 |
| **[🎯 Quick Assist](details/QuickAssist.md)** | Microsoft Quick Assist/Remote Help | **QuickAssist.tkape** | Andrew Rathbun | 1.1 |
| **[🎯 Recent Folders](details/RecentFolders.md)** | Recent Folders LNK files | **RecentFolders.tkape** | Max Zabuty | 1 |
| **[🎯 RecentFileCache](details/RecentFileCache.md)** | Precursor file to Amcache (RecentFileCache.bcf) on older versions of Windows. It records paths and filenames of recently run applications. | **RecentFileCache.tkape** | Eric Zimmerman | 1.0 |
| **[🎯 Recycle Bin Data Files](details/RecycleBin_DataFiles.md)** | Recycle Bin Data Files | **RecycleBin_DataFiles.tkape** | Joshua Hickman, Andreas Hunkeler (@Karneades), Brian Maloney | 1.2 |
| **[🎯 Recycle Bin Info Files](details/RecycleBin_InfoFiles.md)** | Recycle Bin Info Files | **RecycleBin_InfoFiles.tkape** | Joshua Hickman, Andreas Hunkeler (@Karneades) | 1.0 |
| **[🎯 Recycle Bin Metadata](details/RecycleBin.md)** | Deleted file metadata files ($I*) and raw deleted file contents ($R*) residing within the hidden `$Recycle.Bin` directory on all drives. | **RecycleBin.tkape** | Mark Hallman / Joshua Hickman | 2.0 |
| **[🎯 Registry Hives Msixapps](details/RegistryHivesMSIXApps.md)** | MSIX/APPX App Hives | **RegistryHivesMSIXApps.tkape** | Zach Stanford, Mari DeGrazia, Reece394 | 1.2 |
| **[🎯 Registry Hives Other](details/RegistryHivesOther.md)** | Other Registry Hives | **RegistryHivesOther.tkape** | Andrew Rathbun | 1.1 |
| **[🎯 Roaming Profile](details/RoamingProfile.md)** | User Related Registry Hives, LNK files, etc | **RoamingProfile.tkape** | Scott Downie | 1.1 |
| **[🎯 Sccmclient Logs](details/SCCMClientLogs.md)** | SCCM Client Log Files | **SCCMClientLogs.tkape** | Andrew Rathbun | 1.0 |
| **[🎯 Scheduled Tasks](details/ScheduledTasks.md)** | Scheduled tasks (*.job and XML) | **ScheduledTasks.tkape** | Eric Zimmerman, Reece394 | 1.2 |
| **[🎯 SDB](details/SDB.md)** | Shim SDB FIles | **SDB.tkape** | Troy Larson | 1.0 |
| **[🎯 Signature Catalog](details/SignatureCatalog.md)** | Obtain detached signature catalog files | **SignatureCatalog.tkape** | Mike Pilkington | 1.0 |
| **[🎯 Startup Folders](details/StartupFolders.md)** | Startup Folders | **StartupFolders.tkape** | Jason Ballard | 1.0 |
| **[🎯 Startup Info](details/StartupInfo.md)** | StartupInfo XML Files | **StartupInfo.tkape** | Hadar Yudovich | 1.0 |
| **[🎯 SUM](details/SUM.md)** | SUM Database | **SUM.tkape** | Andrew Rathbun, Yogesh Khatri | 1.1 |
| **[🎯 SUM 5bf76bb6 F742 4c89 8322 887b3e25b3ac](details/SUM_5bf76bb6-f742-4c89-8322-887b3e25b3ac.md)** | SUM Database | **SUM_5bf76bb6-f742-4c89-8322-887b3e25b3ac.tkape** | Andrew Rathbun | 1.0 |
| **[🎯 Suselinux Enterprise Server](details/SUSELinuxEnterpriseServer.md)** | SUSE Linux Enterprise Server on Windows Subsystem for Linux | **SUSELinuxEnterpriseServer.tkape** | Matt Dawson | 1.0 |
| **[🎯 Syscache](details/Syscache.md)** | syscache.hve | **Syscache.tkape** | Phill Moore | 1.0 |
| **[🎯 System Registry Hives](details/RegistryHivesSystem.md)** | System-wide registry database files (SYSTEM, SOFTWARE, SAM, SECURITY). These house core system configuration, hardware parameters, installed applications, and local accounts. | **RegistryHivesSystem.tkape** | Eric Zimmerman / Mark Hallman | 1.0 |
| **[🎯 System Resource Usage Monitor](details/SRUM.md)** | System database (srudb.dat) documenting long-term system resource utilization including network traffic, CPU times, application energy usage, and active background pushes. | **SRUM.tkape** | Mark Hallman | 1.0 |
| **[🎯 USB Device Logs](details/USBDevicesLogs.md)** | Collects setupapi.dev.log files, system setup logs, and hardware device logs detailing external storage connections and driver setups. | **USBDevicesLogs.tkape** | Eric Zimmerman, esecrpm | 1.1 |
| **[🎯 Usbdevices Logs 279b043d 4edf 40a4 A77a Cdb3f6ab37f5](details/USBDevicesLogs_279b043d-4edf-40a4-a77a-cdb3f6ab37f5.md)** | USB devices log files | **USBDevicesLogs_279b043d-4edf-40a4-a77a-cdb3f6ab37f5.tkape** | Eric Zimmerman | 1.0 |
| **[🎯 User Registry Hives](details/RegistryHivesUser.md)** | User-level registry database files (NTUSER.DAT and UsrClass.dat). These store individual user workspace configurations, recent file usage, shellbags, and application habits. | **RegistryHivesUser.tkape** | Eric Zimmerman / Mark Hallman | 1.0 |
| **[🎯 Users Folders](details/UsersFolders.md)** | Users folders Dump | **UsersFolders.tkape** | Vito Alfano | 1.0 |
| **[🎯 USN Journal ($UsnJrnl:$J)](details/$J.md)** | The Update Sequence Number (USN) Change Journal. It records metadata changes to files and folders on an NTFS volume, providing a rolling history of disk operations. | **$J.tkape** | Eric Zimmerman and Andrew Rathbun | 1.1 |
| **[🎯 Virtual Disks](details/VirtualDisks.md)** | Virtual Disks | **VirtualDisks.tkape** | Phill Moore | 1.0 |
| **[🎯 Volume Boot Record ($Boot)](details/$Boot.md)** | The boot sector of an NTFS partition. It contains crucial disk geometry configurations, cluster sizing, and bootstrap code used by the system bootloader. | **$Boot.tkape** | Eric Zimmerman | 1.0 |
| **[🎯 WBEM](details/WBEM.md)** | Web-Based Enterprise Management (WBEM) | **WBEM.tkape** | Mark Hallman | 1.0 |
| **[🎯 Windows App](details/WindowsApp.md)** | WindowsApp Logs | **WindowsApp.tkape** | Vito Alfano | 1.0 |
| **[🎯 Windows Copilot Recall](details/WindowsCopilotRecall.md)** | Windows Copilot+ Recall | **WindowsCopilotRecall.tkape** | Zach Stanford/Phill Moore | 1.0 |
| **[🎯 Windows Error Reporting](details/WER.md)** | Windows Error Reporting files (.wer) and system crash logs. These contain program crash crashdumps, crash times, faulting module names, and command-line arguments. | **WER.tkape** | Troy Larson | 1.1 |
| **[🎯 Windows Firewall](details/WindowsFirewall.md)** | Windows Firewall Logs | **WindowsFirewall.tkape** | Mike Cary | 1.0 |
| **[🎯 Windows Hello](details/WindowsHello.md)** | Windows Hello | **WindowsHello.tkape** | Kevin Pagano | 1.0 |
| **[🎯 Windows Index Search](details/WindowsIndexSearch.md)** | Windows Index Search | **WindowsIndexSearch.tkape** | Mark Hallman, Reece394 | 1.2 |
| **[🎯 Windows Notifications DB](details/WindowsNotificationsDB.md)** | Windows 10 Notification DB | **WindowsNotificationsDB.tkape** | Hadar Yudovich | 1.0 |
| **[🎯 Windows Osupgrade Artifacts](details/WindowsOSUpgradeArtifacts.md)** | Windows OS Upgrade Artifacts | **WindowsOSUpgradeArtifacts.tkape** | Andrew Rathbun | 1.1 |
| **[🎯 Windows Power Diagnostics](details/WindowsPowerDiagnostics.md)** | Windows Power Diagnostics | **WindowsPowerDiagnostics.tkape** | Andrew Rathbun | 1.0 |
| **[🎯 Windows Prefetch](details/Prefetch.md)** | System-generated files (.pf) designed to optimize application launch times. They store program execution metadata, run counts, timestamps, and files loaded during launch. | **Prefetch.tkape** | Eric Zimmerman | 1.0 |
| **[🎯 Windows Subsystemfor Android](details/WindowsSubsystemforAndroid.md)** | Windows Subsystem for Android (WSA) | **WindowsSubsystemforAndroid.tkape** | Andrew Rathbun | 1.0 |
| **[🎯 Windows Telemetry Diagnostics Legacy](details/WindowsTelemetryDiagnosticsLegacy.md)** | Legacy Windows Telemetry and Diagnostics files (*.rbs) | **WindowsTelemetryDiagnosticsLegacy.tkape** | Andrew Rathbun and Josh Mitchell | 1.0 |
| **[🎯 Windows Timeline Database](details/WindowsTimeline.md)** | SQLite database containing user activity logs (ActivitiesCache.db). It records opened files, clipboard copies, application focus histories, and connected external devices. | **WindowsTimeline.tkape** | Lee Whitfield, Thomas DIOT (Qazeer) | 1.1 |
| **[🎯 Windows Update](details/WindowsUpdate.md)** | Windows Update Logs | **WindowsUpdate.tkape** | Rick van Dreunen | 1.0 |
| **[🎯 Xprestore Points](details/XPRestorePoints.md)** | XP Restore Points - System Volume Information directory | **XPRestorePoints.tkape** | Phill Moore | 1.0 |

---

[⬅️ Back to Core OS & File System](core_os_artifacts.md)
