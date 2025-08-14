## 💡 Routing Issues (OBJ. 5.3)
This section explores common routing issues such as multicast flooding, asymmetrical routing, and missing routes, along with their causes and troubleshooting methods.

✅ **Routing Issues**
- **1. Multicast Flooding:**
  - **Definition:** Occurs when a switch's CAM table doesn't have a specific host associated with a multicast MAC address.
  - **Impact:** Multicast traffic is flooded throughout the entire LAN/VLAN, creating unnecessary traffic and wasting resources.
  - **Prevention:** Configure switches to block unknown multicast packets.
- **2. Asymmetrical Routing:**
  - **Definition:** Network packets leave via one path but return via a different path.
  - **Causes:** Can occur with Layer 2 bridge pairs on routers/firewalls, or with load balancing protocols (e.g., HSRP) in High Availability (HA) clusters.
  - **Impact:** Problematic for stateful firewalls and deep packet inspection devices, as they need to see the entire packet flow. Can lead to dropped packets and intermittent connectivity.
  - **Solution:** Adjust firewall placement and internal routing to ensure traffic flows symmetrically (same path in both directions). Place firewalls closer to the systems they protect rather than at the network edge.
- **3. Missing Routes:**
  - **Definition:** A router cannot reach a destination because the necessary route is absent from its routing table.
  - **Causes:**
    - **Static Routes:** Common when manually adding routes; typos or incorrect commands prevent the route from being added.
    - **Dynamic Routing Protocols:** Issues with neighbor state establishment or convergence can prevent routes from being learned.
  - **Troubleshooting:**
    - **Check Routing Table:** Use `show ip route` (Cisco) or `route print` (Windows) to inspect the router's/system's routing table.
    - **Verify Connectivity:** For dynamic routing, ping the destination router to confirm basic connectivity.
    - **Verify Protocol Status:** Ensure the dynamic routing protocol is enabled and functioning correctly.
  - **Solutions:**
    - Statically add the missing route if it's a simple oversight.
    - Troubleshoot the underlying dynamic routing protocol to ensure proper route advertisement and learning.