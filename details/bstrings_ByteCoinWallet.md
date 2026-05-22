# ⚙️ **Bstrings Byte Coin Wallet**
### `File Name: bstrings_ByteCoinWallet.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun, Georg Lauenstein  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Use bstrings to GREP for ByteCoin Wallets

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Bstrings Byte Coin Wallet to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Bstrings Byte Coin Wallet logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Bstrings Byte Coin Wallet timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Use bstrings to GREP for ByteCoin Wallets
Category: KeywordSearches
Author: Andrew Rathbun, Georg Lauenstein
Version: 1.0
Id: 210ca497-ecc6-4084-b8c0-f9dd3aec2d2f
BinaryUrl: https://download.ericzimmermanstools.com/bstrings.zip
ExportFormat: txt
Processors:
    -
        Executable: bstrings.exe
        CommandLine: -d %sourceDirectory% -o '%destinationDirectory%' --lr bytecoin
        ExportFormat: txt
        ExportFile: ByteCoinWallets.txt

# Documentation
# https://github.com/EricZimmerman/bstrings
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# https://binaryforay.blogspot.com/search?q=bstrings
# https://www.sans.org/posters/eric-zimmerman-tools-cheat-sheet/
# https://leanpub.com/eztoolsmanuals
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
