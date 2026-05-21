# **🎯 Memory & Virtualization - Targets**

{% hint style="success" %}

**Target Collection Info:** These targets guide KAPE to collect raw operating system and application forensic files relating to memory & virtualization. Click on any **Short Name** to view a dedicated detail page including forensics value and KAPE target definitions.

{% endhint %}

[⬅️ Back to Memory & Virtualization](memory_virtualization.md)

---

## **Available Targets (.tkape)**

| Short Name | Description | File Name | Author | Version |
| :--- | :--- | :--- | :--- | :--- |
| **[VirtualBox RAM](details/VirtualBoxMemory.md)** | Volatile memory dumps, guest OS configurations, and runtime state records for VirtualBox. | **VirtualBoxMemory.tkape** | Andrew Rathbun | 1.0 |
| **[VirtualBox Logs](details/VirtualBoxLogs.md)** | Diagnostics logs tracking virtualization setups, connected devices, and machine shutdowns. | **VirtualBoxLogs.tkape** | Matt Dawson | 1.0 |
| **[VMware Guest RAM](details/VMwareMemory.md)** | Captures active VMware RAM snapshot files (.vmem) for memory analysis. | **VMwareMemory.tkape** | Andrew Rathbun | 1.0 |
| **[VMware VM Inventory](details/VMwareInventory.md)** | Inventory configurations, VM structures, and registration tables for VMware instances. | **VMwareInventory.tkape** | Andrew Rathbun | 1.0 |
| **[System Memory Dumps](details/MemoryFiles.md)** | Automatically targets physical memory dumps, crashdumps, and active swap/page files on disk. | **MemoryFiles.tkape** | Ahmed Elshaer / Teo Kia Meng | 1.0 |
| **[WSL Filesystems](details/WSL.md)** | WSL configuration states and raw ext4 file containers representing virtualized Linux environments. | **WSL.tkape** | Matt Dawson | 1.0 |
| **[Kali WSL Instances](details/Kali.md)** | User homes, terminal setups, and operational states for Kali Linux in WSL. | **Kali.tkape** | Matt Dawson | 1.0 |
| **[Ubuntu WSL Instances](details/Ubuntu.md)** | System configurations and user storage pools for Ubuntu Linux running inside WSL. | **Ubuntu.tkape** | Matt Dawson | 1.0 |

---

[⬅️ Back to Memory & Virtualization](memory_virtualization.md)
