## 💡 DoS and DDoS Attacks (OBJ 4.2)

This section covers Denial of Service (DoS) and Distributed Denial of Service (DDoS) attacks.

✅ **Denial of Service (DoS) Attack**
- **Definition:** One machine floods a victim system with requests for services, causing the victim to run out of resources (memory, processing power, bandwidth) and eventually crash or become unavailable.
- **Common DoS Techniques:**
  - **TCP SYN Flood:** Attacker initiates multiple TCP sessions by sending SYN packets but never completes the 3-way handshake. Leaves half-open connections that consume server resources.
  - **ICMP Flood (Smurf Attack):** Attacker sends ping to subnet broadcast address with spoofed victim IP. All devices on subnet respond to victim, flooding it.

✅ **Distributed Denial of Service (DDoS) Attack**
- **Definition:** A DoS attack where multiple attacking machines (hundreds, thousands, or more) simultaneously flood a single target server with requests.
- **Mechanism:** Attackers use a botnet (collection of compromised computers) controlled by a Command and Control (C2) server. Individual compromised computers are called zombies.
- **Impact:** Overwhelms target's processing, memory, and bandwidth, leading to exhaustion and crash.
- **Challenge in Cloud:** Cloud services can horizontally scale out to absorb traffic, but victim still pays for resources used by malicious traffic.

✅ **Key Concepts**
- **Botnet:** A collection of compromised computers (zombies) under the control of a single master node (C2 server).
- **Zombie:** An individual compromised computer that is part of a botnet.
- **C2 (Command and Control) Server:** The server used by an attacker to control the botnet.