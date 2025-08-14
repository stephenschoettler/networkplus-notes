## 💡 Routing Tables (OBJ 2.1)

- Routers use **routing tables** (similar to a switch's MAC address table) to determine the best path for forwarding packets.
- These tables contain Layer 3 (IP address) information.
- They map IP addresses to MAC addresses using an ARP cache for local network communication.
- Each packet forwarding decision is based on the router's internal routing table.
- **Default Static Route (0.0.0.0/0):** A special static route that tells the router where to send traffic if it doesn't have a more specific route.
- It acts as a "default gateway" for the router.

✅ **Route Entry Components**
- **Prefix:** Represents the network address. A longer prefix (higher CIDR notation, e.g., /24 vs. /8) indicates a more specific network.
- **Destination Network:** The network the packet is trying to reach.
- **Next Hop:** The next router in the path to the destination network.
- **Port:** The router interface used to send traffic out.
- **Cost (Metric):** A value indicating the "expense" of using a particular route, based on factors like link speed, hop count, etc. Routers prefer routes with lower costs.

✅ **Sources of Routing Information**
- **1. Directly Connected Routes:**
  - Learned automatically when two routers are physically connected.
  - The router knows about networks directly attached to its interfaces.
- **2. Static Routes:**
  - Manually configured by an administrator.
  - Useful for small, stable networks or for specific paths.
- **3. Dynamic Routes:**
  - Learned automatically by exchanging information between routers using **dynamic routing protocols** (e.g., RIP, OSPF, BGP).
  - Routers share their routing tables, allowing them to discover and adapt to network changes.
  - Highly scalable and essential for large, complex networks like the internet.

✅ **Preventing Routing Loops**
- Routing loops occur when packets get stuck in a circular path between routers, consuming resources and preventing delivery.
- Two common techniques to prevent routing loops:
  - **1. Split Horizon:**
    - Prevents a router from advertising a route back out the same interface from which it was learned.
    - Example: If Router A learns about Network X from Router B, Router A will not tell Router B about Network X.
  - **2. Poison Reverse:**
    - A route learned on one interface is advertised back out the same interface, but with a very high (infinite) cost.
    - This explicitly tells other routers that the route is invalid or undesirable, preventing them from using it.