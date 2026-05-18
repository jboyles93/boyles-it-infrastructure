# ☁️ Boyles IT Solutions | SaaS Governance & License Optimization

## 📄 FIN-2007: SaaS Vendor Management & Periodic License Auditing
**Category:** IT Finance & Application Governance  
**Scope:** All Corporate Software-as-a-Service (SaaS) Subscriptions & Seat Allocations  
**Last Updated:** May 2026  

---

### 1. Objective & Cost-Efficiency Philosophy
Software subscriptions represent one of the highest reoccurring operational expenditures at **Boyles IT Solutions**. This framework establishes systematic auditing protocols to eliminate "ghost licensing" (unassigned or underutilized active accounts), streamline vendor compliance, reduce financial waste, and ensure centralized IT oversight for all cloud-based software procurement.

---

### 2. The 30-Day Inactivity Reclamation Rule
To maximize corporate license utilization, the IT department enforces an automated and manual reclamation cycle based on active user engagement data pulled directly via API integrations:

* **The Threshold:** Any assigned enterprise license (e.g., Salesforce Admin, Jira Premium, Adobe Creative Cloud) showing **zero user login activity for 30 consecutive days** is automatically flagged for optimization.
* **The Notification Matrix:** The IT Customer Success Specialist or Service Coordinator sends an automated query to the user and their manager: *"Our identity monitoring indicates your Adobe account has been inactive for 30 days. To optimize resource allocation, this license will be unassigned in 48 hours. Your data configuration will remain saved, and a seat can be re-provisioned instantly via self-service if required."*
* **The Harvesting:** If no business justification is submitted within 48 hours, the license is unassigned and returned to the general enterprise pool, saving immediate seat-cost overages.

---

### 3. Core SaaS Vendor Audit Matrix
The Help Desk team coordinates a mandatory quarterly evaluation of core application suites to realign contract tiers with actual corporate headcounts:

| SaaS Application | Primary Authentication | Audit Frequency | Targeted Metric / Reclamation Trigger |
| :--- | :--- | :--- | :--- |
| 📧 **Google Workspace** | Core IdP | Monthly | Shared drive data leaks & suspended user account retention loops. |
| 🎫 **Jira Service Desk** | Google SAML Single Sign-On | Quarterly | Active agent seats vs. closed/resolved ticket density ratios. |
| 💼 **Salesforce CRM** | Secure SSO Portal | Bi-Monthly | Inactive profile permissions & unassigned pipeline tracking chairs. |
| 🎨 **Adobe Creative Cloud** | Federated Enterprise ID | Quarterly | Verification of active project-based usage metrics. |

---

### 4. Shadow IT Discovery Protocol
* **The Risk:** Employees bypassing IT to purchase unapproved cloud software using corporate expense cards, creating massive security and compliance data leaks.
* **The Remediation:** On a quarterly basis, the IT Coordinator works alongside Finance to audit corporate credit card expense logs against our approved identity provider catalog. Any unauthorized software vendors discovered are flagged, access loops are contained, and the data is formally migrated under centralized single sign-on (SSO) controls.
