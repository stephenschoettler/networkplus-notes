## 💡 Switching and Routing Loops (OBJ. 5.3)
This section explains the concepts of switching and routing loops, their impact on network performance, and the mechanisms used to prevent them.

✅ **Switching Loops (Bridging Loops)**
- **Definition:** Occur when there's more than one active path between a source and destination device in a switched network.
- **Impact:** Broadcast packets are endlessly flooded, leading to broadcast storms, network slowdowns, and potential network collapse.
- **Prevention:**
  - **Spanning Tree Protocol (STP):** Essential for preventing switching loops. STP blocks redundant paths to create a loop-free logical topology.
  - If a switching loop is suspected, it's likely an STP configuration issue.

✅ **Routing Loops**
- **Definition:** Occur when an error in routing algorithms creates a circular route among network devices, causing data packets to endlessly loop between routers.
- **Cause:** Primarily incorrect configurations of routing protocols or misconfigured static routes.
- **Prevention Mechanisms:**
  - **1. Time To Live (TTL):**
    - IP packet headers contain a TTL field.
    - Each router decrements the TTL. If TTL reaches 0, the packet is dropped, effectively ending the loop.
  - **2. Split-Horizon:**
    - A router configuration that prevents a route from being advertised back in the direction it was learned from.
    - Ensures a router doesn't send a route back to the same router that advertised it.
  - **3. Route Poisoning:**
    - If a router detects a connected route has failed, it "poisons" the route by setting its metric to an infinitely high number. This discourages other routers from using that route. (Happens automatically with some routing protocols).
  - **4. Hold-down Timers:**
    - Used with distance-vector routing protocols (e.g., RIP).
    - Routers will not advertise or accept routes that are in a "hold-down" state for a set period (e.g., 180 seconds for RIP). This prevents bad routes from being quickly re-advertised.
  - **5. Careful Use of Static Routes:**
    - Static routes have a very low administrative distance (high trustworthiness) and can override dynamically learned routes.
    - Misconfigured static routes are a common cause of routing loops. Exercise caution when implementing them.