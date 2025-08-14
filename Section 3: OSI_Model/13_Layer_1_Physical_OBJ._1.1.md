## 💡 Layer 1: Physical Layer (OBJ 1.1)

The Physical Layer (Layer 1) is where **bits** (binary ones and zeros) are transmitted across the network. It includes all physical and electrical characteristics of the network (e.g., copper, fiber, radio frequency). You don't need to memorize TDM, StatTDM, and FDM specifics, but understand that multiplexing makes limited resources more efficient.

✅ **Bit Representation**
- Copper wire: Voltage levels (e.g., 0V for zero, +/-5V for one).
- Fiber optic: Light (light on for one, light off for zero).
- **Transition Modulation:** Switching between modes to represent bits.

✅ **Cabling and Connectors**
- RJ45 connectors for Cat 5/6 cables.
- Wiring standards: TIA/EIA-568A and TIA/EIA-568B.
- **Crossover Cable:** One end A standard, one end B standard (flips transmit/receive bits).
- **Straight-through Cable (Patch Cable):** Both ends B standard.

✅ **Physical Topology**
- How devices are physically cabled together (e.g., bus, ring, star, mesh). This is a Layer 1 issue.

✅ **Communication Synchronization**
- How the receiving end knows when to accept bits.
- **Asynchronous Communication:** Uses start and stop bits; communication happens out of sync (like voicemail).
- **Synchronous Communication:** Uses a common time source (clock) for real-time communication.

✅ **Bandwidth Utilization**
- **Broadband:** Divides bandwidth into separate channels (e.g., cable TV with multiple channels).
- **Baseband:** Uses all of the frequency of the cable all of the time (e.g., wired Ethernet, telephone).

✅ **Multiplexing (for Baseband)**
- Allows multiple users to share a single baseband connection more efficiently.
- **Time-Division Multiplexing (TDM):** Each session takes turns using dedicated time slots.
- **Statistical Time-Division Multiplexing (StatTDM):** Dynamically allocates time slots based on necessity (more efficient than TDM).
- **Frequency-Division Multiplexing (FDM):** Splits the medium into channels based on frequency (similar to broadband).

✅ **Layer 1 Devices**
- **Cables:** Fiber optic, Ethernet, coaxial.
- **Wireless Media:** Bluetooth, Wi-Fi, NFC (radio frequencies).
- **Infrastructure Devices:**
  - **Hubs:** "Dumb" devices that simply repeat whatever they receive to all other ports.
  - **Access Points:** (Can operate at Layer 1 for basic signal transmission).
  - **Media Converters:** Convert signals from one media type to another (e.g., coaxial to fiber).
- Layer 1 devices are "dumb" repeaters; they have no logic or intelligence.