## 💡 Stateless Address Autoconfiguration (SLAAC) (OBJ 3.4)

- SLAAC is a mechanism within the IPv6 protocol suite.
- It allows devices on an IPv6 network to **configure their own IP addresses autonomously**.
- It does so without the need for a centralized DHCP server.
- It simplifies network configuration, makes IP assignment seamless, and reduces administrative overhead.

✅ **Why SLAAC was Created**
- Addresses the challenges of manually assigning IP addresses in large, complex networks.
- Provides a more **efficient and autonomous** way for devices to obtain IP addresses compared to traditional static assignment or even DHCP.
- Enhances network efficiency, eliminates potential for IP conflicts, and streamlines the integration of new devices.

✅ **The Five-Step SLAAC Process**
- **1. Device Initiation:**
  - A device first generates a **temporary link-local address** (e.g., `fe80::/10`). This allows it to communicate on its local segment.
- **2. Router Solicitation (RS):**
  - The device sends out a **Router Solicitation (RS)** message to discover any local routers on the network.
- **3. Router Advertisement (RA):**
  - In response to the RS, local routers send back a **Router Advertisement (RA)** message.
  - This RA message contains the **network prefix** (e.g., `2001:db8:abcd::/64`) and other network configuration information.
- **4. Address Configuration:**
  - The device combines the **network prefix** received from the RA with its own **unique identifier** (derived from its MAC address using EUI-64 or a randomly generated interface ID) to create a complete and unique global unicast IPv6 address.
- **5. Final Check (Duplicate Address Detection - DAD / Neighbor Solicitation):**
  - Before using the newly configured IP address, the device performs a **Neighbor Solicitation** (part of Duplicate Address Detection - DAD).
  - This ensures that no other device on the network is already using the same IP address, preventing conflicts.

✅ **Key Benefits of SLAAC**
- **Self-Sufficiency:** Devices can configure themselves.
- **Scalability:** Easily integrates new devices into growing networks.
- **No DHCP Server Needed:** Reduces infrastructure requirements for basic IP assignment.