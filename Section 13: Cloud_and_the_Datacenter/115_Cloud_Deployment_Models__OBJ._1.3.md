## 💡 Cloud Deployment Models (OBJ 1.3)

Cloud deployment models define how cloud computing resources are made available to users and organizations. Each model has different characteristics regarding ownership, management, and access. Choosing a cloud deployment model involves weighing the trade-offs between cost, security, control, and flexibility based on an organization's specific needs and risk tolerance.

✅ **Main Cloud Deployment Models**
- **1. Public Cloud:**
  - **Concept:** Cloud services are made available to the general public over the internet by a third-party service provider (e.g., Google Drive, AWS, Azure).
  - **Characteristics:** Inexpensive, quick to deploy, highly scalable.
  - **Security:** Resources are shared (multi-tenancy), which can introduce security concerns if not properly managed by the provider.
- **2. Private Cloud:**
  - **Concept:** Cloud infrastructure operated solely for a single organization. It can be managed internally or by a third party.
  - **Characteristics:** High control over security and data, dedicated resources.
  - **Cost:** More expensive than public clouds due to the need to procure and manage all hardware and software.
  - **Use Case:** Chosen when security and strict control over data are paramount (e.g., government, financial institutions).
- **3. Hybrid Cloud:**
  - **Concept:** Combines two or more distinct cloud infrastructures (e.g., private cloud + public cloud) that remain unique entities but are bound together by standardized technology.
  - **Characteristics:** Offers flexibility to host sensitive data in a private cloud while leveraging public cloud resources for less sensitive or burstable workloads.
  - **Security:** Requires careful management of data flow and security policies between different environments.
- **4. Community Cloud:**
  - **Concept:** Cloud infrastructure shared by several organizations that have common concerns (e.g., security requirements, compliance, mission).
  - **Characteristics:** Costs are shared among participants.
  - **Security:** Inherits security risks from all participating organizations; requires careful mitigation.

✅ **Resource Sharing Models**
- **1. Multi-tenancy:**
  - **Concept:** The same physical resources (servers, storage) are used by multiple organizations.
  - **Characteristics:** Highly efficient, cost-effective.
  - **Security Concern:** "Noisy neighbor" effect (one tenant's activity impacting others) or potential for data exposure if not properly isolated.
- **2. Single-tenancy:**
  - **Concept:** A single organization is assigned to a particular resource (e.g., a dedicated server).
  - **Characteristics:** Enhanced security and performance due to dedicated resources.
  - **Cost:** More expensive and less efficient than multi-tenancy.