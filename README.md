# homelab-infrastructure
Personal infrastructure lab built using Linux, virtualization, and monitoring tools to practice networking, system administration, and security concepts.

---

## Overview

This homelab simulates a small infrastructure environment with:

- Linux gateway
- NAT and IPv4 forwarding
- Virtualization using Proxmox
- Infrastructure monitoring
- DNS filtering
- SSH-based remote management

The lab is used to practice **Linux administration, networking, and infrastructure monitoring**.

---

## Hardware

| Device         | Specs                                      | Role                                  | Notes                                                       |
| -------------- | ------------------------------------------ | ------------------------------------- |------------------------------------------------------------ |
| Arch Laptop    | HP EliteBook 840 G3, 16GB RAM, 256GB NVMe  | Daily driver + Gateway + Zabbix Server| NAT/IPv4 forwarding, MASQUERADE, Tailscale VPN, Proxmox nodes|
|Proxmox Node 1  | HP ProDesk 600 G5 SFF, 8GB RAM, 256GB NVMe | Primary virtualization host           | qm 1 : Ubuntu Server, LXC Snipe-IT, static IP |
| Mobile Hotspot | wifi (wlan0)  or Mobile etherthing         | Internet source                       | Provides temporary internet; either Arch or Proxmox can connect|      
| Nokia Modem    | ADSL modem                                 | Dumb switch                           | DHCP off, provides LAN connectivity to Proxmox nodes            |                              
## Network Architecture

![Network Diagram](network-diagram.png)

Network configuration:

- Subnet: 192.168.1.0/24
- Gateway: 192.168.1.105
- DNS: Pi-hole (192.168.1.150)
- Secondary DNS: 1.1.1.1
-----
## Virtual Machines & Containers

### Proxmox Host

**VM 1**
Ubuntu Server  
Zabbix Agent

**VM 2**
Pi-hole DNS filtering

**LXC Containers**

Planned:
- Snipe-IT (IT asset management)


## Services Running
Zabbix
Pi-hole
Monitoring

### Zabbix Monitoring
Infrastructure monitoring for:
- Proxmox node
- system performance
- network health

-------

### Pi-hole DNS
Network-wide DNS filtering and ad blocking.

----

# Skills Demonstrated

- Linux system administration
- Network configuration and NAT
- Virtualization using Proxmox
- Infrastructure monitoring using Zabbix
- DNS filtering with Pi-hole
- SSH remote administration

---

## Future Improvements

- Deploy Snipe-IT container
- Add SIEM monitoring
- Infrastructure automation scripts
- Expand monitoring dashboards
