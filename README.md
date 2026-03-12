# homelab-infrastructure
Personal infrastructure lab built using Linux, virtualization, and monitoring tools to practice networking, system administration, and security concepts.


## Devices & Roles

| Device             | Specs                                      | Role                                   | Notes                                                                                           |
| -------------- | ------------------------------------------ | ------------------------------------- |------------------------------------------------------------ |
| Arch Laptop    | HP EliteBook 840 G3, 16GB RAM, 256GB NVMe  | Daily driver + Gateway + Zabbix Server| NAT / IPv4 forwarding, MASQUERADE, optional Tailscale VPN, monitors Proxmox nodes               |
|Proxmox Node 1  | HP ProDesk 600 G5 SFF, 8GB RAM, 256GB NVMe | Primary virtualization host           | VMs: Linux server, Windows Server (light), LXC containers (Snipe-IT), static IP, mostly offline |
| Mobile Hotspot | wifi (wlan0)  or Mobile etherthing         | Internet source                       | Provides temporary internet; either Arch or Proxmox can connect|      
| Nokia Modem    | ADSL modem                                 | Dumb switch                           | DHCP off, provides LAN connectivity to Proxmox nodes            |                              
