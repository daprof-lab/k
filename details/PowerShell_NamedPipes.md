# ⚙️ **Power Shell Named Pipes**
### `File Name: PowerShell_NamedPipes.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Named Pipes List

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Named Pipes to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Named Pipes logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Named Pipes timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Named Pipes List
Category: Network Activity
Author: Max Zabuty
Version: 1.0
Id: f1f5f93d-d03b-45f4-bf72-7b8f9dc7ac23
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-ChildItem -Path '\\.\pipe\' |  Sort Length | Select FullName, Length, IsReadOnly, Exists, CreationTime, LastAccessTime | Export-Csv -Encoding UTF8 -NoTypeInformation -Path '%destinationDirectory%\Named Pipes.csv'"
        ExportFormat: csv
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-ChildItem -Path '\\.\pipe\' |  Sort Length | Select FullName, Length, IsReadOnly, Exists, CreationTime, LastAccessTime | ConvertTo-Json | Out-File -Encoding UTF8 -FilePath '%destinationDirectory%\Named Pipes.json'"
        ExportFormat: json

# Documentation
# https://docs.microsoft.com/en-us/windows/win32/ipc/named-pipes
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
