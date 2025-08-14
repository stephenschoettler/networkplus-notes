## 💡 Understanding WAN Connections (OBJ 1.5)

As a network technician, you'll encounter various WAN connection types, but from the local network's perspective, the interface often looks similar. Regardless of the underlying WAN technology (fiber, cable, satellite, cellular), the connection point to the local network often presents a standard Ethernet (RJ45) interface, simplifying the local network setup.

✅ **Common WAN Connection Types and Their Local Interface**
- **1. Cable Modem:**
  - **Connection:** Uses a coaxial cable (like for TV) to connect to the modem.
  - **Local Interface:** The modem converts the signal and provides an **RJ45 (Ethernet) port** (e.g., for Cat6 cable) to connect to your local network's router or switch.
  - **Example:** Verizon Fios (though fiber-based, often converts to coax or Ethernet outside the home).
- **2. Fiber Optic Modem (ONT - Optical Network Terminal):**
  - **Connection:** Fiber optic cable runs to a media converter or ONT.
  - **Local Interface:** The ONT converts the optical signal to an electrical signal, providing an **RJ45 (Ethernet) port** for local network connection.
  - **Note:** Some fiber deployments might convert to coaxial cable outside the home, then use a cable modem-like device.
- **3. Satellite Modem:**
  - **Connection:** Uses a coaxial cable to connect to a satellite dish on the roof.
  - **Local Interface:** The satellite modem converts the signal and provides an **RJ45 (Ethernet) port** for local network connection.
  - **Use Case:** Common in remote areas without other broadband options.
- **4. Cellular Connections:**
  - **Devices:** Smartphones, tablets, dedicated cellular modems, or mobile hotspots.
  - **Local Interface:** These devices have an embedded cellular modem. They can provide internet access to other devices via:
    - **Wi-Fi Hotspot:** The cellular device acts as a wireless access point.
    - **USB Tethering:** Direct USB connection to a computer.
    - **Ethernet Port:** Some dedicated cellular modems or fixed cellular home internet devices may have an RJ45 port.