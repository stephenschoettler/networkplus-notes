## 💡 MAC Flooding (OBJ 4.2)

MAC Flooding is a network attack technique that attempts to compromise the security of a network switch by overflowing its MAC address table (also known as CAM table).

✅ **Normal Switch Operation**
- A switch uses its MAC table to associate each switch port with the MAC address of the connected device, ensuring efficient data forwarding to the correct recipient.

✅ **Mechanism**
- An attacker inundates the switch with fake MAC addresses until the MAC address table fills up.

✅ **Impact**
- Once the MAC table is full, the switch enters a "fail-safe" mode and starts acting like a hub, broadcasting packets to all switch ports instead of only the destination. This compromises network security and efficiency.

✅ **Reasons for MAC Flooding Attacks**
- **1. Data Snooping:** By forcing the switch to broadcast traffic, an attacker can snoop (capture) sensitive data from the network by placing their network card in promiscuous mode. This breaches confidentiality.
- **2. Disruption of Services:** Overwhelming the network with unnecessary traffic can degrade performance and cause a Denial of Service (DoS) attack.
- **3. Bypassing Security Measures:** Can bypass MAC address filtering (MAC-based access control) on switches or wireless access points, allowing unauthorized devices to connect.

✅ **How MAC Flooding is Performed**
- Attackers use specialized tools to generate numerous random MAC addresses and rapidly send frames with these fake addresses to the switch.

✅ **Detection of MAC Flooding**
- **Anomaly-Based IDS:** Intrusion Detection Systems configured for anomaly detection can identify unusual increases in MAC address entries or spikes in broadcast traffic.
- **Network Monitoring Tools:** Alert administrators about unusual traffic patterns or sudden changes in network metrics.

✅ **Mitigation Strategies**
- **1. Port Security:** Configure switches to limit the number of MAC addresses allowed on a single port.
- **2. Limit MAC Addresses per Port:** Set a specific limit on the number of MAC addresses a switch port can learn.
- **3. VLANs (Network Segmentation):** Implement VLANs to divide the network into smaller segments, limiting the impact of an attack.
- **4. Implement 802.1X:** For stronger authentication and control over devices connecting to the network.