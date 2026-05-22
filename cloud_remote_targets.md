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
| **[🎯 AnyDesk Remote](details/AnyDesk.md)** | AnyDesk logs, configuration settings, user session profiles, and speed test databases. | **AnyDesk.tkape** | Andrew Rathbun, Scott Hanson, and Nicole Jao | 1.5 |
| **[🎯 Box Drive Metadata](details/BoxDrive_Metadata.md)** | Box Cloud Storage Metadata | **BoxDrive_Metadata.tkape** | Chad Tilbury | 1.1 |
| **[🎯 Box Drive User Files](details/BoxDrive_UserFiles.md)** | Box Cloud Storage Files | **BoxDrive_UserFiles.tkape** | Chad Tilbury | 1.0 |
| **[🎯 Dropbox Sync Metadata](details/Dropbox_Metadata.md)** | SQL databases detailing Dropbox file synchronization timelines, file ids, and hashes. | **Dropbox_Metadata.tkape** | Chad Tilbury and Andrew Rathbun | 1.5 |
| **[🎯 Dropbox User Files](details/Dropbox_UserFiles.md)** | Local Dropbox synchronization directories and cached operational databases. | **Dropbox_UserFiles.tkape** | Chad Tilbury | 1.0 |
| **[🎯 Event Logs RDP](details/EventLogs-RDP.md)** | Collect Win7+ RDP related Event logs | **EventLogs-RDP.tkape** | Mark Hallman, esecrpm | 1.1 |
| **[🎯 Event Logs RDP Eae7bdd6 93f1 4e06 Ae0f 2c64c9f1c7c6](details/EventLogs-RDP_eae7bdd6-93f1-4e06-ae0f-2c64c9f1c7c6.md)** | Collect Win7+ RDP related Event logs | **EventLogs-RDP_eae7bdd6-93f1-4e06-ae0f-2c64c9f1c7c6.tkape** | Mark Hallman | 1.0 |
| **[🎯 Google Drive Backup Sync User Files](details/GoogleDriveBackupSync_UserFiles.md)** | Google Backup and Sync Storage Files | **GoogleDriveBackupSync_UserFiles.tkape** | Chad Tilbury | 1.0 |
| **[🎯 Google Drive Metadata](details/GoogleDrive_Metadata.md)** | Sync databases (cloud_graph.db) tracking local folder configurations and Google Drive storage sync timelines. | **GoogleDrive_Metadata.tkape** | Chad Tilbury | 1.1 |
| **[🎯 LogMeIn Client](details/LogMeIn.md)** | Session configurations, activity logs, and system settings for LogMeIn remote access. | **LogMeIn.tkape** | Drew Ervin | 1.0 |
| **[🎯 M Remote NG](details/mRemoteNG.md)** | mRemoteNG | **mRemoteNG.tkape** | Markus Einarsson (@einarssonm) | 1.0 |
| **[🎯 MegaSync Client](details/Megasync.md)** | MegaSync synchronization metadata, active downloads list, and connected user accounts. | **Megasync.tkape** | Vito Alfano | 1.0 |
| **[🎯 Moba Xterm](details/MobaXTerm.md)** | MobaXTerm | **MobaXTerm.tkape** | Andrew Rathbun | 1.0 |
| **[🎯 OneDrive Sync Metadata](details/OneDrive_Metadata.md)** | System databases (e.g., .dat, .previous.dat) documenting file states and shared OneDrive folders. | **OneDrive_Metadata.tkape** | Chad Tilbury, Brian Maloney | 2.0 |
| **[🎯 OneDrive User Files](details/OneDrive_UserFiles.md)** | Local folder trees and offline files synchronized via Microsoft OneDrive. | **OneDrive_UserFiles.tkape** | Chad Tilbury | 1.0 |
| **[🎯 RDP Bitmap Cache](details/RDPCache.md)** | Cached display tiles from Remote Desktop sessions. Reconstructs screens viewed by remote attackers. | **RDPCache.tkape** | Hadar Yudovich | 1.1 |
| **[🎯 RDP Event Logs](details/RDPLogs.md)** | Windows Event Logs mapping Terminal Services connections, logins, and session timeouts. | **RDPLogs.tkape** | Drew Ervin | 1.0 |
| **[🎯 Rdpjumplist](details/RDPJumplist.md)** | RDP Jumplist Files | **RDPJumplist.tkape** | Vito Alfano | 1.0 |
| **[🎯 Remote Desktop Manager](details/RemoteDesktopManager.md)** | A Target to collect files that are related to Remote Desktop Manager from Devolutions | **RemoteDesktopManager.tkape** | ogmini | 1.0 |
| **[🎯 Remote Manipulator System](details/RemoteManipulatorSystem.md)** | Remote Manipulator System (RMS) | **RemoteManipulatorSystem.tkape** | raggadhub based on RemoteUtilities_App.tkape by Ryan McVicar | 1.0 |
| **[🎯 Remote Utilities App](details/RemoteUtilities_app.md)** | Remote Utilities | **RemoteUtilities_app.tkape** | Ryan McVicar | 1.1 |
| **[🎯 ScreenConnect Client](details/ScreenConnect.md)** | Logs, server configs, and diagnostic metrics from ConnectWise/ScreenConnect agents. | **ScreenConnect.tkape** | Drew Ervin | 1.0 |
| **[🎯 Splashtop Remote](details/Splashtop.md)** | Splashtop local log structures, active sessions, and client credentials databases. | **Splashtop.tkape** | Andrew Rathbun, Yogesh Khatri, Evangelos Dragonas | 2.0 |
| **[🎯 Supremo Remote Desktop](details/SupremoRemoteDesktop.md)** | Supremo Remote Desktop Control Logs | **SupremoRemoteDesktop.tkape** | epoxigen | 1.1 |
| **[🎯 TeamViewer Logs](details/TeamViewerLogs.md)** | Connection history logs, remote ID configurations, and session diagnostic tables for TeamViewer. | **TeamViewerLogs.tkape** | Hadar Yudovich, Sam Smoker | 2.0 |
| **[🎯 Vnclogs](details/VNCLogs.md)** | VNC Logs | **VNCLogs.tkape** | Phill Moore, Evangelos Dragonas | 1.3 |
| **[🎯 Win SCP](details/WinSCP.md)** | WinSCP | **WinSCP.tkape** | Andrew Rathbun | 1.0 |

---

[⬅️ Back to Cloud Storage & Remote Access](cloud_remote.md)
