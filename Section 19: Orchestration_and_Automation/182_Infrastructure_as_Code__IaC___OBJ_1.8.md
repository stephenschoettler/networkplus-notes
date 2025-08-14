## 💡 Infrastructure as Code (IaC) (OBJ 1.8)

Infrastructure as Code (IaC) is the managing and provisioning of infrastructure through code, not manual processes. Infrastructure includes virtual machines, servers, clients, and virtual network devices (switches, routers, firewalls).

✅ **Benefits of IaC**
- Faster deployment, less error-prone, more secure, reusable, cost reduction, basis for cloud scaling.

✅ **Key Areas of IaC Implementation**
- **1. Scripting:** Automating ordered series of actions with logic.
- **2. Security Templates & Policies:** Applying standardized configurations (network settings, ACLs, etc.).
- **3. Orchestration:** Coordinating installation/configuration across multiple systems simultaneously.

✅ **"Special Snowflakes" (Anti-Pattern)**
- **Definition:** Systems deviating from standard IaC configuration templates.
- **Problem:** Adds security risk, creates configuration/support issues, leads to troubleshooting headaches.
- **Recommendation:** Strive for consistency and eliminate "special snowflakes" for a stable network baseline.