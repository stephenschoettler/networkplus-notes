## 💡 Power over Ethernet (PoE) Issues (OBJ. 5.2)
This section covers common issues encountered with Power over Ethernet (PoE) implementations, including power budget limitations and standard mismatches, along with their troubleshooting and resolution.

✅ **Power over Ethernet (PoE) Issues**
- **Definition:** Technology allowing network cables to carry both electrical power and data over a single line.
- **Uses:** IP cameras, VoIP phones, Wi-Fi access points.

✅ **PoE Standards**
- **PoE (IEEE 802.3af):**
  - Provides up to 15.4 watts (W) of DC power at the source.
  - Guaranteed minimum of 12.95W at the endpoint device (due to cable loss).
- **PoE+ (IEEE 802.3at):**
  - Enhanced version of PoE.
  - Provides up to 30W of DC power at the source.
  - Guaranteed minimum of 25.5W at the endpoint device.

✅ **Common PoE Issues & Troubleshooting**
- **1. Power Budget Exceeded:**
  - **Problem:** The total power demand of all connected PoE devices exceeds the PoE switch's (or injector's) maximum power capacity.
  - **Symptoms:** PoE devices may randomly restart, refuse to power on, or behave erratically.
  - **Troubleshooting:**
    - Calculate the cumulative power requirements of all connected devices.
    - Compare this sum to the PoE source's total power budget.
  - **Solution:** Remove non-essential devices or upgrade the PoE switch to one with a higher power budget.
- **2. Incorrect Standard:**
  - **Problem:** A mismatch between the PoE standard required by the endpoint device and the standard provided by the PoE switch.
  - **Example:** A PoE+ device (needs up to 30W) connected to an older PoE switch (provides max 15.4W).
  - **Symptoms:** Endpoint device may not function properly or may not power on at all.
  - **Troubleshooting:**
    - Verify the PoE standard supported by both the endpoint device and the PoE switch.
    - Ensure compatibility (e.g., a PoE+ device needs a PoE+ capable source).
  - **Solutions:**
    - Replace the switch with one that supports the required PoE standard.
    - Use a **PoE Injector** (a device that adds power to an Ethernet cable) that matches the required PoE standard to provide sufficient power to the endpoint device.