# ⚙️ **Power Shell Ollama AI Manifests**
### `File Name: PowerShell_Ollama_AI_Manifests.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** DReneau  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Ollama-AI Manifests

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Ollama AI Manifests to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Ollama AI Manifests logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Ollama AI Manifests timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Ollama-AI Manifests
Category: PowerShell
Author: DReneau
Version: 1.0
Id: 48146441-174c-43a6-8dd0-8c317f1004e2
ExportFormat: txt
Processors:
  -
    Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
    CommandLine: "$destinationPath = '%destinationDirectory%\\ollama_combined_manifests.txt'; Remove-Item -Path $destinationPath -ErrorAction SilentlyContinue; $users = Get-ChildItem -Path '%SourceDirectory%\\Users' -Directory; foreach ($user in $users) { $ollamaPath = Join-Path $user.FullName '.ollama'; if (Test-Path $ollamaPath) { $modelsPath = Join-Path $ollamaPath 'models\\manifests'; if (Test-Path $modelsPath) { Get-ChildItem -Path $modelsPath -Recurse -File | ForEach-Object { $modelName = $_.Name; $fileContent = Get-Content -Path $_.FullName -Raw -ErrorAction SilentlyContinue; if ($fileContent -match '\"mediaType\"') { $entry = ('{0} | {1}' -f $_.FullName, $fileContent); Add-Content -Path $destinationPath -Value $entry; Add-Content -Path $destinationPath -Value \"`r`n`r`n\"; } } } } }"
    ExportFormat: txt

# Documentation
# https://ollama.com/blog | https://github.com/ollama/ollama | https://hub.docker.com/r/ollama/ollama
# Ollama is used for self-hosted AI inference, and it supports many models out of the box.
# Ollama serves as the backend for common AI projects such as OpenWebUI, among others.
# The code will identify the installed Models, the Model Integrity hash and the Ollama PrivateKey.
# .\kape.exe --msource c:\ --mdest k:\case-12345\Kape\mout --module powershell_ollama_ai_manifests
# https://www.wiz.io/blog/probllama-ollama-vulnerability-cve-2024-37032
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
