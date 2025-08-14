## 💡 Internet Control Message Protocol (ICMP) (OBJ 1.4)

ICMP is a network layer protocol primarily used for **diagnosing network communication issues** and providing information about network problems. Understand that ICMP is a diagnostic tool, not for data transfer. Be aware of its common uses (ping, traceroute) and associated attack types (flood, ping of death).

✅ **ICMP Overview**
- **Purpose:** A network layer protocol primarily used for **diagnosing network communication issues** and providing information about network problems.
- **Not a Transport Protocol:** Unlike TCP or UDP, ICMP is *not* used for sending data between systems.
- **Operation:** Operates at the network layer (Layer 3) and is encapsulated within IP packets.
- **Uses:** Indicates unreachable hosts/services, expired Time-to-Live (TTL), or full router buffers.

✅ **PING Utility**
- Uses ICMP to send an **ICMP Echo Request** message to test host reachability.
- Receiving host responds with an **ICMP Echo Reply**.
- Measures **roundtrip time (latency)**.

✅ **ICMP Message Structure**
- **Header:**
  - **Type:** Indicates message type (1 byte).
  - **Code:** Provides additional context (1 byte).
  - **Checksum:** For error checking (2 bytes).
- **Data Section:** Varies based on message type (e.g., identifier and sequence number for Echo Request/Reply).

✅ **ICMP Reliability**
- ICMP lacks reliability mechanisms found in TCP (no guaranteed delivery, no ordering, no error correction). It's designed for speed and simplicity, not data integrity or security.

✅ **ICMP-based Attacks**
- **1. ICMP Flood Attack (Ping Flood):**
  - **Mechanism:** Overwhelming a target with a large number of ICMP Echo Request packets (pings) without waiting for replies.
  - **Goal:** Consume target's resources (bandwidth, processing power) leading to a **Denial of Service (DoS)**.
  - **DDoS (Distributed Denial of Service):** Amplified DoS attack using a network of compromised computers (botnets).
- **2. Ping of Death:**
  - **Mechanism:** Exploits a vulnerability in older, unpatched systems by sending malformed or oversized ICMP packets (larger than 65,535 bytes).
  - **Goal:** Cause buffer overflows, system crashes, or DoS on vulnerable systems.
  - **Note:** Most modern systems are no longer vulnerable due to improved security measures.

✅ **Blocking ICMP**
- Many network administrators block ICMP traffic at firewalls/routers to harden security. However, this makes troubleshooting network connectivity harder as tools like ping and traceroute become ineffective.