# ⚙️ **Bstrings Crypto Wallets**
### `File Name: bstrings_CryptoWallets.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Run all bstrings Crypto Wallet-related Modules

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Bstrings Crypto Wallets to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Bstrings Crypto Wallets logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Bstrings Crypto Wallets timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Run all bstrings Crypto Wallet-related Modules
Category: Modules
Author: Andrew Rathbun
Version: 1.0
Id: 47eb13e8-3bed-49fe-9192-fb0c14eb937d
BinaryUrl: https://ericzimmerman.github.io/
ExportFormat: txt
Processors:
    -
        Executable: bstrings_AeonWallet.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: bstrings_BitCoinWallet.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: bstrings_ByteCoinWallet.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: bstrings_CryptoWallets.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: bstrings_DashCoinWallet.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: bstrings_DashCoinWallet2.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: bstrings_FantomCoinWallet.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: bstrings_MoneroWallet.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: bstrings_SumoKoinWallet.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation
# N/A
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
