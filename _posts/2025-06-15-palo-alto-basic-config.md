# Basic Palo Alto Firewall Setup

Quick guide to get a Palo Alto firewall (PA-Series/VM) running for a simple LAN-to-WAN setup.

## What You Need
- Palo Alto firewall with admin access (`admin/admin`).
- PC on MGT port (default: `192.168.1.1/24`).
- Basic IP knowledge.

## Steps
1. **Connect to Firewall**:
   - SSH to `192.168.1.1` or GUI at `https://192.168.1.1`.
   - Test: `ping 192.168.1.1`.

2. **Set Management IP**:
   ```bash
   configure
   set deviceconfig system ip-address 192.168.10.10 netmask 255.255.255.0 default-gateway 192.168.10.1 dns-setting servers primary 8.8.8.8
   commit
