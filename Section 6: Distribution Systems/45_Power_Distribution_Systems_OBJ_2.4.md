## 💡 Power Distribution Systems (OBJ 2.4)

Power Distribution Systems are crucial for ensuring consistent and reliable power delivery to networking equipment and infrastructure. When designing data centers, integrate UPS, PDU, and generators for comprehensive power redundancy. Always consider power loads and voltage requirements for new equipment.

✅ **1. UPS (Uninterruptible Power Supply)**
- **Purpose:** Provides emergency power when the main power fails (battery backup).
- **Features:** Often includes line conditioning and protection against surges/spikes.
- **Duration:** Good for short-duration outages (15-30 minutes typically).
- **Placement:** Can be per-rack, or larger systems for multiple racks/entire data centers (though expensive).

✅ **2. PDU (Power Distribution Unit)**
- **Purpose:** Specialized device for distributing electrical power to network components and computing equipment.
- **Features:** Advanced power strips with power monitoring and control features.
- **Protection:** Provides protection from surges, spikes, and undervoltage, but *not* complete power loss.
- **Usage:** Often combined with a UPS or generator for full power redundancy.

✅ **3. Generators**
- **Purpose:** Provide longer-term power during extended outages.
- **Types:** Powered by diesel, gasoline, or propane.
- **Integration:** Requires time to start up, so typically paired with a UPS (UPS handles initial load, then generator takes over via an automatic transfer switch).

✅ **4. Power Loads**
- **Importance:** Managing power loads is critical to prevent circuit overloads and ensure efficient power usage.
- **Load Balancing:** Ensures even power distribution, preventing excessive load on single circuits (which can cause outages or hardware damage).
- **Planning:** New equipment additions require calculating projected power utilization and proper placement to balance loads across the data center.

✅ **5. Voltage Considerations**
- **Definition:** Electric potential difference.
- **Regional Differences:** Voltages vary by region (e.g., 120V in US, 230V in Europe).
- **Mismatch Risk:**
  - Connecting a 230V device to a 120V source: Device won't power on (no damage). Use a transformer.
  - Connecting a 120V device to a 230V source: Device will be damaged or catch fire due to overvoltage.
- **Modern Devices:** Many are dual-voltage or auto-switching, but always verify manufacturer specifications.