## 💡 Multicast Routing (OBJ 2.1)

- Multicast Routing's goal is to send traffic once to a **Class D IP address** (multicast group).
- Only devices that want the information receive it.
- This achieves efficient delivery to multiple recipients without sending duplicate data to each.
- **Trade-off:** PIM-DM offers immediate optimization at the cost of higher resource usage, while PIM-SM is more resource-efficient but takes time to find the optimal path.

✅ **IGMP (Internet Group Management Protocol)**
- Used by **clients and routers** to manage multicast group memberships.
- Allows clients to **join** a multicast group and receive messages.
- **Versions:**
  - **IGMPv1:** Clients could request to join; routers periodically queried if clients still wanted to be part of the group.
  - **IGMPv2:** Introduced the ability for clients to send **leave messages** to exit a group, reducing unnecessary traffic.
  - **IGMPv3:** Allowed clients to request multicast from a **specific source** (Source Specific Multicast - SSM), enabling more granular control (e.g., choosing a specific video stream).

✅ **PIM (Protocol Independent Multicast)**
- Used by **multicast-enabled routers** to route multicast traffic and form a multicast distribution tree.
- Works in conjunction with IGMP (IGMP handles client-router, PIM handles router-router).
- **Two Main Modes:**
  - **1. PIM-DM (Dense Mode)**
    - **Mechanism:** Uses a "flood and prune" behavior.
    - **Flood:** Initially, multicast traffic is flooded to *all* routers in the network.
    - **Prune:** Routers that do not have active multicast group members (or downstream routers with members) send "prune" messages to stop receiving the traffic.
    - **Characteristics:**
      - Provides an **immediate optimal path** from the start.
      - **Resource-intensive:** High initial traffic due to flooding.
      - Less commonly used in modern networks due to performance impact.
  - **2. PIM-SM (Sparse Mode)**
    - **Mechanism:** Uses a "shared distribution tree" initially, then transitions to a "shortest path tree."
    - **Shared Tree:** Traffic is sent to a central **Rendezvous Point (RP)**, and then distributed to interested receivers.
    - **Shortest Path Tree (SPT):** Over time, routers learn the optimal path from the source to the receiver and switch to a more direct, efficient path.
    - **Characteristics:**
      - **Resource-efficient:** Only sends traffic to interested branches, reducing network load upfront.
      - Takes longer to achieve the optimal path compared to PIM-DM.
      - **Most commonly used** in modern networks due to its efficiency.