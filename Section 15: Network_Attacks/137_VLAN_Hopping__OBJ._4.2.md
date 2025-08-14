## 💡 VLAN Hopping (OBJ 4.2)

VLAN (Virtual Local Area Network) is used to partition a broadcast domain and isolate network segments at Layer 2 (data link layer). It increases security by forcing traffic between VLANs to use Layer 3 routing, allowing ACLs to be applied. VLAN Hopping is a technique that exploits misconfigurations or vulnerabilities to direct traffic to a different VLAN without proper authorization, bypassing segmentation.

✅ **Methods of VLAN Hopping**
- **1. Double Tagging (VLAN Tagging Attack):**
  - **Mechanism:** Attacker sends a frame with two 802.1Q VLAN tags (inner for target VLAN, outer for native VLAN of trunk port). Switch removes outer tag and forwards based on inner tag.
  - **Limitation:** Typically a one-way attack. Used for blind attacks or DoS.
  - **Mitigation:** Change default native VLAN ID; never add user devices to native VLAN.
- **2. Switch Spoofing (DTP Spoofing):**
  - **Mechanism:** Attacker impersonates a switch and uses DTP to negotiate a trunk port.
  - **Exploit:** If switch port is set to auto-negotiate trunking, it establishes a trunk link with attacker.
  - **Impact:** Attacker gains access to all VLANs on the trunk.
  - **Mitigation:** Disable dynamic trunking protocols (DTP) on all user-facing switch ports.
- **3. MAC Table Overflow (CAM Table Overflow / MAC Flooding):**
  - **Mechanism:** Attacker floods the switch's CAM table with fake MAC addresses.
  - **Exploit:** Switch "fails open" and acts like a hub, broadcasting all traffic to all ports.
  - **Impact:** Bypasses VLAN segmentation; all traffic becomes visible to attacker.
  - **Mitigation:** Port security, MAC address authentication, IDS.