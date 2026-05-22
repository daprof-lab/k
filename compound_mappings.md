# 🧩 KAPE Compound Mappings & Incident Response Playbooks

Welcome to the **KAPE Compound Mappings & Incident Response Playbooks** guide. As a forensic analyst, one of your most critical decisions is determining which targets and modules to execute based on the incident context. 

KAPE uses **Compounds** (compound targets `.tkape` and compound modules `.mkape`) to group multiple individual configurations together, allowing you to run comprehensive collections in a single command. 

This guide serves as a definitive roadmap mapping out exactly what is included in these compounds, what is left out, and how to build custom target combinations for common investigation playbooks.

---

## 🗺️ **KAPE Compound Target Mappings**

Compound targets collect a predefined suite of individual forensic artifacts. Below is a mapping of the most common compound targets and the individual targets they automatically execute.

| Compound Target (`.tkape`) | Sub-Targets Included | Best Used For |
| :--- | :--- | :--- |
| **`KapeTriage.tkape`** | `Antivirus.tkape`, `CloudStorage_Metadata.tkape`, `EventLogs.tkape`, `EvidenceOfExecution.tkape`, `FileSystem.tkape`, `LNKFilesAndJumpLists.tkape`, `Notepad.tkape`, `PowerShellConsole.tkape`, `RecycleBin_InfoFiles.tkape`, `RegistryHives.tkape`, `RemoteAdmin.tkape`, `ScheduledTasks.tkape`, `SRUM.tkape`, `SUM.tkape`, `WER.tkape`, `WBEM.tkape`, `WebBrowsers.tkape`, `WindowsTimeline.tkape` | **Full Host Triage**. The default standard for standard Windows workstation triage collections. |
| **`!SANS_Triage.tkape`** | `Antivirus.tkape`, `EventLogs.tkape`, `EvidenceOfExecution.tkape`, `FileSystem.tkape`, `LNKFilesAndJumpLists.tkape`, `PowerShellConsole.tkape`, `RecycleBin.tkape`, `RegistryHives.tkape`, `ScheduledTasks.tkape`, `WindowsTimeline.tkape` | **Rapid Host Triage**. Standard collection mapping directly to the SANS DFIR triage recommendation. |
| **`!BasicCollection.tkape`** | `EventLogs.tkape`, `RegistryHives.tkape`, `EvidenceOfExecution.tkape` (Shimcache/Amcache/Prefetch) | **Ultra-Fast Recon**. Pulls only the most critical execution and log assets to assess compromise state. |
| **`FileSystem.tkape`** | `$MFT.tkape`, `$LogFile.tkape`, `$Boot.tkape`, `$J.tkape` | **File System Analysis**. Targets low-level NTFS file system structures for deep deletion and timestamp audits. |
| **`RegistryHives.tkape`** | `RegistryHivesSystem.tkape`, `RegistryHivesUser.tkape` | **Registry Triage**. Gathers all system hives (`SYSTEM`, `SOFTWARE`, `SAM`, `SECURITY`) and user hives (`NTUSER.DAT`, `UsrClass.dat`). |
| **`WebBrowsers.tkape`** | `Chrome.tkape`, `EdgeChromium.tkape`, `Firefox.tkape`, `BraveBrowser.tkape`, `Opera.tkape`, `Vivaldi.tkape` | **User Web Activity**. Focuses exclusively on browser histories, session states, downloads, and bookmarks. |

---

## ⚙️ **KAPE Compound Module Mappings**

Compound modules execute a series of external command-line tools in sequence to parse raw forensic files into structured, timeline-friendly spreadsheets.

| Compound Module (`.mkape`) | Sub-Modules (Parsers) Executed | Output Format |
| :--- | :--- | :--- |
| **`!EZParser.mkape`** | `AmcacheParser.mkape`, `AppCompatCacheParser.mkape`, `EvtxECmd.mkape`, `JLECmd.mkape`, `LECmd.mkape`, `MFTECmd.mkape`, `PECmd.mkape`, `RBCmd.mkape`, `RecentFileCacheParser.mkape`, `RECmd_DFIRBatch.mkape`, `SBECmd.mkape`, `SQLECmd.mkape`, `SrumECmd.mkape`, `SumECmd.mkape`, `WxTCmd.mkape` | **CSV Tables** (Structured timelines for Eric Zimmerman's entire suite of tools) |
| **`KAPE_Automation.mkape`** | Executes comprehensive parsers against the entire output of a triage folder, automatically running all standard analytical plugins. | **CSV & JSON Tables** |
| **`LogParser.mkape`** | `iisGeoLocate.mkape`, `LogParser_ApacheAccessLogs.mkape`, `LogParser_RDPUsageEvents.mkape` | **CSV Tables** |
| **`bstrings.mkape`** | `bstrings_URLs.mkape`, `bstrings_IPv4.mkape`, `bstrings_Emails.mkape` | **Text & CSV Logs** (Regex patterns extracted from bulk unallocated data) |
| **`Reghunter.mkape`** | `RegRipper.mkape` (User, System, Software, and SAM plugins executed sequentially) | **Text Reports** |

---

## ⚠️ **What's Missing? (Volatile & High-Volume Data)**

While compounds are highly effective, they intentionally **exclude** high-volume or highly volatile data sources to ensure KAPE remains fast, lightweight, and stealthy on production hosts. 

> [!WARNING]
> You **MUST** select and execute the following targets/modules manually if your case context demands them:
> 
> * **Physical Active Memory (RAM)**:
>   * *Why it's missing*: A full RAM dump matches the size of system RAM (e.g. 16GB–64GB) and takes minutes to write, making it too large for standard triage.
>   * *How to include*: Run **`DumpIt_Memory.mkape`** or **`MagnetForensics_RAMCapture.mkape`** manually on live systems.
> * **Third-Party Collaboration Chat Logs**:
>   * *Why it's missing*: Workplace chat apps like Slack, Microsoft Teams, and Discord sync dynamic LevelDB or SQLite databases that are heavily tailored to specific environments.
>   * *How to include*: Add **`Slack.tkape`**, **`Discord.tkape`**, or **`MicrosoftTeams.tkape`** to your target configuration.
> * **Full Web Browser Caches**:
>   * *Why it's missing*: Browser cache directories store downloaded images, javascript, and page files that can easily grow to several gigabytes of volatile files.
>   * *How to include*: Include **`BrowserCache.tkape`** if you need to recover deleted images, network assets, or web script files.
> * **Syncing User Cloud Files**:
>   * *Why it's missing*: Compounds collect the *metadata* databases (e.g. `OneDrive_Metadata.tkape`, `GoogleDrive_Metadata.tkape`) tracking file synchronizations, but do *not* download the actual files stored in the cloud.
>   * *How to include*: Run **`OneDrive_UserFiles.tkape`** or **`Dropbox_UserFiles.tkape`** to collect the actual synced directory content.

---

## 🛡️ **Forensic Playbooks by Case Scenario**

Use these suggested common target and module configurations to tailor your collections for specific investigations. For each playbook, we map out the exact parameters you need to provide to both the **Target Selections (`--target`)** and **Module Selections (`--module`)** phases.

### 💻 **Playbook A: Rapid Host Triage**

**Scenario**: Generic Compromise Audit — Perform a generic compromise audit on a workstation to establish a rapid timeline of active system events and process execution.

#### 1. Target Selections (`--target`)
| Role / Component | Target Link | Forensic Rationale & Operational Guidance |
| :--- | :--- | :--- |
| **Primary Base** | [KapeTriage](details/KapeTriage.md) | Standard workstation triage. Pulls `$MFT`, event logs, registry hives, evidence of execution, and web history. |
| **Manual Addition** | [Antivirus & EDR Suites](threat_hunting_targets.md) | Gathers active local antivirus engine threat history logs (e.g. [Windows Defender](details/WindowsDefender.md), [CrowdStrike Falcon](details/CrowdStrikeFalcon.md), or [ESET](details/ESET.md)) to identify previously blocked threats. |
| **Manual Addition** | [PowerShell Transcripts](details/PowerShellTranscripts.md) | Collects PowerShell transcript execution files to inspect custom command strings run by the attacker. |

#### 2. Module Selections (`--module`)
| Role / Component | Module Link | Forensic Rationale & Operational Guidance |
| :--- | :--- | :--- |
| **Primary Base** | [!EZParser](details/!EZParser.md) | Automatically processes Eric Zimmerman's entire suite of parsing tools (Amcache, Prefetch, JumpLists, Registry) to output structured CSV timelines. |
| **Manual Addition** | [WinDefendDetectionHist](details/WinDefendDetectionHist.md) | Parses raw Windows Defender detection history folders into readable CSV/text structures to map threat parameters. |
| **Manual Addition** | [PowerShell_ConvertPSHistoryTo-CSV](details/PowerShell_ConvertPSHistoryTo-CSV.md) | Automatically parses PowerShell console history commands to a structured table for rapid review. |

---

### ☣️ **Playbook B: Ransomware Hunting**

**Scenario**: Ransomware Staging & Malware Persistence — You suspect an active ransomware deployment, rootkit persistence, or modular malware staging on a system.

#### 1. Target Selections (`--target`)
| Role / Component | Target Link | Forensic Rationale & Operational Guidance |
| :--- | :--- | :--- |
| **Primary Base** | [KapeTriage](details/KapeTriage.md) | Obtains the core operating system structures, registry hives, execution histories, and event logs. |
| **Manual Addition** | [FileSystem](details/FileSystem.md) | Collects low-level NTFS system structures (`$MFT`, `$LogFile`, `$Boot`, `$UsnJrnl`) to trace rapid file renaming, modification, and encryption. |

#### 2. Module Selections (`--module`)
| Role / Component | Module Link | Forensic Rationale & Operational Guidance |
| :--- | :--- | :--- |
| **Primary Base** | [!EZParser](details/!EZParser.md) | Generates the primary analytical spreadsheets mapping process execution times. |
| **Specialized Scanner** | [Chainsaw](details/Chainsaw.md) or [Hayabusa](details/Hayabusa.md) | Runs lightning-fast Sigma rule matches against raw Windows Event Logs to locate lateral movement, process execution, and privilege escalation indicators. |
| **Live Acquisition** | [DumpIt Memory](details/DumpIt_Memory.md) | **Execute first on the live system** to dump physical RAM before KAPE accesses disk, preserving active network connections, volatile process spaces, and decryption keys. |
| **Manual Addition** | [RegRipper](details/RegRipper.md) & [Reghunter Core Suite](details/Reghunter.md) | Deeply parses system and user registry hives, running specialized checks to locate autoruns, malicious service keys, and shellcode loaders. |
| **Manual Addition** | [MFTECmd Parser](details/MFTECmd.md) | Processes raw `$MFT` records and `$UsnJrnl` logs to timeline bulk folder modifications and file creations typical of ransomware scripts. |

---

### 🕵️ **Playbook C: Insider Threat**

**Scenario**: Data Exfiltration & IP Theft — An employee is suspected of uploading proprietary corporate IP to personal cloud storage, downloading databases, or leaking secrets via chat channels prior to departure.

#### 1. Target Selections (`--target`)
| Role / Component | Target Link | Forensic Rationale & Operational Guidance |
| :--- | :--- | :--- |
| **Primary Base** | [KapeTriage](details/KapeTriage.md) | Provides the base operating system activity, recent file access, and USB connection history. |
| **Manual Addition** | [Slack Desktop](details/Slack.md) & [Microsoft Teams](details/MicrosoftTeams.md) | Captures direct chat databases (`LevelDB`/`SQLite`) to extract chat logs, channels, direct messages, and shared attachment listings. |
| **Manual Addition** | [OneDrive User Files](details/OneDrive_UserFiles.md) / [Dropbox User Files](details/Dropbox_UserFiles.md) | Collects actual synced local folders rather than just metadata catalogs, preserving copies of files synced to personal clouds. |
| **Manual Addition** | [Global Browser Caches](details/BrowserCache.md) | Collects cached web assets, exfiltrated files, and session logs to reconstruct upload workflows. |

#### 2. Module Selections (`--module`)
| Role / Component | Module Link | Forensic Rationale & Operational Guidance |
| :--- | :--- | :--- |
| **Primary Base** | [!EZParser](details/!EZParser.md) | Parses user-centric shell shortcuts, LNK files, and Registry hives to map file access habits. |
| **Specialized Parser** | [OneDrive Explorer](details/OneDriveExplorer.md) | Decrypts and parses OneDrive sync log databases to reconstruct folder listings, synchronization histories, deletion timestamps, and SHA-1 hashes. |
| **Specialized Parser** | [SrumECmd SRUM Parser](details/SrumECmd.md) | Extracts the System Resource Usage Monitor database to audit application network traffic usage over the past 30 days to trace bulk uploads and exfiltration. |
| **Specialized Parser** | [Universal Browser Parser](details/BrowserParser.md) | Consolidates Chrome, Edge, and Firefox history logs to trace web storage interactions, external emails, and download files. |
| **Manual Addition** | [Teams LevelDB Parser](details/TeamsParser.md) | Decrypts and indexes Teams communication logs to rebuild chat histories and channel threads. |
| **Manual Addition** | [TeraCopy Database Parser](details/SQLite3_TeraCopy_Main.md) | Parses local TeraCopy logs to identify files copied directly to external USB or network volumes. |

---

### 💾 **Playbook D: Low-Level Deletion**

**Scenario**: Anti-Forensics & File Deletion Recovery — The suspect is known to have run cleaning utilities (like CCleaner or BleachBit) or manually deleted evidence folders, and you need to perform deep MFT recovery.

#### 1. Target Selections (`--target`)
| Role / Component | Target Link | Forensic Rationale & Operational Guidance |
| :--- | :--- | :--- |
| **Primary Base** | [FileSystem](details/FileSystem.md) | Captures NTFS low-level system files (`$MFT`, `$LogFile`, `$Boot`, `$UsnJrnl`) crucial for auditing file system interactions and deleted directories. |
| **Manual Addition** | [Recycle Bin Metadata](details/RecycleBin.md) | Gathers deleted files metadata (`$I*`) and raw deleted contents (`$R*`) to trace manual trash movements. |
| **Manual Addition** | [USB Device Logs](details/USBDevicesLogs.md) | Gathers system setup logs, hardware registration, and device history to verify if an external cleaning tool drive was connected. |

#### 2. Module Selections (`--module`)
| Role / Component | Module Link | Forensic Rationale & Operational Guidance |
| :--- | :--- | :--- |
| **Primary Base** | [!EZParser](details/!EZParser.md) | Parses base registry settings and system shortcut link files. |
| **Specialized Parser** | [MFTECmd Parser](details/MFTECmd.md) | Performs a deep-dive parser of the `$MFT` record logs and USN change journaling to trace deleted file metadata and directory path structures. |
| **Specialized Parser** | [LECmd Link File Parser](details/LECmd.md) & [JLECmd Jump List Parser](details/JLECmd.md) | Validates shortcuts (`.lnk` files) and jump lists to see if they point to files or target directories that have since been deleted from the drive. |
| **Specialized Parser** | [RBCmd Recycle Bin Parser](details/RBCmd.md) | Reconstructs Recycle Bin transactions, correlating user SIDs with original deleted names, paths, and deletion times. |
| **Manual Addition** | [USBDetective](details/USBDetective.md) | Processes setupapi and USB registry settings to build complete timelines of when external clean-up tools or flash drives were mounted. |

---

## 📈 Summary Checklist for Investigators

When preparing your KAPE deployment:
1. [ ] **Select a Base Compound Target** corresponding to your speed constraints (`KapeTriage.tkape` or `!SANS_Triage.tkape`).
2. [ ] **Select corresponding Base Modules** (`!EZParser.mkape`) to establish your primary CSV spreadsheet timeline.
3. [ ] **Assess Volatility Needs**: Do you need a RAM dump? (If yes, acquire memory *first* before running target file collections by checking the memory dump modules).
4. [ ] **Append Case-Specific Targets**: Does the case involve cloud syncs, AV logs, or chat communications? Manually append the individual target selections.
5. [ ] **Append Corresponding Analytical Modules**: Ensure you match your target additions with their corresponding parsing modules (e.g. `TeamsParser` for Teams, `OneDriveExplorer` for OneDrive, `WinDefendDetectionHist` for Defender).
6. [ ] **Run Specialized Scanners** (`Chainsaw` or `Hayabusa` for Sigma rules, `bstrings` for URL matching) against the parsed triage output to isolate indicators of compromise (IOCs).
