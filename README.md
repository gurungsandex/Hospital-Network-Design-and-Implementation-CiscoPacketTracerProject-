# Hospital-Network-Design-and-Implementation-CiscoPacketTracerProject-
This project is a Hospital Network Design and Implementation built in Cisco Packet Tracer.

# Why this project matters:
- It gives important networking concepts like VLANs, Subnetting, Routing (OSPF), DHCP, Redundancy, and LAN/WAN design.
- It's an excellent hands-on learning experience for networking professionals preparing for real-world IT and cybersecurity roles.

# Project Details
- Two Main Sites: HQ and Branch
- Server Site for hosting DHCP and DNS
- 9 VLANs for department segmentation
- Subnetting is properly implemented for each VLAN.
- OSPF configured for dynamic routing.
- Redundant ISP Routers added for Internet Failover.
- DHCP Server used to assign IPs dynamically.
- DNS Server added for domain name resolution.

# Network Diagram
<img width="1428" alt="network diagram" src="https://github.com/user-attachments/assets/59dde4ea-c9a0-4c41-bc28-08ac312171cf" />


# VLAN Table
<img width="660" alt="vlan table" src="https://github.com/user-attachments/assets/7a4f4ea6-1f9e-469b-b245-3b1e8724a7f5" />

# Commands 
**Basic Router and Switch Setup**
- enable
- configure terminal
- hostname [Device-Name]
- enable secret [password]
- no ip domain-lookup

**VLAN Creation (on Switches)**
- vlan 10
- name ADMIN
- exit
- vlan 20
- name BILLING
- exit
....

**Assign Ports to VLAN (Access Mode)**
- interface fastEthernet0/1
- switchport mode access
- switchport access vlan 10
- exit
.....


**Trunk Ports (Switch to Router or Switch to Switch)**
- interface gigabitEthernet0/1
- switchport trunk encapsulation dot1q
- switchport mode trunk
- exit

**OSPF Configuration (Dynamic Routing)**
- router ospf 1
- network 192.168.100.0 0.0.0.255 area 0
- network 192.168.102.64 0.0.0.15 area 0
- exit

**IP Helper Address (On Router Interfaces) - Tell VLAN where to get DHCP from**
Example for VLAN 90 Interface:
- interface gigabitEthernet0/0.90
- ip helper-address 192.168.102.67
- exit

# DHCP Server Setup (on DHCP Server)
<img width="1050" alt="dhcp pool" src="https://github.com/user-attachments/assets/c03b8822-4c84-441a-934b-bf6df6928bbf" />

    
# Conclusion
This project showcases a full real-world hospital network with enterprise-level design practices such as:
✅ VLAN segmentation

✅ DHCP and DNS services

✅ Redundancy setup

✅ OSPF dynamic routing

✅ Server hosting

✅ Wireless and wired connectivity

I am actively updating this project to add new features and technologies, such as:
    🔒 Firewall Rules and Access Control Lists (ACLs)
    🏳️‍🌈 VLAN Spanning Tree Protocol (STP) for Loop Prevention
    📈 SNMP Network Monitoring Configuration
    📊 Syslog Servers for Network Logging
    🛡️ VPN Setup between HQ and Branch (future phase)
    ☁️ Cloud Connectivity Simulation


It's a living project — updated regularly to incorporate more technologies and best practices as I continue growing as a Network Engineer and Cybersecurity Professional.
I hope this project inspires others to build, test, and upgrade their own networks!


# Take the initiative to dive into this project yourself and start working hands-on.
- Clone this repository
- Open the .pkt file with Cisco Packet Tracer (Version XX or later)
- Explore the topology, configurations, and server settings
- Feel free to modify, improve, or build on top of this project!








