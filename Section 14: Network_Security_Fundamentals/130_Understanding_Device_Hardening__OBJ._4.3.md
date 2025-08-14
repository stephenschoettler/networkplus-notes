## 💡 Understanding Device Hardening (OBJ 4.3)

Device Hardening's purpose is to secure a system by reducing its attack surface. This involves ensuring only necessary applications and services are running. Services are applications that run in the background of the operating system.

✅ **Hardening Techniques (Disabling Unneeded Services/Applications)**
- **1. Windows:**
  - **GUI Method (`services.msc`):** Stop service, change startup type to "Disabled."
  - **Command Line:** (`sc stop [service_name]`, `net stop [service_name]`, `sc config [service_name] start= disabled`).
  - **Use Case:** Disabling Windows Update for centralized patch management, stopping malware.
- **2. macOS (and Linux - similar commands):**
  - **GUI Method (Activity Monitor):** Find process, "Force Quit."
  - **Command Line:** (`top` to find PID, then `kill [PID]`).
  - **Use Case:** Stopping/disabling malware or unnecessary background processes.

✅ **Importance of Disabling Unneeded Services/Applications**
- Unneeded services/applications consume resources and can introduce vulnerabilities.
- Disabling them reduces the attack surface, making the system more secure.
- Helps in removing malware that runs as a background process.