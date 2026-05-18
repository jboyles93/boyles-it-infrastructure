# 💻 Boyles IT Solutions | Endpoint Management & MDM Policy

## 📄 SEC-2006: Mobile Device Management (MDM) & Compliance Standard
**Category:** Device Security & Endpoint Governance  
**Scope:** All Corporate-Owned Laptops, Desktops, and Mobile Handsets  
**Last Updated:** May 2026  

---

### 1. Objective & Automation Philosophy
To protect the corporate network and safeguard sensitive client resources, all endpoint hardware issued by **Boyles IT Solutions** must be enrolled in our centralized **Mobile Device Management (MDM)** architecture prior to deployment. This framework ensures automated configuration enforcement, continuous security patching, and rapid remote remediation capabilities.

---

### 2. MDM Baseline Security Profiles
The moment a device connects to the internet on Day 1, the MDM agent automatically deploys and locks down a mandatory corporate baseline configuration profile:

| Operating System | MDM Platform | Mandatory Hardware Controls | Update & Patching Windows |
| :--- | :--- | :--- | :--- |
| 🍏 **macOS** | Kandji / Jamf Pro | FileVault 2 Encryption, Local Firewall Enabled, Password Manager Forced. | Security Patches: **Within 48 Hours** Major Upgrades: Deferred 30 Days |
| 🪟 **Windows 11** | Microsoft Intune | BitLocker (XTS-AES-256), Windows Defender Active, USB Storage Restricted. | Quality Patches: **Weekly (Fridays)** Feature Updates: Deferred 60 Days |
| 🐧 **Linux Desktop** | Custom Configuration | Full Disk Encryption (LUKS), SSH Root Login Disabled, AppArmor Enforced. | Security Repositories: **Automated Daily Sync** |

---

### 3. Remote Wipe & Incident Remediation Protocol
In the event that a corporate asset is reported lost, stolen, or unrecovered following an employee offboarding window, IT Operations executes an immediate remote remediation protocol:

1. **The Remote Kill-Switch:** From the centralized MDM console, the IT Technician issues a cryptographic **Remote Wipe** command targeting the missing serial number.
2. **The Execution Mechanism:** The moment the device powers on and connects to any cellular or Wi-Fi network, the MDM agent receives the command and immediately triggers a destructive local factory reset, destroying the disk encryption keys and making data recovery impossible.
3. **Audit Log Retention:** The technician logs the successful wipe confirmation token into the asset's history folder within SnipeIT for internal auditing and insurance validation.
