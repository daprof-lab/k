# **💻 Core OS & File System**

{% hint style="info" %}

**Investigator Note:** This section contains targets and modules for the most critical Windows internal artifacts, including the MFT, Registry Hives, execution evidence (Prefetch/Amcache), and historical OS data (SRUM/Timeline).

{% endhint %}

{% tabs %}

{% tab title="🎯 Targets (.tkape)" %}

| File Name | Description | Author | Version |
| :---- | :---- | :---- | :---- |
| **$MFT.tkape** | $MFT | Eric Zimmerman | 1.0 |
| **$J.tkape** | $J (UsnJrnl) | Eric Zimmerman / Andrew Rathbun | 1.1 |
| **$LogFile.tkape** | $LogFile | Eric Zimmerman | 1.0 |
| **$Boot.tkape** | $Boot | Eric Zimmerman | 1.0 |
| **Prefetch.tkape** | Prefetch files | Eric Zimmerman | 1.0 |
| **RegistryHivesSystem.tkape** | System level/related Registry hives | Eric Zimmerman / Mark Hallman | 1.0 |
| **RegistryHivesUser.tkape** | User Related Registry hives | Eric Zimmerman / Mark Hallman | 1.0 |
| **LNKFilesAndJumpLists.tkape** | LNK Files and jump lists | Eric Zimmerman / Andrew Rathbun / Yogesh Khatri | 1.3 |
| **ThumbCache.tkape** | Thumbcache DB | Eric Zimmerman | 1.0 |
| **SRUM.tkape** | System Resource Usage Monitor (SRUM) Data | Mark Hallman | 1.0 |
| **Amcache.tkape** | Amcache.hve | Eric Zimmerman | 1.0 |
| **RecentFileCache.tkape** | RecentFileCache | Eric Zimmerman | 1.0 |
| **WindowsTimeline.tkape** | ActivitiesCache.db collector | Lee Whitfield / Thomas DIOT | 1.1 |
| **EvidenceOfExecution.tkape** | Evidence of execution related files | Eric Zimmerman | 1.1 |
| **RecycleBin.tkape** | Recycle Bin DataAndInfo | Mark Hallman / Joshua Hickman | 2.0 |
| **USBDevicesLogs.tkape** | USB devices log files | Eric Zimmerman / esecrpm | 1.1 |
| **WER.tkape** | Windows Error Reporting | Troy Larson | 1.1 |
| **BITS.tkape** | Microsoft BITS persistent files | Jos Clephas | 1.0 |

{% endtab %}

{% tab title="⚙️ Modules (.mkape)" %}

| File Name | Description | Author | Version |
| :---- | :---- | :---- | :---- |
| **MFTECmd.mkape** | MFTECmd: process all files handled by MFTECmd | Eric Zimmerman | 1.0 |
| **PECmd.mkape** | PECmd: process prefetch files | Eric Zimmerman / Andrew Rathbun | 1.1 |
| **LECmd.mkape** | LECmd: process .lnk files | Eric Zimmerman | 1.1 |
| **JLECmd.mkape** | JLECmd: process jumplist files | Eric Zimmerman | 1.1 |
| **RBCmd.mkape** | RBCmd: process recycle bin artifacts | Eric Zimmerman | 1.0 |
| **SrumECmd.mkape** | SrumECmd: SRUM Parser | Andrew Rathbun | 1.1 |
| **AmcacheParser.mkape** | AmcacheParser: extract program execution information | Eric Zimmerman | 1.1 |
| **AppCompatCacheParser.mkape** | AppCompatCacheParser: extract AppCompatCache (shimcache) information | Eric Zimmerman | 1.1 |
| **RecentFileCacheParser.mkape** | RecentFileCacheParser: extract file names | Eric Zimmerman | 1.0 |
| **RegRipper.mkape** | RegRipper: parse all supported hives | ZeArioch / Phill Moore | 1.1 |
| **Reghunter.mkape** | Execute all Reghunter modules | Georg Lauenstein | 1.0 |
| **WxTCmd.mkape** | WxTCmd.exe: process Windows Timeline/Activities Cache files | Mike Cary | 1.0 |
| **PowerShell\_RecycleBinParsing.mkape** | Parses Recycle Bin and exports to CSV/JSON | Max Zabuty | 1.0 |

{% endtab %}

{% endtabs %}