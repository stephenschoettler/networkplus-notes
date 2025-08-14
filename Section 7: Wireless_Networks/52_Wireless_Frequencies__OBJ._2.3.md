## 💡 Wireless Frequencies (OBJ 2.3)

Wireless networks transmit data over specific radio frequency bands. Each band has different characteristics affecting speed, range, and performance.
**Frequency Band Trade-offs:**
- **2.4 GHz:** Best Range & Penetration | Slower Speed | High Interference
- **5 GHz:** Good Speed | Shorter Range | Less Interference
- **6 GHz:** Best Speed | Shortest Range | Least Interference

✅ **2.4 GHz Band**
- **Characteristics:**
  - **Longer Range:** Better at penetrating solid objects (walls, floors).
  - **Slower Speeds:** Lower data throughput compared to 5 GHz and 6 GHz.
  - **High Interference:** This band is crowded with many overlapping channels and interference from other devices (microwaves, cordless phones, Bluetooth).
- **Channels:**
  - Divided into 11-14 channels (depending on region), each 22 MHz wide.
  - **Significant Overlap:** Most channels interfere with each other.
  - **Non-Overlapping Channels:** In the US, only channels **1, 6, and 11** do not overlap and should be used to minimize interference.

✅ **5 GHz Band**
- **Characteristics:**
  - **Shorter Range:** Less effective at penetrating solid objects.
  - **Faster Speeds:** Higher data throughput due to more available bandwidth and wider channels.
  - **Less Interference:** More non-overlapping channels available (up to 24).
- **Channel Bonding:**
  - **Concept:** Merging two or more adjacent 20 MHz channels to create a wider channel (40 MHz, 80 MHz, or 160 MHz).
  - **Benefit:** Increases data throughput (more bandwidth).
  - **Trade-off:** Reduces the number of available non-overlapping channels, potentially increasing interference in dense environments.

✅ **6 GHz Band (Wi-Fi 6E)**
- **Characteristics:**
  - **Fastest Speeds:** Offers the most bandwidth and the fastest connections.
  - **Least Congestion:** A relatively new spectrum with many non-overlapping channels (up to 59).
  - **Shortest Range:** Has the least ability to penetrate solid objects.
  - **Use Case:** Ideal for high-density areas and applications demanding the highest speeds.

✅ **Key Wireless Management Features**
- **Dynamic Frequency Selection (DFS) & Transmit Power Control (TPC):**
  - Part of the **802.11h** standard, primarily for the 5 GHz band.
  - **DFS:** Requires devices to detect and avoid channels used by radar systems.
  - **TPC:** Allows devices to adjust their transmit power to the minimum required, reducing interference and power consumption.
- **Band Steering:**
  - **Concept:** A feature on dual-band or tri-band access points that encourages capable client devices to connect to the less congested and faster 5 GHz or 6 GHz bands, leaving the 2.4 GHz band for older devices.
  - **Benefit:** Optimizes overall network performance and efficiency.