# Singularity (Pi 3B) Reinstall Checklist

## Step 1: Flash Image
- [ ] Download Raspberry Pi OS Lite (64-bit)
- [ ] Flash to microSD using Raspberry Pi Imager

## Step 2: Boot & Config
- [ ] Boot Pi 3B
- [ ] Set hostname → singularity
- [ ] Set static IP → 10.10.10.20 (or DHCP reservation)
- [ ] Enable SSH and copy SSH key from control station

## Step 3: OpenCanary Setup
- [ ] Install Python3 and pip
- [ ] `pip3 install opencanary`
- [ ] Copy default config and edit (~/.opencanary.conf)
- [ ] Enable and start opencanaryd service
- [ ] Verify logs appear in /var/log/opencanary/

## Step 4: Connectivity Test
- [ ] From Exoplanet: `ping singularity`
- [ ] SSH in → `ssh pi@singularity`

## Step 5: Save configs to repo
- [ ] Commit `config/singularity-opencanary.conf` to GitHub
