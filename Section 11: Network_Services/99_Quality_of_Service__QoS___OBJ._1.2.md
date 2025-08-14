## 💡 Quality of Service (QoS) (OBJ 1.2)

QoS enables the strategic optimization of network performance by prioritizing different types of traffic in converged networks (networks carrying voice, data, and video over the same infrastructure). It ensures proper delivery of critical services (e.g., voice calls need low latency), optimizes bandwidth utilization, and improves user experience by ensuring critical applications perform well.

✅ **Key QoS Categories (Impact on User Experience)**
- **1. Delay (Latency):**
  - **Definition:** The time a packet takes to travel from source to destination (measured in milliseconds).
  - **Impact:** Critical for real-time applications like voice and video; even small delays can cause noticeable issues (e.g., echoes in calls). Less critical for data traffic (e.g., checking bank balances).
- **2. Jitter:**
  - **Definition:** Uneven arrival of packets, meaning the delay varies between packets.
  - **Impact:** Especially problematic for Voice over IP (VoIP) and video, leading to distorted or jumbled audio/video (e.g., "My name is... Jason" instead of "My name is Jason").
- **3. Drops (Packet Loss):**
  - **Definition:** Occurs during network congestion when routers cannot keep up with demand and discard packets.
  - **Impact:**
    - For TCP traffic, packets are retransmitted, leading to slower performance.
    - For UDP traffic (common in VoIP/video), dropped packets are not retransmitted, leading to missing audio/video segments (e.g., voice cutting out).
  - QoS aims to prevent drops for critical traffic.

✅ **Effective Bandwidth: The Bottleneck Concept**
- **Definition:** The actual usable bandwidth in a network path, determined by the **slowest link** in that path.
- **Analogy:** Like water flowing through pipes; the overall flow is limited by the narrowest pipe.
- **Importance:** Understanding effective bandwidth is crucial for designing QoS policies, as it highlights where congestion is most likely to occur.