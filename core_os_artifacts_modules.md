# **⚙️ Core OS & File System - Modules**

{% hint style="success" %}

**Module Execution Info:** These modules process data collected under the Core OS & File System category using specialized analytical tools. Click on any **Short Name** to view a dedicated detail page including use-cases and KAPE module definitions.

{% endhint %}

[⬅️ Back to Core OS & File System](core_os_artifacts.md)

---

## **Available Modules (.mkape)**

| Short Name | Description | File Name | Author | Version |
| :--- | :--- | :--- | :--- | :--- |
| **[⚙️ ALL](details/!ALL.md)** | Run all modules | **!ALL.mkape** | Eric Zimmerman | 1 |
| **[⚙️ AmcacheParser](details/AmcacheParser.md)** | Runs AmcacheParser to parse Amcache.hve hives, extracting executable execution paths, hashes, compiler times, and installation statuses. | **AmcacheParser.mkape** | Eric Zimmerman | 1.1 |
| **[⚙️ AppCompatCacheParser (Shimcache)](details/AppCompatCacheParser.md)** | Runs AppCompatCacheParser to extract execution records from the SYSTEM registry hive, locating file paths and execution status. | **AppCompatCacheParser.mkape** | Eric Zimmerman | 1.1 |
| **[⚙️ Bstrings Aeon Wallet](details/bstrings_AeonWallet.md)** | Use bstrings to GREP for Aeon Wallets | **bstrings_AeonWallet.mkape** | Andrew Rathbun, Georg Lauenstein | 1.1 |
| **[⚙️ Bstrings Bit Coin Wallet](details/bstrings_BitCoinWallet.md)** | Use bstrings to GREP for BitCoin Wallets | **bstrings_BitCoinWallet.mkape** | Andrew Rathbun, Georg Lauenstein | 1.1 |
| **[⚙️ Bstrings Bitlocker](details/bstrings_Bitlocker.md)** | Use bstrings to GREP for Bitlocker recovery keys | **bstrings_Bitlocker.mkape** | Chris Kudless, Georg Lauenstein | 1.1 |
| **[⚙️ Bstrings Byte Coin Wallet](details/bstrings_ByteCoinWallet.md)** | Use bstrings to GREP for ByteCoin Wallets | **bstrings_ByteCoinWallet.mkape** | Andrew Rathbun, Georg Lauenstein | 1.0 |
| **[⚙️ Bstrings Credit Cards](details/bstrings_CreditCards.md)** | Use bstrings to GREP for Credit Card numbers | **bstrings_CreditCards.mkape** | Andrew Rathbun, Georg Lauenstein | 1.1 |
| **[⚙️ Bstrings Dash Coin Wallet](details/bstrings_DashCoinWallet.md)** | Use bstrings to GREP for DashCoin Wallets | **bstrings_DashCoinWallet.mkape** | Andrew Rathbun, Georg Lauenstein | 1.1 |
| **[⚙️ Bstrings Dash Coin Wallet2](details/bstrings_DashCoinWallet2.md)** | Use bstrings to GREP for DashCoin Wallets | **bstrings_DashCoinWallet2.mkape** | Andrew Rathbun, Georg Lauenstein | 1.1 |
| **[⚙️ Bstrings Email](details/bstrings_Email.md)** | Use bstrings to GREP for email addresses | **bstrings_Email.mkape** | Andrew Rathbun, Georg Lauenstein | 1.1 |
| **[⚙️ Bstrings Fantom Coin Wallet](details/bstrings_FantomCoinWallet.md)** | Use bstrings to GREP for FantomCoin Wallets | **bstrings_FantomCoinWallet.mkape** | Andrew Rathbun, Georg Lauenstein | 1.1 |
| **[⚙️ Bstrings Macaddresses](details/bstrings_MACAddresses.md)** | Use bstrings to GREP for MAC Addresses | **bstrings_MACAddresses.mkape** | Andrew Rathbun, Georg Lauenstein | 1.1 |
| **[⚙️ Bstrings Monero Wallet](details/bstrings_MoneroWallet.md)** | Use bstrings to GREP for Monero Wallets | **bstrings_MoneroWallet.mkape** | Andrew Rathbun, Georg Lauenstein | 1.2 |
| **[⚙️ Bstrings SSN](details/bstrings_SSN.md)** | Use bstrings to GREP for US Social Security numbers | **bstrings_SSN.mkape** | Andrew Rathbun, Georg Lauenstein | 1.1 |
| **[⚙️ Bstrings Sumo Koin Wallet](details/bstrings_SumoKoinWallet.md)** | Use bstrings to GREP for SumoKoin Wallets | **bstrings_SumoKoinWallet.mkape** | Andrew Rathbun, Georg Lauenstein | 1.1 |
| **[⚙️ Bstrings UNC](details/bstrings_UNC.md)** | Use bstrings to GREP for UNC Paths | **bstrings_UNC.mkape** | Andrew Rathbun, Georg Lauenstein | 1.1 |
| **[⚙️ Bstrings Usphone](details/bstrings_USPhone.md)** | Use bstrings to GREP for US Phone Numbers | **bstrings_USPhone.mkape** | Andrew Rathbun, Georg Lauenstein | 1.1 |
| **[⚙️ Bstrings Win Path](details/bstrings_WinPath.md)** | Use bstrings to GREP for Windows style paths | **bstrings_WinPath.mkape** | Andrew Rathbun, Georg Lauenstein | 1.1 |
| **[⚙️ Bstrings Zip Codes](details/bstrings_ZipCodes.md)** | Use bstrings to GREP for US Zip Codes | **bstrings_ZipCodes.mkape** | Andrew Rathbun, Georg Lauenstein | 1.1 |
| **[⚙️ JLECmd Jump List Parser](details/JLECmd.md)** | Runs JLECmd to process taskbar Jump Lists, recovering pinned applications and recent user document browsing habits. | **JLECmd.mkape** | Eric Zimmerman | 1.1 |
| **[⚙️ LECmd Link File Parser](details/LECmd.md)** | Runs LECmd to parse Windows LNK shortcut files, revealing target file specs, network paths, volume serial numbers, and MAC addresses. | **LECmd.mkape** | Eric Zimmerman | 1.1 |
| **[⚙️ Mftecmd $boot](details/MFTECmd_$Boot.md)** | MFTECmd: process $Boot files | **MFTECmd_$Boot.mkape** | Eric Zimmerman | 1.0 |
| **[⚙️ Mftecmd $I30](details/MFTECmd_$I30.md)** | MFTECmd: process $INDX/$I30 files | **MFTECmd_$I30.mkape** | Phill Moore | 1.0 |
| **[⚙️ Mftecmd $J](details/MFTECmd_$J.md)** | MFTECmd: process $J / $UsnJrnl$J files | **MFTECmd_$J.mkape** | Eric Zimmerman, Thomas DIOT, Reece394 | 1.2 |
| **[⚙️ Mftecmd $MFT](details/MFTECmd_$MFT.md)** | MFTECmd: process $MFT files | **MFTECmd_$MFT.mkape** | Eric Zimmerman | 1.0 |
| **[⚙️ Mftecmd $MFT Bodyfile](details/MFTECmd_$MFT_bodyfile.md)** | MFTECmd: process $MFT files and output a bodyfile for mactime / tsk | **MFTECmd_$MFT_bodyfile.mkape** | Angry-Bender | 1.0 |
| **[⚙️ Mftecmd $MFT File Listing](details/MFTECmd_$MFT_FileListing.md)** | MFTECmd: process $MFT files, then output file listing | **MFTECmd_$MFT_FileListing.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Mftecmd $MFT Process Mftslack](details/MFTECmd_$MFT_ProcessMFTSlack.md)** | MFTECmd: process $MFT files with FILE slack recovery | **MFTECmd_$MFT_ProcessMFTSlack.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Mftecmd $SDS](details/MFTECmd_$SDS.md)** | MFTECmd: process $SDS files | **MFTECmd_$SDS.mkape** | Eric Zimmerman | 1.0 |
| **[⚙️ Mftecmd Bulk Extractor Carved Mftrecords](details/MFTECmd_BulkExtractorCarvedMFTRecords.md)** | MFTECmd: process bulk extractor carved MFT files | **MFTECmd_BulkExtractorCarvedMFTRecords.mkape** | Phill Moore | 1.0 |
| **[⚙️ MFTECmd Parser](details/MFTECmd.md)** | Executes Eric Zimmerman's MFTECmd tool to process raw `$MFT`, `$Boot`, `$LogFile`, and `$J` files into structured, timeline-friendly CSV tables. | **MFTECmd.mkape** | Eric Zimmerman | 1.0 |
| **[⚙️ Ntfslog Tracker $J Cecd789d 90c9 4cc8 943d B1d5008071b9](details/NTFSLogTracker_$J_cecd789d-90c9-4cc8-943d-b1d5008071b9.md)** | NTFS Log Tracker: process $J files | **NTFSLogTracker_$J_cecd789d-90c9-4cc8-943d-b1d5008071b9.mkape** | Hyun Yi @hyuunnn | 1.0 |
| **[⚙️ Ntfslog Tracker $log File C0966e7a 1cc6 4bf7 Be28 871caa8de3da](details/NTFSLogTracker_$LogFile_c0966e7a-1cc6-4bf7-be28-871caa8de3da.md)** | NTFS Log Tracker: process $LogFile files | **NTFSLogTracker_$LogFile_c0966e7a-1cc6-4bf7-be28-871caa8de3da.mkape** | Hyun Yi @hyuunnn | 1.0 |
| **[⚙️ PECmd Prefetch Parser](details/PECmd.md)** | Runs PECmd to process Windows Prefetch files (.pf), mapping process execution times, loaded DLL lists, and launching directories. | **PECmd.mkape** | Eric Zimmerman and Andrew Rathbun | 1.1 |
| **[⚙️ Plaso](details/Plaso.md)** | plaso end to end test | **Plaso.mkape** | Mark Hallman | 1.0 |
| **[⚙️ Power Shell Accessibility Features](details/PowerShell_AccessibilityFeatures.md)** | Checks for Debugger registry value and file integrity of specific Windows features | **PowerShell_AccessibilityFeatures.mkape** | Max Zabuty | 1.0 |
| **[⚙️ Power Shell Active Drives](details/PowerShell_ActiveDrives.md)** | Active Drives List | **PowerShell_ActiveDrives.mkape** | Max Zabuty | 1.0 |
| **[⚙️ Power Shell Bitlocker Key Extraction](details/PowerShell_Bitlocker_Key_Extraction.md)** | Extract Bitlocker Key via powershell | **PowerShell_Bitlocker_Key_Extraction.mkape** | Vito Alfano | 1.0 |
| **[⚙️ Power Shell Bitlocker Status](details/PowerShell_Bitlocker_Status.md)** | Extract Bitlocker status details | **PowerShell_Bitlocker_Status.mkape** | Vito Alfano | 1.0 |
| **[⚙️ Power Shell Defender Exclusions](details/PowerShell_Defender_Exclusions.md)** | Windows Defender Exclusions | **PowerShell_Defender_Exclusions.mkape** | nov3mb3r | 1.0 |
| **[⚙️ Power Shell DLL List](details/PowerShell_DLL_List.md)** | DLL List | **PowerShell_DLL_List.mkape** | nov3mb3r, JorZay | 1.1 |
| **[⚙️ Power Shell Docker Containers](details/PowerShell_Docker_Containers.md)** | Docker Container Details | **PowerShell_Docker_Containers.mkape** | DReneau | 1.1 |
| **[⚙️ Power Shell Drivers](details/PowerShell_Drivers.md)** | Drivers List | **PowerShell_Drivers.mkape** | Max Zabuty | 1.0 |
| **[⚙️ Power Shell Local Admin](details/PowerShell_LocalAdmin.md)** | Gathers detailed list of local admin users | **PowerShell_LocalAdmin.mkape** | Vito Alfano | 1.0 |
| **[⚙️ Power Shell Local Group List](details/PowerShell_Local_Group_List.md)** | Gathers detailed list of local groups | **PowerShell_Local_Group_List.mkape** | Vito Alfano | 1.0 |
| **[⚙️ Power Shell Local Groups](details/PowerShell_LocalGroups.md)** | Local Groups List | **PowerShell_LocalGroups.mkape** | Max Zabuty | 1.0 |
| **[⚙️ Power Shell Local Users](details/PowerShell_LocalUsers.md)** | Local Users List | **PowerShell_LocalUsers.mkape** | Max Zabuty | 1.0 |
| **[⚙️ Power Shell Named Pipes](details/PowerShell_NamedPipes.md)** | Named Pipes List | **PowerShell_NamedPipes.mkape** | Max Zabuty | 1.0 |
| **[⚙️ Power Shell Net Neighbor](details/PowerShell_NetNeighbor.md)** | Displaying ARP Table using PowerShell | **PowerShell_NetNeighbor.mkape** | Max Zabuty | 1.0 |
| **[⚙️ Power Shell Net Route](details/PowerShell_NetRoute.md)** | Collecting Network Routing Table Information | **PowerShell_NetRoute.mkape** | Max Zabuty | 1.0 |
| **[⚙️ Power Shell Net User Administrators](details/PowerShell_NetUserAdministrators.md)** | Gathers Basic System Information Using the Net Command (members of local administrator group) | **PowerShell_NetUserAdministrators.mkape** | Andreas Hunkeler (@Karneades) | 1.0 |
| **[⚙️ Power Shell Parse Scheduled Tasks](details/PowerShell_ParseScheduledTasks.md)** | Scheduled Task XMLs Parser | **PowerShell_ParseScheduledTasks.mkape** | Vikas Singh(@vikas891) | 1.0 |
| **[⚙️ Power Shell Process Cmdline](details/PowerShell_Process_Cmdline.md)** | Process Commandline | **PowerShell_Process_Cmdline.mkape** | nov3mb3r | 1.0 |
| **[⚙️ Power Shell Process List Cim Instance](details/PowerShell_ProcessList_CimInstance.md)** | Display running processes and context information | **PowerShell_ProcessList_CimInstance.mkape** | Markus Neis, Swisscom | 1.0 |
| **[⚙️ Power Shell Process List WMI](details/PowerShell_ProcessList_WMI.md)** | Display a running process list with a variety of fields | **PowerShell_ProcessList_WMI.mkape** | piesecurity | 1.0 |
| **[⚙️ Power Shell Processes](details/PowerShell_Processes.md)** | Display a running process list with a variety of fields - modified | **PowerShell_Processes.mkape** | Max Zabuty | 1.0 |
| **[⚙️ Power Shell Processes Including Services](details/PowerShell_ProcessesIncludingServices.md)** | Processes list including the services running them | **PowerShell_ProcessesIncludingServices.mkape** | Max Zabuty | 1.0 |
| **[⚙️ Power Shell Services List](details/PowerShell_Services_List.md)** | Retrieves basic information about active running services. It replaces the command net start. | **PowerShell_Services_List.mkape** | Vito Alfano | 1.0 |
| **[⚙️ Power Shell Smbmapping](details/PowerShell_SMBMapping.md)** | Retrieves the Server Message Block (SMB) client directory mappings. It replaces the command net use. | **PowerShell_SMBMapping.mkape** | Vito Alfano, Max Zabuty | 1.0 |
| **[⚙️ Power Shell Smbopen File](details/PowerShell_SMBOpenFile.md)** | Retrieves basic information about the files that are open via SMB | **PowerShell_SMBOpenFile.mkape** | Vito Alfano, Max Zabuty | 1.0 |
| **[⚙️ Power Shell Smbsession](details/PowerShell_SMBSession.md)** | Retrieves basic information about active SMB sessions. It replaces the command net use. | **PowerShell_SMBSession.mkape** | Vito Alfano, Max Zabuty | 1.0 |
| **[⚙️ Power Shell Startup Commands](details/PowerShell_Startup_Commands.md)** | Commands on Startup | **PowerShell_Startup_Commands.mkape** | nov3mb3r | 1.0 |
| **[⚙️ Power Shell System Information](details/PowerShell_SystemInformation.md)** | Specific System Information | **PowerShell_SystemInformation.mkape** | Max Zabuty | 1.0 |
| **[⚙️ Power Shell Tcpconnections](details/PowerShell_TCPConnections.md)** | TCP Established Connections including DNSCache and process information | **PowerShell_TCPConnections.mkape** | Max Zabuty | 1.0 |
| **[⚙️ Power Shell User List](details/PowerShell_User_List.md)** | Gathers detailed list of local users | **PowerShell_User_List.mkape** | Vito Alfano | 1.0 |
| **[⚙️ Power Shell Wmiproviders](details/PowerShell_WMIProviders.md)** | Output of WMI Event Consumers, Filters, and Filter to Consumer Binders - All to CSV and JSON | **PowerShell_WMIProviders.mkape** | Max Zabuty | 1.0 |
| **[⚙️ Power Shell Wmirepository Auditing](details/PowerShell_WMIRepositoryAuditing.md)** | Collect WMI repository information | **PowerShell_WMIRepositoryAuditing.mkape** | Andreas Hunkeler (@Karneades) | 1.0 |
| **[⚙️ PowerShell Recycle Bin Parser](details/PowerShell_RecycleBinParsing.md)** | Parses Windows Recycle Bin directory states using lightweight PowerShell scripts, outputting mapped paths and file sizes to structured files. | **PowerShell_RecycleBinParsing.mkape** | Max Zabuty | 1.0 |
| **[⚙️ RBCmd Recycle Bin Parser](details/RBCmd.md)** | Runs RBCmd to parse Windows Recycle Bin metadata files, resolving raw deleted files to original paths, file sizes, and deletion times. | **RBCmd.mkape** | Eric Zimmerman | 1.0 |
| **[⚙️ RecentFileCache Parser](details/RecentFileCacheParser.md)** | Parses legacy RecentFileCache.bcf files to recover application execution histories from older versions of Windows. | **RecentFileCacheParser.mkape** | Eric Zimmerman | 1.0 |
| **[⚙️ Recmd All Reg Executables Found Or Run](details/RECmd_AllRegExecutablesFoundOrRun.md)** | RECmd: AllRegExecutablesFoundOrRun | **RECmd_AllRegExecutablesFoundOrRun.mkape** | Andrew Rathbun | 1.1 |
| **[⚙️ Recmd Basic System Info](details/RECmd_BasicSystemInfo.md)** | RECmd: BasicSystemInfo | **RECmd_BasicSystemInfo.mkape** | Andrew Rathbun | 1.1 |
| **[⚙️ Recmd Bcdboot Volume](details/RECmd_BCDBootVolume.md)** | RECmd: BCDBootVolume | **RECmd_BCDBootVolume.mkape** | Andrew Rathbun | 1.1 |
| **[⚙️ Recmd Dfirbatch](details/RECmd_DFIRBatch.md)** | RECmd: DFIR | **RECmd_DFIRBatch.mkape** | Andrew Rathbun | 1.2 |
| **[⚙️ Recmd Installed Software](details/RECmd_InstalledSoftware.md)** | RECmd: InstalledSoftware | **RECmd_InstalledSoftware.mkape** | Andrew Rathbun | 1.1 |
| **[⚙️ Recmd Recmd Batch MC](details/RECmd_RECmd_Batch_MC.md)** | RECmd: RECmd_Batch_MC | **RECmd_RECmd_Batch_MC.mkape** | Andrew Rathbun | 1.1 |
| **[⚙️ Recmd Registry Aseps](details/RECmd_RegistryASEPs.md)** | RECmd: RegistryASEPs | **RECmd_RegistryASEPs.mkape** | Andrew Rathbun | 1.1 |
| **[⚙️ Recmd Software Aseps](details/RECmd_SoftwareASEPs.md)** | RECmd: SoftwareASEPs | **RECmd_SoftwareASEPs.mkape** | Andrew Rathbun | 1.1 |
| **[⚙️ Recmd Software Classes Aseps](details/RECmd_SoftwareClassesASEPs.md)** | RECmd: SoftwareClassesASEPs | **RECmd_SoftwareClassesASEPs.mkape** | Andrew Rathbun | 1.1 |
| **[⚙️ Recmd Software Wo W6432aseps](details/RECmd_SoftwareWoW6432ASEPs.md)** | RECmd: SoftwareWoW6432ASEPs | **RECmd_SoftwareWoW6432ASEPs.mkape** | Andrew Rathbun | 1.1 |
| **[⚙️ Recmd System Aseps](details/RECmd_SystemASEPs.md)** | RECmd: SystemASEPs | **RECmd_SystemASEPs.mkape** | Andrew Rathbun | 1.1 |
| **[⚙️ Recmd User Activity](details/RECmd_UserActivity.md)** | RECmd: UserActivity | **RECmd_UserActivity.mkape** | Andrew Rathbun | 1.1 |
| **[⚙️ Recmd User Classes Aseps](details/RECmd_UserClassesASEPs.md)** | RECmd: UserClassesASEPs | **RECmd_UserClassesASEPs.mkape** | Andreas Hunkeler (@Karneades) | 1.1 |
| **[⚙️ RegRipper Hive Parser](details/RegRipper.md)** | Runs the RegRipper framework to parse user, system, software, and sam hives using targeted forensic plugins. | **RegRipper.mkape** | ZeArioch <https://{github,twitter}.com/ZeArioch>, Phill Moore, Andreas Hunkeler (@Karneades) | 1.1 |
| **[⚙️ Sbecmd](details/SBECmd.md)** | SBECmd: process shellbags | **SBECmd.mkape** | Barrie Hill | 1.0 |
| **[⚙️ Sqlecmd](details/SQLECmd.md)** | SQLECmd: process SQLite databases | **SQLECmd.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Sqlecmd Hunt](details/SQLECmd_Hunt.md)** | SQLECmd: process SQLite databases with Hunt mode | **SQLECmd_Hunt.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ SrumECmd SRUM Parser](details/SrumECmd.md)** | Runs SrumECmd to parse srudb.dat databases, detailing historic application network uploads, downloads, battery usage, and CPU times. | **SrumECmd.mkape** | Andrew Rathbun | 1.1 |
| **[⚙️ Sum Ecmd](details/SumECmd.md)** | SumECmd: Process Microsoft User Access Logs | **SumECmd.mkape** | Andrew Rathbun | 1.1 |
| **[⚙️ Tzworks Evtwalk64 Event Logs Application Events](details/TZWorks_evtwalk64_EventLogs_ApplicationEvents.md)** | Parses Application event log using TZWorks evtwalk64 | **TZWorks_evtwalk64_EventLogs_ApplicationEvents.mkape** | Justin Price | 1.0 |
| **[⚙️ Windows Gp Result](details/Windows_GpResult.md)** | gpresult | **Windows_GpResult.mkape** | NVISO (@NVISOsecurity) | 0.1 |
| **[⚙️ Windows Klist](details/Windows_klist.md)** | Gets Kerberos Tickets | **Windows_klist.mkape** | Max Zabuty | 1.0 |
| **[⚙️ Windows Manage BDE Bit Locker Keys](details/Windows_ManageBDE_BitLockerKeys.md)** | Collect BitLocker recovery key for a volume | **Windows_ManageBDE_BitLockerKeys.mkape** | troyla@microsoft.com | 1.1 |
| **[⚙️ Windows Manage BDE Bit Locker Status](details/Windows_ManageBDE_BitLockerStatus.md)** | Check for BitLocker volumes | **Windows_ManageBDE_BitLockerStatus.mkape** | troyla@microsoft.com | 1.1 |
| **[⚙️ Windows Ms Info](details/Windows_MsInfo.md)** | msinfo | **Windows_MsInfo.mkape** | NVISO (@NVISOsecurity) | 0.1 |
| **[⚙️ Windows Nbtstat Net Bioscache](details/Windows_nbtstat_NetBIOSCache.md)** | NBTStat_NETBIOS_Cache | **Windows_nbtstat_NetBIOSCache.mkape** | Mike Cary, Max Zabuty | 1.0 |
| **[⚙️ Windows Nbtstat Net Biossessions](details/Windows_nbtstat_NetBIOSSessions.md)** | NBTStat_NETBIOS_Sessions | **Windows_nbtstat_NetBIOSSessions.mkape** | Mike Cary, Max Zabuty | 1.0 |
| **[⚙️ Windows Net Accounts](details/Windows_Net_Accounts.md)** | Gathers Basic System Information Using the Net Command (Accounts) | **Windows_Net_Accounts.mkape** | piesecurity | 1.0 |
| **[⚙️ Windows Net File](details/Windows_Net_File.md)** | Gathers Basic System Information Using the Net Command (File) | **Windows_Net_File.mkape** | piesecurity | 1.0 |
| **[⚙️ Windows Net Local Group](details/Windows_Net_LocalGroup.md)** | Gathers Basic System Information Using the Net Command (LocalGroup) | **Windows_Net_LocalGroup.mkape** | piesecurity | 1.0 |
| **[⚙️ Windows Net Session](details/Windows_Net_Session.md)** | Gathers Basic System Information Using the Net Command (Session) | **Windows_Net_Session.mkape** | piesecurity | 1.0 |
| **[⚙️ Windows Net Share](details/Windows_Net_Share.md)** | Gathers Basic System Information Using the Net Command (Share) | **Windows_Net_Share.mkape** | piesecurity | 1.0 |
| **[⚙️ Windows Net Start](details/Windows_Net_Start.md)** | Gathers Basic System Information Using the Net Command (Running Services) | **Windows_Net_Start.mkape** | piesecurity | 1.0 |
| **[⚙️ Windows Net Stat](details/Windows_NetStat.md)** | NetStat | **Windows_NetStat.mkape** | Mike Cary | 1.0 |
| **[⚙️ Windows Net Use](details/Windows_Net_Use.md)** | Gathers Basic System Information Using the Net Command (Use) | **Windows_Net_Use.mkape** | piesecurity | 1.0 |
| **[⚙️ Windows Net User](details/Windows_Net_User.md)** | Gathers Basic System Information Using the Net Command (User) | **Windows_Net_User.mkape** | piesecurity | 1.0 |
| **[⚙️ Windows Netsh Portproxy](details/Windows_netsh_portproxy.md)** | PortProxy configuration | **Windows_netsh_portproxy.mkape** | Andreas Hunkeler (@Karneades) | 1.0 |
| **[⚙️ Windows Nltest](details/Windows_nltest.md)** | Collects Domain Information | **Windows_nltest.mkape** | Max Zabuty | 1.0 |
| **[⚙️ Windows Schtasks](details/Windows_schtasks.md)** | Displays all scheduled tasks | **Windows_schtasks.mkape** | Brian Maloney | 1.2 |
| **[⚙️ Windows System Info](details/Windows_SystemInfo.md)** | Gathers Basic System Information | **Windows_SystemInfo.mkape** | piesecurity | 1.0 |
| **[⚙️ WxTCmd Timeline Parser](details/WxTCmd.md)** | Runs WxTCmd to parse Windows Timeline SQLite databases (ActivitiesCache.db), timelines user application focuses, opened documents, and clipboard logs. | **WxTCmd.mkape** | Mike Cary | 1.0 |

---

[⬅️ Back to Core OS & File System](core_os_artifacts.md)
