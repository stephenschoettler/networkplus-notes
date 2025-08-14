## 💡 Network Cable Limitations (OBJ. 5.2)
This section details the limitations and considerations for various network cable types, including twisted pair, coaxial, twinaxial, and fiber optic, along with their applications and environmental factors.

✅ **Network Cable Limitations & Considerations**
- **1. Twisted Pair Copper Cables (Ethernet Categories):**
  - **CAT 5 (100BASE-TX):** 100 Mbps up to 100m.
  - **CAT 5e (1000BASE-T):** 1 Gbps up to 100m.
  - **CAT 6 (1000BASE-T / 10GBASE-T):** 1 Gbps up to 100m; 10 Gbps up to 55m.
  - **CAT 6a (10GBASE-T):** 10 Gbps up to 100m.
  - **CAT 7 (10GBASE-T):** 10 Gbps up to 100m.
  - **CAT 8 (40GBASE-T):** 40 Gbps up to 30m.
  - **General Rule:** Max distance for most twisted pair is 100 meters due to attenuation.
- **2. Coaxial and Twinaxial Copper Cables:**
  - **Coaxial:** Up to 100 Mbps at 500m (Ethernet). Offers longer distance than twisted pair but lower speeds.
  - **Twinaxial:** Up to 10 Gbps at 5m (newer versions up to 100 Gbps at 7m). Used for short, high-speed connections.
- **3. Fiber Optic Cables:**
  - **General:** Uses light signals, immune to EMI. Offers much higher speeds and longer distances than copper.
  - **Multimode Fiber (MMF):** Shorter distances (e.g., 100 Mbps up to 2km, 1 Gbps up to 550m, 10 Gbps up to 400m).
  - **Singlemode Fiber (SMF):** Longer distances (e.g., 1 Gbps up to 5km, 10 Gbps up to 10km).
- **4. Cable Considerations:**
  - **Shielded Twisted Pair (STP) vs. Unshielded Twisted Pair (UTP):**
    - STP: Has foil shielding around pairs and/or overall cable. Provides better protection against EMI/RFI. More expensive, less flexible. Used in noisy environments (e.g., radio stations, factories).
    - UTP: No shielding. Inexpensive, easy to install, lightweight, flexible. Most common in LANs.
  - **Note:** Fiber is immune to EMI.
  - **Plenum vs. Riser Rated Cables:**
    - **Plenum Cables:** Used in air-handling spaces (e.g., above drop ceilings, under raised floors). Have a higher fire rating, made with fire-retardant plastic (low smoke PVC or FEP) to prevent toxic smoke/fumes. Can be used in riser spaces.
    - **Riser Cables:** Used for vertical runs between floors in a building (e.g., in risers or elevator shafts). Designed to prevent flame spread upwards. Cannot be used in plenum spaces (release smoke/chemicals when burned).
- **5. Cable Applications:**
  - **Rollover (Console) Cable:**
    - Purpose: Connects a computer terminal directly to a router's console port for out-of-band management.
    - Wiring: Typically flat, light blue. RJ45 on one end, often DB9 serial on the other.
  - **Crossover Cable:**
    - Purpose: Connects two similar Ethernet devices directly without a switch/router (e.g., PC to PC, router to router, switch to switch).
    - Wiring: TIA-568-B on one end, TIA-568-A on the other (transmit and receive pairs are swapped).
  - **Power over Ethernet (PoE):**
    - Purpose: Delivers both data and electrical power over a single twisted pair Ethernet cable.
    - Requirements: Requires CAT 5e or better cable.
    - Power Levels: Can provide 15.4W to 100W depending on PoE standard and number of twisted pairs used.
    - Distance: Limited to 100 meters like other Ethernet.