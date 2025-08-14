## 💡 Virtual Local Area Network (VLAN) (OBJ 2.2)

A VLAN is a **logical subdivision** of a network that segments it into separate **broadcast domains**. VLANs allow you to group hosts together logically, even if they are not connected to the same physical switch. This is achieved through software configuration rather than physical cabling. VLANs are a fundamental tool for network administrators, providing a flexible and powerful way to segment networks, enhance security, improve performance, and manage resources more efficiently.

✅ **Why Use VLANs?**
- **Enhanced Security:**
  - Isolates sensitive data (e.g., HR department) from other parts of the network.
  - Traffic between VLANs must be routed through a Layer 3 device (router or Layer 3 switch), allowing for the application of Access Control Lists (ACLs) to filter traffic.
- **Improved Performance:**
  - Reduces the size of broadcast domains, which decreases unnecessary broadcast traffic and improves overall network performance.
- **Increased Management:**
  - Provides greater control over network management by allowing for separate policies and controls to be applied to different VLANs.
- **Improved Cost Efficiency:**
  - Allows for better utilization of existing network infrastructure by logically segmenting a single physical switch into multiple virtual switches, reducing the need for additional hardware.

✅ **How VLANs Work: Key Concepts**
- **1. VLAN Tagging (802.1Q):**
  - **Mechanism:** As a data frame passes through a VLAN-aware switch, a **VLAN tag** (VLAN ID) is added to the frame.
  - **Purpose:** This tag identifies which VLAN the frame belongs to, ensuring it is only forwarded to ports that are members of the same VLAN.
  - **VLAN Trunking:** A single physical link between switches (a "trunk") can carry traffic for multiple VLANs by using these tags.
- **2. VLAN Database:**
  - **Purpose:** Switches maintain a VLAN database that stores all VLAN configurations for that switch.
  - **Cisco Example:** On Cisco switches, this database is stored in a file named `VLAN.DAT`.
- **3. Switch Virtual Interface (SVI):**
  - **Purpose:** A virtual Layer 3 interface on a switch that allows it to perform **inter-VLAN routing** (routing traffic between different VLANs) without the need for a separate, external router.
  - **Function:** The SVI acts as the default gateway for devices within its associated VLAN.