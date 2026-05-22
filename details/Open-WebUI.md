# ⚙️ **Open Web UI**
### `File Name: Open-WebUI.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** DReneau  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Open WebUI Parsers

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Open Web UI to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Open Web UI logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Open Web UI timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Open WebUI Parsers
Category: AI
Author: DReneau
Version: 1.0
Id: 23f770d6-43b7-4657-a7cb-a6d79d772918
ExportFormat: txt
Processors:
    -
        Executable: PowerShell_OpenWebUI_Account_Parser.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_OpenWebUI_Chat_Parser.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_OpenWebUI_Document_Parser.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PowerShell_Docker_Containers.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation
# https://github.com/open-webui/open-webui
# https://docs.docker.com/reference/cli/docker/container/ls/
# This module combines Open WebUI artifacts located in Docker Desktop logs.
# .\kape.exe --msource c:\ --mdest k:\case-12345\Kape\mout --module open-webui
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
