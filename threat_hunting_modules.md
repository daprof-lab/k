# **⚙️ Threat Hunting, AV & Logs - Modules**

{% hint style="success" %}

**Module Execution Info:** These modules process data collected under the Threat Hunting, AV & Logs category using specialized analytical tools. Click on any **Short Name** to view a dedicated detail page including use-cases and KAPE module definitions.

{% endhint %}

[⬅️ Back to Threat Hunting, AV & Logs](threat_hunting.md)

---

## **Available Modules (.mkape)**

| Short Name | Description | File Name | Author | Version |
| :--- | :--- | :--- | :--- | :--- |
| **[⚙️ CertUtil Activity Parser](details/CertUtil_Parser.md)** | Extracts execution histories, remote download URLs, and command sequences logged by Certutil. | **CertUtil_Parser.mkape** | DReneau, Paul CABON - CERT Cwatch - Almond | 2.0 |
| **[⚙️ Chainsaw Event Scanner](details/Chainsaw.md)** | High-speed Rust-based EVTX engine to search log folders using Sigma rules and custom queries. | **Chainsaw.mkape** | Andrew Rathbun | 2.1 |
| **[⚙️ EvtxECmd Event Parser](details/EvtxECmd.md)** | Extracts and parses EVTX logs into highly detailed structured CSV/JSON forensic timelines. | **EvtxECmd.mkape** | Eric Zimmerman | 1.0 |
| **[⚙️ Hayabusa Event Parser](details/Hayabusa.md)** | Fast Event Log (EVTX) timeline generator applying Sigma detection rules to locate lateral movement. | **Hayabusa.mkape** | Andrew Rathbun, Georg Lauenstein (sure[secure]) | 1.1 |
| **[⚙️ Kape Research Event Logs XML](details/KapeResearch_EventLogs_XML.md)** | EvtxECmd: Convert Windows Event Log files (.evtx) to XML for research | **KapeResearch_EventLogs_XML.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Kape Research Registry Amcache JSON](details/KapeResearch_Registry_Amcache_JSON.md)** | RECmd: Convert Amcache.hve Registry hive to JSON for research | **KapeResearch_Registry_Amcache_JSON.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Kape Research Registry BBI JSON](details/KapeResearch_Registry_BBI_JSON.md)** | RECmd: Convert BBI Registry hive to JSON for research | **KapeResearch_Registry_BBI_JSON.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Kape Research Registry BCD Template JSON](details/KapeResearch_Registry_BCD-Template_JSON.md)** | RECmd: Convert BCD-Template Registry hive to JSON for research | **KapeResearch_Registry_BCD-Template_JSON.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Kape Research Registry COMPONENTS JSON](details/KapeResearch_Registry_COMPONENTS_JSON.md)** | RECmd: Convert COMPONENTS Registry hive to JSON for research | **KapeResearch_Registry_COMPONENTS_JSON.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Kape Research Registry DEFAULT JSON](details/KapeResearch_Registry_DEFAULT_JSON.md)** | RECmd: Convert DEFAULT Registry hive to JSON for research | **KapeResearch_Registry_DEFAULT_JSON.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Kape Research Registry DRIVERS JSON](details/KapeResearch_Registry_DRIVERS_JSON.md)** | RECmd: Convert DRIVERS Registry hive to JSON for research | **KapeResearch_Registry_DRIVERS_JSON.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Kape Research Registry ELAM JSON](details/KapeResearch_Registry_ELAM_JSON.md)** | RECmd: Convert ELAM Registry hive to JSON for research | **KapeResearch_Registry_ELAM_JSON.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Kape Research Registry NTUSER JSON](details/KapeResearch_Registry_NTUSER_JSON.md)** | RECmd: Convert NTUSER.dat Registry hive to JSON for research | **KapeResearch_Registry_NTUSER_JSON.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Kape Research Registry SAM JSON](details/KapeResearch_Registry_SAM_JSON.md)** | RECmd: Convert SAM Registry hive to JSON for research | **KapeResearch_Registry_SAM_JSON.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Kape Research Registry SECURITY JSON](details/KapeResearch_Registry_SECURITY_JSON.md)** | RECmd: Convert SECURITY Registry hive to JSON for research | **KapeResearch_Registry_SECURITY_JSON.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Kape Research Registry SOFTWARE JSON](details/KapeResearch_Registry_SOFTWARE_JSON.md)** | RECmd: Convert SOFTWARE Registry hive to JSON for research | **KapeResearch_Registry_SOFTWARE_JSON.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Kape Research Registry Sys Cache JSON](details/KapeResearch_Registry_SysCache_JSON.md)** | RECmd: Convert SysCache Registry hive to JSON for research | **KapeResearch_Registry_SysCache_JSON.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Kape Research Registry SYSTEM JSON](details/KapeResearch_Registry_SYSTEM_JSON.md)** | RECmd: Convert SYSTEM Registry hive to JSON for research | **KapeResearch_Registry_SYSTEM_JSON.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Kape Research Registry Userdiff JSON](details/KapeResearch_Registry_userdiff_JSON.md)** | RECmd: Convert userdiff Registry hive to JSON for research | **KapeResearch_Registry_userdiff_JSON.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Kape Research Registry Usr Class JSON](details/KapeResearch_Registry_UsrClass_JSON.md)** | RECmd: Convert UsrClass.dat Registry hive to JSON for research | **KapeResearch_Registry_UsrClass_JSON.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Kape Research Registry VSMIDK JSON](details/KapeResearch_Registry_VSMIDK_JSON.md)** | RECmd: Convert VSMIDK Registry hive to JSON for research | **KapeResearch_Registry_VSMIDK_JSON.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Log4j Vulnerability Scanner](details/log4j-scanner.md)** | Checks local storage for vulnerable Log4j libraries, helping secure internal systems. | **log4j-scanner.mkape** | Georg Lauenstein | 1.0 |
| **[⚙️ Loki IOC Scanner](details/Loki_Scan.md)** | Light and fast Incident Response scanner mapping systems against public YARA and MD5 signatures. | **Loki_Scan.mkape** | Georg Lauenstein and Andrew Rathbun | 1.0 |
| **[⚙️ SANS DeepBlueCLI](details/DeepblueCLI.md)** | Evaluates Windows Security and System logs to identify credential dumping and user creations. | **DeepblueCLI.mkape** | Garrett Martin | 1.0 |
| **[⚙️ Thor IOC Scanner](details/Thor_Scan.md)** | Performs high-performance scanning across folders using advanced YARA signatures and threat indices. | **Thor_Scan.mkape** | Andrew Rathbun | 1.0 |
| **[⚙️ Zircolite Sigma Scanner](details/Zircolite_Scan.md)** | Applies standard Sigma rules directly against EVTX directories using SQLite query engines. | **Zircolite_Scan.mkape** | Pedro Sanchez Cordero | 1.0 |

---

[⬅️ Back to Threat Hunting, AV & Logs](threat_hunting.md)
