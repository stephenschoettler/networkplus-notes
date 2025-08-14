## 💡 Ethernet Fundamentals (OBJ 2.2)

Ethernet is the clear winner of the "Layer 2 wars," it is the number one protocol used for Layer 2 communications in most modern Local Area Networks (LANs). It has evolved from older coaxial cable (10Base2, 10Base5) to modern twisted-pair copper (10Base-T and beyond) and fiber optic cabling. Use **switches** instead of hubs in modern Ethernet networks. Switches create separate collision domains for each port, allowing devices to operate in full-duplex mode, which eliminates collisions and significantly increases network performance.

✅ **Network Access Methods**
- **1. Deterministic:**
  - **Concept:** An organized and orderly method where devices must wait their turn to transmit.
  - **Analogy:** A classroom where students must raise their hand and be called on by the teacher (a central authority) to speak.
  - **Mechanism:** Often uses a token-passing system (e.g., Token Ring).
  - **Pros:** No collisions.
  - **Cons:** Inefficient; can waste bandwidth if a device has nothing to send during its turn.
- **2. Contention-Based:**
  - **Concept:** A more chaotic method where any device can transmit at any time if the network is clear.
  - **Analogy:** A casual conversation among friends at a pub; people naturally take turns, but sometimes talk over each other (collisions).
  - **Mechanism:** Ethernet uses **CSMA/CD**.
  - **Pros:** More efficient use of bandwidth as devices don't have to wait for a token.

✅ **CSMA/CD (Carrier Sense Multiple Access with Collision Detection)**
- The method Ethernet uses to manage its contention-based access.
- **CS (Carrier Sense):** Devices "listen" to the network to check if it's busy before transmitting.
- **MA (Multiple Access):** Multiple devices share the same network medium and have the ability to access it.
- **CD (Collision Detection):**
  - If two devices transmit simultaneously, a **collision** occurs.
  - Both devices detect the collision, stop transmitting, and wait for a **random back-off timer** to expire before attempting to retransmit.
  - This random wait makes it unlikely they will collide again.

✅ **Collision Domains**
- **Definition:** A section of a network where data packets can collide with one another.
- **Hubs:** All devices connected to a hub are in the **same collision domain**. This leads to more collisions as more devices are added.
- **Switches:** Each port on a switch is its **own separate collision domain**. This drastically reduces collisions and increases network efficiency.

✅ **Half-Duplex vs. Full-Duplex**
- **Half-Duplex:** Can only send OR receive at one time (like a walkie-talkie).
- Required for devices in the same collision domain (e.g., connected to a hub).
- **Full-Duplex:** Can send AND receive simultaneously.
- Possible when a device is in its own collision domain (e.g., connected to a switch port), as there is no chance of collision.