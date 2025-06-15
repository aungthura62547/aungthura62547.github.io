# Basic Palo Alto Firewall Configuration

## Overview
This guide walks you through the initial configuration of a Palo Alto Networks Next-Generation Firewall (NGFW), such as a PA-Series or VM-Series, to get it up and running in a lab or small network. As a network engineer, you’ll learn to set up the management interface, security zones, data interfaces, a basic security policy, and NAT rules to allow internet access. This post is perfect for beginners or those setting up a firewall for the first time.

- **Target Audience**: Network engineers new to Palo Alto or setting up a lab.
- **Prerequisites**: 
  - Basic networking knowledge (IP addressing, subnets).
  - Access to a Palo Alto firewall (physical or virtual) with admin credentials (default: `admin/admin`).
  - A computer connected to the firewall’s management (MGT) port or console port.
  - Internet access for license activation and updates.

## Key Concepts
- **Management Interface**: Used for GUI/CLI access, typically on the MGT port (default IP: `192.168.1.1/24`).
- **Security Zones**: Logical groupings (e.g., `trust`, `untrust`) to control traffic between interfaces.
- **Virtual Router**: Handles routing, including static routes for network connectivity.
- **Security Policies**: Rules to allow or block traffic based on source, destination, and application.
- **NAT Rules**: Translate private IPs to public IPs for internet access.

## Step-by-Step Guide
Follow these steps to configure a basic Palo Alto firewall setup with a LAN (inside) and WAN (outside) interface, allowing internet access.

### 1. Connect to the Firewall
- **GUI Access**:
  - Connect an Ethernet cable from your computer to the firewall’s MGT port.
  - Set your computer’s IP to `192.168.1.2/24` (gateway: `192.168.1.1`).
  - Open a browser and navigate to `https://192.168.1.1`.
  - Log in with `admin/admin` (change the password later for security).
- **CLI Access**:
  - Use a serial console cable (9600-8-N-1) with a terminal emulator (e.g., PuTTY).
  - Alternatively, SSH to `192.168.1.1` after setting the management IP.
- **Verify Connectivity**:
  ```bash
  ping 192.168.1.1
