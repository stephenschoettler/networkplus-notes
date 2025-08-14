## 💡 SCADA and ICS (OBJ 4.1)

Operational Technology (OT) refers to communication networks designed to implement industrial control systems, interacting with the physical world (e.g., opening/closing valves, power generation, turning lights on/off). It differs from IT (information technology) which focuses on data and business systems.

✅ **Industrial Control Systems (ICS)**
- **Definition:** Provides mechanisms for workflow and process automation by controlling machinery using embedded devices designed for specific functions.
- **Use:** Heavily used in critical infrastructure (power, water, healthcare, telecommunications, national security).
- **Security Priorities:** Prioritizes Availability and Integrity over Confidentiality.
  - **Availability is paramount:** Downtime in manufacturing/critical infrastructure is very costly.
  - **Confidentiality is least important:** Historically, these systems were isolated (air-gapped) from the internet, relying on physical boundaries for security.
- **Components:**
  - **Fieldbus:** Digital serial data communication used to interconnect PLCs.
  - **PLCs (Programmable Logic Controllers):** Digital computers used in industrial settings for automation (assembly lines, robotics). Interconnected via fieldbus with sensors and I/O devices.
  - **HMI (Human-Machine Interface):** Local control panel or software on a computer used to program PLCs and monitor the system (input/output for human operators).
  - **Control Server:** Governs the automation process.
  - **DCS (Distributed Control System):** Multiple ICSs interconnected, usually within one building/facility.

✅ **Supervisory Control and Data Acquisition (SCADA)**
- **Definition:** A type of industrial control system used to manage large-scale, multi-site devices and equipment spread over a geographic region from a host computer.
- **Scope:** Interconnects many ICS and DCS plants through a Wide Area Network (WAN).
- **WAN Connection:** Can use cellular, microwave, satellite, fiber, or VPN-based LAN.
- **Example:** Smart meter systems used by electric companies (meters send usage data over cellular to a central SCADA server).