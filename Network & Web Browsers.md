# **🌐 Network & Web Browsers**

{% hint style="info" %}

**Investigator Note:** Targets and Modules related to browser history, downloads, extensions, as well as core OS networking artifacts (ARP cache, DNS cache, routing tables, and IIS/Apache logs).

{% endhint %}

{% tabs %}

{% tab title="🎯 Targets (.tkape)" %}

| File Name | Description | Author | Version |
| :---- | :---- | :---- | :---- |
| **Chrome.tkape** | Chrome | Eric Zimmerman / Andrew Rathbun | 1.4 |
| **EdgeChromium.tkape** | Microsoft Edge Chromium Artifacts | Chad Tilbury / Andrew Rathbun | 1.4 |
| **Firefox.tkape** | Firefox | Eric Zimmerman / Andrew Rathbun | 1.2 |
| **BraveBrowser.tkape** | Brave Browser | Cassie Doemel | 1.0 |
| **Opera.tkape** | Opera | Andrew Rathbun | 1.0 |
| **Vivaldi.tkape** | Vivaldi Artifacts | Sebastian Søgaard / Yogesh Khatri | 1.1 |
| **ChromeExtensions.tkape** | Chrome Extension Files | piesecurity / Reece394 | 1.1 |
| **BrowserCache.tkape** | Browser Caches | Bjorn Vanhaeren / Reece394 | 1.2 |
| **Windows\_IPConfig.mkape** | IPConfig | Mike Cary | 1.0 |
| **Windows\_DNSCache.mkape** | DNSCache | Mike Cary | 1.0 |
| **Windows\_ARPCache.mkape** | ARPCache | Mike Cary | 1.0 |
| **Windows\_RoutingTable.mkape** | RoutingTable | Mike Cary | 1.0 |
| **IISLogFiles.tkape** | IIS Log Files | Troy Larson | 3.0 |
| **ApacheAccessLog.tkape** | Apache Access Log | Hadar Yudovich | 1.0 |
| **OpenVPNClient.tkape** | OpenVPN Client Config and Log | Mathias Frank | 1.0 |
| **FileZillaClient.tkape** | FileZilla XML and SQLite Log Files | Dennis Reneau | 1.0 |

{% endtab %}

{% tab title="⚙️ Modules (.mkape)" %}

| File Name | Description | Author | Version |
| :---- | :---- | :---- | :---- |
| **BrowserParser.mkape** | Parse most artifacts in a browser to CSV or JSON | Sebastian Søgaard | 1.0 |
| **NirSoft\_WebBrowserPassView.mkape** | WebBrowserPassView \- Nirsoft | Pedro Sanchez Cordero | 1.1 |
| **NirSoft\_BrowsingHistoryView.mkape** | Browsing History View \- Nirsoft | Mike Cary | 1.1 |
| **iisGeoLocate.mkape** | Geolocate IP addresses found in IIS logs | Andrew Rathbun | 1.0 |
| **LogParser\_ApacheAccessLogs.mkape** | LogParser Apache Access Log | Hadar Yudovich | 1.0 |
| **PowerShell\_DnsClientCache.mkape** | Displaying DNS Client Cache | Max Zabuty | 1.0 |
| **bstrings\_URLs.mkape** | Use bstrings to GREP for URLs | Chris Kudless / Georg Lauenstein | 1.1 |
| **bstrings\_IPv4.mkape** | Use bstrings to GREP for IPv4 addresses | Chris Kudless / Georg Lauenstein | 1.2 |

{% endtab %}

{% endtabs %}