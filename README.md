# homelab-infrastructure
Personal infrastructure lab built using Linux, virtualization, and monitoring tools to practice networking, system administration, and security concepts.


## Hardware & Roles

| Device         | Specs                                      | Role                                  | Notes                                                       |
| -------------- | ------------------------------------------ | ------------------------------------- |------------------------------------------------------------ |
| Arch Laptop    | HP EliteBook 840 G3, 16GB RAM, 256GB NVMe  | Daily driver + Gateway + Zabbix Server| NAT/IPv4 forwarding, MASQUERADE, Tailscale VPN, Proxmox nodes|
|Proxmox Node 1  | HP ProDesk 600 G5 SFF, 8GB RAM, 256GB NVMe | Primary virtualization host           | qm 1 : Ubuntu Server, LXC Snipe-IT, static IP |
| Mobile Hotspot | wifi (wlan0)  or Mobile etherthing         | Internet source                       | Provides temporary internet; either Arch or Proxmox can connect|      
| Nokia Modem    | ADSL modem                                 | Dumb switch                           | DHCP off, provides LAN connectivity to Proxmox nodes            |                              
# Services
Zabbix
Pi-hole
Monitoring

# Skills Demonstrated

- Linux system administration
- Network configuration and NAT
- Virtualization using Proxmox
- Infrastructure monitoring using Zabbix
- DNS filtering with Pi-hole
- SSH remote administration
