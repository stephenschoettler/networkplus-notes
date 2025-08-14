## 💡 Rogue Device and Attacks (OBJ 4.2)

A **Rogue Device** is any unauthorized device or service connected to a corporate or private network that allows unauthorized individuals to connect to that network. Network devices are identified by MAC addresses and IP addresses. Digital certificates (IPSec, HTTPS) can be used to ensure only authorized devices connect.

✅ **Types of Rogue Devices/Systems**
- **1. Network Taps:** Physical devices attached to cabling to record packets. A rogue tap is controlled by an adversary.
- **2. Wireless Access Points (WAPs):**
  - **Rogue AP (connected to network):** An unauthorized AP connected to the physical network, allowing adversaries wireless access.
  - **Evil Twin AP (not connected to network):** An attacker sets up an AP mimicking a legitimate one (e.g., "Starbucks Wi-Fi") to trick users into connecting, allowing traffic capture.
- **3. Servers:** Adversaries may set up rogue servers (e.g., honeypots to harvest credentials, or servers used for ARP poisoning/name resolution corruption to divert traffic).
- **4. Wired/Wireless Clients:** Personal laptops, smartphones, etc., brought into the network without authorization. These devices are uncontrolled and can introduce malware or be used for unauthorized activities.
- **5. Software:** Unauthorized software installed on workstations (e.g., malicious DHCP/DNS servers, malware, covert spying software).
- **6. Virtual Machines (VMs):** Unauthorized VMs can be spun up to create rogue servers/services.
- **7. Smart Appliances (IoT):** Printers, webcams, VoIP handsets, VTC systems, washing machines, refrigerators, smart TVs. These are internet-connected and can be potential vulnerabilities if not managed.

✅ **Rogue Device Detection Mechanisms**
- **1. Visual Inspection:** Physically checking ports and switches for unauthorized devices.
- **2. Inventory/Audits:** Regular (monthly/quarterly) inventories to compare against a baseline of expected devices.
- **3. Network Mapping & Host Discovery:** Using enumeration scanners (e.g., Nmap) to identify hosts, services, and OS versions. Helps detect new/unauthorized devices.
- **4. Wireless Monitoring:** Scanning airwaves for unknown/unidentifiable SSIDs or APs (e.g., an "Evil Twin" AP).
- **5. Packet Sniffing & Traffic Flows:** Identifying unauthorized protocols or unusual peer-to-peer communication flows.
- **6. NAC (Network Access Control) & IDS (Intrusion Detection Systems):** Can prevent/detect unauthorized devices from accessing the network.