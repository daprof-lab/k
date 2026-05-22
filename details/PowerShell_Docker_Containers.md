# ⚙️ **Power Shell Docker Containers**
### `File Name: PowerShell_Docker_Containers.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** DReneau  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Docker Container Details

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Docker Containers to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Docker Containers logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Docker Containers timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Docker Container Details
Category: LiveResponse
Author: DReneau
Version: 1.1
Id: 87bf8201-6256-45ad-8b2b-a6034235db53
ExportFormat: txt
Processors:
  - Executable: C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe
    CommandLine: "$filePath = '%destinationDirectory%\\docker_container_info.txt'; $dockerOutput = (docker version | Out-String).TrimEnd() + [System.Environment]::NewLine + [System.Environment]::NewLine + (docker ps --all --format 'ID: {{.ID}} | Name: {{.Names}} | Image: {{.Image}} | Size: {{.Size}} | Status: {{.Status}} | Command: {{.Command}}' | Out-String).TrimEnd(); Set-Content -Path $filePath -Value $dockerOutput -Encoding UTF8;"
    ExportFormat: txt

# Documentation
# https://docs.docker.com/reference/cli/docker/container/ls/
# This module combines Docker ps and Docker version commands. Output is based on installed Docker and the status.
# Example:
# .\kape.exe --msource C:\kape\path\to\acquired\Windows\System32\config --mdest C:\kape\out --module powershell_docker_containers
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
