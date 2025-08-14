## 💡 Fiber Cable Issues (OBJ. 5.2)
This section addresses common issues encountered with fiber optic cables, including incorrect transceivers, reversed transmit/receive connections, and dirty optical cables, along with their troubleshooting and resolution.

✅ **Fiber Cable Issues**
- **1. Incorrect Transceivers:**
  - **Transceiver:** A device combining a transmitter and receiver, used to convert network connections (e.g., fiber to electrical). Operates at OSI Layer 1.
  - **Problem:** Using the wrong type of SFP (Small Form-Factor Pluggable) transceiver for the specific fiber cable or connection type (e.g., longwave SFP with shortwave fiber).
  - **Impact:** Data loss, loss of connectivity.
  - **Troubleshooting:** Ensure the correct transceiver model is used for the device and the associated cabling. Many are hot-pluggable for easy replacement.
- **2. Transmit/Receive (TX/RX) Reversed:**
  - **Problem:** The transmit cable from one device is connected to the transmit port of another, and vice-versa (instead of transmit to receive). Common in fiber connections with two separate cables.
  - **Impact:** No valid link or connection established.
  - **Troubleshooting:**
    - Physically swap the TX and RX cables at one end of the connection.
    - Check LED link activity lights on the Network Interface Card (NIC) or switch port to confirm link establishment.
- **3. Dirty Optical Cables:**
  - **Problem:** Dust, dirt, or fingerprints on the end faces of fiber optic cables or connectors. Even small particles can block light.
  - **Impact:** Major performance issues, connection problems, signal blockage.
  - **Detection:**
    - Large amount of errors over the fiber connection.
    - Performance slowdowns.
    - Fiber light meter (compares decibel reading to a clean baseline).
  - **Cleaning Methods:**
    - **Dry Cleaning:** Use a dry cleaning cloth with light pressure to remove dust/dirt. Can be used for cable ends or ports.
    - **Wet Cleaning:** Use a lint-free cloth lightly moistened with fiber optic cleaning solution (e.g., 91%+ isopropanol alcohol). Effective for removing oil residues like fingerprints.