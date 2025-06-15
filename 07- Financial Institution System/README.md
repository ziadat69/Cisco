# Financial Services Ltd (JFSL) Network Design and Implementation

This repository contains the complete network design and implementation for Jubilee Financial Services Ltd (JFSL), a finance service provider based in Nairobi, Kenya. The design is built using Cisco Packet Tracer and follows a robust hierarchical network model with an emphasis on security, scalability, redundancy, and performance.
Project Overview



## JFSL operates across two floors of an eleven-story building, with five departments:

   1th Floor: Human Resource (HR), Customer Service (CS), Marketing (MK)

   2th Floor: Legal Management (LM), Information Technology (IT)

Each department has user devices, IP phones, and WiFi access points. The company requires a secure and efficient network infrastructure that includes LAN, WAN, and an external server site.
Key Requirements

    Separate VLAN and subnet for each department with inter-VLAN routing.

    Voice VLAN (VID 120) for IP phones across all departments.

    Dynamic IP addressing for user devices via dedicated DHCP servers hosted offsite.

    Static IP addressing for server-side devices.

    Redundant internet connections using two ISPs (Safaricom and JTL) with load balancing.

    VoIP telephony configured on Cisco Catalyst 2811 router.

    Site-to-site IPsec VPN between HQ and external server location.

    Network security via Access Control Lists (ACL), SSH access restricted to ICT department.

    Switch port security using sticky MAC address method.

    Routing with OSPF across routers and multilayer switches.

    NAT and PAT configuration on edge routers.

    Wireless network on each floor for user connectivity.

    Fully tested and validated network topology and configurations.



![Netzwerkdiagramm](ciscopic.png) 

![Netzwerkdiagramm](ciscopic.png)


## Technologies and Concepts Implemented

    Hierarchical Network Design Model with redundancy

    VLAN creation and subnetting for data and voice traffic

    Inter-VLAN Routing on multilayer switches (SVI)

    DHCP for dynamic IP allocation (Data and Voice)

    SSH configuration and access control with ACLs

    OSPF routing protocol on routers and switches

    NAT/PAT for outbound internet traffic with ACL rules

    Port Security on server site switches

    VoIP telephony setup with Cisco routers

    Site-to-site IPsec VPN for secure WAN communication



## The topology satisfies all user and management requirements with verified, tested, and working configurations. It includes:

    Two Cisco Catalyst 2911 routers (HQ and server-side)

    One Cisco Catalyst 2811 router for VoIP

    Two multilayer switches at HQ

    Six access switches connected to respective departments

    Connections to two ISP providers for redundancy

    Wireless Access Points on every department floor

## Getting Started

    Prerequisites:

        Cisco Packet Tracer installed (recommended version 8.x or above)

    Load the Packet Tracer File:
    Open the provided .pkt file in Cisco Packet Tracer to explore the full network design and configuration.

    Explore Configurations:
    View detailed device configurations including VLANs, ACLs, DHCP settings, OSPF routing, VoIP setup, NAT, and VPN.

    Test Communication:
    Verify device connectivity, VoIP calls, internet access redundancy, and VPN tunnel functionality.

## Files Included

    pk7.pkt — Cisco Packet Tracer project file


