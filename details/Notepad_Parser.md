# ⚙️ **Notepad TabState Parser**
### `File Name: Notepad_Parser.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** DReneau  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Restores active unsaved session data and raw text contents from Windows 11 Notepad tab state files.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Notepad TabState Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Notepad TabState Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Notepad TabState Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: A Module to parse (Windows 11+) Notepad TabState files.
Category: Windows
Author: DReneau
Version: 1.0
Id: b5a8a229-4897-4bda-a8f0-f2246362664f
BinaryUrl: https://github.com/AbdulRhmanAlfaifi/notepad_parser/releases/download/v0.1.0/notepad_parser.exe
ExportFormat: json
Processors:
  - Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
    CommandLine: "Get-ChildItem -Recurse '%sourceDirectory%' -Filter '*.bin' | Where-Object { $_.FullName -like '*Microsoft.WindowsNotepad_8wekyb3d8bbwe\\LocalState\\TabState*' } | ForEach-Object { $outputFile = Join-Path '%destinationDirectory%' ([System.IO.Path]::GetFileNameWithoutExtension($_.FullName) + '.json'); $tempFile = Join-Path '%destinationDirectory%' ([System.IO.Path]::GetFileNameWithoutExtension($_.FullName) + '_temp.json'); & '%kapeDirectory%\\Modules\\bin\\notepad_parser.exe' \"$($_.FullName)\" -f jsonl -o $tempFile; if (Test-Path $outputFile) { Remove-Item $outputFile }; Rename-Item $tempFile $outputFile }"
    ExportFormat: json

# Documentation
# https://u0041.co/posts/articals/exploring-windows-artifacts-notepad-files/
# Windows 11 Notepad stores a cache of recently opened files. This cache contains valuable information, such as file paths, file contents, and other useful data.
# This parser written by AbdulRhman Alfaifi will parse the Windows 11 Notepad cache, specifically the TabState.
# The Notepad artifacts are stored here: "%LOCALAPPDATA%\Packages\Microsoft.WindowsNotepad _8wekyb3d8bbwe\LocalState"
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
