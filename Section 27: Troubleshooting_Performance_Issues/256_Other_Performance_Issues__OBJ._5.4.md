## 💡 Other Performance Issues (OBJ. 5.4)
This section covers various other performance issues that can arise in a network, including optical link budget problems, certificate issues, licensing problems, BYOD challenges, and hardware failures.

✅ **Low Optical Link Budgets**
- **Definition:** Calculation considering anticipated signal losses along a fiber optic connection.
- **Causes:** Distance, multiplexing, cable bends, imperfect connections, patches, splices.
- **Symptoms:** Reduced transmission efficiency, slower speeds, downtime.
- **Measurement:** Optical Time-Domain Reflectometer (OTDR) measures losses/reflections in dB/km.
- **Standard loss:** 0.25 dB/km for standard fiber. Higher indicates low budget.
- **Troubleshooting:** Increase transmitter power, improve splice quality.

✅ **Certificate Issues**
- Digital certificates: Used for identity verification (e.g., HTTPS, 802.1X EAP).
- **Common causes for "untrusted" SSL/TLS certificates:**
  - Not signed by a trusted Certificate Authority (CA).
  - Expired certificate.
  - Server lacks a trusted root certificate.
- **Troubleshooting (if you own the server):** Purchase/renew certificate from trusted CA, install correctly.
- **Troubleshooting (802.1X EAP):** Ensure certificates are trusted, not expired, and properly installed on devices/clients.

✅ **License Feature Issues**
- Occur when a device feature is not enabled due to licensing.
- **Troubleshooting:**
  - 1. Determine loaded license.
  - 2. Compare with features it unlocks.
  - 3. Contact manufacturer if features are missing despite correct license.
  - 4. Procure correct license if the wrong one was purchased.

✅ **BYOD (Bring Your Own Device) Challenges**
- Networking focus (not security): Supporting diverse devices (Windows, macOS, ChromeOS).
- Troubleshooting difficulty: Distinguishing between device, software, or network issues.
- Operational expenditure (OpEx) increase due to labor for support/troubleshooting.
- Network access considerations: Wired vs. wireless, MAC address registration/whitelisting, separate VLANs for BYOD devices.

✅ **Hardware Failures**
- Can occur in routers, switches, firewalls, clients, servers.
- **Troubleshooting:**
  - 1. Identify failing device.
  - 2. Identify failing component (many are field-replaceable).
  - 3. Replace defective component (e.g., power supply, interface card/module).
  - 4. For major failures (e.g., motherboard), replace the entire device:
    - Get spare device.
    - Mount in rack.
    - Load backup configurations.
    - Reconnect cables.
    - Restore service.
    - Return failed device for repair/disposal.