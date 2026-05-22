# ⚙️ **Moba Xterm Master Pass**
### `File Name: MobaXterm_Master_Pass.mkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Module to extract a copy of MobaXterm encrypted master password

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Moba Xterm Master Pass to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Moba Xterm Master Pass logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Moba Xterm Master Pass timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Module to extract a copy of MobaXterm encrypted master password
Category: Live Response
Author: Vito Alfano
Version: 1.0
Id: 4ca41e3e-918e-419f-b7cf-22a8cdb1da0f
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\cmd.exe
        CommandLine: /c reg export "HKEY_CURRENT_USER\Software\Mobatek\MobaXterm\M" %destinationDirectory%\Mobaterm_MasterPass_key.txt
        ExportFormat: txt

# Documentation
# https://xmcyber.com/blog/extracting-encrypted-credentials-from-common-tools-2/
# https://github.com/XMCyber/XMCredentialsDecryptor
```
---

[⬅️ Back to Cloud Storage & Remote Access Modules](../cloud_remote_modules.md)
