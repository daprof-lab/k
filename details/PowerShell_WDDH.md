# ⚙️ **Power Shell WDDH**
### `File Name: PowerShell_WDDH.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Paul CABON - CERT Cwatch  
**Version:** 1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows Defender Detection History parser

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell WDDH to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell WDDH logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell WDDH timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Windows Defender Detection History parser
Category: Antivirus
Author: Paul CABON - CERT Cwatch 
Version: 1
BinaryUrl: https://github.com/cert-orangecyberdefense/wddh-parser
Id: 44f18055-a944-4549-9858-d52a47420993
ExportFormat: json
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -c "Set-Location '%sourceDirectory%\ProgramData\Microsoft\Windows Defender\Scans\History\Service\'; & %kapeDirectory%\Modules\bin\wddh.exe -D DetectionHistory"
        ExportFormat: json
        ExportFile: WDDH.json

# Documentation
# https://www.orangecyberdefense.com/global/blog/cybersecurity/digging-into-windows-defender-detection-history-wddh
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
