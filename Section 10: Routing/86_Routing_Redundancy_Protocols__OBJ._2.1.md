## 💡 Routing Redundancy Protocols (OBJ 2.1)

- Routing Redundancy Protocols prevent communication disruptions.
- They ensure continuous network availability and reliability by automatically rerouting traffic in case of a path or device failure.
- First Hop Redundancy Protocols (FHRP) are a set of protocols designed to provide automatic failover to a backup router if the primary router fails.

✅ **Benefits of FHRP**
- **1. Reliability:** Ensures communications remain active even if a single router fails by rerouting traffic.
- **2. Load Balancing:** Can distribute network traffic across multiple routers to prevent overwhelming a single device, increasing efficiency.
- **3. Seamless Transitions:** Data continues to flow properly with quick and seamless redirection to a standby router, often unnoticed by end-users.

✅ **Critical Components for FHRP**
- **Virtual IP:** An IP address not bound to a specific physical device, serving as a single default gateway for network devices. FHRP redirects traffic from this Virtual IP to the active physical router.
- **Subinterface:** Allows a single physical interface on a router/switch to be subdivided into multiple logical interfaces, each configurable independently (e.g., for different VLANs). This is cost-efficient and aids traffic management.

✅ **Key First Hop Redundancy Protocols**
- **1. HSRP (Hot Standby Router Protocol)**
  - **Developer:** Cisco proprietary.
  - **Function:** Establishes a fault-tolerant default gateway.
  - **Mechanism:** One router is elected as the **active router** (handles routing), and another as the **standby router** (waits to take over if active fails).
  - **Preemption:** A higher-priority router can take over as active if it comes online after the initial election.
- **2. VRRP (Virtual Router Redundancy Protocol)**
  - **Developer:** Open standard (not tied to a specific vendor).
  - **Function:** Similar to HSRP, providing redundancy for a virtual IP.
  - **Mechanism:** One router is designated as the **master router** (handles routing), others serve as backups. If the master fails, a backup automatically takes over.
  - **Benefit:** High compatibility across different networking equipment brands.
- **3. GLBP (Gateway Load Balancing Protocol)**
  - **Developer:** Cisco proprietary.
  - **Function:** Takes redundancy a step further by adding **load balancing capabilities**.
  - **Mechanism:** All configured routers can **simultaneously forward packets**, effectively distributing the traffic load. Achieved by assigning a different **Virtual MAC address** to each GLBP group member.
  - **Benefit:** Optimizes network resource utilization while still providing redundancy.