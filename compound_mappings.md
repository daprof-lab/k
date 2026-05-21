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

Use these suggested common target and module configurations to tailor your collections for specific investigations.

{% tabs %}
{% tab title="💻 Playbook A: Rapid Host Triage" %}
### **Scenario**: Generic Compromise Audit
Perform a generic compromise audit on a workstation to establish a rapid timeline of active system events and process execution.

* **Primary Targets**: 
  * [KapeTriage](details/KapeTriage.md) (Pulls MFT, standard event logs, registry, execution evidence, web history).
* **Primary Modules**: 
  * [!EZParser](details/!EZParser.md) (Parses standard artifacts to clean timelines).
* **Critical Manual Additions**:
  * [Antivirus Suite](details/Antivirus.md) (Tailor to the specific endpoint AV deployed).
  * [PowerShell Transcripts](details/PowerShellTranscripts.md) (Crucial if attackers are living off the land via command-line PowerShell scripts).
{% endtab %}

{% tab title="☣️ Playbook B: Ransomware Hunting" %}
### **Scenario**: Ransomware Staging & Malware Persistence
You suspect an active ransomware deployment, rootkit persistence, or modular malware staging on a system.

* **Primary Targets**: 
  * [KapeTriage](details/KapeTriage.md) (Pulls core OS elements).
* **Primary Modules**:
  * [!EZParser](details/!EZParser.md) (Timeline generation).
  * [Chainsaw](details/Chainsaw.md) or [Hayabusa](details/Hayabusa.md) (Runs lightning-fast Sigma rule matches against raw event logs to locate lateral movement or process injection).
* **Critical Manual Additions**:
  * **Memory Acquisition**: Run [DumpIt Memory](details/DumpIt_Memory.md) immediately on the live system before target collection to preserve active connections, process maps, and volatile memory spaces.
  * **Registry Autostarts**: Include [RegRipper](details/RegRipper.md) and [Reghunter Core Suite](details/Reghunter.md) to extract deep registry keys holding persistence mechanisms.
{% endtab %}

{% tab title="🕵️ Playbook C: Insider Threat" %}
### **Scenario**: Data Exfiltration & IP Theft
An employee is suspected of uploading proprietary corporate IP to personal cloud storage, downloading databases, or leaking secrets via chat channels prior to departure.

* **Primary Targets**:
  * [KapeTriage](details/KapeTriage.md)
  * [Slack Desktop](details/Slack.md) & [Microsoft Teams](details/MicrosoftTeams.md) (Capture direct chat database histories).
  * [OneDrive User Files](details/OneDrive_UserFiles.md) / [Dropbox User Files](details/Dropbox_UserFiles.md) (Pull raw synced directories).
* **Primary Modules**:
  * [OneDrive Explorer](details/OneDriveExplorer.md) (Decrypt and parse OneDrive metadata logs to map synced directories, deletion timestamps, and SHA-1 hashes).
  * [SrumECmd](details/SrumECmd.md) (Identify byte-level data transmissions per application executable over a 30-day window to map exfiltration paths).
  * [Universal Browser Parser](details/BrowserParser.md) (Extract complete download records and web access timelines).
{% endtab %}

{% tab title="💾 Playbook D: Low-Level Deletion" %}
### **Scenario**: Anti-Forensics & File Deletion Recovery
The suspect is known to have run cleaning utilities (like CCleaner or BleachBit) or manually deleted evidence folders, and you need to perform deep MFT recovery.

* **Primary Targets**:
  * [FileSystem](details/FileSystem.md) (Focuses on MFT, USN Journal, and Transaction Logs).
  * [USB Device Logs](details/USBDevicesLogs.md) (Audit setup logs and hardware history).
* **Primary Modules**:
  * [MFTECmd Parser](details/MFTECmd.md) (Deep-dive parsing of `$MFT` record logs and USN change journaling to trace deleted file metadata).
  * [LECmd Link File Parser](details/LECmd.md) & [JLECmd Jump List Parser](details/JLECmd.md) (Verify if shortcut files or jump lists point to directories and filenames that no longer exist on disk).
  * [RBCmd Recycle Bin Parser](details/RBCmd.md) (Reconstruct `$I` metadata logs mapping GUI Recycle Bin deletions).
{% endtab %}
{% endtabs %}

---

## 📈 Summary Checklist for Investigators

When preparing your KAPE deployment:
1. [ ] **Select a Base Compound Target** corresponding to your speed constraints (`KapeTriage.tkape` or `!SANS_Triage.tkape`).
2. [ ] **Assess Volatility Needs**: Do you need a RAM dump? (If yes, acquire memory *first* before running target file collections).
3. [ ] **Assess High-Volume Needs**: Does the case involve exfiltration via cloud directories or chat channels? (If yes, manually append individual application targets).
4. [ ] **Execute Zimmerman's Compound Parser** (`!EZParser.mkape`) to establish your primary CSV spreadsheet timeline.
5. [ ] **Run Specialized Scanners** (`Chainsaw` or `Hayabusa` for Sigma rules, `bstrings` for URL matching) against the parsed triage output to isolate indicators of compromise (IOCs).
