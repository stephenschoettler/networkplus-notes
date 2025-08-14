## 💡 Software Defined Network (SDN) (OBJ 1.8)

Software Defined Network (SDN) is an approach to networking that uses software-based controllers or Application Programming Interfaces (APIs) to communicate with underlying hardware infrastructure and direct traffic on a network. Its core idea is to decouple the control plane from the data plane, allowing network intelligence to be centralized and managed by software. SDN has application-aware capabilities, allowing intelligent decisions based on application requirements for optimal performance and resource utilization. SDN is a critical part of Infrastructure as Code (IaC), enabling scripted automation and orchestration for network provisioning.

✅ **Three Planes of Network Architecture**
- **1. Control Plane:**
  - **Role:** Makes decisions about how traffic should be prioritized, secured, and switched/routed.
  - **SDN:** Functions are moved out of physical devices and into a centralized, virtualized controller.
- **2. Data Plane (Forwarding Plane):**
  - **Role:** Carries user traffic; performs actual switching and routing of data.
  - **Traditional & SDN:** Remains on the physical network devices.
- **3. Management Plane:**
  - **Role:** Administers routers/switches, monitors traffic conditions and network status.
  - **SDN:** Centralized policy management, allowing administrators to define and enforce policies from a single control point.

✅ **Advantages of SDN**
- Flexibility & Scalability: Easier to manage and control network traffic, improving scalability.
- Vendor Agnostic: Can mix and match products from different vendors due to common API calls.
- Speed & Agility: Faster network establishment and ability to add automation/policy management.
- Automated Deployment: Enables fully automated deployment of networks within the cloud.
- High Velocity/Availability: Critical for high-velocity/high-availability architectures and disaster recovery.
- Security Data Collection: Easier to collect security data as everything is treated as software.

✅ **Disadvantages/Challenges of SDN**
- Single Point of Failure: If the SDN controller loses connectivity, the entire network could go down or lose control. Requires hardening and protection of the controller.

✅ **Types of SDN**
- **1. Open SDN:** Relies on open-source technologies (OpenFlow, OpFlex, OpenStack).
- **2. Hybrid SDN:** Employs traditional SDN protocols alongside conventional protocols.
- **3. SDN Overlay:** Uses software to create layers of network abstraction (virtualized network layers) on top of the physical network.