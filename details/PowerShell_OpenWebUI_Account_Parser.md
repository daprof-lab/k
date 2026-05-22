# ⚙️ **Power Shell Open Web UI Account Parser**
### `File Name: PowerShell_OpenWebUI_Account_Parser.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** DReneau  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Open WebUI User Account Parser - Extract new user account, passwords, and roles  (Docker Desktop).

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Open Web UI Account Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Open Web UI Account Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Open Web UI Account Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Open WebUI User Account Parser - Extract new user account, passwords, and roles  (Docker Desktop).
Category: LiveResponse
Author: DReneau
Version: 1.0
Id: 5dbf2b24-2740-44ea-bca9-5b8dd90c592d
ExportFormat: txt
Processors:
  -
    Executable: C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe
    CommandLine: "$filePath = '%destinationDirectory%\\open-webui_account_data.txt'; try { $dockerInfo = (docker ps --all --filter 'name=webui' --format 'ID: {{.ID}} | Name: {{.Names}} | Image: {{.Image}} | Size: {{.Size}} | Status: {{.Status}} | Command: {{.Command}}' | Out-String).TrimEnd(); if (-not $dockerInfo) { Set-Content -Path $filePath -Value 'Docker Desktop Not Active' -Encoding UTF8; exit } $dockerLogs = docker ps --filter 'name=webui' --format '{{.ID}}' | ForEach-Object { docker logs $_ 2>&1 | ForEach-Object { if ($_ -match 'INFO \\[open_webui.apps.webui.models.auths\\] authenticate_user:') { $_ + [System.Environment]::NewLine } elseif ($_ -match 'name=') { $_ + [System.Environment]::NewLine } } } | Out-String; $output = $dockerInfo + [System.Environment]::NewLine + [System.Environment]::NewLine + $dockerLogs; Set-Content -Path $filePath -Value $output -Encoding UTF8; } catch { Set-Content -Path $filePath -Value 'Docker Desktop Not Active' -Encoding UTF8; exit }"
    ExportFormat: txt

# Documentation
# https://docs.openwebui.com/getting-started/logging/
# https://docs.docker.com/reference/cli/docker/container/ls/
# This module combines "docker ps" and "docker Logs" filtering on the Open WebUI container ID from "docker ps."
# User accounts and passwords are then extracted and written to "open-webui_account_data.txt."
# Example:
# .\kape.exe --msource c:\ --mdest k:\Kape\Case_1234\mout --module powershell_openwebui_account_parser
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
