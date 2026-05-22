# 🎯 **Open Sshserver**
### `File Name: OpenSSHServer.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Matt Dawson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
OpenSSH Server Config and Logs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Open Sshserver to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Open Sshserver events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Open Sshserver storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: OpenSSH Server Config and Logs
Author: Matt Dawson
Version: 1.0
Id: 6c290fef-f9be-43af-a987-44709d8f7921
RecreateDirectories: true
Targets:
    -
        Name: OpenSSH Server Config File
        Category: Apps
        Path: C:\ProgramData\ssh\
        FileMask: 'sshd_config'
        Comment: "Config file can hold information on allowed/denied users"
    -
        Name: OpenSSH Server Logs
        Category: Apps
        Path: C:\ProgramData\ssh\logs\
        FileMask: '*'
        Comment: "OpenSSH server logs"
    -
        Name: OpenSSH Host ECDSA Key
        Category: Apps
        Path: C:\ProgramData\ssh\
        FileMask: 'ssh_host_ecdsa_key'
        Comment: "Retrieves the host ECDSA key"
    -
        Name: OpenSSH Host ED25519 Key
        Category: Apps
        Path: C:\ProgramData\ssh\
        FileMask: 'ssh_host_ed25519_key'
        Comment: "Retrieves the host ED25519 key"
    -
        Name: OpenSSH Host DSA Key
        Category: Apps
        Path: C:\ProgramData\ssh\
        FileMask: 'ssh_host_dsa_key'
        Comment: "Retrieves the host DSA key"
    -
        Name: OpenSSH Host RSA Key
        Category: Apps
        Path: C:\ProgramData\ssh\
        FileMask: 'ssh_host_rsa_key'
        Comment: "Retrieves the host RSA key"
    -
        Name: OpenSSH User Authorized Keys
        Category: Apps
        Path: C:\Users\%user%\.ssh\
        FileMask: 'authorized_keys'
        Comment: "Retrieves the user's authorised public keys"
    -
        Name: OpenSSH User Authorized Keys 2
        Category: Apps
        Path: C:\Users\%user%\.ssh\
        FileMask: 'authorized_keys2'
        Comment: "Retrieves the user's authorised public keys from the second file"
    -
        Name: OpenSSH Authorized Administrator Keys
        Category: Apps
        Path: C:\ProgramData\ssh\
        FileMask: 'administrators_authorized_keys'
        Comment: "Retrieves the administrator group's authorised public keys"

# Documentation
# https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_server_configuration
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
