# ⚙️ **Bstrings Monero Wallet**
### `File Name: bstrings_MoneroWallet.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun, Georg Lauenstein  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
Use bstrings to GREP for Monero Wallets

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Bstrings Monero Wallet to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Bstrings Monero Wallet logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Bstrings Monero Wallet timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Use bstrings to GREP for Monero Wallets
Category: KeywordSearches
Author: Andrew Rathbun, Georg Lauenstein
Version: 1.2
Id: 139184fb-5b2e-4e4f-a9df-6da76f138841
BinaryUrl: https://download.ericzimmermanstools.com/bstrings.zip
ExportFormat: txt
Processors:
    -
        Executable: bstrings.exe
        CommandLine: -d %sourceDirectory% -o '%destinationDirectory%' --lr monero
        ExportFormat: txt
        ExportFile: MoneroWallets.txt

# Documentation
# https://github.com/EricZimmerman/bstrings
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# https://binaryforay.blogspot.com/search?q=bstrings
# https://www.sans.org/posters/eric-zimmerman-tools-cheat-sheet/
# https://leanpub.com/eztoolsmanuals
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
