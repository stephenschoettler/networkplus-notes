## 💡 Network Performance Metrics (OBJ 3.2)

Network Performance Monitoring is the end-to-end monitoring of end-user experience, from workstation to final destination. As a network administrator, it's crucial to monitor these three key metrics (latency, bandwidth/throughput, and jitter) to ensure network performance and availability.

✅ **Three Key Metrics**
- **1. Latency:**
  - **Definition:** Time it takes for data to reach its destination across a network (round trip time).
  - **Measurement:** Reported in milliseconds (ms), often using `ping` command.
  - **Impact:** High latency slows down network performance, especially for real-time applications (streaming video, VoIP, gaming).
- **2. Bandwidth vs. Throughput:**
  - **Bandwidth:** Theoretical maximum rate of data transfer under ideal conditions.
  - **Throughput:** Actual measure of data successfully transferred from source to destination (real-world speed).
  - **Measurement:** Often measured using speed tests (e.g., speedtest.net).
  - **Impact:** Factors like Wi-Fi, network congestion, and other users can cause throughput to be lower than theoretical bandwidth.
- **3. Jitter:**
  - **Definition:** Variation in the delay of data packets over a network connection. Packets arrive out of order or with inconsistent delays.
  - **Impact:** Significant problem for real-time applications (video conferencing, VoIP, VDI). Causes audio/video distortions (e.g., "robot voice," speeding up/slowing down).
  - **Cause:** Network congestion (buffers filling up, then emptying quickly).
  - **Prevention:** Proper Quality of Service (QoS) implementation (prioritizing voice/video traffic), ensuring sufficient network capacity.

✅ **Packet Loss**
- Occurs when network devices drop packets due to full buffers during congestion.
- TCP retransmissions due to packet loss can further increase network load.