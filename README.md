# WireGuard VPN Setup on Raspberry Pi
Project Overview
This project demonstrates the creation of a secure VPN using WireGuard on a Raspberry Pi, enabling remote access to a Windows laptop and a MacBook over an encrypted network. The goal is to provide a secure way to connect and communicate across devices via a private VPN, ensuring data privacy and security.

# Tools Used
WireGuard (VPN software)
Raspberry Pi (VPN server)
Windows OS (Client)
macOS (Client)
SSH (For secure remote access)
Features
Secure VPN: Implements WireGuard VPN on Raspberry Pi, providing encrypted communication between devices.
Cross-Platform Compatibility: Enables remote access between Windows and macOS machines.
Data Privacy: Secures communication channels and shields traffic from external networks.
Prerequisites
Before starting, ensure you have the following:

# A Raspberry Pi running Linux.
WireGuard installed on your Raspberry Pi, Windows laptop, and MacBook.
SSH access to the Raspberry Pi for remote configuration.
Setup Instructions
Install WireGuard on the Raspberry Pi by following the steps in the official documentation here.

Configure the Raspberry Pi as the WireGuard server:

# Generate public and private keys.
Set up the WireGuard server configuration file with proper IP address ranges and firewall rules.
Install WireGuard on your clients (Windows and Mac) and import the .ovpn configuration files for both devices.

Connect Clients to the VPN by enabling the WireGuard interface on your Windows laptop and MacBook.

Verify the Connection:

Ping between devices or check if the remote devices are accessible.
Usage
Once the setup is complete, use the WireGuard client on each device to initiate a connection to the VPN. All traffic between the devices will now be routed securely through the WireGuard VPN.

# Future Plans
Integrating additional devices into the VPN.
Automating the configuration process with scripts.
Adding monitoring and logging features for network traffic.

# License
This project is licensed under the MIT License.
