# 🎯 **Developer Cloud Credentials**
### `File Name: DeveloperCloudCredentials.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Aashiq Ahmed  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Collect common developer and cloud credential artifacts useful during incident response

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Developer Cloud Credentials to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Developer Cloud Credentials events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Developer Cloud Credentials storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Collect common developer and cloud credential artifacts useful during incident response
Author: Aashiq Ahmed
Version: 1.0
Id: 9f1fd9c2-6c9b-4c0e-9e6b-1e0d5a9d7a21
RecreateDirectories: true

Targets:
  -
    Name: AWS CLI Credentials
    Category: Credentials
    Path: C:\Users\%user%\.aws\
    FileMask: 'credentials'
    Comment: "Collects AWS CLI credential file"

  -
    Name: AWS CLI Config
    Category: Credentials
    Path: C:\Users\%user%\.aws\
    FileMask: 'config'
    Comment: "Collects AWS CLI config file"

  -
    Name: Kubernetes Config
    Category: Credentials
    Path: C:\Users\%user%\.kube\
    FileMask: 'config'
    Comment: "Collects Kubernetes client config"

  -
    Name: Docker Config
    Category: Credentials
    Path: C:\Users\%user%\.docker\
    FileMask: 'config.json'
    Comment: "Collects Docker client configuration"

  -
    Name: Git Credentials
    Category: Credentials
    Path: C:\Users\%user%\
    FileMask: '.git-credentials'
    Comment: "Collects Git stored credentials"

  -
    Name: Git Config
    Category: Credentials
    Path: C:\Users\%user%\
    FileMask: '.gitconfig'
    Comment: "Collects Git user configuration"

  -
    Name: SSH Config
    Category: Credentials
    Path: C:\Users\%user%\.ssh\
    FileMask: 'config'
    Comment: "Collects SSH client configuration"

  -
    Name: SSH Known Hosts
    Category: Credentials
    Path: C:\Users\%user%\.ssh\
    FileMask: 'known_hosts'
    Comment: "Collects SSH known_hosts file"

  -
    Name: npm User Config
    Category: Credentials
    Path: C:\Users\%user%\
    FileMask: '.npmrc'
    Comment: "Collects npm user configuration"

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
