# Secure-Pi: An Advanced AI-Powered Cybersecurity Testbed

## Project Overview
This project is a self-contained, high-performance cybersecurity testbed built on a Raspberry Pi 5. Its primary goal is to demonstrate the practical application of AI in network security by detecting and analyzing simulated attacks. The system is designed to be a portfolio piece for a WGU capstone and a presentation to the CCD AI committee, showcasing skills in hardware integration, system administration, and machine learning.

The project uses a multi-device setup to simulate a real-world attack-and-defense scenario, with a centralized AI-powered defender, a dedicated honeypot, and a mobile attacker.

---

## Key Features
- **AI-Powered Threat Detection:** Leverages a Hailo-8L AI Accelerator to perform real-time analysis of network traffic and identify malicious behavior.  
- **High-Speed & Secure System:** Runs the operating system and applications from a fast NVMe SSD for superior performance and reliability.  
- **Controlled Lab Environment:** Uses an isolated network with a dedicated attacker and honeypot to ensure all testing is safe and contained.  
- **Modular & Professional:** Built with high-quality components and a professional aesthetic, suitable for a capstone project.  
- **Comprehensive Logging & Reporting:** Collects and analyzes logs from all devices, with a dashboard for visualization and final reporting.  

---

## System Architecture
- **Defender:** Raspberry Pi 5 (Polaris), running the AI defense stack.  
- **Attacker:** Raspberry Pi Zero WH (Halley), running Pwnagotchi.  
- **Honeypot:** Raspberry Pi 3B (Singularity), acting as a decoy for attackers.  
- **Control Station:** VM (Exoplanet), providing remote management.  

**Data Flow:**  
Halley (attacker) → generates malicious traffic  
Singularity (honeypot) → captures logs and events  
Polaris (defender) → ingests/analyzes logs with AI → produces alerts & final report  

---

## Hardware & Software Stack

**Hardware**
- Raspberry Pi 5 (16GB) — *Polaris*  
- Sunfounder Pironman 5 case with tower cooler + RGB fans  
- Lexar NM620 512GB NVMe SSD  
- Hailo-8L M.2 AI Module (13T)  
- Official Raspberry Pi 27W USB-C PD power supply  
- Raspberry Pi Zero WH — *Halley* (attacker)  
- Raspberry Pi 3B — *Singularity* (honeypot)  
- Control Station VM — *Exoplanet*  

**Software**
- Raspberry Pi OS Lite (64-bit)  
- Suricata (IDS)  
- OpenCanary (honeypot service)  
- TensorFlow Lite + Hailo toolchain (AI inference)  
- Tools: tcpdump, ssh, rsync  

---

## Network Naming & IP Scheme
| Device              | Role                | Hostname    | Static IP   |
|---------------------|---------------------|-------------|-------------|
| Raspberry Pi 5      | Defender/Server     | Polaris     | 10.10.10.10 |
| Raspberry Pi 3B     | Honeypot/Victim     | Singularity | 10.10.10.20 |
| Raspberry Pi ZeroWH | Attacker            | Halley      | 10.10.10.30 |
| VM                  | Control Station     | Exoplanet   | 10.10.10.40 |

---

## Project Roadmap

### ✅ Phase 1: Hardware Setup & System Foundation (Complete)
- Assembled Pironman 5 kit and installed OS on NVMe SSD.  
- Configured and verified all fans (RGB + tower cooler).  
- Cleaned up redundant kernel versions; system stable on `6.6.44-v8-16k+`.  
- Established secure SSH access.  
- Configured isolated lab network.  

### 🔜 Phase 2: Building the AI-Powered Defense Stack (In Progress)
- Set up Pi Zero WH and Pi 3B with attacker/honeypot roles.  
- Install and configure Suricata on Polaris.  
- Implement data collection pipeline and AI model.  

### 📊 Phase 3: Finalizing the Deliverables
- Build the final dashboard and reporting tools.  
- Write and submit the WGU capstone report.  
