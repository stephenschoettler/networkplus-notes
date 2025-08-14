## 💡 Internet of Things (IoT) (OBJ 4.1)

The Internet of Things (IoT) is a global network of appliances and personal devices equipped with sensors, software, and network connectivity to report state and configuration data. These devices are managed remotely over IP networks. Examples include building/home automation (HVAC, lighting, security), IP video systems, audiovisual systems, physical access control, and scientific/industrial equipment.

✅ **Components of IoT Devices**
- **1. Hub and Control System:** Central point of communication for IoT devices, especially those using different protocols (Z-Wave, Zigbee) than Wi-Fi/Bluetooth (e.g., Amazon Echo).
- **2. Smart Devices:** IoT endpoints that connect to a central hub to provide automation/function (e.g., smart light bulbs, video doorbells, thermostats).
- **3. Wearables:** IoT devices designed as accessories to be worn (e.g., smartwatches, fitness trackers, smart glasses).
- **4. Sensors:** Measure various physical parameters (temperature, sound, light, humidity, motion, heart rate, etc.).

✅ **Security Considerations & Best Practices for IoT**
- **1. Understand Endpoints:** Each IoT device introduces new vulnerabilities. Assess its security posture before connecting.
- **2. Track and Manage:** Don't allow uncontrolled connection of IoT devices. Implement good configuration management and proper processes for testing, installing, and operating them.
- **3. Patch Vulnerabilities:** IoT devices are often insecure. Patch them where possible. If no patches exist, conduct risk management to determine if the risk is acceptable or if additional mitigations (e.g., separate VLAN) are needed.
- **4. Conduct Test and Evaluation:** Thoroughly test and evaluate IoT devices (e.g., using penetration testing) on a test network/lab before connecting to production. Don't blindly trust manufacturer claims.
- **5. Change Default Credentials:** Default usernames/passwords are a huge vulnerability. Change them before deploying to production.
- **6. Use Encryption Protocols:** Utilize encryption to the maximum extent possible to secure data sent/received by these IoT devices.
- **7. Segment IoT Devices:**
  - **Crucial:** Place IoT devices in their own VLANs and subnets.
  - **Goal:** Prevent interference with the production network and contain potential breaches (e.g., Target breach via HVAC system).
  - Consider a physically separate IoT-only network if possible.