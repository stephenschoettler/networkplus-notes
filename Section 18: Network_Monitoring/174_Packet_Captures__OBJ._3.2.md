## 💡 Packet Captures (OBJ 3.2)

Packet Captures aim to capture all data going to or from a network device or across a network segment (e.g., using a SPAN port).

✅ **Common Fields in a Packet Capture**
- **Number:** Packet number in the capture sequence.
- **Time:** Elapsed time since the capture started (important for correlation with other logs).
- **Source:** Source IP address.
- **Destination:** Destination IP address.
- **Protocol:** (e.g., TCP, UDP, ARP, ICMP).
- **Length:** Size of the packet in bytes.
- **Info:** Header information, including flags (SYN, ACK, FIN, RST), sequence numbers, window size, source/destination ports.

✅ **Identifying Attacks from Packet Captures**
- **1. Port Scan:**
  - **Characteristics:** Many SYN packets sent from one source IP to various destination ports on a single target IP, without corresponding SYN-ACKs or ACKs (unless the port is open and the scan completes the handshake).
  - **Purpose:** Reconnaissance to find open ports/services.
- **2. SYN Flood (Denial of Service - DoS):**
  - **Characteristics:** Many SYN packets sent from one source IP to a single target IP/port. No (or very few) SYN-ACKs or ACKs from the destination.
  - **Mechanism:** Attacker sends SYN, but doesn't complete the 3-way handshake, leaving half-open connections that consume resources on the target server, leading to a denial of service.
- **3. Distributed Denial of Service (DDoS):**
  - **Characteristics:** Similar to SYN flood (many SYN packets to a single target IP/port), but the source IPs are varied (coming from multiple different machines).
  - **Mechanism:** Multiple compromised machines (botnet) attack a single target simultaneously.
  - **Distinction from DoS:** Multiple sources vs. single source.

✅ **Exam Tips**
- Packet capture snippets on the exam will be short (5-20 lines).
- Focus on the most obvious pattern to identify the attack type.
- Look for patterns in source/destination IPs, protocols, and flags.