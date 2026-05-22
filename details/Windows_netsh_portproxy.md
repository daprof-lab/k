# ⚙️ **Windows Netsh Portproxy**
### `File Name: Windows_netsh_portproxy.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andreas Hunkeler (@Karneades)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
PortProxy configuration

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Netsh Portproxy to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Netsh Portproxy logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Netsh Portproxy timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: PortProxy configuration
Category: LiveResponse
Author: Andreas Hunkeler (@Karneades)
Version: 1.0
Id: a7e6344e-2680-447f-223e-e79ad3aa0e65
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\netsh.exe
        CommandLine: interface portproxy show all
        ExportFormat: txt
        ExportFile: netsh_portproxy.txt

# Documentation
#   https://www.fireeye.com/blog/threat-research/2019/01/bypassing-network-restrictions-through-rdp-tunneling.html
#   https://adepts.of0x.cc/netsh-portproxy-code/
#   https://www.dfirnotes.net/portproxy_detection/
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
