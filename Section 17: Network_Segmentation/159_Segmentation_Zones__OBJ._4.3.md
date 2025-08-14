## 💡 Segmentation Zones (OBJ 4.3)

Segmentation Zones use firewalls, boundary devices, and Access Control Lists (ACLs) to create distinct network zones with specific rules for traffic flow.

✅ **Three Main Zones**
- **1. Trusted Zone (Inside Zone):**
  - **Definition:** Your local area network (LAN) or intranet.
  - **Trust Level:** Fully trusted by the organization.
  - **Traffic Flow:** Generally allows outbound traffic to the internet (untrusted zone) and return traffic for requested resources. Inbound unsolicited traffic is typically blocked.
- **2. Untrusted Zone (Outside Zone):**
  - **Definition:** External networks like the internet or other networks you connect to.
  - **Trust Level:** Not trusted by the organization.
  - **Traffic Flow:** Inbound unsolicited traffic is generally blocked to the trusted zone.
- **3. Screened Subnet (DMZ - Demilitarized Zone):**
  - **Definition:** A semi-trusted zone located between the trusted and untrusted zones. Isolated from the private network by one or more firewalls.
  - **Purpose:** Hosts devices that need to accept inbound connections from the internet (internet-facing hosts) without exposing the internal trusted network.
  - **Content:** Typically contains public-facing servers (web servers, email servers), communication servers, proxy servers, remote access servers, or extranet capabilities.
  - **Traffic Flow:**
    - Internet to Screened Subnet: Allowed for specific services (e.g., HTTP/S for web servers, SMTP/POP3/IMAP for email servers).
    - Screened Subnet to Internet: Generally allowed for outbound requests.
    - Trusted Zone to Screened Subnet: Traffic is typically filtered by a firewall, treating the DMZ as less trusted than the internal network.
    - Screened Subnet to Trusted Zone: Heavily restricted and filtered by a firewall to prevent attackers from pivoting from a compromised DMZ host into the internal network.
  - **Security:** Hosts in the DMZ should be heavily hardened (bastion hosts). It acts as a choke point where security devices (IDS, IPS, UTM) can be placed.