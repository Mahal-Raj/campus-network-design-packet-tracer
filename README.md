# Campus Network Design & Implementation (Cisco Packet Tracer)

![Cisco Packet Tracer](https://img.shields.io/badge/Tool-Cisco%20Packet%20Tracer-blue)
![Project Type](https://img.shields.io/badge/Type-Network%20Simulation-green)
![Level](https://img.shields.io/badge/Level-Enterprise-orange)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 📌 Project Overview

This project demonstrates the design and implementation of an enterprise-level Campus Network using Cisco Packet Tracer.

The network is designed using a three-tier hierarchical architecture consisting of:

- Core Layer  
- Distribution Layer  
- Access Layer  

The implementation includes VLAN segmentation, Inter-VLAN routing (Router-on-a-Stick), DHCP configuration, trunking, server setup, and complete end-to-end connectivity testing.

This project showcases practical enterprise networking skills and Cisco device configuration knowledge.

---

## 🎯 Objectives

- Design a scalable and structured campus network
- Implement VLAN segmentation for departmental isolation
- Configure Inter-VLAN routing
- Set up DHCP for dynamic IP allocation
- Establish secure communication between departments
- Perform network testing and validation

---

## 🏗️ Network Architecture

### 🔹 Core Layer
- Provides backbone connectivity
- Handles routing between distribution devices
- Centralized traffic management

### 🔹 Distribution Layer
- Performs Inter-VLAN routing
- Enforces policies
- Connects Access layer to Core layer

### 🔹 Access Layer
- Connects end-user devices
- Assigns VLANs to switch ports
- Provides direct network access

---

## 🛠️ Technologies & Concepts Used

- Cisco Packet Tracer (8.x)
- VLAN Configuration
- 802.1Q Trunking
- Router-on-a-Stick
- DHCP Server Configuration
- Static Routing
- OSPF (if implemented)
- DNS / HTTP Server (optional)
- Wireless Access Point (optional)

---

## 🗺️ Network Features

- Multiple VLANs for departmental separation
- Trunk links between switches
- Router sub-interface configuration
- DHCP-based automatic IP assignment
- Server integration
- Successful cross-VLAN communication
- Simulation mode packet verification

---

## 📊 VLAN & IP Addressing Scheme

| VLAN | Department | Network Address     | Default Gateway   |
|------|------------|--------------------|------------------|
| 10   | Admin      | 192.168.10.0/24    | 192.168.10.1     |
| 20   | IT         | 192.168.20.0/24    | 192.168.20.1     |
| 30   | HR         | 192.168.30.0/24    | 192.168.30.1     |
| 40   | Students   | 192.168.40.0/24    | 192.168.40.1     |

---

## ⚙️ Configuration Highlights

### VLAN Creation (Switch)

```
vlan 10
 name ADMIN

vlan 20
 name IT

vlan 30
 name HR
```

### Access Port Configuration

```
interface fastEthernet0/1
 switchport mode access
 switchport access vlan 10
```

### Trunk Configuration

```
interface gigabitEthernet0/1
 switchport mode trunk
```

### Router-on-a-Stick Configuration

```
interface g0/0.10
 encapsulation dot1Q 10
 ip address 192.168.10.1 255.255.255.0
```

### DHCP Configuration

```
ip dhcp pool ADMIN
 network 192.168.10.0 255.255.255.0
 default-router 192.168.10.1
 dns-server 8.8.8.8
```

---

## 🧪 Testing & Validation

The following validations were performed:

- Same-VLAN connectivity tests
- Inter-VLAN communication verification
- DHCP IP address assignment check
- End-to-end ping tests
- Packet simulation tracking in Packet Tracer

All connectivity tests were successfully verified.

---


---

## 🚀 How to Run This Project

1. Install Cisco Packet Tracer (version 8.x recommended)
2. Download or clone this repository
3. Explore device configurations
4. Test connectivity using command prompt within Packet Tracer

---

## 📘 Learning Outcomes

This project demonstrates understanding of:

- Enterprise campus network design principles
- VLAN segmentation and trunking
- Inter-VLAN routing configuration
- DHCP deployment
- Hierarchical network architecture
- Network troubleshooting and validation

---

## 🔒 Future Enhancements

- Implement Access Control Lists (ACLs)
- Configure Spanning Tree Protocol (STP)
- Add EtherChannel for redundancy
- Implement full OSPF dynamic routing
- Add firewall and security policies

---

## 👤 Author

Sukhraj Singh  
Bachelor of Computer Science  
Networking & Systems Enthusiast  

---

