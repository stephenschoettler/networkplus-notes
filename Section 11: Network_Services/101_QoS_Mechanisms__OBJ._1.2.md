## 💡 QoS Mechanisms (OBJ 1.2)

Various mechanisms are used to implement QoS, allowing networks to prioritize and manage traffic effectively.

✅ **Core QoS Mechanisms**
- **1. Classification:**
  - **Purpose:** Placing traffic into different categories based on its type (e.g., email, web, voice, video).
  - **Method:** Analyzes packet headers, ports, and protocols without altering the packet itself.
- **2. Marking:**
  - **Purpose:** Altering bits within a frame or packet to indicate its QoS category or priority.
  - **Method:** Uses fields like **IP Precedence** (first 3 bits of ToS byte) or **DSCP (DiffServ Code Point)** (first 6 bits of ToS byte) in the IP header.
- **3. Congestion Management (Queuing):**
  - **Purpose:** Manages traffic when a device receives data faster than it can transmit, buffering excess traffic in queues.
  - **Queuing Algorithms:**
    - **Weighted Fair Queuing (WFQ):** Gives each traffic flow a fair share of bandwidth, taking turns.
    - **Low-Latency Queuing (LLQ):** Prioritizes high-priority traffic (e.g., VoIP) to be emptied first, potentially causing delays for lower-priority traffic.
    - **Weighted Round-Robin (WRR):** A hybrid approach that assigns weights to different traffic categories, allowing higher-priority traffic to be sent more frequently while still giving lower-priority traffic a turn.
- **4. Congestion Avoidance:**
  - **Purpose:** Proactively drops packets to prevent queues from becoming completely full and causing widespread congestion.
  - **Method:** **Random Early Detection (RED):** As a queue approaches its maximum capacity, RED starts dropping packets randomly, with lower-priority traffic often being dropped first. This signals congestion to senders, prompting them to reduce their transmission rates.
- **5. Policing vs. Shaping:**
  - **Policing:**
    - **Action:** Discards packets that exceed a configured rate limit ("speed limit").
    - **Impact:** Results in packet drops and retransmissions, which can increase network load.
    - **Best for:** High-speed interfaces where retransmissions are less impactful.
  - **Shaping:**
    - **Action:** Buffers (delays) packets that exceed a configured rate limit instead of discarding them.
    - **Impact:** Smooths out traffic bursts, preventing drops and retransmissions.
    - **Best for:** Slower-speed interfaces (e.g., T1, dial-up) where retransmissions would severely impact performance.
- **6. Link Efficiency:**
  - **Purpose:** Maximizing the utilization of available bandwidth, especially on slower links.
  - **Techniques:**
    - **Compression:** Reduces the size of data payloads (e.g., VoIP payloads can be significantly compressed). **Compressed RTP (CRTP)** compresses VoIP headers.
    - **Link Fragmentation and Interleaving (LFI):** Breaks large packets into smaller fragments and interleaves them with smaller, high-priority packets (e.g., voice). This prevents large data packets from monopolizing the link and causing delay/jitter for real-time traffic.