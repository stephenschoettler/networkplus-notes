## 💡 Log Aggregation with Syslog (OBJ 3.2)

Manually reviewing logs from thousands of network devices is impossible. Syslog (System Logging Protocol) is used to send logs from network devices (routers, switches, servers, clients) to a centralized server.

✅ **Syslog Components**
- **Client:** Device sending log information.
- **Server:** Centralized server receiving and storing logs (Syslog server, SIM, SEM, or SIEM).
- **Communication:** Logs are sent over UDP port 514.

✅ **Benefits of Centralized Logging**
- Easier analysis and review.
- Normalization and correlation of events to see trends.

✅ **Syslog Severity Levels (0-7)**
- **0 - Emergency:** System unstable.
- **1 - Alert:** Condition needs immediate correction.
- **2 - Critical:** Primary application failure, immediate attention.
- **3 - Error:** System not functioning properly.
- **4 - Warning:** Error will occur if action isn't taken soon.
- **5 - Notice:** Unusual but not error conditions.
- **6 - Informational:** Normal operational message.
- **7 - Debugging:** Information for developers.
- **Logging Decisions:** Administrators determine which levels to log and retention period.

✅ **Types of Network Device Logs**
- **1. Network Traffic Logs:**
  - **Content:** Information about traffic flows (source IP/port, destination IP/port, MAC, time, packet length, TTL).
  - **Use:** Analyze traffic patterns, identify abnormal spikes, detect unexpected protocols/ports.
  - **Key:** Understanding "normal" traffic (baseline) to identify "abnormal."
- **2. Audit Logs (Audit Trails):**
  - **Content:** Record of events and changes on a device (e.g., configuration changes, user logins).
  - **Use:** Determine who made changes and what changes were made.
- **3. Windows-Specific Logs (viewed in Event Viewer):**
  - **Application Log:** Software information.
  - **Security Log:** Security-related events (logins, audits).
  - **System Log:** Operating system information.