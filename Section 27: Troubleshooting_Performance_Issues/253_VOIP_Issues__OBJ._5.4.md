## 💡 VoIP Issues (OBJ. 5.4)
This section focuses on common issues encountered with Voice over Internet Protocol (VoIP) communications, specifically latency and jitter, and provides solutions to mitigate these problems.

✅ **VoIP (Voice over Internet Protocol)**
- Set of protocols for real-time streaming voice and video.
- Requires very low latency and high Quality of Service (QoS) for good performance.

✅ **VoIP Issues**
- **Latency:**
  - Definition: Time for a signal to reach its destination (measured in milliseconds).
  - Impact: Noticeable delays, echoes in calls.
  - Acceptable levels: Ideally under 50-100 milliseconds for high-quality VoIP.
  - Example: Satellite internet connections often have high latency due to signal travel time.
- **Jitter:**
  - Definition: Variation in the delay over time (packets arriving out of order).
  - Impact: Robotic or static-like audio, pieces of words arriving out of sequence.
  - Cause: Packets taking different routes or high latency.
  - VoIP often uses UDP, which doesn't guarantee packet order, making jitter a significant concern.

✅ **Solutions for Latency and Jitter**
- **1. Increase Overall Network Performance:** Improve network infrastructure end-to-end.
- **2. Implement Quality of Service (QoS):**
  - Mechanism to prioritize certain traffic over others.
  - Configure network devices to identify and prioritize VoIP packets.
  - **Benefit:** Reduces latency and jitter within your local network.
  - **Limitation:** QoS settings only apply within your network; they are not guaranteed on public networks like the internet. However, setting QoS locally still gives VoIP traffic a "headstart."