## 💡 Assigning IPv4 Addresses (OBJ 1.7)

IPv4 addresses can be assigned in two primary ways: Static (manual) or Dynamic (automatic). Remember the four key components DHCP provides! If a device has a `169.254.x.x` IP, it indicates a DHCP issue or network connectivity problem preventing it from reaching a DHCP server.

✅ **Static Assignment (Manual)**
- Manually configuring IP address, subnet mask, default gateway, and DNS server on each device.
- **Pros:** Precise control.
- **Cons:** Time-consuming, highly prone to human error (typos, duplicate IPs), impractical for large networks.

✅ **Dynamic Assignment (Automatic)**
- Devices automatically obtain IP configuration from a server.
- **Pros:** Quicker, easier, less error-prone, scalable for any network size.

✅ **Four Essential IP Configuration Components (for both Static & Dynamic)**
- **1. IP Address:** Unique identifier for the device on the network.
- **2. Subnet Mask:** Defines the network and host portions of an IP address.
- **3. Default Gateway:** The IP address of the router that allows communication outside the local network segment.
- **4. DNS Server:** Translates domain names (e.g., `google.com`) into IP addresses.
- **WINS (Windows Internet Name Service):** An alternative to DNS for name resolution within Windows domains (NetBIOS names to IPs).

✅ **Dynamic IP Assignment Methods**
- **1. BOOTP (Bootstrap Protocol):**
  - **Concept:** Oldest method (1985), used for diskless workstations.
  - **Mechanism:** Used a static database of MAC-to-IP mappings.
  - **Note:** Largely replaced by DHCP due to its static nature.
- **2. DHCP (Dynamic Host Configuration Protocol):**
  - **Concept:** Modern, widely used protocol for automatic IP assignment.
  - **Mechanism:** Assigns IPs from a defined "scope" or "pool" of addresses.
  - **Leases:** IPs are "borrowed" for a set "lease" time; clients can renew leases.
  - **Benefits:** Provides all four key IP configuration components (IP, Subnet Mask, Gateway, DNS) automatically.
- **3. APIPA (Automatic Private IP Addressing):**
  - **Concept:** Self-assigned IP address when a device cannot reach a DHCP server.
  - **IP Range:** `169.254.x.x` (Class B private address range).
  - **Limitation:** Allows communication *only* within the local network segment (devices with other APIPA addresses). Cannot communicate with devices outside this segment (e.g., no internet access) because there's no default gateway.
- **4. ZeroConf (Zero Configuration Networking):**
  - **Concept:** Newer technology based on APIPA, designed for automatic network configuration without manual setup or central servers.
  - **Features:**
    - Assigns IPv4 link-local addresses (similar to APIPA, non-routable).
    - **mDNS (multicast DNS):** Resolves computer names to IP addresses without a central DNS server.
    - **Service Discovery:** Automatically finds available network services (e.g., printers, scanners, shared folders).
  - **Implementations:**
    - **Apple:** Bonjour
    - **Microsoft Windows:** LLMNR (Link-Local Multicast Name Resolution)
    - **Linux:** SystemD (specifically `systemd-resolved`)
  - **Benefit:** Simplifies networking for small, ad-hoc networks.