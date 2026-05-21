# 🎯 **BITS Persistent Jobs**
### `File Name: BITS.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Jos Clephas  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
System database folder for the Background Intelligent Transfer Service (BITS). BITS is widely abused by threat actors to establish stealthy persistent file downloads.

---

## 🔍 **Investigative Use-Cases**
* **Backdoor Download Auditing**: Identify active BITS transfer queues that reference external malicious URLs and payload locations.
* **Malicious Command Persistence**: Scan BITS jobs that are configured to launch post-download command payloads automatically.
* **Network Exfiltration Checking**: Detect exfiltration schedules configured to run in the background using BITS bandwidth throttling.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: 'Microsoft BITS (Background Intelligent Transer Service) persistent files'
Author: Jos Clephas
Version: 1.0
Id: bd55a936-7c4d-46a5-b7bb-a4e4064683d2
RecreateDirectories: true
Targets:
    -
        Name: BITS files
        Category: Persistence
        Path: C:\ProgramData\Microsoft\Network\Downloader\
        Recursive: true

# Documentation
# https://www.sans.org/reading-room/whitepapers/forensics/bits-forensics-39195
# https://cyberforensicator.com/2019/05/12/using-mitre-attck-for-forensics-bits-jobs-t1197/
# https://www.thedfirspot.com/post/a-bits-of-a-problem-investigating-bits-jobs
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
