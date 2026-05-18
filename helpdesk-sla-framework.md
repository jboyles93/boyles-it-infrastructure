# 🛠️ Boyles IT Solutions | Help Desk Workflow & SLA Framework

## 📄 OPS-2003: Incident Management and Service Level Agreements
**Category:** IT Service Management (ITSM)  
**Scope:** Help Desk Operations & Ticket Lifecycle  
**Last Updated:** May 2026  

---

### 1. Objective & Philosophy
At **Boyles IT Solutions**, our technical support pipeline is engineered around a user-first, metric-driven philosophy. This framework defines our active ticket queues, triage methodologies, and mandatory **Service Level Agreements (SLA)**. By establishing strict response and resolution thresholds, we ensure high organizational uptime, clear communication, and consistent **Customer Success** delivery.

---

### 2. Ticket Severity & SLA Matrix
All incoming requests filed via the Boyles IT Service Desk or emailed to support are automatically triaged into one of four distinct severity tiers based on business impact:

| Severity Level | Business Impact Criteria | Target Response | Target Resolution | Escalation Path |
| :--- | :--- | :--- | :--- | :--- |
| 🚨 **P1 - Critical** | **System Down:** Core infrastructure failure affecting all users (e.g., central network outage, email server offline). | **< 15 Mins** | **< 2 Hours** | Lead Systems Admin & Director |
| ⚠️ **P2 - High** | **Work Blocked:** Individual user completely stopped from working (e.g., active account lockouts, complete hardware failure). | **< 1 Hour** | **< 4 Hours** | Tier 2 IT Technician |
| 🔵 **P3 - Medium** | **Degraded Performance:** User can work, but system functionality is limited (e.g., intermittent VPN drops, local software errors). | **< 4 Hours** | **< 24 Hours** | Help Desk Queue |
| 🟢 **P4 - Low** | **General Inquiry / Request:** Scheduled tasks or informational queries (e.g., onboarding requests, hardware provisioning, general questions). | **< 8 Hours** | **< 3 Days** | Service Coordinator |

---

### 3. Step-by-Step Ticket Lifecycle Workflow

**The Support Pipeline:** `[New Ticket]` ➡️ `[Triage & Tagging]` ➡️ `[Active Troubleshooting]` ➡️ `[Resolution & Sign-off]`

#### Phase 1: Intake & Automated Triage
1. **The Entry Point:** Tickets enter the queue via user portal submission or via an incoming email to `support@boylesitsolutions.com`.
2. **First-Contact Triage:** The Service Coordinator reviews the queue every 30 minutes to verify correct categorization, assign the appropriate severity tier (P1-P4), and tag the ticket (e.g., `#networks`, `#identity`, `#hardware`).

#### Phase 2: Active Escalation Routing
* **Tier 1 Resolution:** The IT Technician claims the ticket from the queue, leaves an initial internal note, and updates the user status to *In Progress*.
* **The Escalation Trigger:** If a P2 or P3 ticket requires senior infrastructure access layers or physical network engineering changes, the technician must document all troubleshooting steps completed so far, tag the Tier 2 engineering group, and formally hand off the ticket within the system.

#### Phase 3: Resolution & Empathetic Sign-off
A ticket is never closed silently. To guarantee customer satisfaction:
1. **User Validation:** The technician must send a closing message verifying the fix. *Example text:* "We have successfully synchronized your account access tokens. Please log back in and reply to this message if you experience any further loading loops."
2. **The 24-Hour Solved Rule:** The ticket status is moved to **Pending Closure**. If the user does not reply or flag a lingering issue within 24 hours, the system automatically transitions the ticket to **Closed**.
