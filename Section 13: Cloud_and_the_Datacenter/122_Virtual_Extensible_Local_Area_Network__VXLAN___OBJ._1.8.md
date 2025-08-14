## 💡 Virtual Extensible Local Area Network (VXLAN) (OBJ 1.8)

VXLAN is a network virtualization technology that encapsulates Ethernet (Layer 2) frames within UDP (Layer 3) packets. Its purpose is to address the scalability limitations of traditional VLANs (limited to 4,096 unique VLAN IDs).

✅ **Mechanism**
- Extends Layer 2 networks over a Layer 3 infrastructure (LAN, WAN, Internet).
- Encapsulates Layer 2 Ethernet frames inside Layer 3 UDP packets.
- Each VXLAN packet includes a 24-bit VXLAN Network Identifier (VNI), supporting over 16 million virtual networks.

✅ **Components**
- **1. VTEPs (VXLAN Tunnel End Points):** Perform encapsulation/de-encapsulation. Implemented in hypervisors or physical switches.
- **2. VXLAN Segment:** A Layer 2 network overlaid onto a Layer 3 network, identified by a unique VNI.

✅ **Benefits of VXLAN**
- **1. Scalability:** Supports over 16 million virtual networks.
- **2. Flexibility:** Extends Layer 2 networks across different data centers/cloud environments over Layer 3.
- **3. Improved Utilization:** More efficient use of network paths and bandwidth.

✅ **Challenges and Considerations**
- **Complexity:** Requires understanding of Layer 2, Layer 3, and network overlays.
- **Overhead:** Encapsulation/de-encapsulation can introduce latency and increase packet size.
- **Multicast Support:** Requires multicast support in the underlying network.
- **Mitigation:** Management and orchestration tools can automate configuration.