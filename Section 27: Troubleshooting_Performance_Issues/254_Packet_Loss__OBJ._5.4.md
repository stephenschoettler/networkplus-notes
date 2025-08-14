## 💡 Packet Loss (OBJ. 5.4)
This section defines packet loss, outlines its common causes, and provides strategies for troubleshooting and preventing it in a network.

✅ **Packet Loss**
- **Definition:** Occurs when data packets fail to reach their intended destination across a network.
- **Symptoms:** Slow internet speeds, video/audio lags, complete communication disruptions, unexplained network slowdowns, jitter during VoIP calls, abrupt disconnections in streaming media.

✅ **Causes of Packet Loss**
- **Network Congestion:** Too much data exceeding network capacity (like a traffic jam).
- **Faulty Router Configurations:** Incorrect router setup leading to misdirected or improperly prioritized data.
- **Bad Cables:** Physically damaged or deteriorating cables disrupting data transmissions.
- **Hardware Failures:** Malfunctioning network devices (switches, routers, modems).

✅ **Troubleshooting Packet Loss**
- **Identify Source:**
  - `ping` command: Checks reachability of a device.
  - `traceroute` command: Maps the path data takes to its destination.
  - Network Monitoring Tools: Provide comprehensive insights into traffic patterns to pinpoint location and cause.
- **Mitigation & Resolution Strategies:**
  - **Network Congestion:** Increase bandwidth, optimize network layout, employ Quality of Service (QoS) to prioritize critical traffic.
  - **Hardware Issues:** Routinely inspect and replace faulty cables, ensure network devices are functioning correctly, check for and implement firmware updates.
  - **Configuration Errors:** Verify configuration settings across all network devices; ensure devices are correctly configured for the network.

✅ **Proactive Measures to Prevent Packet Loss**
- Implement regular network performance monitoring.
- Keep network infrastructure updated and well-maintained.
- Maintain a well-documented network configuration policy to prevent misconfigurations.