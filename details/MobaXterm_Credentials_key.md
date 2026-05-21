# ⚙️ **MobaXterm Decrypter**
### `File Name: MobaXterm_Credentials_key.mkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Decrypts and extracts saved credentials, network host targets, and SSH profiles from MobaXterm.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run MobaXterm Decrypter to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw MobaXterm Decrypter logs to index file anomalies.
* **Incident Impact Assessment**: Leverage MobaXterm Decrypter timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Module to extract a copy of MobaXterm encrypted credentials
Category: Live Response
Author: Vito Alfano
Version: 1.0
Id: 1dc46684-fee1-40ab-9a25-216ec41df4a9
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\cmd.exe
        CommandLine: /c reg export "HKEY_CURRENT_USER\Software\Mobatek\MobaXterm\C" %destinationDirectory%\MobaXterm_Credentials_key.txt
        ExportFormat: txt

# Documentation
# https://xmcyber.com/blog/extracting-encrypted-credentials-from-common-tools-2/
# https://github.com/XMCyber/XMCredentialsDecryptor
```
---

[⬅️ Back to Cloud Storage & Remote Access Modules](../cloud_remote_modules.md)
