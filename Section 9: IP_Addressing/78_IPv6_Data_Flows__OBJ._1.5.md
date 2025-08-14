## 💡 IPv6 Data Flows (OBJ 1.5)

IPv6 data flows describe how information is transmitted from a source to one or more destinations on an IP network. A key change from IPv4 is that IPv6 eliminates the **Broadcast** data flow type and introduces **Anycast**.

✅ **1. Unicast**
- **Concept:** One-to-one communication.
- **Mechanism:** Data is sent from a single source to a single, specific destination IPv6 address.
- **Analogy:** Sending a direct message to one person.
- **Example:** A server sending a file to a single client. If the server needs to send the same file to multiple clients, it sends a separate unicast stream to each.

✅ **2. Multicast**
- **Concept:** One-to-many communication (to a specific group).
- **Mechanism:** Data is sent from a single source to a group of interfaces (devices) that have joined a specific multicast group.
- **IPv6 Multicast Addresses:** Always begin with `FF` (e.g., `FF00::/8`).
- **Analogy:** Sending a message to a group chat; only members of the group receive it.
- **Use Cases:** Video conferencing, streaming media, online gaming, efficient delivery of updates to a subset of devices.

✅ **3. Anycast**
- **Concept:** One-to-nearest communication.
- **Mechanism:** Data is sent from a single source to an IPv6 address that is assigned to multiple interfaces (often geographically dispersed servers or routers). The network's routing protocols deliver the packet to the *closest* interface (based on routing metrics).
- **Analogy:** Calling a toll-free number; your call is routed to the nearest available service center.
- **Purpose:**
  - Efficiently update router tables across a distributed network.
  - Deliver content from Content Delivery Networks (CDNs) or DNS servers, directing users to the closest available resource.
- **Benefit:** Improves efficiency and reduces network load by directing traffic to the optimal (closest) destination, rather than flooding the network (like broadcast) or sending multiple unicast streams.
- **Note:** Anycast addresses are allocated from the unicast address space, so you cannot identify an Anycast address simply by looking at its format.