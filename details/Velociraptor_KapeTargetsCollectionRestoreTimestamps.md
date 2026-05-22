# ⚙️ **Velociraptor Kape Targets Collection Restore Timestamps**
### `File Name: Velociraptor_KapeTargetsCollectionRestoreTimestamps.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Thomas DIOT (Qazeer)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Restore the files original timestamps from a Velociraptor KapeTargets offline collection.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Velociraptor Kape Targets Collection Restore Timestamps to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Velociraptor Kape Targets Collection Restore Timestamps logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Velociraptor Kape Targets Collection Restore Timestamps timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Restore the files original timestamps from a Velociraptor KapeTargets offline collection.
Category: Velociraptor
Author: Thomas DIOT (Qazeer)
Version: 1.0
Id: c244cc7c-76ef-49a0-aaba-f1e0a3e9c693
BinaryUrl: https://gist.github.com/Qazeer/0778877e871e3aea0c2926503df1bb81
ExportFormat: ""
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: ". '%kapeDirectory%\\Modules\\bin\\Restore-VelociraptorKapeTargetsCollectionTimestamps.ps1'; Restore-VelociraptorKapeTargetsCollectionTimestamps -TargetPath '%sourceDirectory%' -MetadataFile '%MetadataFile%'"
        ExportFormat: ""

# Documentation
# Velociraptor KapeTargets offline collection include a JSON file with the original timestamps ($SI MAC) of the collected files.
# The %MetadataFile% parameter must be set through KAPE to specify the file containing the timestamps from the Velociraptor collect.
# The file is usually named "Windows.KapeFiles.Targets%2FAll File Metadata.json" (from the Velociraptor offline collection output).
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
