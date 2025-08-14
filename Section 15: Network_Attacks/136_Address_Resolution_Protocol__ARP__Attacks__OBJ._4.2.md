## 💡 Address Resolution Protocol (ARP) Attacks (OBJ 4.2)

ARP's purpose is to map an IP address to a MAC address on a local area network (LAN). However, ARP is an old protocol with little built-in security, making it vulnerable to various attacks.

✅ **Types of ARP Attacks**
- **1. ARP Spoofing:**
  - **Mechanism:** Attacker sends falsified ARP messages to link their MAC address with the IP address of a legitimate computer or server on the network.
  - **Goal:** To make the attacker's MAC address associated with a legitimate IP, allowing the attacker to receive data meant for that IP.
  - **Impact:** Can be used to initiate an on-path (Man-in-the-Middle) attack.
- **2. ARP Poisoning:**
  - **Mechanism:** A broader form of attack that corrupts the ARP cache (ARP table) in the network. Involves sending malicious ARP packets to a default gateway on a LAN to associate the attacker's MAC address with the IP addresses of multiple LAN devices.
  - **Goal:** To alter network traffic flow on a larger scale.
  - **Impact:** Data interception, session hijacking, Denial of Service (DoS) attacks on the LAN.
  - **Key Difference:** Spoofing is more targeted (single host traffic replacement), while poisoning is larger scale (affecting most/all hosts on a LAN).

✅ **Impacts of ARP Attacks**
- **Data Interception:** Attacker's MAC becomes associated with a legitimate IP, allowing them to intercept data.
- **On-Path Attacks:** ARP spoofing/poisoning is often a precursor to Man-in-the-Middle attacks.
- **Network Disruptions/DoS:** Can lead to significant network disruptions and DoS conditions on the LAN.

✅ **Detection of ARP Attacks**
- **ARP Monitoring Tools:** Monitor ARP address mappings and alert on unusual ARP traffic patterns.
- **Intrusion Detection Systems (IDS):** Can detect anomalies and traffic patterns indicative of ARP spoofing/poisoning.

✅ **Mitigation Strategies**
- **1. Static ARP Entries:** Manually configure static ARP entries on devices. (Impractical for large/dynamic networks).
- **2. Dynamic ARP Inspection (DAI):** A feature on modern switches that inspects ARP packets and drops untrusted ones.
- **3. Network Segmentation (VLANs):** Limits the scope of an ARP attack.
- **4. VPNs and Encryption Technologies:** Encrypts data in transit, preventing reading/modification even if ARP spoofing is successful.