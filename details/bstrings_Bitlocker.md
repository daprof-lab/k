# ⚙️ **Bstrings Bitlocker**
### `File Name: bstrings_Bitlocker.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Chris Kudless, Georg Lauenstein  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Use bstrings to GREP for Bitlocker recovery keys

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Bstrings Bitlocker to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Bstrings Bitlocker logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Bstrings Bitlocker timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Use bstrings to GREP for Bitlocker recovery keys
Category: KeywordSearches
Author: Chris Kudless, Georg Lauenstein
Version: 1.1
Id: 828d447b-5a26-4f09-a6d8-fa50b4d0b525
BinaryUrl: https://download.ericzimmermanstools.com/bstrings.zip
ExportFormat: txt
Processors:
    -
        Executable: bstrings.exe
        CommandLine: -d %sourceDirectory% -o '%destinationDirectory%' --lr bitlocker
        ExportFormat: txt
        ExportFile: BitlockerRecoveryKeys.txt

# Documentation
# https://github.com/EricZimmerman/bstrings
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# https://binaryforay.blogspot.com/search?q=bstrings
# https://www.sans.org/posters/eric-zimmerman-tools-cheat-sheet/
# https://leanpub.com/eztoolsmanuals
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
