# ⚙️ **CertUtil Activity Parser**
### `File Name: CertUtil_Parser.mkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** DReneau, Paul CABON - CERT Cwatch - Almond  
**Version:** 2.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Extracts execution histories, remote download URLs, and command sequences logged by Certutil.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run CertUtil Activity Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw CertUtil Activity Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage CertUtil Activity Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: A Module to parse Certutil activity
Category: Windows
Author: DReneau, Paul CABON - CERT Cwatch - Almond
Version: 2.0
Id: 7d18d1ad-13b5-435c-a5f1-063093e39646
BinaryUrl: https://github.com/AbdulRhmanAlfaifi/CryptnetURLCacheParser/releases/tag/1.1/CryptnetUrlCacheParser.exe
ExportFormat: csv
Processors:
  - Executable: CryptnetUrlCacheParser.exe
    CommandLine: "-d \"%sourceDirectory%\\Windows\\System32\\config\\systemprofile\\AppData\\LocalLow\\Microsoft\\CryptnetUrlCache\\Metadata\" \"%sourceDirectory%\\Windows\\SysWOW64\\config\\systemprofile\\AppData\\LocalLow\\Microsoft\\CryptnetUrlCache\\Metadata\" \"%sourceDirectory%\\Users\\*\\AppData\\LocalLow\\Microsoft\\CryptnetUrlCache\\MetaData\" -o \"%destinationDirectory%\\Certutil_Parsed.csv\""
    ExportFormat: csv

# Documentation
# https://u0041.co/posts/articals/certutil-artifacts-analysis/
# https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/certutil
# https://thinkdfir.com/2020/07/30/certutil-download-artefacts/
# Certutil is a Windows utility used by threat actors to download arbitrary files/tools using Land Binary (LOLBin)  techniques.
# Certutil can also be used to base64 encode/decode and calculate file hashes.
```
---

[⬅️ Back to Threat Hunting, AV & Logs Modules](../threat_hunting_modules.md)
