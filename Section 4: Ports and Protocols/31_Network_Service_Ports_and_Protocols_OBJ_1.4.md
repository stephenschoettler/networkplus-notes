## 💡 Network Service Ports and Protocols (OBJ 1.4)

This section covers various network service ports and protocols. Understand the purpose of each service and its associated port numbers. Note that DNS uses both TCP and UDP, and Syslog can use either depending on reliability needs.

✅ **DNS (Domain Name System)**
- **Purpose:** Translates human-friendly domain names (e.g., www.example.com) into IP addresses.
- **Port:** 53 (UDP for queries/responses, TCP for larger messages like zone transfers).
- Acts like the "internet's phone book."

✅ **DHCP (Dynamic Host Configuration Protocol)**
- **Purpose:** Automates the assignment of IP addresses, subnet masks, gateways, and other network parameters to client devices.
- **Ports:**
  - 67 (UDP): DHCP servers listen for client requests.
  - 68 (UDP): DHCP clients receive responses.

✅ **SQL Services (Structured Query Language)**
- **Purpose:** Protocols used by database servers to manage, query, and control operations from client applications.
- **Common Ports (not a single standard):**
  - Microsoft SQL Server: 1433 (TCP).
  - MySQL: 3306 (TCP).

✅ **SNMP (Simple Network Management Protocol)**
- **Purpose:** Collects information from and configures network devices (servers, printers, hubs, switches, routers) over an IP network.
- **Ports:**
  - 161 (UDP): SNMP managers communicate with SNMP agents (polling).
  - 162 (UDP): Agents send unsolicited trap messages (reporting information).
- Crucial for network diagnostics and performance monitoring.

✅ **Syslog (System Logging Protocol)**
- **Purpose:** Standard for message logging, allowing devices to send event messages to a central syslog server.
- **Port:** 514 (UDP by default, TCP for reliability).
- Syslog servers store, process, or forward logs.