# **🎯 Threat Hunting, AV & Logs - Targets**

{% hint style="success" %}

**Target Collection Info:** These targets guide KAPE to collect raw operating system and application forensic files relating to threat hunting, av & logs. Click on any **Short Name** to view a dedicated detail page including forensics value and KAPE target definitions.

{% endhint %}

[⬅️ Back to Threat Hunting, AV & Logs](threat_hunting.md)

---

## **Available Targets (.tkape)**

| Short Name | Description | File Name | Author | Version |
| :--- | :--- | :--- | :--- | :--- |
| **[🎯 Avast Antivirus](details/Avast.md)** | Collects threat databases, active scan logs, and quarantine records from Avast systems. | **Avast.tkape** | Drew Ervin and Dhiral Panjwani | 1.1 |
| **[🎯 AVG](details/AVG.md)** | AVG Antivirus Data | **AVG.tkape** | Kirtan Shah and Dhiral Panjwani | 1.1 |
| **[🎯 Avira Avlogs](details/AviraAVLogs.md)** | Avira Logs | **AviraAVLogs.tkape** | Fabian Murer and Dhiral Panjwani | 1.1 |
| **[🎯 Bitdefender Antivirus](details/Bitdefender.md)** | Antivirus detection logs, file scanning logs, and quarantine configurations. | **Bitdefender.tkape** | Drew Ervin, Ahmed Elshaer | 1.1 |
| **[🎯 Combofix](details/Combofix.md)** | ComboFix Antivirus Data | **Combofix.tkape** | Drew Ervin | 1.0 |
| **[🎯 CrowdStrike Falcon](details/CrowdStrikeFalcon.md)** | Telemetry diagnostic configurations, local cache updates, and installation status from the Falcon agent. | **CrowdStrikeFalcon.tkape** | Cardinsou | 1.0 |
| **[🎯 Cybereason](details/Cybereason.md)** | Cybereason Sensor/Detection Logs | **Cybereason.tkape** | piesecurity | 1.0 |
| **[🎯 Cylance Antivirus](details/Cylance.md)** | Local threat telemetry logs, configuration profiles, and scan logs from Cylance Protect. | **Cylance.tkape** | Ron Rader | 1.0 |
| **[🎯 Elastic Defend](details/ElasticDefend.md)** | Elastic Defend Data | **ElasticDefend.tkape** | AlliedPterodactyl | 1.0 |
| **[🎯 Emsisoft](details/Emsisoft.md)** | Emsisoft Antivirus Logs | **Emsisoft.tkape** | blueskycyber | 1.0 |
| **[🎯 ESET Antivirus](details/ESET.md)** | Event logs, scanned threat metadata, and protection modules status for ESET. | **ESET.tkape** | Drew Ervin, Phill Moore | 1.3 |
| **[🎯 Fsecure](details/FSecure.md)** | F-Secure Antivirus Data | **FSecure.tkape** | Drew Ervin | 1.0 |
| **[🎯 Hitman Pro](details/HitmanPro.md)** | HitmanPro Antivirus Data | **HitmanPro.tkape** | Drew Ervin | 1.0 |
| **[🎯 Malwarebytes Agent](details/Malwarebytes.md)** | Scanning logs, threat hits, active exclusions, and quarantine databases for Malwarebytes. | **Malwarebytes.tkape** | Drew Ervin & Kirtan Shah | 1.1 |
| **[🎯 Manage Engine Logs](details/ManageEngineLogs.md)** | ManageEngine Log Files | **ManageEngineLogs.tkape** | Whitney Champion, Phill Moore | 1.1 |
| **[🎯 Mc Afee](details/McAfee.md)** | McAfee Log Files | **McAfee.tkape** | Sam Smoker | 1.1 |
| **[🎯 Mc Afee E PO](details/McAfee_ePO.md)** | McAfee ePO Log Files | **McAfee_ePO.tkape** | Doug Metz | 1.0 |
| **[🎯 Microsoft Safety Scanner](details/MicrosoftSafetyScanner.md)** | Microsoft Safety Scanner | **MicrosoftSafetyScanner.tkape** | Geir Olav Skei | 1.0 |
| **[🎯 Mongo Dblogs](details/MongoDBLogs.md)** | MongoDB Log Files (Windows) | **MongoDBLogs.tkape** | Eric Capuano | 1.0 |
| **[🎯 Mssqlerror Log](details/MSSQLErrorLog.md)** | MS SQL ErrorLogs | **MSSQLErrorLog.tkape** | Troy Larson | 1.0 |
| **[🎯 Nginxlogs](details/NGINXLogs.md)** | NGINX Log Files | **NGINXLogs.tkape** | Eric Capuano | 1.0 |
| **[🎯 Power Shell Console](details/PowerShellConsole.md)** | PowerShell Console Log File | **PowerShellConsole.tkape** | Mike Cary, 2thewes, Vikas Singh | 1.2 |
| **[🎯 PowerShell Transcripts](details/PowerShellTranscripts.md)** | Complete console recording logs capture raw commands, arguments, outputs, and script blocks. | **PowerShellTranscripts.tkape** | Andrew Rathbun and Chad Tilbury | 1.2 |
| **[🎯 Rogue Killer](details/RogueKiller.md)** | RogueKiller Anti-Malware (by Adlice Software) | **RogueKiller.tkape** | Drew Ervin | 1.0 |
| **[🎯 Secure Age](details/SecureAge.md)** | SecureAge Antivirus Logs | **SecureAge.tkape** | Andrew Rathbun | 1.0 |
| **[🎯 SentinelOne Logs](details/SentinelOne.md)** | Operational log databases, network diagnostics, and agent states for SentinelOne EDR. | **SentinelOne.tkape** | Kirtan Shah | 1.0 |
| **[🎯 Sophos](details/Sophos.md)** | Sophos Data | **Sophos.tkape** | Drew Ervin, Reece394 | 1.1 |
| **[🎯 Superanti Spyware](details/SUPERAntiSpyware.md)** | SUPERAntiSpyware Data | **SUPERAntiSpyware.tkape** | Drew Ervin | 1.0 |
| **[🎯 Symantec AV Logs](details/Symantec_AV_Logs.md)** | Symantec AV Logs | **Symantec_AV_Logs.tkape** | Brian Maloney | 1.3 |
| **[🎯 Total AV](details/TotalAV.md)** | TotalAV Antivirus Data | **TotalAV.tkape** | Kirtan Shah | 1.0 |
| **[🎯 Trend Micro Security](details/TrendMicro.md)** | Logs documenting detected security alerts, file blocks, and quarantine activities. | **TrendMicro.tkape** | Drew Ervin, Paul Cabon CERT Almond | 2.0 |
| **[🎯 VIPRE](details/VIPRE.md)** | VIPRE Data | **VIPRE.tkape** | Drew Ervin | 1.0 |
| **[🎯 Webroot](details/Webroot.md)** | Webroot Antivirus | **Webroot.tkape** | Drew Ervin | 1.0 |
| **[🎯 Win Defend Detection Hist](details/WinDefendDetectionHist.md)** | Windows Defender Threat DetectionHistory files | **WinDefendDetectionHist.tkape** | Jordan Klepser | 1.1 |
| **[🎯 Windows Defender](details/WindowsDefender.md)** | Detection logs, scan configurations, quarantined assets metadata, and logs from Microsoft AV. | **WindowsDefender.tkape** | Drew Ervin | 1.0 |
| **[🎯 Windows Event Logs](details/EventLogs.md)** | System-wide EVTX log files containing core security audits, application logs, and system events. | **EventLogs.tkape** | Eric Zimmerman | 1.0 |

---

[⬅️ Back to Threat Hunting, AV & Logs](threat_hunting.md)
