# Melbourne Health Services – Network Design and Security Implementation

## 📘 Project Overview

Melbourne Health Services is a healthcare organization based in Australia, operating from two sites within the same city: a main hospital (HQ) and a branch hospital located approximately 20 km away. The organization plans to transition from a third-party IT provider to an in-house IT infrastructure. This project focuses on designing and implementing a secure, scalable, and cost-effective hierarchical network architecture using Cisco Packet Tracer.


![Netzwerkdiagramm](ciscopic6.png)


## 🏥 Network Requirements

- **Locations**: Headquarter (HQ) & Branch
- **HQ Departments**: MLOCS, MER, MRM, IT, CS
- **Branch Departments**: NSO, HL, HR, MK, FIN
- **Each department** receives its own VLAN and subnet
- **Guest/Ward Area (GWA)** VLAN at both locations
- **Central Server Room** at HQ with DNS, DHCP, Web, and Mail servers
- **Secure communication** between HQ and Branch via IPSec VPN
- **Redundant Internet access** through two ISPs per site

## ⚙️ Network Technologies & Features

- Hierarchical network design (Core, Distribution, Access layers)
- VLAN architecture per department
- Inter-VLAN routing via Multilayer Switches
- OSPF as the dynamic routing protocol
- Serial WAN link between HQ and Branch routers
- IP subnetting based on `192.168.100.0/24`
- DHCP for dynamic IP assignment
- Static IP addressing for servers
- SSH for secure remote management
- NAT Overload (PAT) for Internet access
- Port security using sticky MAC addresses
- Site-to-site IPSec VPN between HQ and Branch
- Extended Access Control Lists (ACLs) to manage network access
- Wireless LANs (WLANs) with Access Points for each department
- Redundant Internet links via ISPs:
  - `195.136.17.0/30`
  - `195.136.17.4/30`
  - `195.136.17.8/30`
  - `195.136.17.12/30`

## 📐 Subnetting Details

Using the `192.168.100.0/24` private IP range:

- HQ departments: ~60 devices each → `/26` subnets
- Branch departments: ~30 devices each → `/27` subnets
- Separate subnets for GWA and server infrastructure

## 🔐 Security Configurations

- **SSH** access enabled on all routers and Layer 3 switches
- **ACLs** used to restrict access between departments and services
- **IPSec VPN** between HQ and Branch to secure WAN traffic
- **Port Security** enabled on server switchports (Sticky MAC, violation mode: shutdown)

## 🧪 Testing & Validation

✔ Inter-department communication verified  
✔ Internet access via NAT/PAT functioning  
✔ Inter-VLAN routing tested  
✔ VPN tunnel is active and encrypts traffic  
✔ ACLs successfully enforce access policies  
✔ WLAN connectivity available in all departments  
✔ DHCP assigns IPs correctly  
✔ SSH access and Port Security active  

## 📁 Project Files

- pr6.pkt`: Cisco Packet Tracer project file




## 🧑‍💻 Author

This project was created as a practical simulation of a hospital network infrastructure, focusing on data Confidentiality, Integrity, and Availability (CIA Triad).

---





