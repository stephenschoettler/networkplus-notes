## 💡 Understanding Firewalls (OBJ 4.3)

Firewalls are network security devices that monitor and filter network traffic based on established rule sets (ACLs). They act as a barrier between networks.

✅ **Access Control Lists (ACLs)**
- **Definition:** Rule sets placed on firewalls, routers, or other network devices to permit or deny traffic through an interface.
- **Order of Operations:** Rules are processed in a top-down manner. The first matching rule is applied, and processing stops for that packet.
- **Best Practice:** Place most specific rules at the top, more generic rules at the bottom.
- **Implicit Deny:** Many firewalls have an implied "deny all" rule at the end. It's best practice to explicitly add a "deny all" rule at the end of every ACL to ensure only authorized traffic passes.
- **Logging:** Actions (especially deny actions) should be logged for auditing and troubleshooting.
- **Rule Components:** Type of traffic (protocol), source, destination, and action (permit/deny).

✅ **Types of Firewalls**
- **1. Hardware-Based Firewall:**
  - Dedicated physical device (e.g., SOHO router/firewall combo).
  - Protects an entire network segment.
  - **Configuration:** Often via web-based interface.
  - **Example:** Blocking outbound Telnet (port 23), specific game ports (e.g., 666), or FTP (ports 20-21).
  - Inbound rules often configured via "port forwarding" or "port triggering" to allow specific traffic.
- **2. Software-Based Firewall (Host-Based Firewall):**
  - Software running on an individual computer/device (e.g., Windows Defender Firewall, macOS Firewall).
  - Protects that single device.
  - **Configuration:** Via GUI (e.g., Windows Defender Firewall with Advanced Security, macOS Security & Privacy -> Firewall).
  - **Windows Defender Firewall:** Allows granular control (inbound/outbound rules, specific ports/protocols, programs, network profiles - Domain, Private, Public). Can export policies.
  - **macOS Firewall:** Simpler GUI, allows/blocks applications. Less granular control via GUI; more advanced control requires command-line tools (PF, IPFW). Includes "stealth mode" to prevent responses to ping sweeps.

✅ **Overall**
- Firewalls, whether hardware or software, rely on ACLs to define their protection based on configured rules.