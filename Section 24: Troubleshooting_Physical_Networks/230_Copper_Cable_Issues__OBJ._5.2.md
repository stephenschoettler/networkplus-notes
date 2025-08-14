## 💡 Copper Cable Issues (OBJ. 5.2)
This section addresses common issues encountered with copper network cables, including incorrect pinouts, bad ports, opens, and shorts, along with their causes, detection, and resolution methods.

✅ **Copper Cable Issues**
- **1. Incorrect Pinouts:**
  - **Definition:** Wires within a twisted-pair cable are not connected to the correct pins in the connector (patch panel, wall jack, or RJ445 connector).
  - **Standard:** TIA-568-B is a common wiring standard (e.g., white/orange, orange, white/green, blue, white/blue, green, white/brown, brown).
  - **Troubleshooting:**
    - Visual inspection of patch panel, wall jack, or RJ45 connector.
    - Use a **cable tester** or **wire mapping tool** to verify the pinout.
  - **Resolution:** Disconnect and re-punch wires, or replace the RJ45 connector.
- **2. Bad Ports:**
  - **Definition:** A faulty Ethernet port on a Network Interface Card (NIC), switch, or router.
  - **Troubleshooting:**
    - Use a **loopback plug** and specialized software to test the port.
  - **Resolution:**
    - For NICs: Replace the NIC or add an expansion card.
    - For switches/routers: Move the connection to another available port. For modular devices, replace the interface card.
- **3. Opens:**
  - **Definition:** A break in one or more wires within the cable, preventing signal transmission.
  - **Causes:** Disconnected cable, cut wire, broken wire.
  - **Troubleshooting:**
    - A **cable tester** will report an "open."
    - Test each segment of the connection (patch cable, wall jack, patch panel) to pinpoint the break.
- **4. Shorts:**
  - **Definition:** Two or more wires within the cable are accidentally connected together (touching).
  - **Causes:** Poorly made cable, wires touching inside an RJ45 connector, physical damage to the cable.
  - **Troubleshooting:**
    - A **cable tester** will report a "short."
    - Often caused by faulty RJ45 termination; try re-terminating the connector.
    - Visually inspect the entire cable for damage.
  - **Resolution:** Rewire the RJ45 connector, or replace the cable with a known good one.

✅ **Key Testing Tools**
- **Cable Tester / Wire Mapping Tool:** For incorrect pinouts, opens, and shorts.
- **Loopback Plug:** For testing bad ports on NICs, switches, or routers.