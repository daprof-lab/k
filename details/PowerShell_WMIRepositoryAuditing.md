# ⚙️ **Power Shell Wmirepository Auditing**
### `File Name: PowerShell_WMIRepositoryAuditing.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andreas Hunkeler (@Karneades)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Collect WMI repository information

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Wmirepository Auditing to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Wmirepository Auditing logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Wmirepository Auditing timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Collect WMI repository information
Category: LiveResponse
Author: Andreas Hunkeler (@Karneades)
Version: 1.0
Id: cebffd14-901a-44fd-9960-e3a781acc1d9
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "write 'Event Filter'; write ' '; Get-WMIObject -Namespace root\Subscription -Class __EventFilter; write ' '; write 'EventConsumer'; write ' '; Get-WMIObject -Namespace root\Subscription -Class __EventConsumer; write ' '; write 'FilterToConsumerBinding'; write ' '; Get-WMIObject -Namespace root\Subscription -Class __FilterToConsumerBinding"
        ExportFormat: txt
        ExportFile: wmi-repository-auditing.txt

# Documentation
# https://www.sans.org/blog/investigating-wmi-attacks/
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
