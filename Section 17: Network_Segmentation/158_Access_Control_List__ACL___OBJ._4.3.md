## 💡 Access Control List (ACL) (OBJ 4.3)

An Access Control List (ACL) is a list of permissions (rules) associated with a system or network resource, applied to packet filtering devices (routers, Layer 3 switches, firewalls). Its purpose is to control the flow of traffic (permit/deny) into or out of networks and can also define QoS levels.

✅ **Rule Components**
- **Action:** Permit or Deny.
- **Protocol/Application:** (e.g., TCP, UDP, specific port numbers like 22 for SSH, 80 for HTTP).
- **Source:** Source IP address/range.
- **Destination:** Destination IP address/range.

✅ **Processing Order**
- Processed from top to bottom (sequentially).
- The first matching rule is applied, and processing stops for that packet.
- **Best Practice:** Place most specific rules at the top, and most generic rules at the bottom.
- **Implicit Deny:** Many firewalls have an unwritten "deny all" rule at the very end of an ACL. It's best practice to explicitly add a "deny all" rule at the end of every ACL, even if the device has an implicit deny. This ensures only explicitly permitted traffic passes.

✅ **Types of Allow/Deny Rules**
- **1. Explicit Allow:** A rule that specifically permits certain traffic.
- **2. Explicit Deny:** A rule that specifically blocks certain traffic.
- **3. Implicit Deny:** An unwritten "deny all" rule at the very end of an ACL.
- **Best Practice:** Always include an explicit `deny ip any any` (or equivalent) as the last rule in an ACL, even if the device has an implicit deny. This ensures only explicitly permitted traffic passes.

✅ **Common Traffic to Block at the Firewall (Examples)**
- Private/Loopback/Multicast/Experimental IP ranges coming from the internet (indicates spoofing).
- Protocols that should only be used locally (e.g., ICMP, DHCP, OSPF, SMB) if coming from the internet (unless via a secure tunnel like VPN).
- IPv6 traffic: If not actively using IPv6, block it at the firewall to prevent misconfigurations from being exploited.

✅ **Role-Based Access Control (RBAC) for ACL Management**
- Defines privileges and responsibilities for administrative users who control firewalls and their ACLs.
- Users are put into groups based on roles/job functions.
- Permissions are assigned based on roles (e.g., a switch technician might only be able to enable/disable ports, not modify Layer 3 ACLs).