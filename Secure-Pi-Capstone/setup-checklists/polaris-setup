# Polaris (Pi 5) Initial Setup Checklist

## Date: Sept 27–28, 2025

### Step 1: Base System
- [x] Flashed **Raspberry Pi OS Lite (64-bit)** to NVMe SSD via Pironman 5.
- [x] Booted Pi 5 and set hostname → `polaris`.
- [x] Assigned static IP → `10.10.10.10`.
- [x] Enabled SSH access and connected from Exoplanet (control VM).

### Step 2: System Updates & Tools
- [x] Updated OS with `apt update && apt full-upgrade`.
- [x] Installed essential tools: `git`, `python3-pip`, `i2c-tools`, etc.

### Step 3: Pironman 5 Case & Fans
- [x] Installed Pironman software (`~/pironman`).
- [x] Confirmed `pironman-cli` commands working.
- [x] Located and edited `~/pironman/config.txt`.
- [x] Set RGB options, fan temp threshold = 50 °C.
- [x] Tested manual fan control with `pironman-cli --fan`.
- [x] Verified **case fans working**.
- [x] Troubleshot **tower cooler fan** (initially stopped after boot).
- [x] Downgraded kernel (6.12 → 6.6.16 → 6.6.44).
- [x] Enabled I²C and reinstalled support packages.
- [x] Confirmed **tower fan now functional** (spins at threshold).
- [x] Removed unused kernel versions from `/lib/modules`.

### Step 4: Status
✅ All fans operational (2× case RGB fans + tower cooler).  
✅ System stable on **kernel 6.6.44**.  
✅ Polaris ready for next phase: Suricata + AI stack setup.
