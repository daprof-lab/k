# **📦 Compound & Automation Packages**

{% hint style="info" %}

**Investigator Note:** Don't want to specify targets one by one? Compound Targets collect entire triage packages at once. Compound Modules automate the execution of multiple parsers in a single command.

{% endhint %}

---

## **Explore Category Contents**

Select a sub-page below to browse the full forensic components in this category.

### 🎯 [Browse Targets (.tkape)](compound_targets.md)
> Collect comprehensive triage sets, filesystems, and logs using pre-packaged master lists.
> * **8 Targets Available** (e.g., `KapeTriage.tkape`, `!SANS_Triage.tkape`, `FileSystem.tkape`)
> * [View All Targets &rarr;](compound_targets.md)

### ⚙️ [Browse Modules (.mkape)](compound_modules.md)
> Run automated processing suites and sync tools to parse entire triage folders simultaneously.
> * **7 Modules Available** (e.g., `!EZParser.mkape`, `LogParser.mkape`, `!!ToolSync.mkape`)
> * [View All Modules &rarr;](compound_modules.md)

---

## 📊 **Category Quick Stats**

| Metric | Details |
| :--- | :--- |
| **📁 Focus Area** | Triage collections, automated tool chains, and global map/target synchronization scripts |
| **🎯 Total Targets** | **8** configuration files |
| **⚙️ Total Modules** | **7** parser plugins |

---

## 💡 **Key Highlighted Artifacts**

* **Comprehensive Triages (KapeTriage, SANS_Triage, BasicCollection)**: One-click actions to collect all critical artifacts including Event Logs, MFT, Registry Hives, Prefetch, LNK files, and web history at once. Recommended for initial system triage.
* **Server Triage**: Focuses specifically on common server artifacts (e.g., server event logs, web services configuration).
* **EZParser Module (!EZParser)**: Automates the execution of all Eric Zimmerman command-line tools against their respective collected targets, saving substantial manual analysis time.
* **Global Sync (!!ToolSync)**: Instantly fetches and synchronizes new KAPE Maps, Targets, and Modules from Github to keep your forensic workstation up to date.