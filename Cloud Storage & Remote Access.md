# **☁️ Cloud Storage & Remote Access**

{% hint style="info" %}

**Investigator Note:** Look here for evidence of data exfiltration (Dropbox, OneDrive) and unauthorized lateral movement via Remote Desktop Protocol (RDP) or third-party remote management tools (AnyDesk, TeamViewer).

{% endhint %}

{% tabs %}

{% tab title="🎯 Targets (.tkape)" %}

| File Name | Description | Author | Version |
| :---- | :---- | :---- | :---- |
| **AnyDesk.tkape** | AnyDesk | Andrew Rathbun / Scott Hanson | 1.5 |
| **TeamViewerLogs.tkape** | TeamViewer Logs | Hadar Yudovich / Sam Smoker | 2.0 |
| **RDPLogs.tkape** | RDP Logs | Drew Ervin | 1.0 |
| **RDPCache.tkape** | RDP Cache Files | Hadar Yudovich | 1.1 |
| **ScreenConnect.tkape** | ScreenConnect Data (ConnectWise Control) | Drew Ervin | 1.0 |
| **Splashtop.tkape** | Splashtop | Andrew Rathbun / Yogesh Khatri | 2.0 |
| **LogMeIn.tkape** | LogMeIn Data | Drew Ervin | 1.0 |
| **Ammyy.tkape** | Ammyy Data | Drew Ervin | 1.0 |
| **Dropbox\_UserFiles.tkape** | Dropbox Cloud Storage Files | Chad Tilbury | 1.0 |
| **Dropbox\_Metadata.tkape** | Dropbox Cloud Storage Metadata | Chad Tilbury / Andrew Rathbun | 1.5 |
| **OneDrive\_UserFiles.tkape** | Microsoft OneDrive Storage Files | Chad Tilbury | 1.0 |
| **OneDrive\_Metadata.tkape** | Microsoft OneDrive Storage Metadata | Chad Tilbury / Brian Maloney | 2.0 |
| **GoogleDrive\_Metadata.tkape** | Google Drive Metadata | Chad Tilbury | 1.1 |
| **Megasync.tkape** | MegaSync Data Collection | Vito Alfano | 1.0 |

{% endtab %}

{% tab title="⚙️ Modules (.mkape)" %}

| File Name | Description | Author | Version |
| :---- | :---- | :---- | :---- |
| **OneDriveExplorer.mkape** | Process OneDrive .dat and .previous.dat files | Brian Maloney | 1.3 |
| **BMC-Tools\_RDPBitmapCacheParser.mkape** | BMC-Tools: RDP Bitmap Cache parser | dingtoffee | 1.1 |
| **LogParser\_RDPUsageEvents.mkape** | LogParser RDP Usage events | Brian Maloney / Thomas DIOT | 1.1 |
| **MobaXterm\_Credentials\_key.mkape** | Extract MobaXterm encrypted credentials | Vito Alfano | 1.0 |
| **WinSCP\_Session.mkape** | Extract a copy of WinSCP encrypted credentials | Vito Alfano | 1.0 |

{% endtab %}

{% endtabs %}