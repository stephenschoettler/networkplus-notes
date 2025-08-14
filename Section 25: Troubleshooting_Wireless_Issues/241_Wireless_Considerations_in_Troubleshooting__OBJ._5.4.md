## 💡 Wireless Considerations in Troubleshooting (OBJ. 5.4)
This section delves into various wireless considerations crucial for effective troubleshooting, including antenna types, channel utilization, site surveys, and access point association times.

✅ **Wireless Considerations in Troubleshooting**
- **1. Antennas:**
  - **Omnidirectional:** Radiates RF waves in all directions equally (e.g., typical indoor APs). Signal strength (RSSI) decreases with distance.
  - **Dipole (Bi-directional):** Radiates in two directions.
  - **Yagi (Unidirectional):** Focuses RF waves in one direction, allowing longer distances with less power (e.g., site-to-site links).
  - **Parabolic Grid/Dish (Unidirectional):** Similar to Yagi, for longer site-to-site distances.
  - **Placement:**
    - Outdoor (site-to-site): Unidirectional (Yagi/Parabolic) with clear Line of Sight (LoS). Environmental factors (trees, snow, rain) can block LoS.
    - Indoor: Omnidirectional (ceiling mount) or unidirectional patch (wall mount, facing inward).
  - **Polarization:** Orientation of the electric field (vertical or horizontal).
    - Most Wi-Fi uses vertical polarization (antennas pointing upward).
    - Mismatch can cause poor RSSI even when close to AP. Try flipping antenna orientation.
- **2. Channel Utilization:**
  - **Definition:** Measure of airtime utilization for a specific frequency/channel.
  - **Ideal:** Keep under ~30% for fast wireless.
  - **Impact of High Utilization:** Collisions, data corruption/loss, slower speeds due to devices waiting to transmit.
  - **CSMA/CA (Collision Avoidance):** "Listen before talk" approach. Devices perform Clear Channel Assessment (CCA) and random back-off if channel is busy.
- **3. Site Surveys:**
  - **Purpose:** Planning and designing wireless networks for optimal coverage, data rates, capacity, roaming, and QoS.
  - **Information Gathered:** AP locations, power levels (EIRP), overlapping coverage, other networks on same channels.
  - **Benefits:** Identify less busy channels, determine need for frequency band upgrades (e.4 GHz to 5 GHz for more non-overlapping channels), ensure proper coverage, identify physical obstacles.
- **4. Wireless Access Point Association Times:**
  - **Process (7 steps):**
    - 1. Client sends probe request.
    - 2. AP responds with probe response (if compatible).
    - 3. Client sends 802.11 authentication frame.
    - 4. AP acknowledges authentication.
    - 5. Client sends association request.
    - 6. AP processes and responds with association ID (success).
    - 7. Client performs data transfer (after DHCP IP assignment).
  - **Factors Affecting Time:** Network load, signal strength.
  - **Speeding Up Association:** Clients in high signal strength (high RSSI) areas will associate faster.