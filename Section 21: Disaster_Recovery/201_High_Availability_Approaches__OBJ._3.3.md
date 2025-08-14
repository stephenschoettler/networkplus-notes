## 💡 High Availability Approaches (OBJ. 3.3)
This section explores various high availability approaches, including network redundancy fundamentals, active-active and active-passive strategies, load balancers, and Content Delivery Networks (CDNs), all aimed at minimizing downtime and ensuring continuous network operations.

✅ **High Availability Approaches**
- Strategies to maintain continuous network operations with minimal downtime.

✅ **Network Redundancy Fundamentals**
- Servers with multiple NICs (Network Interface Cards) for load balancing/failover.
- Redundant cabling/pathways between switches, routers, and to the internet.

✅ **High Availability Strategies**
- **1. Active-Active Approach:**
  - Multiple systems run simultaneously, sharing the load.
  - Maximizes resource utilization; seamless failover (performance may degrade).
  - Example: Two NICs combine for 2Gbps; if one fails, the other continues at 1Gbps.
- **2. Active-Passive Approach:**
  - Primary system active; standby system idle until primary fails.
  - Reliable fallback; less efficient resource utilization.
  - Example: Generator (passive) takes over when primary power (active) fails.
- **3. Load Balancers:**
  - Distribute traffic across multiple servers to prevent overload.
  - Monitor server health and reroute traffic from failed nodes.
  - Crucial for Active-Active setups.
- **4. Content Delivery Networks (CDNs):**
  - Geographically distributed servers caching content closer to users.
  - Reroute requests on server failure/high traffic for uninterrupted service.