# 🔧 Polaris SSD Setup (External via UGREEN Enclosure)

This document describes how to set up the **Lexar NM620 512GB SSD** for use with Polaris (Raspberry Pi 5) in the **UGREEN CM850 USB4 enclosure**. The SSD serves as the **primary boot drive** and **data storage hub** for the Secure-Pi project.

---

## 🧰 Hardware Layout
- **Inside Pironman 5:**  
  - Raspberry Pi 5 (16GB)  
  - Hailo-8L AI Accelerator (internal PCIe slot)  

- **External:**  
  - Lexar NM620 512GB NVMe SSD in UGREEN CM850 USB4 enclosure  
  - Connected to Polaris via USB-C → USB-C cable  

---

## 🔹 Step 1: Flash Raspberry Pi OS
1. Connect the SSD enclosure to your PC.  
2. Open **Raspberry Pi Imager**.  
3. Select **Raspberry Pi OS Lite (64-bit)**.  
4. In **Advanced Settings (⚙️ gear)**:  
   - Enable **SSH**.  
   - Username: `sky`  
   - Hostname: `polaris`  
   - (Optional) Set up Wi-Fi.  
5. Flash the OS to the SSD and safely eject.  

---

## 🔹 Step 2: Boot from SSD
1. Connect the SSD enclosure to Polaris.  
2. Power on the Raspberry Pi 5.  
3. It should boot directly from the SSD (ensure EEPROM is updated for USB boot).  

Check with:
```bash
lsblk
