# Deep-In-Net: Networking Fundamentals

![Server Room](https://learn.zone01oujda.ma/api/content/root/01-edu_module/content/deep-in-net/pictures/serverRoomMeme.jpg)

##  Project Overview

**Deep-In-Net** is a comprehensive exploration of fundamental networking concepts using **Cisco Packet Tracer**. This project covers the design, configuration, and troubleshooting of network infrastructures, ranging from simple peer-to-peer connections to complex multi-subnet routing environments.

As a Cloud and DevOps-focused project, it emphasizes understanding the OSI model, essential protocols (DHCP, DNS, FTP, HTTP/S), and the command-line interface (CLI) for network management.

##  Learning Objectives

- **Device Mastery:** Identify and configure Hubs, Switches, and Routers.
- **Protocol Proficiency:** Implement and manage DHCP, DNS, FTP, and HTTPS.
- **OSI Model Analysis:** Understand which layers different devices and protocols operate on.
- **Subnetting & Routing:** Design logical network segments and manage routing tables.
- **Linux Integration:** Use standard networking commands for troubleshooting.

---

## Tools & Prerequisites

- **Cisco Packet Tracer:** The primary simulation environment.
- **CLI Knowledge:** Familiarity with Linux commands (`ping`, `traceroute`, `ip addr`) and Cisco IOS.
- **Methodology:** All IP calculations and configurations were performed manually without the use of IP Subnet Calculators.

---

## 📂 Project Structure

The repository is organized by exercises, each represented by a `.pkt` (Packet Tracer) file.

```bash
.
├── ex01.pkt      # Basic Physical Connectivity (Cables)
├── ex02.pkt      # Layer 2 Devices (Hubs vs Switches)
├── ex03.pkt      # Network Services (DHCP, DNS, FTP, HTTPS)
├── ex04.pkt      # Layer 3 Basics (Routers & Gateways)
├── ex05.pkt      # Subnet Communication I
├── ex06.pkt      # Routing Tables & Static Routing
├── ex07.pkt      # Subnet Communication II
├── ex08.pkt      # Complex Multi-Subnet Architecture
└── README.md     # Documentation
```

---

## Exercise Breakdown & Knowledge Base

### Exercise 1: Physical Layer & Cables

    *   **Goal:** Establish direct communication between PC pairs
    *   **Key Concept:** Understanding **RJ-45** cables.
    *   **Straight-through:** Used to connect dissimilar devices (e.g., PC to Switch).
    *   **Crossover:** Used to connect similar devices (e.g., PC to PC, or Switch to Switch).

### Exercise 2: Layer 2 - Hubs vs. Switches

*   **Goal:** Create star topologies using intermediate devices.
*   **Key Concept:** 
    *   **Hub (Layer 1):** Broadcasts data to all ports; creates a single collision domain.
    *   **Switch (Layer 2):** Uses MAC addresses to send data only to the specific destination; reduces collisions.

### Exercise 3: Network Services & Protocols

*   **Goal:** Build a server-heavy infrastructure.
*   **Configurations:**
    *   **DHCP Server:** Dynamic IP assignment for all workstations.
    *   **HTTPS Server:** Secured web traffic. `HTTP` disabled.
    *   **FTP Server:** User `deepinnet` with `RWDNL` (Read, Write, Delete, Name, List) permissions.
    *   **DNS Server:** 
        *   `deep-in-net.local` -> `192.168.1.99`
        *   `deep-in-net.com` -> CNAME to `deep-in-net.local`
*   **Protocol Table:**

| Protocol | Port | OSI Layer | Transport |
| :--- | :--- | :--- | :--- |
| DHCP | 67/68 | Layer 7 (App) | UDP |
| DNS | 53 | Layer 7 (App) | UDP/TCP |
| HTTP | 80 | Layer 7 (App) | TCP |
| HTTPS | 443 | Layer 7 (App) | TCP |
| FTP | 20/21 | Layer 7 (App) | TCP |

### Exercise 4: Layer 3 - Routing

*   **Goal:** Connect two PCs in different networks using a Router.
*   **Key Concept:** The **Default Gateway**. It acts as the exit point for traffic leaving the local subnet to reach a different network.

### Exercise 5-8: Advanced Subnetting & Static Routing

*   **Goal:** Interconnecting multiple subnets (Subnet 1, 2, and 3).
*   **Routing Table:** A data table stored in a router that lists the routes to particular network destinations. 
*   **Static Routing:** Manually configuring the next-hop IP address for specific destination networks in the Router's CLI.

---

## Essential Networking Commands

Throughout this project, the following commands were used for configuration and verification:

| Command | Purpose |
| :--- | :--- |
| `hostname` | Verify/Set the device name. |
| `ipconfig` | (Windows/PT) View IP configuration. |
| `ping` | Test end-to-end connectivity (ICMP). |
| `traceroute` | Map the path packets take to a destination. |
| `show ip route` | (Cisco) View the current routing table. |
| `show ip int brief` | (Cisco) Quick status of all interfaces. |

---
## Final Network

![Final Network](https://learn.zone01oujda.ma/api/content/root/01-edu_module/content/deep-in-net/pictures/ex08.jpg)

---

## 🔗 Resources
*   [Cisco Networking Basics](https://www.cisco.com/c/en/us/solutions/small-business/resource-center/networking/networking-basics.html)
*   [OSI Model Explained](https://www.cloudflare.com/learning/network-layer/what-is-the-osi-model/)
*   [Cisco IOS Command Reference](https://www.cisco.com/c/en/us/td/docs/ios-xml/ios/fundamentals/command/cf_command_ref.html)

---
*Developed as part of the Deep-In-Net module for Cloud/DevOps training.*