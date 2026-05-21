# **🎯 Threat Hunting, AV & Logs - Targets**

{% hint style="success" %}

**Target Collection Info:** These targets guide KAPE to collect raw operating system and application forensic files relating to threat hunting, av & logs. Click on any **Short Name** to view a dedicated detail page including forensics value and KAPE target definitions.

{% endhint %}

[⬅️ Back to Threat Hunting, AV & Logs](threat_hunting.md)

---

## **Available Targets (.tkape)**

| Short Name | Description | File Name | Author | Version |
| :--- | :--- | :--- | :--- | :--- |
| [**Windows Event Logs**](details/EventLogs.md) | System-wide EVTX log files containing core security audits, application logs, and system events. | **EventLogs.tkape** | Eric Zimmerman | 1.0 |
| [**Windows Defender**](details/WindowsDefender.md) | Detection logs, scan configurations, quarantined assets metadata, and logs from Microsoft AV. | **WindowsDefender.tkape** | Drew Ervin | 1.0 |
| [**CrowdStrike Falcon**](details/CrowdStrikeFalcon.md) | Telemetry diagnostic configurations, local cache updates, and installation status from the Falcon agent. | **CrowdStrikeFalcon.tkape** | Cardinsou | 1.0 |
| [**SentinelOne Logs**](details/SentinelOne.md) | Operational log databases, network diagnostics, and agent states for SentinelOne EDR. | **SentinelOne.tkape** | Kirtan Shah | 1.0 |
| [**Trend Micro Security**](details/TrendMicro.md) | Logs documenting detected security alerts, file blocks, and quarantine activities. | **TrendMicro.tkape** | Drew Ervin / Paul Cabon | 2.0 |
| [**Bitdefender Antivirus**](details/Bitdefender.md) | Antivirus detection logs, file scanning logs, and quarantine configurations. | **Bitdefender.tkape** | Drew Ervin / Ahmed Elshaer | 1.1 |
| [**Malwarebytes Agent**](details/Malwarebytes.md) | Scanning logs, threat hits, active exclusions, and quarantine databases for Malwarebytes. | **Malwarebytes.tkape** | Drew Ervin / Kirtan Shah | 1.1 |
| [**Avast Antivirus**](details/Avast.md) | Collects threat databases, active scan logs, and quarantine records from Avast systems. | **Avast.tkape** | Drew Ervin / Dhiral Panjwani | 1.1 |
| [**ESET Antivirus**](details/ESET.md) | Event logs, scanned threat metadata, and protection modules status for ESET. | **ESET.tkape** | Drew Ervin / Phill Moore | 1.3 |
| [**Cylance Antivirus**](details/Cylance.md) | Local threat telemetry logs, configuration profiles, and scan logs from Cylance Protect. | **Cylance.tkape** | Ron Rader | 1.0 |
| [**PowerShell Transcripts**](details/PowerShellTranscripts.md) | Complete console recording logs capture raw commands, arguments, outputs, and script blocks. | **PowerShellTranscripts.tkape** | Andrew Rathbun / Chad Tilbury | 1.2 |

---

[⬅️ Back to Threat Hunting, AV & Logs](threat_hunting.md)
