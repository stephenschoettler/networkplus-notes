## 💡 VLAN Issues (OBJ. 5.3)
This section addresses common issues related to Virtual Local Area Networks (VLANs), including communication problems, routing misconfigurations, and best practices for effective VLAN implementation.

✅ **VLAN (Virtual Local Area Network) Issues**
- **VLAN Communication:**
  - Traffic between different VLANs *must* be routed (using a router or Layer 3 switch) for devices to communicate.
  - Devices within the same VLAN must belong to the same logical subnet.

✅ **Common VLAN Issues & Troubleshooting**
- **1. Improper Routing Setup:**
  - Problem: Devices in different VLANs cannot communicate.
  - Cause: No router or Layer 3 switch configured to route traffic between VLANs.
  - Solution: Implement a router or Layer 3 switch with interfaces in each VLAN to enable inter-VLAN routing.
- **2. Missing Default Gateway:**
  - Problem: Clients cannot communicate outside their VLAN (e.g., to the internet).
  - Cause: Clients lack a configured default gateway that points to the router interface for their VLAN.
  - Solution: Configure the router interface connected to each VLAN to act as the default gateway for that VLAN's subnet.
- **3. Not Using VLANs (Large Broadcast Domain):**
  - Problem: All traffic defaults to VLAN 1, creating a single, very large broadcast domain. This leads to network slowdowns, especially for servers, due to excessive broadcast traffic.
  - Solution: Implement VLANs to segment the network.
    - Break up large broadcast domains into smaller, more manageable ones.
    - Assign devices (e.g., servers, workstations) to appropriate, separate VLANs.
    - Use routers or Layer 3 switches to route traffic between these smaller broadcast domains.

✅ **Best Practices**
- Always ensure proper routing is configured between VLANs.
- Use VLANs to segment your network, reducing broadcast domain size and improving performance.
- Assign devices to specific VLANs (e.g., a dedicated server VLAN) rather than relying solely on the default VLAN 1.