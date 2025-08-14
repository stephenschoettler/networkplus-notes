## 💡 Duplicate Addresses (OBJ. 5.3)
This section explains the causes, impacts, detection methods, and prevention strategies for duplicate MAC and IP addresses within a network.

✅ **Duplicate Addresses**
- **1. Duplicate MAC Addresses (Layer 2):**
  - **MAC Address:** A unique 12-digit hexadecimal hardware address (48 bits) assigned during manufacturing.
  - **Causes:**
    - Manufacturing error (rare).
    - Locally-administered addresses (self-assigned, often indicates MAC spoofing).
    - Virtual machines (VMs) if not managed by a Logical Domain Manager (LDM).
  - **Impact:**
    - Switch CAM table flapping (constantly updating location of the same MAC address between different ports).
    - Intermittent or no network connectivity for affected devices.
  - **Detection:**
    - Intermittent network connectivity issues for two devices.
    - Protocol analyzer (e.g., Wireshark) inspecting ARP traffic.
    - `show arp` command on a switch (look for same MAC on different ports).
  - **Prevention:**
    - **Port Security:** Configure switch ports to allow only a single MAC address.
    - **Logical Domain Manager (LDM):** For VMs, ensures unique MAC address assignment by the hypervisor.
    - **Resolution:** Reset MAC address to burned-in address, replace NIC, or remove the device.
- **2. Duplicate IP Addresses (Layer 3):**
  - **Definition:** Also known as an IP Address Conflict; two or more devices on the same network have the same IP address.
  - **Causes:**
    - **Static Assignment Errors:** Manually assigning an IP already in use or a typo.
    - **DHCP Server Issues:** DHCP server incorrectly assigns an IP already in use.
    - **Rogue DHCP Server:** An unauthorized DHCP server hands out IPs that conflict with the legitimate server's assignments.
    - **Static IP in DHCP Range:** A device is statically assigned an IP that falls within the DHCP server's dynamic pool.
  - **Impact:** Intermittent connectivity for both devices using the same IP. Routers may not know where to send return traffic.
  - **Detection:**
    - Network connectivity issues for affected clients.
    - Check client's IP configuration (static vs. dynamic).
    - `show arp` command on a router (look for same IP with different MACs or on different interfaces).
  - **Resolution:**
    - If statically assigned, change to DHCP or assign a unique static IP.
    - If DHCP-related, troubleshoot the DHCP server or rogue DHCP server.