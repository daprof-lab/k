# 🎯 **Vpnclients**
### `File Name: VPNClients.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Evangelos Dragonas - Paul CABON CERT Almond  
**Version:** 2.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
VPN Clients

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Vpnclients to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Vpnclients events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Vpnclients storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: VPN Clients
Author: Evangelos Dragonas - Paul CABON CERT Almond
Version: 2.0
Id: 75244f93-1df6-4db7-a4be-e20481f38ff1
RecreateDirectories: true
Targets:
    -
        Name: Proton VPN
        Category: VPN
        Path: ProtonVPN.tkape
    -
        Name: OpenVPN
        Category: VPN
        Path: OpenVPNClient.tkape
    -
        Name: Palo Alto GlobalProtect VPN
        Category: VPN
        Path: PaloAlto.tkape
    -
        Name: Forti Client VPN
        Category: VPN
        Path: FortiClientVPN.tkape
    -
        Name: Ivanti Pulse Secure
        Category: VPN
        Path: PulseSecure.tkape

# Documentation
# To do: Add more targets for both enterprise (Cisco AnyConnect, Fortinet, etc.) and consumer VPN providers (NordVPN, ExpressVPN, etc.).
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
