## 💡 Wired Network Topology (OBJ 1.6)

A **network topology** refers to the arrangement of elements (links, nodes, clients, servers) in a computer network. Understand the advantages and disadvantages of each topology and their suitability for different scenarios.

✅ **Physical vs. Logical Topology**
- **Physical Topology:** Shows how network devices and components are physically cabled and connected (e.g., on a floor plan).
- **Logical Topology:** Shows how traffic flows through the network, not necessarily the physical layout.

✅ **Types of Wired Network Topologies**
- **1. Point-to-Point Topology:**
  - Simplest form: direct connection between two devices.
  - Used for connecting a computer to a peripheral (printer, scanner).
  - Can be used for WAN connections between two remote offices.
  - Not scalable for larger networks.
- **2. Ring Topology:**
  - Each device connected to two other devices, forming a circular data path.
  - Data travels in one direction (clockwise or counter-clockwise).
  - Prevents data collisions due to unidirectional flow.
  - If one node fails, it can disrupt the entire network (unless redundant connections exist).
  - **FDDI (Fiber Distributed Data Interface):** A dual-ring structure (primary and secondary) providing redundancy, used for high bandwidth over fiber optic lines (up to 200 km).
- **3. Bus Topology:**
  - All network devices connected to a single central cable (backbone/bus).
  - Data sent by any device is available to all, but only the intended recipient processes it.
  - Easy to install, requires less cable.
  - Entire network disabled if main cable fails.
  - Performance decreases with more devices due to increased data collisions.
  - Older technology, not commonly used in modern environments.
- **4. Star Topology:**
  - Most common network layout today (e.g., home networks).
  - Each node connects to a **centralized connection point** (normally a network switch).
  - Robust: Failure of one link doesn't affect others.
  - Entire network depends on the functioning of the central switch; if it fails, the network becomes inoperable.
- **5. Hub-and-Spoke Topology:**
  - Variation of the star topology.
  - Centralized node (hub) connects to multiple nodes (spokes).
  - Spokes are not directly connected to each other; data must go through the hub.
  - Commonly used in airlines and telecommunication networks.
  - Allows consolidation of smaller regional offices to a central hub, saving costs on long-distance links.
- **6. Mesh Topology:**
  - Features a point-to-point connection between every single device on the network.
  - **Full-Mesh:** Every node connected to every other node.
    - High redundancy and robustness.
    - Very expensive and complex to install due to the high number of cables/ports required (connections = n * (n-1) / 2).
  - **Partial-Mesh:** A less interlinked version where some nodes are fully meshed, while others connect to only one or two devices.
    - Offers some benefits of mesh without the full cost/complexity.