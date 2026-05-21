# **⚙️ Threat Hunting, AV & Logs - Modules**

{% hint style="success" %}

**Module Execution Info:** These modules process data collected under the Threat Hunting, AV & Logs category using specialized analytical tools. Click on any **Short Name** to view a dedicated detail page including use-cases and KAPE module definitions.

{% endhint %}

[⬅️ Back to Threat Hunting, AV & Logs](threat_hunting.md)

---

## **Available Modules (.mkape)**

| Short Name | Description | File Name | Author | Version |
| :--- | :--- | :--- | :--- | :--- |
| **[Thor IOC Scanner](details/Thor_Scan.md)** | Performs high-performance scanning across folders using advanced YARA signatures and threat indices. | **Thor_Scan.mkape** | Andrew Rathbun | 1.0 |
| **[Loki IOC Scanner](details/Loki_Scan.md)** | Light and fast Incident Response scanner mapping systems against public YARA and MD5 signatures. | **Loki_Scan.mkape** | Georg Lauenstein / Andrew Rathbun | 1.0 |
| **[Hayabusa Event Parser](details/Hayabusa.md)** | Fast Event Log (EVTX) timeline generator applying Sigma detection rules to locate lateral movement. | **Hayabusa.mkape** | Andrew Rathbun / Georg Lauenstein | 1.1 |
| **[Chainsaw Event Scanner](details/Chainsaw.md)** | High-speed Rust-based EVTX engine to search log folders using Sigma rules and custom queries. | **Chainsaw.mkape** | Andrew Rathbun | 2.1 |
| **[EvtxECmd Event Parser](details/EvtxECmd.md)** | Extracts and parses EVTX logs into highly detailed structured CSV/JSON forensic timelines. | **EvtxECmd.mkape** | Eric Zimmerman | 1.0 |
| **[Zircolite Sigma Scanner](details/Zircolite_Scan.md)** | Applies standard Sigma rules directly against EVTX directories using SQLite query engines. | **Zircolite_Scan.mkape** | Pedro Sanchez Cordero | 1.0 |
| **[SANS DeepBlueCLI](details/DeepblueCLI.md)** | Evaluates Windows Security and System logs to identify credential dumping and user creations. | **DeepblueCLI.mkape** | Garrett Martin | 1.0 |
| **[Log4j Vulnerability Scanner](details/log4j-scanner.md)** | Checks local storage for vulnerable Log4j libraries, helping secure internal systems. | **log4j-scanner.mkape** | Georg Lauenstein | 1.0 |
| **[CertUtil Activity Parser](details/CertUtil_Parser.md)** | Extracts execution histories, remote download URLs, and command sequences logged by Certutil. | **CertUtil_Parser.mkape** | DReneau / Paul CABON | 2.0 |

---

[⬅️ Back to Threat Hunting, AV & Logs](threat_hunting.md)
