## 💡 Dynamic Host Configuration Protocol (DHCP) (OBJ 3.4)

- DHCP automates the process of assigning IP addresses and other network configuration information to client devices.
- **Memory Aid:** "DORA the Explorer" (Discover, Offer, Request, Acknowledge).

✅ **Benefits of DHCP**
- **Automation:** Eliminates manual IP configuration, saving significant labor in large networks.
- **Error Reduction:** Minimizes human error (typos, incorrect settings).
- **IP Conflict Prevention:** Ensures each device gets a unique IP from a defined pool, preventing conflicts.

✅ **DHCP Scope, Exclusions, and Reservations**
- **Scope:** A defined range of valid IP addresses available for assignment to devices on a subnet.
- **Excluded Range:** Specific IP addresses within a scope that the DHCP server will *not* hand out (e.g., for statically assigned devices like printers or servers).
- **DHCP Reservation:** Assigns a specific IP address from the scope to a device based on its MAC address. The device always receives the same IP, but the assignment is managed by DHCP, not manual static configuration. Ideal for devices needing consistent IPs in large networks.

✅ **The DORA Process: How DHCP Works**
- **D**iscover: Client broadcasts a message to find a DHCP server.
- **O**ffer: DHCP server offers an available IP address from its scope.
- **R**equest: Client requests to use the offered IP address.
- **A**cknowledge: DHCP server acknowledges the request and assigns the IP address along with other configuration details (lease).

✅ **Key Information Provided by DHCP**
- **IP Address:** The unique address for the device on the network.
- **Subnet Mask:** Defines the network and host portions of the IP address.
- **Default Gateway:** The IP address of the router that allows the device to communicate outside its local network.
- **DNS Server IP:** The IP address of the Domain Name System server for name resolution.

✅ **DHCP Lease Times**
- The duration for which a client can use an assigned IP address.
- Typically 24 hours for home networks, but can be longer (e.g., 7 or 30 days) in corporate networks.
- Longer lease times can make troubleshooting easier in cybersecurity scenarios by providing more stable IP assignments.

✅ **Alternate Configurations (When DHCP Fails)**
- If a device cannot reach a DHCP server or fails to get a proper configuration, it defaults to an alternate configuration.
- **APIPA (Automatic Private IP Addressing):** A common default fallback. The device self-assigns an IP address in the 169.254.0.0/16 range. These IPs are only usable for local network communication.
- **Static Fallback:** An administrator can configure a device to fall back to a known good static IP address instead of APIPA.

✅ **DHCP Relays and IP Helper Addresses**
- **DHCP Relay:** A host (often a router) that forwards DHCP packets between clients and servers when they are on different subnets.
- **IP Helper Address:** Configured on a router's interface to direct DHCP (and other UDP broadcasts) requests to a DHCP server located on a different subnet. Essential for cross-subnet DHCP communication.
- DHCP operates using **UDP (User Datagram Protocol)**, making it a "fire and forget" method of communication.