# Halley (Pi Zero WH) Reinstall Checklist

## Step 1: Flash Image
- [ ] Download Pwnagotchi Bullseye build (jayofelony or chosen release)
- [ ] Flash to microSD using Raspberry Pi Imager
- [ ] Edit config files for usb0 networking if needed

## Step 2: Boot & Config
- [ ] Boot Pi Zero
- [ ] Set hostname → halley
- [ ] Set static IP → 10.10.10.30 (or use DHCP reservation)
- [ ] Enable SSH and copy SSH key from control station

## Step 3: Pwnagotchi Setup
- [ ] Edit `/etc/pwnagotchi/config.yml`
  - name = "halley"
  - handshakes directory = /home/pi/handshakes/
  - web ui = enabled
- [ ] Enable systemd service and test status
- [ ] Verify handshakes appear in /home/pi/handshakes/

## Step 4: Connectivity Test
- [ ] From Exoplanet: `ping halley`
- [ ] SSH in → `ssh pi@halley`

## Step 5: Save configs to repo
- [ ] Commit `config/halley-pwnagotchi.conf` to GitHub
