# ⚙️ **Power Shell Accessibility Features**
### `File Name: PowerShell_AccessibilityFeatures.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Checks for Debugger registry value and file integrity of specific Windows features

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Accessibility Features to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Accessibility Features logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Accessibility Features timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Checks for Debugger registry value and file integrity of specific Windows features
Category: Persistence
Author: Max Zabuty
Version: 1.0
Id: e3444190-b58e-4fe7-8048-e0bb1f40b3c7
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: >
            -Command "$features = @(\"sethc.exe\", \"utilman.exe\", \"AtBroker.exe\", \"Narrator.exe\", \"Magnify.exe\", \"DisplaySwitch.exe\", \"osk.exe\"); $results = @(); foreach ($feature in $features) { $regPath = \"HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Image File Execution Options\$feature\"; $result = @{FeatureName = $feature; Debugger = $null; IsValid = $null}; if (Test-Path -Path \"$regPath\Debugger\") { $result.Debugger = Get-ItemPropertyValue -Path $regPath -Name Debugger } else { $result.Debugger = \"No Debugger\" }; $filePath = \"C:\Windows\System32\$feature\"; $sfcOutput = sfc /VERIFYFILE=$filePath; $sfcOutput = $sfcOutput[5].Split(\"`0\") -join \"\"; if ($sfcOutput -like \"Windows Resource Protection did not find any integrity violations.\") { $result.IsValid = \"Valid\" } elseif ($sfcOutput -match \"Windows Resource Protection could not perform the requested operation\") { $result.IsValid = \"Error: Could not perform operation\" } else { $result.IsValid = \"File not found or invalid\" }; $results += $result }; $customResults = $results | ForEach-Object {[PSCustomObject]@{FeatureName = $_.FeatureName; Debugger = $_.Debugger; IsValid = $_.IsValid}}; $customResults | Export-Csv -NoTypeInformation -Encoding UTF8 -Path \"%destinationDirectory%\AccessibilityFeaturesCheck.csv\" "
        ExportFormat: csv
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: >
            -Command "$features = @(\"sethc.exe\", \"utilman.exe\", \"AtBroker.exe\", \"Narrator.exe\", \"Magnify.exe\", \"DisplaySwitch.exe\", \"osk.exe\"); $results = @(); foreach ($feature in $features) { $regPath = \"HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Image File Execution Options\$feature\"; $result = @{FeatureName = $feature; Debugger = $null; IsValid = $null}; if (Test-Path -Path \"$regPath\Debugger\") { $result.Debugger = Get-ItemPropertyValue -Path $regPath -Name Debugger } else { $result.Debugger = \"No Debugger\" }; $filePath = \"C:\Windows\System32\$feature\"; $sfcOutput = sfc /VERIFYFILE=$filePath; $sfcOutput = $sfcOutput[5].Split(\"`0\") -join \"\"; if ($sfcOutput -like \"Windows Resource Protection did not find any integrity violations.\") { $result.IsValid = \"Valid\" } elseif ($sfcOutput -match \"Windows Resource Protection could not perform the requested operation\") { $result.IsValid = \"Error: Could not perform operation\" } else { $result.IsValid = \"File not found or invalid\" }; $results += $result }; $customResults = $results | ForEach-Object {[PSCustomObject]@{FeatureName = $_.FeatureName; Debugger = $_.Debugger; IsValid = $_.IsValid}}; $customResults  | ConvertTo-Json | Out-File -Encoding UTF8 -FilePath '%destinationDirectory%\AccessibilityFeaturesCheck.json' "
        ExportFormat: json

# Documentation
# https://support.microsoft.com/en-us/windows/discover-windows-accessibility-features-8b1068e6-d3b8-4ba8-b027-133dd8911df9
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
