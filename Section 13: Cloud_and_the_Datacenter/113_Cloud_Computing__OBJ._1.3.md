## 💡 Cloud Computing (OBJ 1.3)

Cloud computing involves delivering computing services (servers, storage, databases, networking, software, analytics, intelligence) over the Internet ("the cloud"). General benefits include reduced IT costs, increased flexibility, improved scalability, and enhanced reliability.

✅ **Key Characteristics of Cloud Computing**
- **1. High Availability (HA):**
  - **Concept:** Services experience very little downtime. Cloud services are built to be highly reliable and fault-tolerant.
  - **Measurement:** Often measured in "nines" (e.g., "five nines" = 99.999% uptime, meaning only ~5 minutes of downtime per year).
  - **Mechanism:** Achieved by having redundant systems (e.g., multiple web servers for one website), so if one fails, others take over seamlessly.
- **2. Scalability:**
  - **Concept:** The ability to increase or decrease computing resources to meet changing demand.
  - **Vertical Scaling (Scale Up):** Adding more resources (CPU, RAM, storage) to an existing server or node.
  - **Horizontal Scaling (Scale Out):** Adding more instances of servers or nodes to distribute the load, often behind a load balancer.
  - **Benefit:** Allows systems to handle growth from a few users to millions without significant upfront investment in hardware.
- **3. Rapid Elasticity:**
  - **Concept:** The ability to quickly and automatically scale computing resources up or down in real-time in response to demand fluctuations.
  - **Mechanism:** Achieved through automation and orchestration of virtual machines on physical servers.
  - **Benefit:** Pay only for what you use, and avoid over-provisioning. Crucial for handling sudden spikes in traffic (e.g., viral events).
- **4. Metered Utilization (Measured Service):**
  - **Concept:** Paying for cloud services based on actual consumption (pay-per-use model).
  - **Mechanism:** Usage is tracked and billed based on metrics like CPU hours, data transfer, storage used, or number of requests.
  - **Distinction:**
    - **Metered:** Pay for exact usage (like a utility bill).
    - **Measured:** Pay for a certain quantity upfront, whether used or not (like a cell phone plan with a data cap). Cloud services are predominantly metered.
- **5. Shared Resources:**
  - **Concept:** Cloud providers pool hardware resources (servers, storage, networking) and share them among multiple customers (multi-tenancy).
  - **Benefit:** Reduces costs for individual users/companies as they don't need to buy and maintain expensive hardware. Providers optimize resource allocation based on collective demand.
- **6. File Synchronization:**
  - **Concept:** The ability to keep files consistent and up-to-date across multiple devices and locations using cloud storage.
  - **Benefit:** Enables distributed teams to collaborate seamlessly on files, as changes made by one user are synchronized to all other users with access.