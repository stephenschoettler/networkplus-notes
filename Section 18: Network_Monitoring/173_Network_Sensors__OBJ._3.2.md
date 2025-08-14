## 💡 Network Sensors (OBJ 3.2)

Network Sensors monitor the performance and health of network devices (routers, switches, firewalls). They are key indicators of proper operation or impending failure.

✅ **Three Key Sensor Measurements**
- **1. Temperature:**
  - **Monitoring:** Devices report internal temperature (intake/exhaust, individual components).
  - **Thresholds:**
    - **Minor:** Alarm when rising, but not yet dangerous.
    - **Major:** Alarm when dangerous; device may "load shed" (turn off functions) to reduce heat.
  - **Impact of High Temp:** Decreased performance, reduced lifespan, catastrophic failure.
- **2. CPU Usage/Utilization:**
  - **Normal Range:** 5-40% utilization.
  - **High Utilization:** Indicates a misconfigured network (e.g., broadcast storm), or a network under attack (e.g., DoS).
  - **Impact of High CPU:** Device becomes unresponsive, drops packets, connection failure.
  - **Causes:** Excessive traffic, complex ACLs, misconfigurations.
- **3. Memory Utilization:**
  - **Normal Range:** Around 40% utilization.
  - **High Utilization (above 80% consistently):** Indicates a larger problem.
  - **Impact of High Memory:** System hangs, processor crashes, undesirable behavior.
  - **Causes:** Excessive loading, misconfigurations, or attack.

✅ **Overall Importance**
- Monitoring these sensors helps identify network configuration or performance issues.
- Alarms triggered by threshold breaches require investigation to find the root cause and restore normal operation within the baseline.