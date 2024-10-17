# WireGuard VPN Setup on Raspberry Pi

This project demonstrates setting up a VPN using WireGuard on a Raspberry Pi, allowing secure connections from multiple devices, including Windows and macOS. The goal is to provide a lightweight and efficient VPN solution for secure access to the local network from remote locations.

## Tools Used
* WireGuard: For VPN setup and secure tunneling.
* Raspberry Pi: Acts as the VPN server running WireGuard.
* Windows and macOS: Devices connected to the VPN server using WireGuard client.
* SSH: Used for server management and client configurations.
* Paramiko & Python: Automating device information retrieval via SSH connections  to be processed and stored.

## Project Overview
This project focuses on creating a WireGuard VPN server on a Raspberry Pi. It demonstrates how to connect both Windows and macOS devices to the VPN server to enable remote secure access to the Raspberry Pi’s network. By utilizing the WireGuard protocol, this solution offers a high-performance VPN with modern cryptography.

## WireGuard Setup Process
1. __Install WireGuard on the Raspberry Pi__

- Begin by installing WireGuard on your Raspberry Pi. You can either use a package manager (e.g., apt) or compile it from source.
- After installation, configure the server to act as a VPN hub for external devices.

2. __Configure the VPN__

- Configure the WireGuard server using the appropriate key pairs, allowed IP ranges, and DNS settings. These configurations are stored in a .conf file, which the server uses to accept incoming connections.

3. __Client Configuration__

- Download and install WireGuard on your Windows and macOS devices.
- Use the WireGuard GUI to generate the necessary public/private keys and create a new tunnel using the server’s information.

## Configuring WireGuard Using the GUI

1. __Install WireGuard__
Download and install the WireGuard application on your system (available for Windows, macOS, and Linux).

2. __Create a New Tunnel__
Open the WireGuard application, then click Create a new tunnel or Add Tunnel.

3. __Generate Key Pairs__
The GUI will generate a public/private key pair for your device. These keys are used for securing the connection.

4. __Configure the Tunnel__
In the configuration window, input your connection details:

- PrivateKey: Generated for your device.
- Address: Client's IP address, provided by the VPN server.
- DNS: Optionally specify the DNS server (e.g., 8.8.8.8).

5. __Add Peer (Server Information)__
Add the VPN server information:

- PublicKey: Public key of the VPN server.
- Endpoint: Server IP and port (e.g., vpn.example.com:51820).
- AllowedIPs: Use 0.0.0.0/0, ::/0 to route all traffic through the VPN.

6. __Activate the Connection__
Once configured, click Activate or Save to bring the VPN tunnel online.