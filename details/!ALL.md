# ⚙️ **ALL**
### `File Name: !ALL.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Run all modules

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run ALL to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw ALL logs to index file anomalies.
* **Incident Impact Assessment**: Leverage ALL timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Run all modules
Category: Default
Author: Eric Zimmerman
Version: 1
Id: 9f3cfd60-79a9-4dc6-82b5-e9220d885b38
ExportFormat: csv
FileMask: ""
Processors:
    -
        #Values starting with * need to be enclosed in single quotes because * denotes a reference in yaml
        Executable: '*.mkape'
        CommandLine: ""
        ExportFormat: ""
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
