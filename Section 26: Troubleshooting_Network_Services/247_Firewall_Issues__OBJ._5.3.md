## 💡 Firewall Issues (OBJ. 5.3)
This section covers common issues encountered with firewalls, including connectivity problems and misconfigurations of Access Control Lists (ACLs), along with troubleshooting methodologies.

✅ **Firewall Issues**
- **Purpose:** Network security devices that monitor and filter network traffic based on established rule sets. Act as a barrier between networks.
- **Types:**
  - **Host-based Firewall:** Software running on an individual computer/device (e.g., Windows Defender Firewall). Protects that single device.
  - **Network-based Firewall:** Hardware/software deployed in-line with network traffic (e.g., at border router). Protects an entire network segment.

✅ **Common Firewall Connectivity Issues**
- Access to protected resources from unprotected networks is blocked.
- Access to unprotected resources from protected networks is blocked.
- Inability to access the firewall's configuration interface.
- Essentially: Traffic is either not going *through* the firewall or not going *to* the firewall.

✅ **General Troubleshooting Methodology**
- Apply the 7-step troubleshooting method and use the OSI model.
- **Layer 1 (Physical):** Verify proper cabling and physical connection (e.g., link lights).
- **Layer 2 (Data Link):** Check communication via MAC addresses (e.g., ARP).
- **Layer 3 (Network):** Confirm correct IP address, subnet mask, and default gateway on the firewall.

✅ **Access Control List (ACL) Troubleshooting (Most Common Issue)**
- ACLs are ordered collections of permit/deny rules.
- **Key Checks for ACLs:**
  - **1. Misconfigured Rule Set:** The rules themselves are incorrect or don't achieve the desired outcome.
  - **2. Typos:** Simple spelling errors in IP addresses, network masks, or port numbers can cause unintended blocking.
  - **3. Incorrect Protocol/Port:** Ensure the correct protocol (TCP/UDP) and port numbers are specified for the intended traffic.
  - **4. Incorrect Source/Destination:** Verify that the correct IP addresses or network ranges are referenced in the rules. A small mask error can block a vast number of unintended IPs.
  - **5. Incorrect Rule Order:** This is CRITICAL. ACLs are processed sequentially from top to bottom.
    - Once a packet matches a rule, processing stops for that packet.
    - **Rule:** Place **most specific** rules at the **top** of the list.
    - **Rule:** Place **most generic** rules at the **bottom** of the list.
    - Example: A broad "deny all TCP traffic" rule at the top will prevent more specific "permit web traffic" rules from ever being hit.
- **Host-based Firewall Specifics:** In addition to IP/port rules, check rules based on applications and services. Ensure they are allowed/denied as intended.