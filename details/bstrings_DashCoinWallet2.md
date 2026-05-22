# ⚙️ **Bstrings Dash Coin Wallet2**
### `File Name: bstrings_DashCoinWallet2.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun, Georg Lauenstein  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Use bstrings to GREP for DashCoin Wallets

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Bstrings Dash Coin Wallet2 to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Bstrings Dash Coin Wallet2 logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Bstrings Dash Coin Wallet2 timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Use bstrings to GREP for DashCoin Wallets
Category: KeywordSearches
Author: Andrew Rathbun, Georg Lauenstein
Version: 1.1
Id: f22fb04f-3268-493b-b100-6861b0f7e953
BinaryUrl: https://download.ericzimmermanstools.com/bstrings.zip
ExportFormat: txt
Processors:
    -
        Executable: bstrings.exe
        CommandLine: -d %sourceDirectory% -o '%destinationDirectory%' --lr dashcoin2
        ExportFormat: txt
        ExportFile: DashCoinWallets2.txt

# Documentation
# https://github.com/EricZimmerman/bstrings
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# https://binaryforay.blogspot.com/search?q=bstrings
# https://www.sans.org/posters/eric-zimmerman-tools-cheat-sheet/
# https://leanpub.com/eztoolsmanuals
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
