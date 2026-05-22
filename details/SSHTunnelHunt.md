# ⚙️ **Sshtunnel Hunt**
### `File Name: SSHTunnelHunt.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Aashiq Ahmed  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Search command history and text artifacts for SSH tunneling and pivoting commands

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Sshtunnel Hunt to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Sshtunnel Hunt logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Sshtunnel Hunt timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Search command history and text artifacts for SSH tunneling and pivoting commands
Category: Apps
Author: Aashiq Ahmed
Version: 1.0
Id: 3a5b2f54-2b1d-4c7a-9a9e-6c7d52b7a8a1
BinaryUrl: https://raw.githubusercontent.com/cyber20233/SSHCommandHunt/main/SSHCommandHunt.ps1
ExportFormat: csv

Processors:
  -
    Executable: powershell.exe
    CommandLine: -ExecutionPolicy Bypass -NoProfile -File .\Modules\bin\SSHCommandHunt.ps1 -Source %sourceDirectory% -Out %destinationDirectory%\SSHCommandHits.csv
    ExportFormat: csv

# Documentation
# Searches artifact text for command patterns associated with SSH tunneling and common pivoting tools such as ssh -L/-R/-D, plink, netsh portproxy, chisel, ngrok, cloudflared, ligolo, frp, and socat.
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
