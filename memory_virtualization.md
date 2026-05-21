# **🧠 Memory & Virtualization**

{% hint style="info" %}

**Investigator Note:** This section handles the collection and analysis of Volatile Memory (RAM), Virtual Machine configurations, and Windows Subsystem for Linux (WSL) environments.

{% endhint %}

{% tabs %}

{% tab title="🎯 Targets (.tkape)" %}

| File Name | Description | Author | Version |
| :---- | :---- | :---- | :---- |
| **VirtualBoxMemory.tkape** | VirtualBox \- Memory | Andrew Rathbun | 1.0 |
| **VirtualBoxLogs.tkape** | Collects VirtualBox log files | Matt Dawson | 1.0 |
| **VMwareMemory.tkape** | VMware \- Virtual Machine Memory | Andrew Rathbun | 1.0 |
| **VMwareInventory.tkape** | VMware \- Virtual Machine Inventory | Andrew Rathbun | 1.0 |
| **MemoryFiles.tkape** | Memory Files | Ahmed Elshaer / Teo Kia Meng | 1.0 |
| **WSL.tkape** | All Windows Subsystem for Linux targets | Matt Dawson | 1.0 |
| **Kali.tkape** | Kali on Windows Subsystem for Linux | Matt Dawson | 1.0 |
| **Ubuntu.tkape** | Ubuntu on Windows Subsystem for Linux | Matt Dawson | 1.0 |

{% endtab %}

{% tab title="⚙️ Modules (.mkape)" %}

| File Name | Description | Author | Version |
| :---- | :---- | :---- | :---- |
| **DumpIt\_Memory.mkape** | DumpIt Memory Acquisition | Doug Metz | 1.2 |
| **MagnetForensics\_RAMCapture.mkape** | Magnet RAM Capture Memory Acquisition | Doug Metz | 1.1 |
| **Belkasoft\_RAMCapture.mkape** | Belkasoft RAM Capture Memory Acquisition | Nick Polosukhin | 1.0 |
| **Volatility\_pslist.mkape** | Post-Process memory images with Volatility (pslist) | Jos Clephas | 1.0 |
| **Volatility\_malfind.mkape** | Post-Process memory images with Volatility (malfind) | Jos Clephas | 1.0 |
| **Volatility\_netscan.mkape** | Post-Process memory images with Volatility (netscan) | Jos Clephas | 1.0 |
| **Volatility\_cmdline.mkape** | Post-Process memory images with Volatility (cmdline) | Jos Clephas | 1.0 |
| **Volatility\_hollowfind.mkape** | Post-Process memory images with Volatility (hollowfind) | Jos Clephas | 1.0 |

{% endtab %}

{% endtabs %}