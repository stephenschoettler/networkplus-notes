## 💡 Routing (OBJ 1.4 & 2.1)

- Routers connect different subnets and networks (internal to external).
- They operate at Layer 3 (Network Layer) of the OSI model.
- Routers separate broadcast domains, improving network efficiency and security.
- For the exam, a Layer 3 switch (multi-layer switch) performing routing functions should be considered a router.
- A "switch" without further qualification refers to a Layer 2 device.

✅ **Basic Routing Process (Layer 2 to Layer 3 Transition)**
- When a device (e.g., PC1) wants to communicate with a device on a different network (e.g., PC2), it sends data to its default gateway (a router).
- The router receives the Layer 2 data frame, strips the Layer 2 information (MAC address), and repackages it as a Layer 3 packet with an IP header.
- The router forwards the IP packet across the WAN connection to the destination network's router.
- The destination router strips the IP header, converts it back to a Layer 2 data frame, and uses the destination device's MAC address to deliver it.

✅ **Topics Covered in this Section**
- Routing fundamentals and how routing works.
- Routing tables: Used to determine data forwarding paths.
- Routing protocols (e.g., RIP, OSPF, BGP).
- Route selection for efficient data transfer.
- Address translation (Static NAT, Dynamic NAT, PAT).
- Routing redundancy protocols (e.g., HSRP, VRRP) for load balancing and redundancy.
- Router configuration.
- Multicast routing (PIM modes).
- Generic Routing Encapsulation (GRE).