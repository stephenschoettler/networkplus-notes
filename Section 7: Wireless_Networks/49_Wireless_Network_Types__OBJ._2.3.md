## 💡 Wireless Network Types (OBJ 2.3)

Wireless networks offer flexibility and scalability by eliminating the need for physical cables.

✅ **Four Main Wireless Network Types**
- **1. Ad Hoc Network (IBSS - Independent Basic Service Set):**
  - **Concept:** Devices connect directly to each other in a peer-to-peer (P2P) fashion without a centralized access point.
  - **Use Case:** Creating quick, temporary networks for tasks like file sharing between two devices.
  - **Limitation:** Typically does not provide internet access as it's isolated from other networks.
- **2. Infrastructure Network:**
  - **Concept:** Devices connect to a central **Wireless Access Point (WAP)**, which bridges the wireless clients to a wired LAN.
  - **Terminology:**
    - **BSSID (Basic Service Set Identifier):** The MAC address of a single WAP.
    - **SSID (Service Set Identifier):** The common, human-readable name of the wireless network (e.g., "DionTraining").
    - **ESS (Extended Service Set):** A configuration with two or more WAPs sharing the same SSID to provide broader coverage.
    - **ESSID (Extended Service Set Identifier):** The SSID used in an ESS configuration.
  - **Use Case:** The most common type of wireless network in homes and offices.
- **3. Point-to-Point (P2P) Wireless Network:**
  - **Concept:** Connects two distinct, fixed locations over longer distances using high-gain directional antennas.
  - **Use Case:** Linking buildings within a campus or providing internet access where cabling is not feasible (e.g., using microwave links).
- **4. Mesh Network:**
  - **Concept:** Each node (access point) can connect to multiple other nodes, creating multiple redundant paths for data.
  - **Characteristics:**
    - **Self-healing:** Can automatically reroute traffic around broken or blocked paths, making it highly resilient and reliable.
    - **Versatile:** Can combine different wireless technologies (Wi-Fi, cellular, microwave, satellite) into a single network.
  - **Use Case:** Large-scale deployments where cabling is impractical (e.g., smart cities, disaster relief operations).

✅ **Autonomous vs. Lightweight Access Points**
- **1. Autonomous Access Point:**
  - **Concept:** A standalone device containing all the intelligence to handle wireless networking functions independently.
  - **Configuration:** Each AP is configured individually.
  - **Use Case:** Small setups, home networks.
- **2. Lightweight Access Point:**
  - **Concept:** A "dumb" access point that offloads most processing and decision-making to a central **Wireless LAN Controller (WLC)**.
  - **Configuration:** Managed centrally by the WLC.
  - **Use Case:** Large enterprise networks with multiple access points, allowing for easier management and global policy updates.