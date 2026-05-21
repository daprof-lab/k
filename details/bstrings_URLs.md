# ⚙️ **bstrings URL Extractor**
### `File Name: bstrings_URLs.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Chris Kudless / Georg Lauenstein  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Scans data using bstrings regex to locate and extract valid web links.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run bstrings URL Extractor to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw bstrings URL Extractor logs to index file anomalies.
* **Incident Impact Assessment**: Leverage bstrings URL Extractor timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Use bstrings to GREP for URLs
Category: KeywordSearches
Author: Chris Kudless, Georg Lauenstein
Version: 1.1
Id: 2a7ec6bd-6228-4542-9b4b-002957b26661
BinaryUrl: https://download.ericzimmermanstools.com/bstrings.zip
ExportFormat: txt
Processors:
    -
        Executable: bstrings.exe
        CommandLine: -d %sourceDirectory% -o '%destinationDirectory%' --lr url3986
        ExportFormat: txt
        ExportFile: URLs.txt

# Documentation
# https://github.com/EricZimmerman/bstrings
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# https://binaryforay.blogspot.com/search?q=bstrings
# https://www.sans.org/posters/eric-zimmerman-tools-cheat-sheet/
# https://leanpub.com/eztoolsmanuals
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
