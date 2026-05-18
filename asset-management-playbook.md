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
