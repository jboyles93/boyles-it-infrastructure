# 🔐 Boyles IT Solutions | Identity & Access Governance Policy

## 📄 SEC-2004: Identity Access Management (IAM) & RBAC Standard
**Category:** Information Security & Compliance  
**Scope:** Identity Provider (IdP) & Google Workspace Administration  
**Last Updated:** May 2026  

---

### 1. Objective & Core Philosophy
This policy establishes the mandatory access control frameworks for all identity profiles, service accounts, and authentication vectors managed by **Boyles IT Solutions**. Every user account provisioned must strictly adhere to the **Principle of Least Privilege (PoLP)**—ensuring employees are granted only the minimum necessary system permissions required to fulfill their specific organizational role.

---

### 2. Role-Based Access Control (RBAC) Matrix
To prevent "privilege creep" and ensure consistent security boundaries, account permissions are mapped strictly to core organizational roles via Google Workspace Organizational Units (OUs):

| Organizational Unit (OU) | Default Access Control Levels | Mandatory Security Controls |
| :--- | :--- | :--- |
| **`BITS / Corporate / HR`** | Read/Write to HR Information Systems (HRIS), BambooHR, restricted Google Drive payroll folders. | Phishing-Resistant MFA, Session Timeout (12 Hours) |
| **`BITS / Support / HelpDesk`** | Tier 1 admin privileges in SnipeIT, Google Workspace basic user reset tools, Jira Service Desk queue. | Push-Notification MFA, Session Timeout (8 Hours) |
| **`BITS / Operations / Success`** | CRM Admin (Salesforce/HubSpot), customer communication logs, product analytics dashboards. | Standard MFA, Session Timeout (24 Hours) |
| **`BITS / Infrastructure / Core`** | Root/Global Admin layers, break-glass cloud console access, network architecture controllers. | Hardware Security Key (FIDO2), Session Timeout (1 Hour) |

---

### 3. Password Complexity & Multi-Factor Authentication (MFA)
* **MFA Enrolment:** Multi-Factor Authentication is non-negotiable and must be enforced at the organizational unit level. New hires are granted a 24-hour grace window upon first login using a temporary backup code to configure their primary authenticator app.
* **Password Expiry Myth:** In alignment with modern NIST SP 800-63B guidelines, routine periodic password changes are **not enforced** unless a specific breach or compromise vector is suspected. Instead, focus is placed on a 14-character minimum length and automated dark-web leak monitoring via our identity manager.
