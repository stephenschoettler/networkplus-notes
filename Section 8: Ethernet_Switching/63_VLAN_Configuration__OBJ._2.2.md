## 💡 VLAN Configuration (OBJ 2.2)

This lesson demonstrates how to create and configure VLANs on a modern SOHO router with a graphical user interface (GUI). The goal is to logically separate a network into different broadcast domains based on departmental functions (e.g., Instructors, Student Support, Executives). VLANs are created logically and then applied to physical switch ports. By assigning native and tagged VLANs to ports, you can control which devices and types of traffic can access different network segments, even when using the same physical switch. While this demonstration uses a GUI, the core concepts of creating VLANs, assigning IDs, and configuring port membership (native/tagged) are the same when using the command-line interface (CLI) on enterprise-grade switches.

✅ **Creating a New VLAN**
- **1. Navigate to Network Settings:** Access the VLAN configuration section of the router's management interface.
- **2. Create New Virtual Network:**
  - **Name:** Assign a descriptive name (e.g., "Instructors").
  - **VLAN ID:** Assign a unique number (e.g., 100). It's good practice to use a logical numbering scheme (e.g., 100s for Instructors, 200s for Support).
  - **Isolation:** Enable network isolation to prevent traffic from flowing between this VLAN and others by default.
  - **Content Filtering:** Apply specific security policies (e.g., "Work") if the device supports it.

✅ **Assigning VLANs to Switch Ports**
- **Purpose:** To control which VLANs are accessible on each physical port of the switch.
- **Port Configuration:**
  - **Native VLAN (Untagged):**
    - **Concept:** The default VLAN for a port. Any untagged device plugged into this port will be placed on this VLAN.
    - **Configuration:** Assign a specific VLAN (e.g., "Instructors" - VLAN 100) as the native VLAN for a port.
  - **Tagged VLANs:**
    - **Concept:** Allows traffic from multiple additional VLANs to pass through the same port. The traffic for these VLANs is tagged with its VLAN ID.
    - **Use Case:** Connecting a VoIP phone and a computer to the same port. The phone's traffic goes to the Voice VLAN (native), and the computer's traffic goes to a Data VLAN (tagged).
  - **Blocking:** By default, all other VLANs should be blocked on the port to enforce segmentation.