## 💡 Wireless Coverage Issues (OBJ. 5.4)
This section addresses common wireless coverage issues, including insufficient signal strength and dead zones, and explores various solutions to extend and optimize wireless network coverage.

✅ **Wireless Coverage Issues**
- **Wireless Coverage:** The physical area around a wireless transmitter where there is sufficient signal strength for a wireless device to operate.
- **Measurement:**
  - **RSSI (Received Signal Strength Indicator):** Measured from the client device (in decibels, more negative = weaker).
  - **EIRP (Effective Isotropic Radiated Power):** Measured from the Access Point (AP) (in dBi).
  - **Site Surveys:** Generate heat maps to visualize signal strength (green = strong, red = weak).

✅ **Insufficient Wireless Coverage Issues**
- **Problem:** Wireless signal is too weak in certain areas.
- **Causes:**
  - **Distance:** Signal strength decreases with distance from the AP.
  - **Physical Obstacles:** Walls, floors, and other building materials attenuate the signal.
- **Symptoms:** Low RSSI, intermittent connectivity, dropped connections, inability to connect.

✅ **Solutions to Extend Wireless Coverage**
- **1. Signal Boosters:** Increase the power of the transmitted signal.
- **2. Stronger Antennas:** Use antennas with a higher dBi rating (e.g., replacing a 5 dBi antenna with a 9 dBi antenna can double the range under ideal conditions).
- **3. Wireless Repeaters:**
  - A Layer 1 device with two radios.
  - Receives a weak signal, boosts it, and retransmits it at full strength.
  - Extends coverage into additional areas.
- **4. Extended Service Set (ESS) / Multiple Access Points (APs):**
  - Deploy multiple APs throughout the coverage area.
  - APs are typically connected via wired Ethernet backhaul.
  - Each AP operates on a different non-overlapping channel (e.g., 1, 6, 11 in 2.4 GHz) to minimize interference.
  - Allows seamless roaming between APs.
- **5. Wireless Mesh Systems:**
  - Combine repeaters and APs into a single device.
  - Rely on internal wireless radios for backhaul between mesh nodes (no need for wired Ethernet to each node).
  - Provides full-house coverage for larger homes/offices.