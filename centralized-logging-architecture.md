# 📊 Boyles IT Solutions | Centralized Logging & Auditing

## 📄 OPS-2009: Open-Source Log Aggregation and Endpoint Monitoring
**Category:** Systems Administration & Security Monitoring  
**Scope:** Automated Infrastructure Telemetry  
**Last Updated:** May 2026  

---

### 1. Objective & Visibility Philosophy
You cannot secure what you cannot see. At **Boyles IT Solutions**, we utilize open-source log aggregation tools to collect local security states, system anomalies, and network telemetry. This documentation details our centralized logging pipeline which acts as our early detection mechanism for internal operational failures and brute-force authentication attempts.

---

### 2. The Telemetry Collection Flow
Our deployment framework uses a lightweight shipping agent to monitor system activities and route logs securely to our parsing layers. 

> **The Pipeline Matrix:** > `[System Endpoint]` ➡️ `[Filebeat Agent]` ➡️ `[Encrypted TLS Tunnel]` ➡️ `[Logstash Central Parser]` ➡️ `[Elastic Security Dashboard]`

* **`/var/log/auth.log`**: Monitored strictly to catch failed SSH attempts, privilege escalations (`sudo` executions), and unauthorized user accounts creation.
* **`/var/log/syslog`**: Evaluated to track local hardware events, daemon errors, or sudden driver crashes across infrastructure deployments.

---

### 3. Automated Configuration Deployment
To eliminate human error during asset tracking installations, we deploy our log monitoring configuration using our customized bash script pipeline: `deploy-log-monitor.sh`. 

This shell script enforces target root security constraints, injects the necessary cryptographic authentication signature keys, generates the deployment configuration dynamically, and binds the shipping routine directly into systemd initialization registers to guarantee data continuity across system reboots.
