# 🎯 **Cert Util**
### `File Name: CertUtil.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** NVISO (@NVISOsecurity), 2thewes  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Certutil

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Cert Util to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Cert Util events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Cert Util storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Certutil
Author: NVISO (@NVISOsecurity), 2thewes
Version: 1.1
Id: ec903d15-64b5-4484-8786-94b2ad90bfb7
RecreateDirectories: true
Targets:
    -
        Name: System CryptnetUrlCache
        Category: FileKnowledge
        Path: C:\Windows\System32\config\systemprofile\AppData\LocalLow\Microsoft\CryptnetUrlCache\
        Recursive: true
    -
        Name: System WOW64 CryptnetUrlCache
        Category: FileKnowledge
        Path: C:\Windows\SysWOW64\config\systemprofile\AppData\LocalLow\Microsoft\CryptnetUrlCache\
        Recursive: true
    -
        Name: User CryptnetUrlCache
        Category: FileKnowledge
        Path: C:\Users\%user%\AppData\LocalLow\Microsoft\CryptnetUrlCache\
        Recursive: true
    -
        Name: INetCache
        Category: FileKnowledge
        Path: C:\Users\%user%\AppData\Local\Microsoft\Windows\INetCache\IE\
        Recursive: true

# Documentation
# https://blog.menasec.net/2019/03/initial-access-execution-evidences-for.html
# https://thinkdfir.com/2020/07/30/certutil-download-artefacts/
# https://github.com/Velocidex/velociraptor/blob/352fec8b9c285b57bb2cc12cb11dc1900f308921/artifacts/definitions/Windows/Forensics/CertUtil.yaml
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
