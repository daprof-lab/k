# **🧠 Memory & Virtualization**

{% hint style="info" %}

**Investigator Note:** This section handles the collection and analysis of Volatile Memory (RAM), Virtual Machine configurations, and Windows Subsystem for Linux (WSL) environments.

{% endhint %}

---

## **Explore Category Contents**

Select a sub-page below to browse the full forensic components in this category.

### 🎯 [Browse Targets (.tkape)](memory_virtualization_targets.md)
> Collect raw volatile memory files, VM snapshots, and WSL user files.
> * **8 Targets Available** (e.g., `VirtualBoxMemory.tkape`, `MemoryFiles.tkape`, `WSL.tkape`)
> * [View All Targets &rarr;](memory_virtualization_targets.md)

### ⚙️ [Browse Modules (.mkape)](memory_virtualization_modules.md)
> Execute RAM acquisition utilities or run Volatility frameworks to extract active OS state information.
> * **8 Modules Available** (e.g., `DumpIt_Memory.mkape`, `MagnetForensics_RAMCapture.mkape`, `Volatility_netscan.mkape`)
> * [View All Modules &rarr;](memory_virtualization_modules.md)

---

## 📊 **Category Quick Stats**

| Metric | Details |
| :--- | :--- |
| **📁 Focus Area** | Physical RAM capture, virtual machine hypervisor configurations, and nested Linux environments |
| **🎯 Total Targets** | **8** configuration files |
| **⚙️ Total Modules** | **8** parser plugins |

---

## 💡 **Key Highlighted Artifacts**

* **Volatile Memory (RAM Files)**: Acquire raw physical memory (using DumpIt, Magnet, Belkasoft) to preserve running processes, open network sockets, unencrypted passwords, and active registry connections.
* **Volatility Post-Processing**: Run plugins like `pslist` (process listing), `netscan` (network status), `cmdline` (arguments used), and `malfind`/`hollowfind` to detect hidden code injections.
* **Virtual Machine Artifacts (VMware & VirtualBox)**: Recover guest OS memories, capture log files, and inspect system virtualization footprints.
* **Windows Subsystem for Linux (WSL - Ubuntu & Kali)**: Collect ext4 filesystems and user databases from integrated WSL installations to investigate cross-platform workflows.