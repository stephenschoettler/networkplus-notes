## 💡 Network Performance Issues (OBJ. 5.4)
This section details common causes of network performance issues, including high CPU usage, high bandwidth usage, poor physical connectivity, malfunctioning network devices, and DNS problems.

✅ **Five Common Causes of Network Performance Issues**
- **1. High CPU Usage in Network Devices**
  - Network devices (routers, switches, firewalls) are computers with CPUs.
  - High CPU utilization leads to slowing down of the device and network.
  - **Symptoms:** Increased latency, jitter, packet loss.
  - **Troubleshooting:**
    - Upgrade to more powerful devices.
    - Simplify processing load (e.g., optimize ACLs).
- **2. High Bandwidth Usage**
  - When bandwidth is high, communications wait, buffers fill, packets can be dropped.
  - Dropped TCP packets are retransmitted, further increasing utilization.
  - **Troubleshooting:**
    - Increase bandwidth size (e.g., pay more to ISP).
    - Perform network flow analysis to identify and manage excessive/unnecessary traffic (e.g., social media).
- **3. Poor Physical Connectivity**
  - Damaged cables can still operate but cause errors and retransmissions, slowing down the network.
  - **Troubleshooting:**
    - Check and test cables one by one.
    - If ISP issue suspected, connect test client directly to demarcation point.
    - Use cable testers for twisted pair and fiber light meters for fiber optic connections.
- **4. Malfunctioning Network Devices**
  - **Causes:** Misconfigurations, hardware failures, old/outdated network operating systems.
  - **Troubleshooting:** Use a systematic troubleshooting method (e.g., 7-step method) to pinpoint the device and determine if it's a configuration or hardware issue.
- **5. DNS Problems**
  - High DNS latency slows down user experience as domain name resolution is a prerequisite for accessing websites.