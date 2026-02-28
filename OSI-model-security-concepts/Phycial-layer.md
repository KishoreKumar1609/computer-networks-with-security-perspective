# Introduction to the OSI model
OSI model is know as the Open System Interconnections developed by the ISO which is a standard framework communicating devices in the network

**Overview of the OSI model** 

| Layer No | Layer Name        | Main Function                                   | Common Protocols / Examples |
|-----------|------------------|-------------------------------------------------|------------------------------|
| 7 | Application Layer | Provides network services to end-user applications | HTTP, HTTPS, FTP, DNS, SMTP |
| 6 | Presentation Layer | Data formatting, encryption, compression | SSL/TLS, JPEG, ASCII |
| 5 | Session Layer | Establishes, manages, and terminates sessions | NetBIOS, RPC |
| 4 | Transport Layer | End-to-end communication and reliability | TCP, UDP |
| 3 | Network Layer | Logical addressing and routing | IP, ICMP, IPsec |
| 2 | Data Link Layer | Physical addressing and error detection | Ethernet, ARP, MAC |
| 1 | Physical Layer | Transmission of raw bits over medium | Cables, Hub, Fiber |


# Physical Layer Security

---

## Overview

The **Physical Layer** is the first layer of the OSI model and is responsible for transmitting raw bits through physical media such as cables, connectors, and wireless signals.
Since this layer deals mainly with hardware and transmission media, it is highly vulnerable to physical and environmental attacks.

---
## Common Physical Layer Components
- Network cables (Ethernet, Fiber Optic)
- Connectors and ports
- Network Interface hardware
- Hubs and switches
- Wireless transmission media (Wi-Fi, Bluetooth)
  
---
## Physical Layer Attack Vectors:

### 1. Cable Interception:
Attackers may gain physical access to network cables and intercept transmitted signals.
#### Possible Attacks
- Cable tapping to capture transmitted data
- Unauthorized connection to exposed Ethernet ports
#### Risk
Sensitive information can be captured during transmission if physical protection is weak.

---
### 2. Wireless Signal Exploitation:
Wireless technologies such as **Wi-Fi** and **Bluetooth** transmit data through open air, making interception easier.
#### Possible Attacks
- Packet sniffing using specialized software
- Unauthorized network access
- Exploitation of weak encryption mechanisms
#### Risk
Weak cryptographic configurations may allow attackers to monitor or access network traffic.

---
### 3. Unauthorized Physical Access:
Improper physical security controls allow attackers direct access to networking infrastructure.
#### Possible Attacks
- Accessing unlocked server or network rooms
- Connecting malicious USB devices or storage media
- Installing rogue hardware devices
- Copying sensitive data using external drives
#### Risk
Physical access can bypass logical and software-based security controls.

---
## Physical Layer Security Measures
### Cable Security
- Use organized and isolated cable management
- Avoid exposed or publicly accessible wiring
- Implement secure cable routing
- Perform regular physical inspections

---
### Wireless Security
- Use strong WiFi encryption protocols such as **WPA2** or **WPA3** 
- Disable unused wireless services
- Monitor unauthorized access points
- Apply strong authentication mechanisms

---
### Physical Access Control
- Restrict access to server and networking rooms
- Implement authorization-based entry systems
- Use surveillance and manual security monitoring
- Disable unused network ports
- Control removable storage device usage

---
## Security Perspective Summary

> Physical layer security focuses on preventing unauthorized physical interaction with networking infrastructure.  
> Even strong software security becomes ineffective if physical access is compromised.
