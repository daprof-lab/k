# **📦 Compound & Automation Packages**

{% hint style="info" %}

**Investigator Note:** Don't want to specify targets one by one? Compound Targets collect entire triage packages at once. Compound Modules automate the execution of multiple parsers in a single command.

{% endhint %}

{% tabs %}

{% tab title="🎯 Targets (.tkape)" %}

| File Name | Description | Author | Version |
| :---- | :---- | :---- | :---- |
| **KapeTriage.tkape** | Comprehensive triage: File System, Registry, Event Logs, Prefetch, SRUM, Browsers, etc. | Scott Downie | 4.2 |
| **\!SANS\_Triage.tkape** | SANS Triage Collection | Mark Hallman | 1.5 |
| **\!BasicCollection.tkape** | Basic Collection | Phill Moore | 1.1 |
| **ServerTriage.tkape** | Artifacts common to servers | Eric Capuano | 1.1 |
| **FileSystem.tkape** | File system metadata | Eric Zimmerman | 1.0 |
| **WebBrowsers.tkape** | Web browser history, bookmarks, etc. | Eric Zimmerman | 1.4 |
| **RegistryHives.tkape** | System and user related Registry hives | Eric Zimmerman | 1.2 |
| **CombinedLogs.tkape** | Event logs, Trace logs, Firewall, PowerShell logs | Mike Cary / Mark Hallman | 1.3 |

{% endtab %}

{% tab title="⚙️ Modules (.mkape)" %}

| File Name | Description | Author | Version |
| :---- | :---- | :---- | :---- |
| **\!EZParser.mkape** | Run all Eric Zimmerman Parsers | Phill Moore | 1.5 |
| **\!\!ToolSync.mkape** | Sync for new Maps, Batch Files, Targets and Modules | Andrew Rathbun / Andreas Hunkeler | 1.0 |
| **KAPE\_Automation.mkape** | Module to run for KAPE automation | Brian Maloney | 1.0 |
| **LogParser.mkape** | LogParser Compound Module | Andrew Rathbun | 1.0 |
| **SOFELK\_Parser.mkape** | Parsing for SOF-ELK Instance | Tony Knutson / Andrew Rathbun | 1.2 |
| **bstrings.mkape** | Run all bstrings Modules | Andrew Rathbun | 1.0 |
| **Reghunter.mkape** | Execute all Reghunter modules | Georg Lauenstein | 1.0 |

{% endtab %}

{% endtabs %}