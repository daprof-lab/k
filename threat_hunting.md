# **🛡️ Threat Hunting, AV & Logs**

{% hint style="info" %}

**Investigator Note:** This section is vital for tracking malware execution and alerts. It contains Windows Event Logs collectors, Antivirus/EDR logs, and powerful IOC scanners like Thor, Loki, Hayabusa, and Chainsaw.

{% endhint %}

{% tabs %}

{% tab title="🎯 Targets (.tkape)" %}

| File Name | Description | Author | Version |
| :---- | :---- | :---- | :---- |
| **EventLogs.tkape** | Event logs | Eric Zimmerman | 1.0 |
| **WindowsDefender.tkape** | Windows Defender Data | Drew Ervin | 1.0 |
| **CrowdStrikeFalcon.tkape** | CrowdStrike Falcon | Cardinsou | 1.0 |
| **SentinelOne.tkape** | Sentinel One Logs | Kirtan Shah | 1.0 |
| **TrendMicro.tkape** | Trend Micro Data | Drew Ervin / Paul Cabon | 2.0 |
| **Bitdefender.tkape** | Bitdefender Antivirus Data | Drew Ervin / Ahmed Elshaer | 1.1 |
| **Malwarebytes.tkape** | Malwarebytes Data | Drew Ervin / Kirtan Shah | 1.1 |
| **Avast.tkape** | Avast Antivirus Data | Drew Ervin / Dhiral Panjwani | 1.1 |
| **ESET.tkape** | ESET Antivirus Data | Drew Ervin / Phill Moore | 1.3 |
| **Cylance.tkape** | Cylance Antivirus Logs | Ron Rader | 1.0 |
| **PowerShellTranscripts.tkape** | PowerShell Transcripts | Andrew Rathbun / Chad Tilbury | 1.2 |

{% endtab %}

{% tab title="⚙️ Modules (.mkape)" %}

| File Name | Description | Author | Version |
| :---- | :---- | :---- | :---- |
| **Thor\_Scan.mkape** | Thor, an IOC and YARA scanner written in Golang | Andrew Rathbun | 1.0 |
| **Loki\_Scan.mkape** | Loki \- Simple IOC and Incident Response Scanner | Georg Lauenstein / Andrew Rathbun | 1.0 |
| **Hayabusa.mkape** | Hayabusa a timeline generator for Windows event logs | Andrew Rathbun / Georg Lauenstein | 1.1 |
| **Chainsaw.mkape** | Chainsaw \- Rapidly Search and Hunt through Event Logs | Andrew Rathbun | 2.1 |
| **EvtxECmd.mkape** | EvtxECmd: process event log files | Eric Zimmerman | 1.0 |
| **Zircolite\_Scan.mkape** | SIGMA-based detection tool for EVTX | Pedro Sanchez Cordero | 1.0 |
| **DeepblueCLI.mkape** | SANS DeepBlueCLI against collected Windows Event Logs | Garrett Martin | 1.0 |
| **log4j-scanner.mkape** | Vulnerability scanner for Log4j2 CVE-2021-44228 | Georg Lauenstein | 1.0 |
| **CertUtil\_Parser.mkape** | Parse Certutil activity | DReneau / Paul CABON | 2.0 |

{% endtab %}

{% endtabs %}