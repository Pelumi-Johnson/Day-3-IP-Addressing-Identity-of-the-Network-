# 🖧 Day 3 | IP Addressing (Identity of the Network)

## 🎯 Objective
Understand what an IP address is and how devices recognize and communicate with each other on a network.

---

## 🧠 Core Idea
Without an IP address, a device exists but cannot be reached.

---

## 🌐 What is an IP Address?

Example:
192.168.1.10

It consists of:
- Network portion (identifies the network)
- Host portion (identifies the device)

### 📸 IP Addressing Concept / Diagram
![IP Address Concept](https://github.com/Pelumi-Johnson/Day-3-IP-Addressing-Identity-of-the-Network-/blob/main/ChatGPT%20Image%20Mar%2027%2C%202026%2C%2002_23_00%20PM.png)

---

## 🧠 Analogy
- Network = street name  
- Host = house number  

Devices on the same network can communicate directly.  
Devices on different networks require a router.

---

## 🧪 Lab Setup

Rebuilt the network topology from memory:
- 1 Router
- 1 Switch
- 2 PCs
- Straight-through cables

### 📸 Rebuilt Topology
![Topology](https://github.com/Pelumi-Johnson/Day-3-IP-Addressing-Identity-of-the-Network-/blob/main/Screenshot%202026-03-27%20024815.png)

---

## ⚙️ IP Configuration

### PC0
IP Address: 192.168.1.10  
Subnet Mask: 255.255.255.0  
Default Gateway: 192.168.1.1  

### PC1
IP Address: 192.168.1.11  
Subnet Mask: 255.255.255.0  
Default Gateway: 192.168.1.1  

### 📸 PC IP Configuration
![PC IP Config](https://github.com/Pelumi-Johnson/Day-3-IP-Addressing-Identity-of-the-Network-/blob/main/Screenshot%202026-03-27%20024942.png)

---

### Router Configuration

enable  
configure terminal  
interface gigabitEthernet 0/0  
ip address 192.168.1.1 255.255.255.0  
no shutdown  

### 📸 Router IP Configuration
![Router IP Config](https://github.com/Pelumi-Johnson/Day-3-IP-Addressing-Identity-of-the-Network-/blob/main/Screenshot%202026-03-27%20025058.png)
---

## 🧠 Subnet Mask Understanding

255.255.255.0 defines the network boundary.

Devices in:
- 192.168.1.x → same network  
- 192.168.2.x → different network  

### 📸 Subnet / Network Boundary Visualization
![Subnet Explanation](subnet.png)

---

## 📡 Connectivity Test

ping 192.168.1.11  

## 💥 Failure Test (Network Break)

Changed PC1 IP to:
192.168.2.11  

### 📸 Failed Communication
![Ping Failure](https://github.com/Pelumi-Johnson/Day-3-IP-Addressing-Identity-of-the-Network-/blob/main/Screenshot%202026-03-27%20025414.png)

---

## 🧠 Key Concepts Learned

- IP address uniquely identifies a device
- Devices must share the same network to communicate directly
- Subnet mask defines network boundaries
- Different networks require routing
- Incorrect IP addressing breaks communication even if connections are correct

---

## 🔁 Practical Reinforcement

- Rebuilt the network from memory
- Assigned IPs manually
- Tested successful communication
- Broke the network intentionally
- Diagnosed and fixed the issue

---

## ✅ Outcome

Developed a clear understanding of how IP addressing enables communication between devices and how subnetting determines network boundaries.

This lab reinforced the importance of understanding both configuration and underlying logic.
