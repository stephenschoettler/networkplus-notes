## 💡 Jumpbox (OBJ 3.5)

An Internet-Facing Host/Server is a host or server that accepts inbound connections from the internet (e.g., web server, email server). These are placed in a screened subnet.

✅ **Screened Subnet (DMZ - Demilitarized Zone)**
- A network segment isolated from the rest of the private network by one or more firewalls.
- Set up to accept connections from the internet over designated ports.
- **Purpose:** To keep forward-facing servers out of the internal network. Acts as a semi-trusted zone.
- Hosts in the screened subnet are not fully trusted by the internal network.
- **Commonly contains:** Email servers, web servers, communication servers, proxy servers, remote access servers, anything providing public services or extranet capabilities.
- **Traffic Flow:**
  - Traffic between the screened subnet and the internal network is typically filtered by a firewall.
  - Intrusion Detection Systems (IDS) are often placed between the screened subnet and the internal network to detect pivot attempts by attackers.

✅ **Bastion Host**
- A host or server placed in the screened subnet that is not configured with any services that run on the local network (e.g., Active Directory).
- Only runs internet-facing services (email, web, remote access).
- Heavily hardened due to its exposure.

✅ **Jumpbox (Jump Server)**
- **Definition:** A hardened server that provides controlled access to other hosts within a sensitive network segment (like a screened subnet).
- **Mechanism:** Administrators first connect to the jumpbox, and then the jumpbox connects to the target host in the screened subnet. This acts as a "pivot" or "stepping stone."
- **Deployment:** Can be a physical PC or a virtual machine (VMs are often preferred for easy hardening, destruction, and rebuilding from a known good image).
- **Security:**
  - The jumpbox and the management workstation used to connect to it should be heavily hardened (minimal software, strict configurations).
  - Access to the jumpbox is tightly controlled (e.g., via firewall rules allowing only the jumpbox to communicate from the internal network to the screened subnet).
- **Purpose:** Prevents direct access from the internal network to sensitive hosts, adding a layer of security and reducing the attack surface.