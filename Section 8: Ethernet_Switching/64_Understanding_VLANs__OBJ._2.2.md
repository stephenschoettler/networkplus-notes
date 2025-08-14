## 💡 Understanding VLANs (OBJ 2.2)

This lesson demonstrates how VLANs logically segment a network into separate broadcast domains using a graphical user interface (GUI) VLAN viewer. It shows how VLANs are created, assigned unique IDs, and how physical switch ports are configured to belong to specific VLANs, enabling logical separation on a single physical switch.

✅ **VLAN Creation and Overview**
- **Default VLAN:** All ports are initially part of a default VLAN (e.g., VLAN 1).
- **Creating Custom VLANs:**
  - Assign a descriptive name (e.g., "Instructors", "Student Support", "Executives").
  - Assign a unique VLAN ID (e.g., 100, 101, 200, 300, 301).
  - Enable **network isolation** for each custom VLAN to prevent inter-VLAN communication by default.
  - Apply content filtering policies (e.g., "Work") as needed.

✅ **VLAN Assignment to Physical Ports (VLAN Viewer)**
- **Purpose:** To control which VLANs are active on each physical port of the switch.
- **Port Configuration:**
  - **Native VLAN (Untagged):**
    - The primary VLAN for a port. Any untagged traffic entering this port is assigned to this VLAN.
    - Example: Assigning "Instructors" (VLAN 100) as the native VLAN for a specific port means only devices belonging to VLAN 100 can connect to it.
  - **Tagged VLANs:**
    - Allows traffic from multiple additional VLANs to pass through the same port. Traffic for these VLANs is "tagged" with their respective VLAN IDs.
    - Example: A port configured for "Instructor VOIP" (VLAN 101) as native, and "Instructors" (VLAN 100) as tagged, allows both a VoIP phone (untagged voice traffic) and a computer (tagged data traffic) to share the same physical port, logically separating their traffic.
  - **Blocking:** By default, all other VLANs are blocked on a port unless explicitly allowed as native or tagged, enforcing network segmentation.

✅ **Logical Segmentation on a Single Switch**
- By configuring native and tagged VLANs on different ports, a single physical switch can host multiple virtual networks.
- This allows for logical separation of departments or traffic types (e.g., data vs. voice) even if they share the same physical hardware.
- Communication between isolated VLANs requires a Layer 3 device (router or Layer 3 switch) to perform inter-VLAN routing.
