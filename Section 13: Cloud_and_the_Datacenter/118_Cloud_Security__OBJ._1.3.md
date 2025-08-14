## 💡 Cloud Security (OBJ 1.3)

A **VPC (Virtual Private Cloud)** is a logically isolated section of a cloud provider's infrastructure where users can launch resources in a virtual network they define. Its purpose is to provide a flexible, scalable, and secure virtual network environment within the cloud, abstracting traditional hardware-based networking to a software level. VPCs are often provisioned and managed through scripted automations and orchestration, making them a key component of IaC.

✅ **Core Components and Features of a VPC**
- **1. Subnets:**
  - Logical divisions within a VPC.
  - **Public Subnets:** Accessible from the internet.
  - **Private Subnets:** Not directly accessible from the internet.
- **2. Route Tables:**
  - Contain rules (routes) that determine where network traffic is directed within the VPC.
- **3. Internet Gateways (IGW):**
  - A component that allows communication between instances in your VPC and the public internet.
- **4. NAT Gateways (Network Address Translation Gateway):**
  - Enables instances in a private subnet to connect to the internet, while preventing inbound connections from the internet.
- **5. Network Access Control Lists (Network ACLs) vs. Security Groups:**
  - Both are virtual firewalls controlling traffic.
  - **Network ACLs:**
    - Operate at the **subnet level**.
    - **Stateless:** Each rule is evaluated independently; return traffic must be explicitly allowed.
  - **Security Groups:**
    - Operate at the **instance level**.
    - **Stateful:** If outbound traffic is allowed, corresponding inbound response traffic is automatically allowed.
  - **Best Practice:** Use both for a multi-layered defense.
- **6. VPC Peering:**
  - Connects two VPCs privately, enabling routing traffic between them without traversing the public internet.
- **7. VPC Endpoints:**
  - Allow private connectivity to cloud provider services from within your VPC, bypassing the internet.
- **8. VPN Connections:**
  - Created between your VPC and remote networks (on-premise) or between two VPCs for secure, encrypted tunnels.

✅ **Advantages of VPCs**
- Increased flexibility, scalability, and security.
- Enables automation of deployments.

✅ **Challenges of VPCs**
- Potential single point of failure if connectivity is lost.
- Requires proper security configuration to prevent unauthorized access.