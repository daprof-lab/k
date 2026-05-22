# ⚙️ **Moba Xterm Passwords Key**
### `File Name: MobaXterm_Passwords_key.mkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Module to extract a copy of MobaXterm encrypted passwords

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Moba Xterm Passwords Key to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Moba Xterm Passwords Key logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Moba Xterm Passwords Key timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Module to extract a copy of MobaXterm encrypted passwords
Category: Live Response
Author: Vito Alfano
Version: 1.0
Id: a7473175-e108-4b93-81cb-49c6e7d37ff9
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\cmd.exe
        CommandLine: /c reg export "HKEY_CURRENT_USER\Software\Mobatek\MobaXterm\P" %destinationDirectory%\MobaXterm_Pass_key.txt
        ExportFormat: txt

# Documentation
# https://xmcyber.com/blog/extracting-encrypted-credentials-from-common-tools-2/
# https://github.com/XMCyber/XMCredentialsDecryptor
```
---

[⬅️ Back to Cloud Storage & Remote Access Modules](../cloud_remote_modules.md)
