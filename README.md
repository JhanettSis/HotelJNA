
## 🚀 Enterprise LAN/WAN Infrastructure: Designing for Resilience

This project provides a technical blueprint and configuration files for a robust, secure, and redundant network infrastructure designed for a multi-department enterprise. It emphasizes centralized security, high availability, and efficient resource management.

---

## ✨ Key Technical Stack & Features

| Feature Area | Technology / Protocol | Core Benefit |
| :--- | :--- | :--- |
| **Routing** | **OSPF** (Open Shortest Path First) | Dynamic routing with **fast convergence** and loop prevention. |
| **Security** | **AAA, TACACS+, SSH** | Centralized, encrypted administrative access and strong user accountability. |
| **Access Control** | **Standard/Extended ACLs** | Granular traffic filtering and strict segregation between sensitive zones. |
| **Segmentation** | **VLANs** (10-80) | Broadcast domain control, improved performance, and security policy enforcement. |
| **IP Management** | **DHCP Services** | Automated, efficient IP address allocation across all user segments. |

---

## 🗺️ Network Topology: Triangular High Availability

The core backbone utilizes a **triangular redundancy** model with three interconnected routers (**R1, R2, R3**) using dedicated serial links.

> 💡 **Benefit:** This structure eliminates single points of failure between routers, ensuring **stable routing** and **critical redundancy** for inter-router communication in the event of a link failure.

---

## 🛡️ Core Security and Management Implementations

### Centralized Management with AAA

* Leveraged the **AAA framework** and **TACACS+** for all remote access (SSH).
* Ensures all administrative login attempts are verified against a **central server**, enforcing strong credentials and providing clear **accounting** records (who, when, what).

### Layer 2 & 3 Segmentation

* Implemented comprehensive **VLAN segmentation** (VLAN 10 through VLAN 80) across all user and server groups (e.g., Sales, HR, Admin, Server Zone).
* Utilized **Access Control Lists (ACLs)** on router interfaces to strictly control traffic flow between these segmented workgroups, protecting sensitive data.

---

## 📈 Performance & Scalability

* **Efficient Routing:** OSPF dynamically handles route calculations, minimizing network downtime and administrative overhead when adding new subnets.
* **Automated IP:** Routers are configured as **DHCP servers** for multiple VLANs, reducing client configuration errors and accelerating deployment time.

Logical separation of departments reduces broadcast domains, isolates traffic, and improves overall network security.
