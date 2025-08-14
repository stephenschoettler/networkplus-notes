## 💡 Cable Distribution Systems (OBJ 2.4)

A **Cable Distribution System** is an organized system to connect the network's backbone (MDF) to intermediate distribution frames (IDFs) and then to end-user wall jacks. It is designed hierarchically for safe, secure, and functional placement. A best practice is to connect wall jacks to patch panels, then use patch cables from the patch panel to the switch. This protects expensive switch ports from wear and tear.

✅ **Components of a Cable Distribution System**
- **1. Demarcation Point (Demarc):**
  - Location where the Internet Service Provider's (ISP) connection ends and your network infrastructure begins.
  - Signifies the entrance of the Wide Area Network (WAN) connection into your facility.
  - ISP is responsible up to this point; your organization is responsible beyond it.
  - Often located in the Main Distribution Frame (MDF).
- **2. Main Distribution Frame (MDF):**
  - Main starting point for all interior cabling distributed throughout the building.
  - All other telecommunications closets (IDFs) connect back to the MDF.
  - Contains the main point of presence router and the **backbone switch**.
- **3. Intermediate Distribution Frame (IDF):**
  - Smaller distribution frames that connect back to the MDF.
  - Houses equipment to support offices and workstations closest to it (e.g., edge switches).
  - Cabling runs from IDFs to individual offices and wall jacks.
- **4. Cable Trays:**
  - Units or assemblies that form a rigid structural system to support cables and raceways.
  - Used for horizontal cable runs (e.g., in drop ceilings or under raised floors).
- **5. Vertical Cross-Connect:**
  - Used for vertical cable runs between floors.
  - Best practice is to minimize vertical runs, typically using trunk cables to connect MDF to IDFs.
- **6. Racks:**
  - House network equipment (switches, routers, patch panels, servers).
  - **Types:**
    - **2-post racks:** For lighter equipment, patch panels, cabling.
    - **4-post racks:** For heavier equipment (servers, UPS, large network hardware).
    - **Wall-mounted racks:** Space-saving for smaller equipment, ideal for limited floor space or edge switches.
    - **Rack enclosures (full cabinet racks):** Fully enclosed, secure, and protected environment for high-value equipment; often lockable.
- **7. Wall Jacks:**
  - Connect end-user devices to the network.
  - Normally configured for RJ-45 (copper) but can be fiber wall jacks.
- **8. Patch Panels:**
  - Device with multiple jacks for connecting and routing circuits.
  - **Purpose:** Keeps data centers/server rooms organized, makes it easier to move, add, or change cabling infrastructure.
  - **Copper Patch Panels:**
    - Front: RJ-45 network ports.
    - Back: 110 punchdown block (for CAT5/newer copper cables).
    - Uses a **punchdown tool** to terminate cables.
  - **Fiber Distribution Panels:**
    - Use fiber connectors (SC, LC, ST, MTRJ) on both front and back.
    - Act as couplers for fiber cables.
    - Can convert one type of fiber connection to another.

✅ **Cable Distribution Flow (Example)**
- Computer connects to wall jack (RJ-45 or fiber patch cable).
- Wall jack's cable runs through walls/ceilings/trays to the IDF.
- Cable terminates into a punchdown block on the back of a patch panel in the IDF.
- Another patch cable connects the front of the patch panel to an open port on the edge switch in the IDF.

✅ **Benefits of a well-designed cable distribution system**
- Hierarchical and organized structure.
- Easier support and maintenance.
- Increased flexibility for moves, adds, and changes.
- Protects expensive network equipment.