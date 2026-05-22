# ⚙️ **Power Shell System Information**
### `File Name: PowerShell_SystemInformation.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Specific System Information

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell System Information to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell System Information logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell System Information timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Specific System Information
Category: LiveResponse
Author: Max Zabuty
Version: 1.0
Id: 92ce6a73-aee4-4040-b827-84973d90c634
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "$systemInfo = @{}; $systemInfo['Host Name'] = $env:COMPUTERNAME; $systemInfo['OS Name'] = (Get-CimInstance Win32_OperatingSystem).Caption; $systemInfo['OS Version'] = (Get-CimInstance Win32_OperatingSystem).Version; $systemInfo['OS Architecture'] = (Get-CimInstance Win32_Processor).AddressWidth.ToString() + '-Bit'; $systemInfo['Original Install Date'] = (Get-CimInstance Win32_OperatingSystem).InstallDate; $systemInfo['System Boot Time'] = (Get-CimInstance Win32_OperatingSystem).LastBootUpTime; $systemInfo['System Manufacturer'] = (Get-CimInstance Win32_ComputerSystem).Manufacturer; $systemInfo['System Model'] = (Get-CimInstance Win32_ComputerSystem).Model; $systemInfo['BIOS Version'] = (Get-CimInstance Win32_BIOS).SMBIOSBIOSVersion; $systemInfo['Boot Device'] = (Get-CimInstance Win32_ComputerSystem).BootDevice; $systemInfo['Time Zone'] = (Get-CimInstance Win32_TimeZone).Caption; $totalPhysicalMemory = [math]::Round((Get-CimInstance Win32_ComputerSystem).TotalPhysicalMemory / 1GB); $systemInfo['Total Physical Memory'] = \"$totalPhysicalMemory GB\"; $systemInfo['Domain'] = (Get-CimInstance Win32_ComputerSystem).Domain; $systemInfo['Logon Server'] = (Get-CimInstance Win32_ComputerSystem).PrimaryOwnerName; $systemInfo['Hotfix(s)'] = (Get-HotFix).HotFixID -join ', '; $networkAdapters = Get-CimInstance Win32_NetworkAdapterConfiguration | Where-Object { $_.IPEnabled }; $networkCards = $networkAdapters | ForEach-Object { $_.Description }; $systemInfo['Network Card(s)'] = $networkCards -join ', '; [PSCustomObject]$systemInfo | Export-Csv -Encoding UTF8 -NoTypeInformation -Path '%destinationDirectory%\System Information.csv'"
        ExportFormat: csv

# Documentation
# https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/fsutil-usn
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
