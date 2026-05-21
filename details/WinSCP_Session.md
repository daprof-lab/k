# ⚙️ **WinSCP Session Parser**
### `File Name: WinSCP_Session.mkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Decrypts WinSCP registry entries to recover saved network targets, usernames, and encrypted passwords.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run WinSCP Session Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw WinSCP Session Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage WinSCP Session Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Module to extract a copy of WinSCP encrypted credentials
Category: Live Response
Author: Vito Alfano
Version: 1.0
Id: e00dac99-3a59-4c59-911c-95eda1769250
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\cmd.exe
        CommandLine: /c reg export "HKEY_CURRENT_USER\Software\Martin Prikryl\WinSCP 2\Sessions" %destinationDirectory%\winscp2_sessions_key.txt
        ExportFormat: txt

# Documentation
# https://xmcyber.com/blog/extracting-encrypted-credentials-from-common-tools-2/
# https://github.com/XMCyber/XMCredentialsDecryptor
```
---

[⬅️ Back to Cloud Storage & Remote Access Modules](../cloud_remote_modules.md)
