## 💡 Collisions and Broadcast Storms (OBJ. 5.4)
This section explains network collisions and broadcast storms, their causes, and methods for detection and prevention to maintain network performance.

✅ **Collisions**
- **Definition:** Occur when two hosts transmit data simultaneously on a shared network medium, making signals unreadable.
- Occur in both wired (CSMA/CD) and wireless (CSMA/CA) networks.
- **Collision Domain:** Network segment where simultaneous transmissions can collide.
  - Hubs: All devices on a hub are in one collision domain.
  - Switches (Layer 2 devices): Each switch port is its own collision domain, preventing collisions between the switch and the connected device.
- **Detection:**
  - Network performance degradation.
  - `show interface` command on network devices:
    - **Collision counter increasing:** Indicates collisions (expected on hubs, problematic on switches).
    - **Deferred counter increasing:** Interface found carrier busy on first attempt (normal on hubs, problematic on switches).
    - **Late collisions:** Collision detected after 5.12 microseconds (indicates issues like incorrect cabling, bad NIC, too many hubs).
    - **Excessive collisions:** Device gives up retransmitting after 16 attempts and drops the frame.
- **Prevention/Mitigation:**
  - Use switches to create smaller collision domains.
  - Turn off auto-negotiation for speed/duplex; hardcode to lower speed and half-duplex if excessive collisions persist (e.g., due to NIC issues or too many clients).

✅ **Broadcast Storms**
- **Definition:** Network overwhelmed by continuous multicast or broadcast traffic.
- **Impact:** Rapid network performance decrease, potential Denial of Service (DoS).
- **Broadcast Addresses:**
  - Layer 2: `FF:FF:FF:FF:FF:FF`
  - Layer 3: `255.255.255.255`
- **Broadcast Domain:** Logical network division where all nodes can reach each other via broadcast at Layer 2.
  - Layer 2 devices (switches): Do NOT break up broadcast domains.
  - Routers or Layer 3 switches: Break up broadcast domains.
- **Causes:**
  - **Too Large Broadcast Domain:** Too many clients in a single broadcast domain (e.g., large flat networks with many switches).
  - **High Volume of DHCP Requests:** Many new hosts attempting to get IP addresses simultaneously (e.g., after a network device reboot).
  - **Switching Loops:** Unintentional loops created by mis-cabled unmanaged switches.
- **Identification:**
  - Rapidly increasing packet counters (especially broadcast packets).
  - Exponential rise in packet loss.
  - Packet analyzers (e.g., Wireshark, TCPdump) showing excessive broadcast/multicast traffic.
- **Prevention:**
  - Implement loop prevention (e.g., enable BPDUs on managed switches).
  - Limit the number of MAC addresses per port (port security).
  - Break up large broadcast domains into smaller ones using routers or multilayer switches.