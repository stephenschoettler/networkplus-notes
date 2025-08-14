## 💡 Basic Network Device Commands (OBJ. 5.5)
This section introduces fundamental commands for troubleshooting and managing network devices like routers, switches, and firewalls, with a focus on their practical application in network diagnostics.

✅ **Basic Network Device Commands**
- Focus: Understanding fundamental commands for routers, switches, and firewalls (network platforms).
- CompTIA exams are vendor-neutral, but commands are often similar to Cisco.

✅ **`show interface`**
- Purpose: Displays statistics for a network interface.
- Usage: `show interface [interface_type/number]` (e.g., `show interface ethernet 1/1`).
- Key Info to Check:
  - **Interface/Line Protocol Status:** Up/Down.
  - **IP Address:** Valid? (APIPA indicates DHCP issue).
  - **Bandwidth:** Matches cable type? (Mismatch suggests cable damage).
  - **MTU Size:** Default 1500 bytes. (Jumbo frames for SANs).
  - **Errors:** Runts, Giants, CRC errors (indicate problems).
  - **Collisions:** Should be 0 on full-duplex switch ports.

✅ **`show config`**
- Purpose: Displays the current system configuration of the device.
- Usage: `show config` (no arguments).
- Key Info: Provides a comprehensive view of device settings (e.g., shared secrets, SNMP, IP settings, DNS, VLAN, STP, ACLs).
- Note: For exam, understand general sections, not every line.

✅ **`show route` (or `show ip route`)**
- Purpose: Displays the current state of the routing table.
- Usage: `show ip route` (most common for IP networks).
- Key Info:
  - **Legend:** Explains route codes (C=Connected, R=RIP, O=OSPF, S=Static, etc.).
  - **Gateway of Last Resort:** Default route for unknown destinations.
  - **Route Derivation:** How the route was learned.
  - **Administrative Distance (AD):** Trustworthiness of source (lower AD = more trusted).
  - **Metric:** Cost to reach destination (lower metric = better path).
  - **Next Hop (`via`):** IP of next router.
  - **Last Update Time.**
  - **Outgoing Interface.**