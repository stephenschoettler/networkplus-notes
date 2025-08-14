## 💡 Zero-Trust Architecture (OBJ 1.8)

**Core Principle:** "Trust nothing and verify everything." No user, device, or transaction is trusted by default, regardless of its location (inside or outside the network perimeter).
**Contrast with Traditional Security:** Traditional security relies on strong perimeters assuming everything inside is trusted. Zero-Trust acknowledges that threats can come from inside or outside and that perimeters are insufficient in a "deperimeterized" world (due to cloud, remote work, mobile tech).
**Goal:** Continuous verification for every device, user, and transaction.

✅ **Two Planes of Zero-Trust Implementation**
- **1. Control Plane:**
  - **Role:** Defines, manages, and enforces policies related to user and system access. Centralized policy decision-making.
  - **Key Elements:**
    - **Adaptive Identity:** Real-time validation of user identity based on behavior, device, location, etc.
    - **Threat Scope Reduction:** Limits user access to only what's needed for work (least privilege) to minimize attack surface and "blast radius" in case of a breach.
    - **Policy-Driven Access Control:** Develops, manages, and enforces user access policies based on roles and responsibilities.
    - **Secured Zones:** Isolated environments for sensitive data, accessible only by users with appropriate permissions.
- **2. Data Plane:**
  - **Role:** Ensures policies defined by the control plane are properly executed, allowing data to flow across the network securely.
  - **Key Elements (Functions):**
    - **Subject System:** The individual or entity attempting access (employee, workstation, application). Authenticity is verified.
    - **Policy Engine:** Cross-references access requests with predefined policies (the "rule book"). Works with the control plane.
    - **Policy Administrator:** Establishes and manages access policies (dictates who accesses what).
    - **Policy Enforcement Point (PEP):** The final step where the decision to grant or deny access is executed. Acts as a gatekeeper, allowing/restricting access based on verification and policy engine's determination. Often considered part of the data plane.

✅ **Overall Importance**
- Provides a robust and adaptable security posture in an evolving digital landscape.
- Proactively defends against threats by continuously reassessing trust at every enforcement point.