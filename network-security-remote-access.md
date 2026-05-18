# 🌐 Boyles IT Solutions | Network Security & Remote Access Blueprint

## 📄 NET-2008: Secure Network Segmentation and Virtual Private Network (VPN) Standard
**Category:** Network Engineering & Information Security  
**Scope:** Corporate Office Networks, Virtual Private Clouds (VPC), and Remote Ingress  
**Last Updated:** May 2026  

---

### 1. Objective & Zero-Trust Network Philosophy
The corporate perimeter no longer exists. At **Boyles IT Solutions**, our network architecture is built around a **Zero-Trust** philosophy: *Never Trust, Always Verify*. This document outlines the mandatory configuration baselines for internal office network segmentation, firewall routing rules, and secure, encrypted remote access frameworks for our distributed workforce.

---

### 2. Office Network Segmentation (VLAN Matrix)
To contain potential malware infections or unauthorized device scanning, physical and wireless office networks are strictly partitioned into isolated Virtual Local Area Networks (VLANs). Traffic cannot cross boundaries without explicitly passing through our firewall inspection layers:

| VLAN ID | Network Name | Target Device Allocations | Access Security Controls |
| :--- | :--- | :--- | :--- |
| **VLAN 10** | `BITS-CORP` | Corporate-owned laptops/desktops enrolled in our MDM system. | Full access to internal staging repositories & local storage arrays. |
| **VLAN 20** | `BITS-GUEST` | Employee personal mobile devices, vendor laptops, and visitors. | Internet access only. Complete client isolation enabled (devices cannot see each other). |
| **VLAN 30** | `BITS-LAB` | Testing servers, local Linux Virtual Machines, and deployment sandboxes. | Completely air-gapped from production databases; restricted internet outbound hooks. |

---

### 3. Secure Remote Access (Enterprise VPN Framework)
Remote employees accessing internal production resources (such as staging environments or local administrative dashboards) must establish a secure cryptographic tunnel using our approved Enterprise VPN standard.

#### The WireGuard Encryption Standard
* **Protocol Baseline:** Our remote infrastructure utilizes tunnels built on the **WireGuard** protocol layer, optimizing speed, maintaining lean codebase footprints, and ensuring robust cryptographic handshake parameters.
* **MFA Integration:** VPN connectivity is explicitly tied to our central Identity Provider (IdP). Successful connection requires both a valid user certificate asset and a secondary time-based one-time password (TOTP) verification token.

#### Local DNS Leak Prevention
To maintain absolute split-tunnel integrity and prevent user tracking or data interception when working from public Wi-Fi access points:
1. **Enforced Handshakes:** The VPN client application locks local DNS resolution parameters to our secure corporate upstream handlers (`1.1.1.1` / `9.9.9.9` via encrypted DNS-over-HTTPS).
2. **Routing Integrity:** Local routing tables are continuously evaluated by the client service to block arbitrary side-channel leakage, ensuring that all corporate data packets travel strictly through the verified cryptographic path.
