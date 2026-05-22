# ⚙️ **Ollama AI**
### `File Name: Ollama-AI.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** DReneau  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Ollama-AI Parsers

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Ollama AI to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Ollama AI logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Ollama AI timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Ollama-AI Parsers
Category: Modules
Author: DReneau
Version: 1.0
Id: 4e934950-54e4-4c6d-a1de-cb24e3872f5e
ExportFormat: txt
Processors:
    -
        Executable: PowerShell_Ollama_AI_Blobs.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_Ollama_AI_Keys.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_Ollama_AI_Manifests.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_Ollama_AI_Models.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_Docker_Containers.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_Ollama_AI_cve-2024-37032.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation
# https://www.youtube.com/watch?v=aHhQvxwkuuw
# Ollama is used for self-hosted AI inference, and it supports many models out of the box.
# Ollama serves as the backend for common AI projects such as OpenWebUI, among others.
# .\kape.exe --msource c:\ --mdest k:\case-12345\Kape\mout --module ollama-ai
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
