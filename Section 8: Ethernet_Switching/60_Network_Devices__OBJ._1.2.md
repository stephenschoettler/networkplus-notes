## 💡 Network Devices (OBJ 1.2)

Understanding the function and evolution of these devices (Hubs, Bridges, Switches, and Routers) is key to understanding modern networking. On the CompTIA exam, unless specified otherwise: a **"switch"** refers to a **Layer 2 device** that forwards based on MAC addresses. A **"router"** refers to a **Layer 3 device** that forwards based on IP addresses. Only consider a switch to have Layer 3 capabilities if the question explicitly calls it a **"Layer 3 switch"** or **"multilayer switch"**.

✅ **Device Evolution and Function**
- **1. Hub (Layer 1 - Physical):**
  - **Function:** A multi-port repeater. Any signal received on one port is regenerated and sent out to *all* other ports.
  - **Collision Domain:** Creates a **single, large collision domain**. All connected devices share the same bandwidth and are prone to collisions.
  - **Broadcast Domain:** Creates a **single broadcast domain**.
  - **Modern Use:** Obsolete; replaced by switches.
- **2. Bridge (Layer 2 - Data Link):**
  - **Function:** Connects two network segments. It learns the MAC addresses of devices on each segment and makes intelligent forwarding decisions based on the destination MAC address.
  - **Collision Domain:** **Breaks up collision domains**. Traffic between devices on the same segment does not cross the bridge.
  - **Broadcast Domain:** Forwards broadcast traffic, so it does **not** break up broadcast domains.
- **3. Switch (Layer 2 - Data Link):**
  - **Function:** A multi-port bridge. It learns the MAC address of each connected device and forwards frames only to the port connected to the destination device.
  - **Collision Domain:** **Each port is its own separate collision domain**. This eliminates collisions and allows for full-duplex communication.
  - **Broadcast Domain:** Operates within a **single broadcast domain**. All broadcast traffic is forwarded to all ports.
- **4. Router (Layer 3 - Network):**
  - **Function:** Connects dissimilar networks (e.g., LAN to WAN). Makes forwarding decisions based on Layer 3 IP addresses.
  - **Collision Domain:** Each port is its own collision domain.
  - **Broadcast Domain:** **Each port is its own separate broadcast domain**. Routers do **not** forward broadcast traffic by default, which is a key function for segmenting networks.
- **5. Layer 3 Switch (Multilayer Switch):**
  - **Function:** Combines the functionality of a Layer 2 switch and a Layer 3 router in a single device. Can perform routing functions.
  - **Collision & Broadcast Domains:** Each port is its own collision domain AND its own broadcast domain.
  - **Use Case:** Often used in enterprise networks for inter-VLAN routing.