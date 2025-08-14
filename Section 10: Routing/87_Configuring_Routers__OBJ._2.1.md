## 💡 Configuring Routers (OBJ 2.1)

- Routers are configured to connect different subnets and forward traffic between them.
- Each router maintains a **routing table** to make forwarding decisions.
- This lesson demonstrates static routing in a network with multiple subnets (HR, IT, Support) connected via a central **backbone router**.
- Routers make decisions based on the destination IP address and their routing tables, forwarding packets hop-by-hop until they reach their destination network.

✅ **Router Interfaces and IP Addressing**
- Routers have multiple interfaces, each connected to a different network segment.
- **Inner Interface:** Connects to the local subnet (e.g., 172.16.0.1/24 for the Support network).
- **Outer Interface:** Connects to another router or external network (often a public IP in real-world scenarios, but private IPs used for internal router-to-router links in this example).
- **`/30 Subnets` for Point-to-Point Links:** For direct connections between two routers, a /30 subnet is efficient as it provides exactly two usable IP addresses (one for each router interface), a network address, and a broadcast address.

✅ **Static Routing Table Configuration**
- In static routing, an administrator manually configures routes in the router's table.
- Each entry specifies:
  - **Destination Network:** The network to be reached (e.g., 192.168.0.0/24 for HR network).
  - **Next Hop:** The IP address of the next router in the path to that destination.
  - **Example:** A router in the Support network (172.16.0.0/24) wanting to reach the HR network (192.168.0.0/24) would have a static route pointing to the Backbone Router's interface as the next hop.

✅ **Packet Flow Through a Routed Network (Example: Ping from Support PC to Web Server)**
- **1. Source PC (Support 1):** Sends a ping to the Web Server (e.g., 192.168.1.12).
- **2. Local Switch (Support Switch):** Forwards the packet to the default gateway (Support Router) because the destination IP is outside the local subnet.
- **3. Support Router:**
  - Receives the packet.
  - Checks its routing table.
  - Finds a static route for the Web Server's network (192.168.1.0/24) pointing to the Backbone Router's interface.
  - Forwards the packet to the Backbone Router.
- **4. Backbone Router:**
  - Receives the packet.
  - Checks its routing table.
  - Finds a static route for the Web Server's network (192.168.1.0/24) pointing to the IT Router's interface.
  - Forwards the packet to the IT Router.
- **5. IT Router:**
  - Receives the packet.
  - Checks its routing table.
  - Realizes the destination (Web Server) is on its directly connected IT network.
  - Forwards the packet to the IT Switch.
- **6. IT Switch:** Uses ARP to find the Web Server's MAC address and delivers the packet.
- **7. Web Server:** Processes the ping and sends a reply back through the same path in reverse.