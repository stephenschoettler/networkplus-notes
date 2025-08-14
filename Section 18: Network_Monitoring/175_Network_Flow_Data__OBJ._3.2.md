## 💡 Network Flow Data (OBJ 3.2)

Network Flow Data's purpose is to monitor network traffic efficiently without capturing every single packet.

✅ **Full Packet Capture (FPC)**
- Captures entire packets (header + payload).
- **Pros:** Provides complete data for deep analysis.
- **Cons:** Generates massive amounts of data, requires significant storage, not practical for continuous monitoring in large networks.

✅ **Flow Analysis (e.g., NetFlow)**
- Relies on a "flow collector" to record metadata and statistics about network traffic, instead of the full packet content.
- **Pros:** Saves significant storage space, highlights trends and patterns, provides alerts for anomalies.
- **Cons:** Does not contain the actual data payload, so cannot inspect content.
- **Metadata includes:** Source/destination IP, source/destination port, protocol, interface, IP type of service.

✅ **Tools for Network Flow Data Analysis**
- **1. NetFlow:**
  - Cisco-developed protocol for reporting network flow information to a structured database.
  - Became a de facto standard (IPFIX - IP Flow Information Export).
  - Defines a "flow" as packets sharing the same characteristics (e.g., same source/destination IP).
- **2. Zeek (formerly Bro):**
  - A hybrid tool that passively monitors the network.
  - Logs full packet captures only for data of potential interest based on configured parameters/rules.
  - **Pros:** Reduces storage/processing requirements compared to FPC, provides full packet data for suspicious activity.
  - Performs data normalization (e.g., to tab-delimited or JSON) for easy import into other tools.
- **3. MRTG (Multi Router Traffic Grapher):**
  - Tool to create graphs showing network traffic flows through network interfaces on routers and switches.
  - Pulls data using SNMP.
  - **Use:** Visualize traffic patterns over time, identify spikes (e.g., unusual traffic between 2 AM and 4 AM) that might indicate offsite backups or malicious data exfiltration.

✅ **Importance of Baselines**
- Understanding "normal" traffic patterns (baselines) is crucial to identify "abnormal" behavior that requires investigation.
- Flow data helps establish and monitor these baselines.