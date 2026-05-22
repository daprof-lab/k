# ⚙️ **Crowd Strike Crowd Response**
### `File Name: CrowdStrike_CrowdResponse.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Mohamed El-Hadidi, Georg Lauenstein  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
CrowdResponse is a lightweight Windows console application designed to aid in the gathering of system information for incident response and security engagements

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Crowd Strike Crowd Response to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Crowd Strike Crowd Response logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Crowd Strike Crowd Response timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: CrowdResponse is a lightweight Windows console application designed to aid in the gathering of system information for incident response and security engagements
Category: LiveResponse
Author: Mohamed El-Hadidi, Georg Lauenstein
Version: 1.0
Id: e137a1ed-5bfd-4ca3-9df1-c1d35624cbb2
BinaryUrl: https://www.crowdstrike.com/wp-content/uploads/2020/03/CrowdResponse.zip
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "& '%kapedirectory%\Modules\bin\CrowdResponse\CrowdResponse.exe' -i %kapedirectory%\Modules\bin\CrowdResponse\config.txt -o %destinationDirectory%\CrowdResponse.xml;&'%kapedirectory%\Modules\bin\CrowdResponse\CRConvert.exe' -v -c -f %destinationDirectory%\CrowdResponse.xml -o %destinationDirectory%;Remove-Item '%destinationDirectory%\CrowdResponse.xml'"
        ExportFormat: csv

# Documentation
# https://www.crowdstrike.com/resources/community-tools/crowdresponse/
# Create a folder "CrowdResponse" within the "Modules\bin" KAPE folder
# Place the "CrowdResponse.zip" archive into "Modules\bin\CrowdResponse" and extract.
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
