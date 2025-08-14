## 💡 DHCP Issues (OBJ. 5.3)
This section covers common issues related to Dynamic Host Configuration Protocol (DHCP), including rogue DHCP servers and IP address scope exhaustion, along with their causes and solutions.

✅ **DHCP (Dynamic Host Configuration Protocol)**
- Purpose: Automatically assigns IP addresses, subnet masks, default gateways, and DNS server IPs to devices joining a network.

✅ **DHCP Issues**
- **1. Rogue DHCP Servers:**
  - **Definition:** An unauthorized DHCP server on the network not under administrative control.
  - **Causes:**
    - **Malicious Attack:** Used to redirect clients to attacker-controlled sites (on-path/man-in-the-middle attacks).
    - **Accidental:** Employees connect personal wireless routers/gateways with built-in DHCP.
  - **Impact:** Can hand out incorrect IP configurations, leading to network connectivity issues or duplicate IP addresses if using the same scope as the legitimate server.
  - **Prevention:**
    - **DHCP Snooping:** Configure on switches to filter untrusted DHCP messages.
    - **Port Security:** Limit MAC addresses per switch port to prevent unauthorized devices.
    - **Intrusion Detection Systems (IDS):** Detect rogue DHCP activity.
- **2. DHCP Scope Exhaustion:**
  - **Definition:** The DHCP server runs out of available IP addresses to assign.
  - **Causes:**
    - Too many devices requesting IPs for the current scope size.
    - Long DHCP lease times, especially with transient users (e.g., public Wi-Fi), as IPs remain reserved even when devices are offline.
  - **Solutions:**
    - **Decrease DHCP Lease Time:** Allows IPs to be returned to the pool faster, especially for transient users.
    - **Increase Scope Size:** Change the subnet mask to allow for more available IP addresses in the DHCP pool.
    - **Decrease Number of Devices Using DHCP:** Implement Port Security or Network Access Control (NAC) to limit unauthorized devices from obtaining IPs.