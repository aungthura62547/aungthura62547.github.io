# Palo Alto Basic Config

## Basic Palo Alto Firewall Setup
Quick guide to get a Palo Alto firewall (PA-Series/VM) running for a simple LAN-to-WAN setup.

## What You Need
- Palo Alto firewall with admin access (`admin/admin`).
- PC on MGT port (default: `192.168.1.1/24`).
- Basic IP knowledge.

## Steps
1. **Connect to Firewall**
```
ssh 192.168.1.1
or GUI at https://192.168.1.1**
ping 192.168.1.1
