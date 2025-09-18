Secure-Pi: An Advanced AI-Powered Cybersecurity Testbed

Project Overview
This project is a self-contained, high-performance cybersecurity testbed built on a Raspberry Pi 5. Its primary goal is to demonstrate the practical application of AI in network security by detecting and analyzing simulated attacks. The system is designed to be a portfolio piece for a WGU capstone and a presentation to the CCD AI committee, showcasing skills in hardware integration, system administration, and machine learning.

The project uses a multi-device setup to simulate a real-world attack-and-defense scenario, with a centralized AI-powered defender, a dedicated honeypot, and a mobile attacker.

Key Features
AI-Powered Threat Detection: Leverages a Hailo-8L AI Accelerator to perform real-time analysis of network traffic and identify malicious behavior.

High-Speed & Secure System: Runs the operating system and applications from a fast NVMe SSD for superior performance and reliability.

Controlled Lab Environment: Uses an isolated network with a dedicated attacker and honeypot to ensure all testing is safe and contained.

Modular & Professional: Built with high-quality components and a professional aesthetic, suitable for a capstone project.

Comprehensive Logging & Reporting: Collects and analyzes logs from all devices, with a dashboard for visualization and final reporting.

System Architecture
Defender: The Raspberry Pi 5, running the AI defense stack.

Attacker: A Raspberry Pi Zero WH running Pwnagotchi.

Honeypot: A Raspberry Pi 3B, acting as a decoy for attackers.

Control Station: A VM on a separate computer for remote management.

Data Flow:
Pwnagotchi (Halley) generates malicious network traffic → Pi 3B (Singularity) acts as a decoy and captures logs → Pi 5 (Polaris) ingests and analyzes logs with AI → Pi 5 produces alerts and a final report.

Hardware & Software Stack
Hardware:

Main Server: Raspberry Pi 5 (16GB)

Case: Sunfounder Pironman 5 with Tower Cooler & Fan

SSD: Lexar NM620 512GB NVMe SSD

AI Accelerator: Hailo-8L M.2 AI Module (13T)

Power Supply: Official Raspberry Pi 27W USB-C PD Power Supply

Attacker: Raspberry Pi Zero WH

Honeypot: Raspberry Pi 3B

Control Station: Virtual Machine

Software:

Operating System: Raspberry Pi OS Lite (64-bit)

IDS: Suricata

Honeypot: OpenCanary (or similar)

AI Framework: TensorFlow Lite / Hailo Toolchain

Tools: tcpdump, ssh, rsync

Network Naming & IP Scheme
The project uses a unified celestial naming theme for a professional and secure lab environment.

Device	Role	Hostname	Static IP
Raspberry Pi 5	Defender/Server	Polaris	10.10.10.10
Raspberry Pi 3B	Honeypot/Victim	Singularity	10.10.10.20
Raspberry Pi Zero WH	Attacker	Halley	10.10.10.30
VM	Control Station	Exoplanet	10.10.10.40

Export to Sheets
Project Roadmap
Phase 1: Hardware Setup & System Foundation (In Progress)

Assemble the Pironman 5 kit and install the OS on the NVMe SSD.

Set up secure SSH access.

Configure the isolated lab network.

Phase 2: Building the AI-Powered Defense Stack

Set up the Pi Zero WH and Pi 3B with their respective software.

Install and configure Suricata on the Pi 5.

Implement the data collection pipeline and AI model.

Phase 3: Finalizing the Deliverables

Build the final dashboard and reporting tools.

Write the WGU capstone report.
