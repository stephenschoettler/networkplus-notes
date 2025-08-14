## 💡 Route Selection (OBJ 2.1)

- When a router has multiple paths to the same destination, it uses **route selection** to determine the optimal path.
- This process involves evaluating the "believability" and "metrics" of each route.
- You don't need to memorize exact AD numbers, but understand the *order* of believability: Directly Connected > Static > Modern IGPs (EIGRP, OSPF) > Older IGPs (RIP) > EGPs.

✅ **Administrative Distance (AD): Believability of a Route**
- **Administrative Distance (AD)** is an index of believability or trustworthiness assigned to different routing information sources.
- **Lower AD values indicate higher believability/trustworthiness.** (Think of it like golf: lower score is better).
- Routers will always prefer a route with a lower AD over a route with a higher AD, even if the higher AD route has a better metric.
- **Order of Believability (from most to least believable):**
  - **1. Directly Connected Routes (AD 0):** Most believable, as the router is directly connected to the network.
  - **2. Static Routes (AD 1):** Next most believable, as they are manually configured by an administrator (the router "trusts its programmer").
  - **3. EIGRP (Internal) (AD 90):** A modern, highly trusted dynamic routing protocol.
  - **4. OSPF (AD 110):** Another widely used and trusted dynamic routing protocol.
  - **5. RIP (AD 120):** An older protocol, generally less trusted than OSPF or EIGRP.
  - **6. External EIGRP (AD 170):** EIGRP routes learned from an external source.
  - **7. Unknown/Unbelievable (AD 255):** Indicates an unreachable or untrusted route (e.g., a route that has gone down).

✅ **Metrics: Quantifying Route "Goodness"**
- **Metrics** are values used by routing protocols to quantify the "goodness" of a path.
- Each routing protocol uses different metrics based on its design (e.g., hop count, bandwidth, delay, cost, reliability).
- **Lower metric values are generally considered better.** (Again, like golf: lower score is better).
- Examples of metrics and their "better" values:
  - **Hop Count:** Lower is better (fewer routers to traverse).
  - **Bandwidth:** Higher is better (more data can flow).
  - **Delay:** Lower is better (less time for data to travel).
  - **Cost:** Lower is better (often derived from bandwidth).
- **Route Selection Process:**
  - **1. Administrative Distance:** A router first considers the **Administrative Distance** to determine the most trustworthy source of routing information.
  - **2. Metric:** If multiple routes from the *same* routing protocol (same AD) exist, the router then uses the protocol's **metric** to choose the best path.