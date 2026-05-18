# 🖥️ Boyles IT Solutions | Asset Management & Lifecycle Playbook

## 📄 POL-2001: IT Asset Governance and Procurement Standard
**Category:** Infrastructure & Operations  
**Scope:** Internal IT Asset Management (SnipeIT Deployment)  
**Last Updated:** May 2026  

---

### 1. Executive Summary & Objective
This policy defines the mandatory lifecycle management pipeline for all physical hardware, software licensing, and virtual assets owned by **Boyles IT Solutions**. By enforcing strict hardware-to-user parity tracking via our centralized SnipeIT instance, the IT operations team ensures 100% inventory accuracy, minimizes hardware shrinkage, and accelerates employee onboarding/offboarding workflows.

---

### 2. Asset Taxonomy & Labeling Matrix
Every physical asset introduced to the network must be physically tagged with a unique, scannable barcode tag and cataloged within SnipeIT using the following standardized taxonomy:

| Asset Category | SnipeIT Status Label | Deprecation Schedule | Naming Convention Example |
| :--- | :--- | :--- | :--- |
| **Laptops / Workstations** | Deployable | 36 Months (Linear) | `BITS-LAP-2026-01` |
| **Enterprise Monitors** | Deployable | 60 Months (Linear) | `BITS-MON-2026-01` |
| **Network Switches/Routers** | Deployable | 48 Months (Linear) | `BITS-NET-2026-01` |
| **Software Licenses (SaaS)** | Subscribed | Annual Renewal | `BITS-LIC-SAAS-01` |

---

### 3. Step-by-Step Asset Provisioning Workflow

#### Phase 1: Receiving and Tagging
1. **Unboxing & Inspection:** Upon physical receipt of hardware, verify the serial number against the procurement invoice.
2. **Asset Tag Application:** Affix a physical tamper-evident asset tag sticker to a visible, non-heat-producing surface on the chassis.
3. **SnipeIT Database Entry:** Log into the Boyles IT SnipeIT instance and select **Create Asset**. 
   * Input the **Asset Tag ID**, **Serial Number**, **Model**, and change the status to **Ready to Deploy**.

---

### 4. User Assignment & Audit Trails (The Active Lifecycle)
When an asset is assigned to an employee (e.g., during onboarding), a formal "Check-Out" handshake must be completed inside SnipeIT.

* **Digital Sign-off:** The employee must log into their workspace portal and explicitly click "Accept" on their hardware inventory dashboard. This generates an electronic receipt signature attached to the asset's history log.
* **Bi-Annual Physical Audits:** Every 6 months, the IT Technician will trigger an inventory verification request via SnipeIT. Users must confirm they are still in physical possession of their assigned asset tag numbers to maintain regulatory compliance.
  
---

### 5. Employee Offboarding & Hardware Reclamation Workflow
When an employee transitions out of Boyles IT Solutions, the IT Service Coordinator coordinates a zero-downtime asset reclamation pipeline.

#### Phase 1: Identity & SaaS Access Revocation
1. **Trigger Event:** HR logs a high-priority termination/departure ticket in the help desk queue.
2. **Session Termination:** Within 15 minutes of the employee's official departure time, the IT Technician uses the Google Workspace Admin console to **Revoke Active Sign-In Sessions**.
3. **Password Rotation:** Trigger a forced administrative password reset and suspend the user account. *Do not delete the account immediately to preserve data inheritance.*
4. **SaaS De-provisioning:** Release software assignments inside SnipeIT (e.g., Jira, Zoom, Adobe licenses) to instantly free up available seats for future hires, saving licensing costs.

#### Phase 2: Physical Hardware Reclamation
1. **The Shipping Protocol:** For remote workers, the IT Customer Success team ships a pre-paid, insured hardware recovery box containing custom foam inserts to the employee’s address.
2. **Check-In Log:** Upon receiving the physical assets back at the IT Depot, inspect the laptop and monitor for physical damage.
3. **SnipeIT Database Update:** Open SnipeIT, select the asset tags, and click **Check-In**. Change the status label from *Deployed* to **Pending Maintenance / Lifecycle Evaluation**.

---

### 6. E-Waste, Deprecation, and Secure Disposal
When a laptop hits its **36-month deprecation limit** or suffers terminal hardware failure, it enters the final decommissioning stage.

1. **Cryptographic Erasure (Sanitization):** The IT Technician boots the machine into a secure environment and runs a full cryptographic wipe (e.g., DBAN or NVMe Secure Erase) to ensure no proprietary corporate data or user data remains on the storage controllers.
2. **Remove Physical Branding:** Peel off all internal asset tags, company stickers, and corporate inventory labels.
3. **Certified E-Waste Disposal:** Hand off the sanitized hardware to a certified R2-compliant electronic recycling vendor. Obtain a **Certificate of Destruction** and upload it as an attachment to the specific asset's archive profile inside SnipeIT.
4. **Final Archive:** Mark the asset status in SnipeIT as **Decommissioned/Destroyed** to permanently close out its lifecycle trail.
