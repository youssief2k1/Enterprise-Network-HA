# Advanced Enterprise Network Infrastructure

This repository contains the design and configuration for a comprehensive enterprise network simulation. The project focuses on implementing a robust, scalable, and secure network infrastructure using advanced routing, switching, and security protocols.

## 📖 Project Overview

The goal of this project is to build a complete enterprise network from the ground up, simulating real-world scenarios that require high availability, security, and efficient traffic management. The design incorporates a hierarchical network model with distinct core, distribution, and access layers, and it establishes connectivity between two separate Autonomous Systems (AS 100 and AS 400).

---

## ✨ Key Features & Technologies Implemented

This project demonstrates a practical application of modern networking principles and includes the configuration of the following technologies:

*   **VLANs:** Network segmentation into four distinct VLANs (10, 20, 30, 40) to isolate traffic and enhance security.
*   **Rapid Spanning Tree Protocol (RSTP):** A loop-free Layer 2 topology with configured primary and secondary root bridges for redundancy.
*   **Hot Standby Router Protocol (HSRP):** First-hop redundancy for client gateways, ensuring seamless failover.
*   **DHCP & DNS:** Centralized DHCP server for automatic IP allocation and internal DNS servers for name resolution.
*   **OSPF (Open Shortest Path First):** Dynamic interior gateway routing within the enterprise network.
*   **BGP (Border Gateway Protocol):** Exterior gateway routing to establish connectivity with an external ISP and between autonomous systems.
*   **NAT (Network Address Translation):**
    *   **Static NAT:** To make an internal web server accessible from the public internet.
    *   **PAT (NAT Overload):** To allow all internal users to access the internet using a single public IP address.
*   **Access Control Lists (ACLs):** Granular traffic filtering to enforce security policies, such as restricting access from a specific VLAN to a public resource.
*   **DHCP Snooping:** A Layer 2 security feature to protect against rogue DHCP servers and mitigate infrastructure attacks.
*   **Telnet:** Enabled for remote management and administration of all network devices.

---

## 🎯 Project Objectives

The project successfully achieved the following 12 technical objectives:

1.  **VLAN Configuration:** Segmented the network using VLANs 10, 20, 30, and 40.
2.  **Spanning Tree Protocol (RSTP):** Established a resilient, loop-free Layer 2 topology.
3.  **Hot Standby Router Protocol (HSRP):** Provided redundant gateway services for end-users.
4.  **DHCP Server:** Deployed a centralized server for automated IP address management.
5.  **DNS Server:** Configured internal name resolution services.
6.  **OSPF Routing:** Implemented dynamic routing for the internal network.
7.  **PAT & Web Server Access:** Enabled internet access for internal clients and configured public access to a web server.
8.  **Static NAT:** Mapped a public IP to the internal web server.
9.  **BGP to ISP:** Established external connectivity via BGP.
10. **Access Control Lists (ACLs):** Implemented a security policy to restrict traffic.
11. **DHCP Snooping:** Secured the network against unauthorized DHCP servers.
12. **Remote Access:** Enabled Telnet for remote device management.

---

## 🌐 Network Topology

The network consists of the following simulated hardware:

*   **12 x** End-user PCs
*   **6 x** Access Layer Switches
*   **4 x** Multilayer (Distribution/Core) Switches
*   **4 x** Routers
*   **3 x** Servers (2 DNS Servers, 1 Web Server)

---

## ⚙️ Configuration Files

This repository can be structured to hold the configuration files for each device. A recommended structure is as follows:
/
├── configs/
│   ├── switches/
│   │   ├── access-sw1.txt
│   │   ├── access-sw2.txt
│   │   ├── dist-sw1.txt
│   │   └── dist-sw2.txt
│   ├── routers/
│   │   ├── R1.txt
│   │   ├── R2.txt
│   │   └──...
│   └── servers/
│       ├── dhcpd.conf
│       └── named.conf
└── README.md
```

---

## ✔️ Verification

The network's functionality was thoroughly tested and validated. Key verification steps included:
*   Successful `ping` tests between all internal VLANs.
*   Confirmed end-to-end connectivity between devices in AS 100 and AS 400.
*   Verification that clients correctly received IP addresses from the DHCP server.
*   Successful DNS queries for internal resources.
*   Validation of the ACL rule blocking specific traffic.
*   Confirmation that PAT and Static NAT were functioning as designed.
*   Successful Telnet connections to network devices for remote management.
