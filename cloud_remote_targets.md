# **🎯 Cloud Storage & Remote Access - Targets**

{% hint style="success" %}

**Target Collection Info:** These targets guide KAPE to collect raw operating system and application forensic files relating to cloud storage & remote access. Click on any **Short Name** to view a dedicated detail page including forensics value and KAPE target definitions.

{% endhint %}

[⬅️ Back to Cloud Storage & Remote Access](cloud_remote.md)

---

## **Available Targets (.tkape)**

| Short Name | Description | File Name | Author | Version |
| :--- | :--- | :--- | :--- | :--- |
| **[🎯 Ammyy Admin](details/Ammyy.md)** | Configuration parameters, server records, and connection diaries from Ammyy Admin. | **Ammyy.tkape** | Drew Ervin | 1.0 |
| **[🎯 AnyDesk Remote](details/AnyDesk.md)** | AnyDesk logs, configuration settings, user session profiles, and speed test databases. | **AnyDesk.tkape** | Andrew Rathbun / Scott Hanson | 1.5 |
| **[🎯 Dropbox Sync Metadata](details/Dropbox_Metadata.md)** | SQL databases detailing Dropbox file synchronization timelines, file ids, and hashes. | **Dropbox_Metadata.tkape** | Chad Tilbury / Andrew Rathbun | 1.5 |
| **[🎯 Dropbox User Files](details/Dropbox_UserFiles.md)** | Local Dropbox synchronization directories and cached operational databases. | **Dropbox_UserFiles.tkape** | Chad Tilbury | 1.0 |
| **[🎯 Google Drive Metadata](details/GoogleDrive_Metadata.md)** | Sync databases (cloud_graph.db) tracking local folder configurations and Google Drive storage sync timelines. | **GoogleDrive_Metadata.tkape** | Chad Tilbury | 1.1 |
| **[🎯 LogMeIn Client](details/LogMeIn.md)** | Session configurations, activity logs, and system settings for LogMeIn remote access. | **LogMeIn.tkape** | Drew Ervin | 1.0 |
| **[🎯 MegaSync Client](details/Megasync.md)** | MegaSync synchronization metadata, active downloads list, and connected user accounts. | **Megasync.tkape** | Vito Alfano | 1.0 |
| **[🎯 OneDrive Sync Metadata](details/OneDrive_Metadata.md)** | System databases (e.g., .dat, .previous.dat) documenting file states and shared OneDrive folders. | **OneDrive_Metadata.tkape** | Chad Tilbury / Brian Maloney | 2.0 |
| **[🎯 OneDrive User Files](details/OneDrive_UserFiles.md)** | Local folder trees and offline files synchronized via Microsoft OneDrive. | **OneDrive_UserFiles.tkape** | Chad Tilbury | 1.0 |
| **[🎯 RDP Bitmap Cache](details/RDPCache.md)** | Cached display tiles from Remote Desktop sessions. Reconstructs screens viewed by remote attackers. | **RDPCache.tkape** | Hadar Yudovich | 1.1 |
| **[🎯 RDP Event Logs](details/RDPLogs.md)** | Windows Event Logs mapping Terminal Services connections, logins, and session timeouts. | **RDPLogs.tkape** | Drew Ervin | 1.0 |
| **[🎯 ScreenConnect Client](details/ScreenConnect.md)** | Logs, server configs, and diagnostic metrics from ConnectWise/ScreenConnect agents. | **ScreenConnect.tkape** | Drew Ervin | 1.0 |
| **[🎯 Splashtop Remote](details/Splashtop.md)** | Splashtop local log structures, active sessions, and client credentials databases. | **Splashtop.tkape** | Andrew Rathbun / Yogesh Khatri | 2.0 |
| **[🎯 TeamViewer Logs](details/TeamViewerLogs.md)** | Connection history logs, remote ID configurations, and session diagnostic tables for TeamViewer. | **TeamViewerLogs.tkape** | Hadar Yudovich / Sam Smoker | 2.0 |

---

[⬅️ Back to Cloud Storage & Remote Access](cloud_remote.md)
