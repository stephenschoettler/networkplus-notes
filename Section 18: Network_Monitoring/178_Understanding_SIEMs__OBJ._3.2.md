## 💡 Understanding SIEMs (OBJ 3.2)

SIEM (Security Information and Event Management) is a system that collects, aggregates, and analyzes security information and event data from various sources across a network. Its purpose is centralized monitoring, threat detection, incident response, and compliance reporting. An example tool is Security Onion (a Linux distribution for threat hunting, enterprise security monitoring, and log management) which includes tools like Elastic Stack (Elasticsearch, Logstash, Kibana) and Bro (now Zeek).

✅ **Data Collection Methods for SIEMs**
- **1. Network Taps / Port Mirroring:**
  - Captures network traffic directly from a switch port (e.g., using `tcpdump` on a sensor).
  - Provides raw packet data for analysis.
- **2. Agents (e.g., Beats for Elastic Stack):**
  - Software installed directly on hosts (servers, workstations) to collect specific logs (e.g., Windows event logs: application, system, security).
  - Configured to forward logs to the SIEM (e.g., `winlogbeat.yml` configured to send to SIEM IP:Port 5044).
  - YAML files are whitespace-sensitive.
- **3. Syslog:**
  - A standard protocol for sending log messages from devices (e.g., routers, firewalls, Linux servers) to a centralized logging server (SIEM).
  - Used for devices that cannot install agents.
  - Typically uses UDP port 514.

✅ **Data Analysis and Visualization (using Kibana)**
- Kibana: A visualization tool (part of Elastic Stack) used to create dashboards, graphs, and tables from aggregated SIEM data.
- **Features:**
  - View network connections, NIDS (Network Intrusion Detection System) alerts (e.g., from Bro/Zeek).
  - Search and filter log data using queries (e.g., `agent.name:PC* AND alert_level:>=5`).
  - Create index patterns to organize and search specific log types (e.g., `logstash-ossec-*`, `logstash-syslog-*`).
  - Allows for "Host Hunting" (analyzing host-specific logs) and "Network Hunting" (analyzing network traffic).

✅ **Benefits of SIEMs**
- Aggregates data from disparate sources into one place for holistic view.
- Enables pattern recognition and anomaly detection across the entire network.
- Crucial for incident detection, threat hunting, and compliance.
- Helps identify malicious activity and unauthorized devices.

✅ **Deployment Options**
- SIEMs can be deployed as software on a server, a hardware appliance, or an outsourced managed service.