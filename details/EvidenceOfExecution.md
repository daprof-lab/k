# 🎯 **Evidence of Execution Suite**
### `File Name: EvidenceOfExecution.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
A comprehensive compound target collecting all execution artifacts (Prefetch, Amcache, RecentFileCache, Shimcache, and system execution databases) in a single instruction.

---

## 🔍 **Investigative Use-Cases**
* **Rapid Execution Triage**: Immediately gather all execution evidence to speed up initial system investigation.
* **Malware Run Investigation**: Correlate Prefetch runs with Amcache installation records and Shimcache flags to verify malware execution.
* **Incident Scope Determination**: Determine if a system was actively compromised by auditing all execution evidence at once.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Evidence of execution related files
Author: Eric Zimmerman
Version: 1.1
Id: 13ba1e33-4899-4843-adf0-c7e6a20d758a
RecreateDirectories: true
Targets:
    -
        Name: Amcache
        Category: ApplicationCompatibility
        Path: Amcache.tkape
    -
        Name: AppCompatPCA
        Category: ApplicationCompatibility
        Path: AppCompatPCA.tkape
    -
        Name: Prefetch
        Category: Prefetch
        Path: Prefetch.tkape
    -
        Name: RecentFileCache
        Category: ApplicationCompatibility
        Path: RecentFileCache.tkape
    -
        Name: Syscache
        Category: Syscache
        Path: Syscache.tkape

# Documentation
# ShimCache is not included in this Compound Target, as that would require pulling the entire SYSTEM Registry Hive. To ensure the ShimCache is pulled and parsed, use RegistryHivesSystem.tkape and parse with AppCompatCacheParser.mkape
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
