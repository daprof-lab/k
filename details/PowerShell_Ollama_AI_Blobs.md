# ⚙️ **Power Shell Ollama AI Blobs**
### `File Name: PowerShell_Ollama_AI_Blobs.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** DReneau  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Ollama-AI Blob Files

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Ollama AI Blobs to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Ollama AI Blobs logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Ollama AI Blobs timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Ollama-AI Blob Files
Category: PowerShell
Author: DReneau
Version: 1.0
Id: a31a4412-f6d4-4098-9ba1-feba2f96ad57
ExportFormat: txt
Processors:
  -
    Executable: C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe
    CommandLine: "$destinationPath = '%DestinationDirectory%\\ollama_combined_blobs.txt'; $usersPath = Join-Path '%SourceDirectory%' 'Users'; Get-ChildItem -Path $usersPath -Directory | ForEach-Object { $modelsPath = Join-Path $_.FullName '.ollama\\models\\blobs'; if (Test-Path $modelsPath) { Get-ChildItem -Path $modelsPath -File | Where-Object { $_.Length -lt 2KB } | ForEach-Object { $fileContent = Get-Content -Path $_.FullName -Raw -ErrorAction SilentlyContinue; if ($fileContent -match '\"model_format\"') { $entry = ('{0} | {1}' -f $_.Name, $fileContent); Add-Content -Path $destinationPath -Value $entry; Add-Content -Path $destinationPath -Value \"`r`n\"; } } } }"
    ExportFormat: txt

# Documentation
# https://ollama.com/blog | https://github.com/ollama/ollama | https://hub.docker.com/r/ollama/ollama
# Ollama is used for self-hosted AI inference, and it supports many models out of the box.
# Ollama serves as the backend for common AI projects such as OpenWebUI, among others.
# .\kape.exe --msource c:\ --mdest k:\case-12345\Kape\mout --module powershell_ollama_ai_blobs
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
