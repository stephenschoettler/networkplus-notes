## 💡 Firewalls (OBJ 1.2)

Firewalls are network security devices that use a set of rules (ACLs) to permit or deny traffic, acting as a barrier to networks. They can be software-based or hardware-based, virtual or physical, host-based or network-based, and can perform Network Address Translation (NAT) or Port Address Translation (PAT).

✅ **Types of Firewalls (by operational principle)**
- **1. Packet-Filtering Firewall (Stateless Firewall):**
  - **Operation:** Inspects individual packets based on their header information (source/destination IP, source/destination port).
  - **Decision:** Permits or denies based solely on predefined rules in its ACL.
  - **Limitation:** Does not track the state of a connection.
- **2. Stateful Firewall:**
  - **Operation:** Inspects traffic as part of a session. Keeps track of active connections.
  - **Decision:** Allows return traffic for sessions initiated from the inside. Blocks unsolicited inbound traffic.
  - **Benefit:** Much more secure and effective than packet-filtering firewalls for two-way communication.
  - **Vulnerability:** Still susceptible to attacks where an internal user initiates a connection to a malicious external site (e.g., phishing attacks).
- **3. Next-Generation Firewall (NGFW):**
  - **Operation:** Operates at Layer 5, 6, and 7 of the OSI model (Application Layer). Performs Deep Packet Inspection (DPI) to analyze the actual content of packets.
  - **Capabilities:** Can filter based on applications, user identity, and advanced threats.
  - **Examples:** Web Application Firewalls (WAFs) are a type of NGFW specific to web servers.

✅ **Access Control Lists (ACLs) in Firewalls**
- **Definition:** Set of rules assigned to a firewall interface.
- **Criteria:** Can permit/deny traffic based on source/destination IP, source/destination port, source/destination MAC address, or protocol.
- **Reading an ACL:** You should be able to read and interpret basic ACL rules (e.g., `permit tcp any any eq 80`).

✅ **Unified Threat Management (UTM) Systems**
- **Definition:** A single device that combines multiple security functions (firewall, router, IDS/IPS, anti-malware, content filtering, etc.).
- **Deployment:** Typically a border device. Can be physical, virtual, or cloud-based.
- **Benefits:** Centralized management, simplified deployment, always-on/updated signatures with threat intelligence.
- **Additional Functions:** Can act as a Network Access Control (NAC) device for authentication/authorization of new devices.