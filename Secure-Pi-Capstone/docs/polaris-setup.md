# 🛰️ Polaris Setup (Raspberry Pi 5 - Defender)

## Step 1: Flash OS to microSD
- Device: Raspberry Pi 5 (16GB)
- Boot Device (temporary): microSD card
- OS: Raspberry Pi OS Lite (64-bit)

**Raspberry Pi Imager settings (example):**
- Hostname: `<choose-a-hostname>`
- Username: `<choose-a-username>`
- Password: `<set-a-secure-password>`
- Wi-Fi SSID: `<your-wifi-ssid>`
- Wi-Fi Password: `<your-wifi-password>`
- SSH: Enable SSH (choose password or key authentication)
- Timezone: `<your-timezone>`

*(Do not store personal passwords or sensitive values in this repo.)*

## Step 2: First Boot
1. Insert the microSD into the Pi 5.
2. Power on the Raspberry Pi 5 inside the Pironman case.
3. Confirm the device shows up on the network.
4. Test SSH:
   ```bash
   ssh <username>@<hostname>.local
