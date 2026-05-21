# **🎯 Network & Web Browsers - Targets**

{% hint style="success" %}

**Target Collection Info:** These targets guide KAPE to collect raw operating system and application forensic files relating to network & web browsers. Click on any **Short Name** to view a dedicated detail page including forensics value and KAPE target definitions.

{% endhint %}

[⬅️ Back to Network & Web Browsers](network_browsers.md)

---

## **Available Targets (.tkape)**

| Short Name | Description | File Name | Author | Version |
| :--- | :--- | :--- | :--- | :--- |
| **[Google Chrome](details/Chrome.md)** | SQL databases for Chrome history, cookies, autofill data, bookmarks, and downloads. | **Chrome.tkape** | Eric Zimmerman / Andrew Rathbun | 1.4 |
| **[Microsoft Edge](details/EdgeChromium.md)** | Chromium-based Edge databases, downloads history, extensions state, and local web state. | **EdgeChromium.tkape** | Chad Tilbury / Andrew Rathbun | 1.4 |
| **[Mozilla Firefox](details/Firefox.md)** | Profile folders, history databases (places.sqlite), cookies, extensions, and bookmarks. | **Firefox.tkape** | Eric Zimmerman / Andrew Rathbun | 1.2 |
| **[Brave Browser](details/BraveBrowser.md)** | Session state, search histories, bookmarks, and core Brave client databases. | **BraveBrowser.tkape** | Cassie Doemel | 1.0 |
| **[Opera Browser](details/Opera.md)** | History records, user downloads, and active session configurations for Opera. | **Opera.tkape** | Andrew Rathbun | 1.0 |
| **[Vivaldi Browser](details/Vivaldi.md)** | Core Chromium-based Vivaldi history database, local state, and configuration tables. | **Vivaldi.tkape** | Sebastian Søgaard / Yogesh Khatri | 1.1 |
| **[Chrome Extensions](details/ChromeExtensions.md)** | Extracted Chromium browser extension packages, local databases, and synced configs. | **ChromeExtensions.tkape** | piesecurity / Reece394 | 1.1 |
| **[Global Browser Caches](details/BrowserCache.md)** | Unified browser cache tables and web assets directories for Chrome, Edge, and Firefox. | **BrowserCache.tkape** | Bjorn Vanhaeren / Reece394 | 1.2 |
| **[Windows IPConfig Details](details/Windows_IPConfig.md)** | Extracts current network adapter configurations, hardware MACs, and assigned IP ranges. | **Windows_IPConfig.mkape** | Mike Cary | 1.0 |
| **[Windows DNS Cache Logs](details/Windows_DNSCache.md)** | Collects active system DNS lookup records, mapping queried domains to resolving IPs. | **Windows_DNSCache.mkape** | Mike Cary | 1.0 |
| **[Windows ARP Cache Logs](details/Windows_ARPCache.md)** | Pulls local Address Resolution Protocol (ARP) tables linking local IPs to MAC addresses. | **Windows_ARPCache.mkape** | Mike Cary | 1.0 |
| **[Windows Routing Tables](details/Windows_RoutingTable.md)** | Gathers the local OS networking routing table, identifying active default gateways. | **Windows_RoutingTable.mkape** | Mike Cary | 1.0 |
| **[IIS Web Server Logs](details/IISLogFiles.md)** | HTTP request logs, client user-agents, IP addresses, and response status from IIS instances. | **IISLogFiles.tkape** | Troy Larson | 3.0 |
| **[Apache Web Server Logs](details/ApacheAccessLog.md)** | Apache access and error log tables documenting remote HTTP traffic. | **ApacheAccessLog.tkape** | Hadar Yudovich | 1.0 |
| **[OpenVPN Client Logs](details/OpenVPNClient.md)** | Remote tunnel configurations, connection handshakes, and OpenVPN client diagnostic logs. | **OpenVPNClient.tkape** | Mathias Frank | 1.0 |
| **[FileZilla Client Sessions](details/FileZillaClient.md)** | XML and SQLite configurations containing recent servers list, transfer logs, and credentials database. | **FileZillaClient.tkape** | Dennis Reneau | 1.0 |

---

[⬅️ Back to Network & Web Browsers](network_browsers.md)
