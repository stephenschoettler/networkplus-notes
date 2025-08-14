## 💡 Routing Fundamentals (OBJ 2.1)

- Routers are essential for connecting devices across different subnets or networks (internal to external).
- Their primary function is to **route traffic** by forwarding it between these distinct networks.
- Routers operate at **Layer 3 (Network Layer)** of the OSI model.
- Unlike Layer 2 switches, routers **separate broadcast domains**, which enhances network efficiency and security.
- In the real world, Layer 3 switches (multi-layer switches) can perform routing functions.
- For the CompTIA Network+ exam, if a device is performing Layer 3 functionality (routing), it should be considered a **router**, regardless of whether it's a dedicated router or a Layer 3 switch.
- If the exam simply refers to a "switch," it implies a standard Layer 2 device.

✅ **Basic Router Operation (Layer 2 to Layer 3 Transition)**
- When a device (e.g., PC1) sends data to a destination on a different network, the data first goes to its default gateway (a router).
- The router receives the **Layer 2 data frame** from the local network.
- It then **repackages** this data as a **Layer 3 packet** by adding an IP header, effectively transitioning from MAC addressing to IP addressing.
- This Layer 3 packet is then forwarded across the Wide Area Network (WAN) connection to the destination network's router.
- The destination router strips the IP header, converts the packet back into a Layer 2 data frame, and uses the destination device's MAC address to deliver it on its local network.
- This process is reversed for return communication.