## 💡 Interference Issues (OBJ. 5.4)
This section addresses common interference issues in wireless networks, including channel interference, attenuation, and multi-path reception, along with their causes and mitigation strategies.

✅ **Interference Issues in Wireless Networks**
- **1. Channel Interference:**
  - **Definition:** Occurs when multiple wireless networks communicate on the same channel, leading to signal overlap.
  - **2.4 GHz Spectrum:** Only three non-overlapping channels (1, 6, 11). Using overlapping channels (e.g., 4 and 6) causes interference.
  - **Impact:** Retransmissions, network slowdowns, data corruption, complete frame loss, unusable network.
  - **Prevention:**
    - **Site Surveys:** Identify channels already in use in the area.
    - **Channel Planning:** In 2.4 GHz, use only channels 1, 6, and 11. Ensure no two access points using the same channel are adjacent or overlapping significantly.
    - **Overlap:** Aim for 10-15% overlap between APs for seamless handoff.
    - **5 GHz Spectrum:** Utilize the 5 GHz band (if possible) as it offers more non-overlapping channels (e.g., 24 channels), significantly reducing interference.
- **2. Attenuation:**
  - **Definition:** Reduction of signal strength between the transmission and receipt of a wireless signal.
  - **Causes:**
    - **Distance:** Signal weakens with increased distance from the transmitter.
    - **Physical Obstacles:** Walls, trees (leaves), snow, heavy rain can absorb or block wireless signals.
    - **Signal Interference/Noise:** Other devices operating on the same or adjacent frequencies.
    - **Antenna/Cable Quality:** Low-quality materials or construction in antennas/cables can lead to higher resistance and more attenuation.
  - **Impact:** Reduced signal strength (lower RSSI), lower data throughput.
  - **Troubleshooting:** Replace low-quality cables or antennas with higher quality, lower-resistance components.
- **3. Multi-path Reception:**
  - **Definition:** Occurs when a wireless signal bounces off objects (e.g., walls) and arrives at the receiver via multiple paths and at different times.
  - **Impact:** Can lead to signal degradation and contribute to attenuation, leading to lower RSSI and reduced throughput.