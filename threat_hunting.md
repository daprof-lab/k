# **🛡️ Threat Hunting, AV & Logs**

{% hint style="info" %}

**Investigator Note:** This section is vital for tracking malware execution and alerts. It contains Windows Event Logs collectors, Antivirus/EDR logs, and powerful IOC scanners like Thor, Loki, Hayabusa, and Chainsaw.

{% endhint %}

---

## **Explore Category Contents**

Select a sub-page below to browse the full forensic components in this category.

### 🎯 [Browse Targets (.tkape)](threat_hunting_targets.md)
> Collect raw forensic artifacts from event logs, PowerShell transcripts, and endpoint antivirus solutions.
> * **11 Targets Available** (e.g., `EventLogs.tkape`, `WindowsDefender.tkape`, `PowerShellTranscripts.tkape`)
> * [View All Targets &rarr;](threat_hunting_targets.md)

### ⚙️ [Browse Modules (.mkape)](threat_hunting_modules.md)
> Audit systems and analyze event logs using modern IOC scanners, Sigma rule parsers, and event engines.
> * **9 Modules Available** (e.g., `Chainsaw.mkape`, `Hayabusa.mkape`, `Thor_Scan.mkape`)
> * [View All Modules &rarr;](threat_hunting_modules.md)

---

## 📊 **Category Quick Stats**

| Metric | Details |
| :--- | :--- |
| **📁 Focus Area** | Operating system event records, terminal executions, and endpoint protection telemetry |
| **🎯 Total Targets** | **11** configuration files |
| **⚙️ Total Modules** | **9** parser plugins |

---

## 💡 **Key Highlighted Artifacts**

* **Windows Event Logs (EVTX)**: The ultimate audit source. Capture security logins, service installations, scheduled tasks, and network connections.
* **Antivirus & EDR (CrowdStrike, SentinelOne, Defender, TrendMicro, etc.)**: Check local quarantine history, detection alerts, agent diagnostic logs, and block events.
* **PowerShell Transcripts**: Review raw command executions, scripting arguments, and malicious payload downloads in terminal sessions.
* **IOC & Threat Scanners (Hayabusa, Chainsaw, Thor, Loki, Zircolite)**: Search across logs using SIGMA rules and threat feeds to locate compromise indicators in seconds.