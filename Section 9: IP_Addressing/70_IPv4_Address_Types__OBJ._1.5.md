## 💡 IPv4 Address Types (OBJ 1.5)

IPv4 addresses are classified into different types based on their purpose and scope.
**Private IP Ranges (Memorize for the exam!):**
- **Class A:** `10.0.0.0` to `10.255.255.255` (10.0.0.0/8)
- **Class B:** `172.16.0.0` to `172.31.255.255` (172.16.0.0/12)
- **Class C:** `192.168.0.0` to `192.168.255.255` (192.168.0.0/16)

✅ **Public vs. Private IPv4 Addresses**
- **1. Public IPv4 Addresses:**
  - **Concept:** Globally unique and routable on the public internet.
  - **Management:** Managed by the Internet Corporation for Assigned Names and Numbers (ICANN) and its five Regional Internet Registries (RIRs) (e.g., ARIN for North America).
  - **Acquisition:** Must be leased or purchased from an Internet Service Provider (ISP).
- **2. Private IPv4 Addresses (RFC 1918):**
  - **Concept:** Non-internet routable addresses used within a local network (LAN).
  - **Benefit:** Can be used by anyone within their own network without registration, which conserves the limited public IPv4 address space.
  - **NAT (Network Address Translation):** A router uses NAT to translate private IP addresses into a single public IP address for internet access, and vice-versa.

✅ **Special IPv4 Address Ranges**
- **1. Loopback / Localhost Address:**
  - **Address:** `127.0.0.1` (the entire `127.0.0.0/8` block is reserved for this).
  - **Purpose:** A special address that a device uses to send a packet to itself.
  - **Use Case:** Used for testing and troubleshooting network protocol software on a local machine without sending traffic onto the network.
- **2. APIPA (Automatic Private IP Addressing):**
  - **Address Range:** `169.254.0.0` to `169.254.255.255` (169.254.0.0/16).
  - **Purpose:** A fallback mechanism. If a device is configured for DHCP but cannot reach a DHCP server, it will self-assign an APIPA address.
  - **Troubleshooting Indicator:** If you see a device with a `169.254.x.x` address, it's a clear sign of a DHCP problem. The device can only communicate with other APIPA devices on the same local segment.