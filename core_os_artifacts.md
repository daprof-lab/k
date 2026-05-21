# **💻 Core OS & File System**

{% hint style="info" %}

**Investigator Note:** This section contains targets and modules for the most critical Windows internal artifacts, including the MFT, Registry Hives, execution evidence (Prefetch/Amcache), and historical OS data (SRUM/Timeline).

{% endhint %}

---

## **Explore Category Contents**

Select a sub-page below to browse the full forensic components in this category.

### 🎯 [Browse Targets (.tkape)](core_os_artifacts_targets.md)
> Collect raw forensic artifacts from the Core OS and File System.
> * **18 Targets Available** (e.g., `$MFT.tkape`, `Prefetch.tkape`, `RegistryHivesSystem.tkape`)
> * [View All Targets &rarr;](core_os_artifacts_targets.md)

### ⚙️ [Browse Modules (.mkape)](core_os_artifacts_modules.md)
> Process the collected Core OS and File System artifacts using specialized analytical tools.
> * **13 Modules Available** (e.g., `MFTECmd.mkape`, `PECmd.mkape`, `AmcacheParser.mkape`)
> * [View All Modules &rarr;](core_os_artifacts_modules.md)

---

## 📊 **Category Quick Stats**

| Metric | Details |
| :--- | :--- |
| **📁 Focus Area** | Windows internal file systems, file execution evidence, and persistent OS logs |
| **🎯 Total Targets** | **18** configuration files |
| **⚙️ Total Modules** | **13** parser plugins |

---

## 💡 **Key Highlighted Artifacts**

* **$MFT & $J (UsnJrnl)**: Track file creation, deletion, modification, and file system movements.
* **Registry Hives**: Retrieve critical OS configuration history, user activity, and persistent autostarts.
* **Prefetch & Amcache**: Essential evidence of process execution to reconstruct a timeline of program runs.
* **SRUM & Windows Timeline**: Capture historical system resource usage and recent user interactions.