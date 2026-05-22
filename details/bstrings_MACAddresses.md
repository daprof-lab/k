# ⚙️ **Bstrings Macaddresses**
### `File Name: bstrings_MACAddresses.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun, Georg Lauenstein  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Use bstrings to GREP for MAC Addresses

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Bstrings Macaddresses to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Bstrings Macaddresses logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Bstrings Macaddresses timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Use bstrings to GREP for MAC Addresses
Category: KeywordSearches
Author: Andrew Rathbun, Georg Lauenstein
Version: 1.1
Id: b24a8be2-f3e6-463f-89f6-97b1e405ddf0
BinaryUrl: https://download.ericzimmermanstools.com/bstrings.zip
ExportFormat: txt
Processors:
    -
        Executable: bstrings.exe
        CommandLine: -d %sourceDirectory% -o '%destinationDirectory%' --lr mac
        ExportFormat: txt
        ExportFile: MacAddress.txt

# Documentation
# https://github.com/EricZimmerman/bstrings
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# https://binaryforay.blogspot.com/search?q=bstrings
# https://www.sans.org/posters/eric-zimmerman-tools-cheat-sheet/
# https://leanpub.com/eztoolsmanuals
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
