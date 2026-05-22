# 🎯 **Open Sshclient**
### `File Name: OpenSSHClient.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Matt Dawson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
OpenSSH Client config, known hosts and keys

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Open Sshclient to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Open Sshclient events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Open Sshclient storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: OpenSSH Client config, known hosts and keys
Author: Matt Dawson
Version: 1.0
Id: 77f56ec6-61ae-450f-b90e-ac60352093ef
RecreateDirectories: true
Targets:
    -
        Name: OpenSSH Config File
        Category: Apps
        Path: C:\Users\%user%\.ssh\
        FileMask: 'config'
        Comment: "Config file can hold usernames, IP addresses and ports, key locations and configured shortcuts for servers e.g. ssh web-server"
    -
        Name: OpenSSH Known Hosts
        Category: Apps
        Path: C:\Users\%user%\.ssh\
        FileMask: 'known_hosts'
        Comment: "Known hosts file can hold a list of connected FQDNs/IP Addresses and ports if they are non-default, as well as public key fingerprints"
    -
        Name: OpenSSH Public Keys
        Category: Apps
        Path: C:\Users\%user%\.ssh\
        FileMask: '*.pub'
        Comment: "Gets all public keys (*.pub). It is more difficult to find private keys as they typically do not have a file extension. However, the .pub files should be able to help find the private keys as they are typically named the same."
    -
        Name: OpenSSH Default RSA Private Key
        Category: Apps
        Path: C:\Users\%user%\.ssh\
        FileMask: 'id_rsa'
        Comment: "Default name for an auto-generated SSH RSA private key"
    -
        Name: OpenSSH Default ECDSA Private Key
        Category: Apps
        Path: C:\Users\%user%\.ssh\
        FileMask: 'id_ecdsa'
        Comment: "Default name for an auto-generated SSH ECDSA private key"
    -
        Name: OpenSSH Default ECDSA-SK Private Key
        Category: Apps
        Path: C:\Users\%user%\.ssh\
        FileMask: 'id_ecdsa_sk'
        Comment: "Default name for an auto-generated SSH ECDSA private key using a Security Key"
    -
        Name: OpenSSH Default ED25519 Private Key
        Category: Apps
        Path: C:\Users\%user%\.ssh\
        FileMask: 'id_ed25519'
        Comment: "Default name for an auto-generated SSH ED25519 private key"
    -
        Name: OpenSSH Default ED25519-SK Private Key
        Category: Apps
        Path: C:\Users\%user%\.ssh\
        FileMask: 'id_ed25519_sk'
        Comment: "Default name for an auto-generated SSH ED25519 private key using a Security Key"
    -
        Name: OpenSSH Default DSA Private Key
        Category: Apps
        Path: C:\Users\%user%\.ssh\
        FileMask: 'id_dsa'
        Comment: "Default name for an auto-generated SSH DSA private key"

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
