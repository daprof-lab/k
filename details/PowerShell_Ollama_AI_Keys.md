# ⚙️ **Power Shell Ollama AI Keys**
### `File Name: PowerShell_Ollama_AI_Keys.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** DReneau  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Ollama-AI Private-Public Key Finder

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Ollama AI Keys to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Ollama AI Keys logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Ollama AI Keys timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Ollama-AI Private-Public Key Finder
Category: PowerShell
Author: DReneau
Version: 1.0
Id: f5a65250-42bd-4c11-80dd-4ab621e0c8b8
ExportFormat: TXT
Processors:
  -
    Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
    CommandLine: "$users = Get-ChildItem -Path '%SourceDirectory%\\Users' -Directory; foreach ($user in $users) { $ollamaPath = Join-Path $user.FullName '.ollama'; $privateKeyPath = Join-Path $ollamaPath 'id_*'; $publicKeyPath = Join-Path $ollamaPath '*.pub'; if (Test-Path $ollamaPath) { $privateKey = Get-ChildItem -Path $privateKeyPath -Exclude *.pub | ForEach-Object { $content = Get-Content -Path $_.FullName -Raw; [PSCustomObject]@{ Name = $_.Name; FilePath = $_.FullName; KeyLocated = $content } }; $privateKeyOutput = $privateKey | ForEach-Object { 'Name: ' + $_.Name + [System.Environment]::NewLine + [System.Environment]::NewLine + 'FilePath: ' + $_.FilePath + [System.Environment]::NewLine + [System.Environment]::NewLine + 'Key: ' + $_.KeyLocated + [System.Environment]::NewLine + [System.Environment]::NewLine }; Set-Content -Path '%destinationDirectory%\\ollama_privatekey.txt' -Value $privateKeyOutput -Encoding UTF8; if (Test-Path $publicKeyPath) { $publicKey = Get-ChildItem -Path $publicKeyPath | ForEach-Object { $pubContent = Get-Content -Path $_.FullName -Raw; 'Name: ' + $_.Name + [System.Environment]::NewLine + [System.Environment]::NewLine + 'FilePath: ' + $_.FullName + [System.Environment]::NewLine + [System.Environment]::NewLine + 'Key: ' + $pubContent + [System.Environment]::NewLine + [System.Environment]::NewLine }; Set-Content -Path '%destinationDirectory%\\ollama_publickey.txt' -Value $publicKey -Encoding UTF8 } } }"
    ExportFormat: TXT

# Documentation
# https://ollama.com/blog | https://github.com/ollama/ollama | https://hub.docker.com/r/ollama/ollama
# Ollama is used for self-hosted AI inference, and it supports many models out of the box.
# Ollama serves as the backend for common AI projects such as OpenWebUI, among others.
# The code will identify the installed Models, the Model Integrity hash and the Ollama PrivateKey.
# .\kape.exe --msource c:\ --mdest k:\case-12345\Kape\mout --module powershell_ollama_ai_keys
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
