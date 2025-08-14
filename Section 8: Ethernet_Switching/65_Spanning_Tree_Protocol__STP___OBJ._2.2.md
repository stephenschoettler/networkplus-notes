## 💡 Spanning Tree Protocol (STP) (OBJ 2.2)

STP (IEEE 802.1d) is a Layer 2 protocol that prevents switching loops by logically blocking redundant paths while keeping them available as backups in case a primary link fails. In networks with redundant physical links between switches (for high availability), switching loops can occur. A loop can cause a **broadcast storm**, where broadcast frames are endlessly forwarded between switches, consuming all available bandwidth and crashing the network. STP ensures network reliability by allowing for redundant physical paths while preventing the logical loops that would otherwise cause broadcast storms. It achieves this by electing a root bridge and then logically blocking redundant paths, which can be automatically unblocked if a primary path fails.

✅ **How STP Works: Building a Loop-Free Topology**
- **1. Elect a Root Bridge:**
  - One switch in the network is elected as the **Root Bridge**, which acts as the central reference point.
  - The switch with the **lowest Bridge ID (BID)** becomes the root.
  - **Bridge ID = Priority Value + MAC Address**. If priorities are equal, the switch with the lowest MAC address wins.
- **2. Determine Port Roles:**
  - **Root Port:** Every non-root bridge selects one **Root Port**, which is the port with the lowest-cost path back to the Root Bridge.
  - **Designated Port:** Every network segment has one **Designated Port**, which is the port on that segment with the lowest-cost path to the Root Bridge. All ports on the Root Bridge are designated ports.
  - **Non-Designated (Blocking) Port:** Any port that is not a Root Port or a Designated Port is put into a **blocking state**. This is the port that breaks the loop. It does not forward data frames but still listens for STP messages (BPDUs).

✅ **STP Port States (Transition Process)**
- When the network topology changes (e.g., a link fails), a blocked port may need to transition to a forwarding state. It goes through these states:
  - **1. Blocking:** Port is logically disabled to prevent loops. It only listens for BPDUs.
  - **2. Listening:** The port listens to BPDUs to determine its role in the spanning tree. No data is forwarded.
  - **3. Learning:** The port learns the MAC addresses of devices on its segment and populates its MAC address table. No data is forwarded.
  - **4. Forwarding:** The port is fully operational and forwards data frames.

✅ **Link Cost**
- **Concept:** STP uses a "cost" value to determine the best path to the root bridge.
- **Inverse Relationship:** **Faster link speed = Lower cost**.
- **Example:** A 10 Gbps link has a lower cost than a 1 Gbps link, so STP will prefer the 10 Gbps path.