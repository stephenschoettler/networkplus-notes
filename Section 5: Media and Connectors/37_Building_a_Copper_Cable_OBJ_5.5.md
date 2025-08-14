## 💡 Building a Copper Cable (OBJ 5.5)

This lesson discusses how to wire copper cables (specifically twisted pair) into RJ45 connectors, focusing on the TIA/EIA-568A and TIA/EIA-568B standards for creating straight-through and crossover cables. You must memorize both the 568A and 568B pinouts. Be prepared for simulation questions where you might need to drag and drop wire colors to the correct pins for straight-through or crossover cables. Remember the DTE/DCE rule and the specific requirement for crossover cables between like devices (e.g., switch to switch) for the exam, unless MDIX is specified.

✅ **Straight-Through Cable (Patch Cable)**
- **Definition:** Has the exact same pinouts on both ends of the cable. Pin 1 on one side connects to Pin 1 on the other side, and so on.
- **Standard:** Most commonly uses the **568B to 568B** wiring scheme.
- **568B Pinout (from Pin 1 to 8):** Orange/White, Orange, Green/White, Blue, Blue/White, Green, Brown/White, Brown.
- **Usage:** Connects a **DTE (Data Terminal Equipment)** to a **DCE (Data Communications Equipment)**, or a DCE to a DTE.
  - **DTE:** Endpoint devices (laptops, desktops, servers, routers).
  - **DCE:** Communication devices (switches, modems, hubs, bridges).
- Example: Computer to Switch.

✅ **Crossover Cable**
- **Definition:** Swaps the send and receive pins on the other end of the cable.
- **Standard:** Uses **568B on one end and 568A on the other end**.
- **568A Pinout (from Pin 1 to 8):** Green/White, Green, Orange/White, Blue, Blue/White, Orange, Brown/White, Brown. (Essentially, the orange and green pairs swap places compared to 568B).
- **Usage:** Connects a **DTE to a DTE** or a **DCE to a DCE**.
- Example: Computer to Computer, Switch to Switch.
- **MDIX (Medium Dependent Interface Crossover):** Most modern switches have MDIX, which automatically detects and corrects for straight-through cables being used where a crossover cable is needed. However, **for the exam, assume switches do NOT support MDIX unless explicitly stated.** Therefore, a switch-to-switch connection requires a crossover cable for the exam.

✅ **Tools for Building Copper Cables**
- **RJ45 Connectors:** The plastic ends that attach to the cable.
- **Wire Stripper:** Used to remove the outer sheath of the cable to expose the twisted pairs.
- **RJ45 Crimper:** Used to cut the cable, push the wires into the connector, and crimp the connector onto the cable.
- **Cable Tester:** Used to verify the pinout and connectivity of the newly made cable.

✅ **Cable Length Limitation**
- Cat5/Cat6 cables have a maximum effective length of **100 meters** (328 feet) before signal degradation occurs. It's recommended to keep runs under 90 meters for leeway.