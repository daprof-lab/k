# ⚙️ **Power Shell Parse Scheduled Tasks**
### `File Name: PowerShell_ParseScheduledTasks.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Vikas Singh(@vikas891)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Scheduled Task XMLs Parser

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Parse Scheduled Tasks to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Parse Scheduled Tasks logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Parse Scheduled Tasks timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Scheduled Task XMLs Parser
Category: LiveResponse
Author: Vikas Singh(@vikas891)
Version: 1.0
Id: ed6df81d-a90a-44ca-b322-1e02e72342dc
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command $ListOfTasks = $ListOfTasks = (Get-ChildItem -File -Path %sourceDirectory% -Recurse).fullname;$ListOfTasks | foreach { $ModifiedTime = (gci -Path $_).LastWriteTimeUtc.toString('yyyy-MM-ddTHH:mm:ss');$xmlFile = [xml](get-content "$_");$Date = $xmlFile.ChildNodes.RegistrationInfo.Date;$Author = $xmlFile.ChildNodes.RegistrationInfo.Author;$Description = $xmlFile.ChildNodes.RegistrationInfo.Description ;$URI = $xmlFile.ChildNodes.RegistrationInfo.URI;$Principals = $xmlFile.ChildNodes.Principals.Principal.UserId;$LogonType = $xmlFile.ChildNodes.Principals.Principal.LogonType;$Enabled = $xmlFile.ChildNodes.Settings.Enabled;$Action = $xmlFile.ChildNodes.Actions.Exec.Command;$Arguments = $xmlFile.ChildNodes.Actions.Exec.Arguments;$ComHandler_ClassID = $xmlFile.ChildNodes.Actions.ComHandler.ClassId; $ComHandler_Data = [string]$xmlFile.ChildNodes.Actions.ComHandler.Data.'#cdata-section';$xmlFile.ChildNodes[1] |ForEach-Object { [PSCustomObject]@{TaskFile_LastModifiedTime = $ModifiedTime;Registration_Date = $Date;Author = $Author ;  Description = $Description ; Task_Name = $URI ;  Principals_UserContext = $Principals;  LogonType = $LogonType  ; Enabled = $Enabled   ; Action_Arguments = $Action + ' ' + $Arguments;ComHandler_ClassID = $ComHandler_ClassID; ComHandler_Data = $ComHandler_Data; } } } 2> $NULL | Export-Csv -Path %destinationDirectory%\Parsed_Tasks_XML.csv -NoTypeInformation
        ExportFormat: csv

# Documentation
# Module Source: DIR containing the Scheduled Tasks XML files
# For e.g. for a triage image mounted as E Drive, E:\C:\Windows\system32\Tasks
# More information below:
# https://vikas-singh.notion.site/Parse-Scheduled-Tasks-XMLs-36ec152e7d2a4d269bba6c9565c3b5cd
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
