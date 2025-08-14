## 💡 Understanding Network Devices (OBJ 1.2)

Many devices, especially in Small Office/Home Office (SOHO) environments, are **combination devices** that integrate multiple network functions into a single box. For the CompTIA Network+ exam, it's crucial to understand the distinct function of each device, regardless of how they are marketed or combined. A **"wireless router"** is a combination device. A **"wireless access point"** is a Layer 2 device that provides wireless connectivity. A **"switch"** is a Layer 2 device for wired connectivity. A **"router"** is a Layer 3 device for connecting different networks.

✅ **The "All-in-One" Wireless Router**
- A typical device marketed as a "wireless router" is often a combination of four distinct devices:
  - **1. Router:** Connects the internal LAN to the external WAN (internet) and makes Layer 3 routing decisions.
  - **2. Switch:** Provides multiple Ethernet ports for connecting wired devices on the LAN.
  - **3. Wireless Access Point (WAP):** Provides Wi-Fi connectivity for wireless devices.
  - **4. Media Converter:** Converts the signal from one media type to another (e.g., from the coaxial cable of a cable modem to the Ethernet used by the internal switch).

✅ **Standalone Network Components**
- **1. Media Converter:**
  - **Purpose:** Converts a signal from one physical media type to another.
  - **Example:** An HDMI to Ethernet converter allows sending video signals over long distances using Cat5/Cat6 cable, which has a longer range than HDMI cable.
- **2. Switch:**
  - **Purpose:** Connects multiple devices on a LAN, forwarding traffic based on MAC addresses.
  - **Unmanaged Switch:** A simple, "dumb" switch that provides basic connectivity without advanced features like VLANs. Each port is a separate collision domain.
- **3. Wireless Access Point (WAP):**
  - **Purpose:** A true WAP is simply a media converter that bridges a wired Ethernet network to a wireless network.
  - **Distinction:** A standalone WAP typically has only one Ethernet port to connect to the main network, whereas a combination "wireless router" has multiple switch ports.