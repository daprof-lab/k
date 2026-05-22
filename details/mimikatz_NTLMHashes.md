# ⚙️ **Mimikatz Ntlmhashes**
### `File Name: mimikatz_NTLMHashes.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Banaanhangwagen  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Retrieve NTLM-hashes of all the user accounts

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Mimikatz Ntlmhashes to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Mimikatz Ntlmhashes logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Mimikatz Ntlmhashes timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Retrieve NTLM-hashes of all the user accounts
Category: Passwords
Author: Banaanhangwagen
Version: 1.0
Id: 899fd6c5-c957-42cf-a4f7-d62f4430b6b2
BinaryUrl: https://github.com/gentilkiwi/mimikatz/releases
ExportFormat: txt
Processors:
    -
        Executable: mimikatz.exe
        CommandLine: -foobar "log %destinationDirectory%\NTLM_hashes.txt" version "lsadump::sam /system:%sourceDirectory%\SYSTEM /sam:%sourceDirectory%\SAM" exit
        ExportFormat: txt

# Documentation
# https://github.com/gentilkiwi/mimikatz
# https://www.varonis.com/blog/what-is-mimikatz/
# This module extracts the Windows NTLM hashes for every user account. The command is a little bit dirty, but it works.
# Point the 'module source' to the acquired "\Windows\System32\config" folder
# mimikatz.exe (x64) must be put in 'Modules\bin' folder
# Attention: your antivirus may not appreciate the program; whitelist it.
#
# Remember: NTLM-hash 31d6cfe0d16ae931b73c59d7e0c089c0 means "blank"
#
# Example:
# .\kape.exe --msource C:\kape\path\to\acquired\Windows\System32\config --mdest C:\kape\out --module ntlm-hashes
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
