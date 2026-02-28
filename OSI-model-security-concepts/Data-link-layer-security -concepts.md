# Data Link Layer Security
---
## Overview
The **Data Link Layer (Layer 2)** is responsible for node-to-node communication within a local network.  
It handles **physical addressing**, frame transmission, and error detection using **MAC addresses**.
Since this layer operates inside local networks, attackers often exploit it to perform interception and impersonation attacks.

---
## Common Data Link Layer Components
- MAC Addressing
- Ethernet Frames
- Switches and Bridges
- ARP (Address Resolution Protocol)
- VLANs
---

## Data Link Layer Attack Vectors
### 1. MAC Address Spoofing
MAC address spoofing occurs when an attacker changes their device's MAC address to impersonate another legitimate device on the network.
#### Possible Attacks
- Bypassing network access controls
- Device impersonation
- Unauthorized network access

#### Risk
Attackers may gain trusted network access by pretending to be an authorized system.

---
### 2. ARP Cache Poisoning
**ARP** maps IP addresses to MAC addresses within a local network.
Attackers manipulate ARP tables by sending forged ARP responses.
#### Possible Attacks
- Man-in-the-Middle (MITM) attacks
- Traffic interception
#### Risk
Network traffic can be redirected through the attacker’s system without user awareness.

---
### 3. MAC Address Flooding
MAC flooding targets network switches by overwhelming them with fake MAC addresses.
This forces the switch to send traffic to all the ports.
#### Possible Attacks
- Exhausting switch MAC address tables
- Forcing switch behavior similar to a hub
- Traffic sniffing across the network
#### Risk
Attackers may capture network traffic intended for other devices.

---
## Data Link Layer Security Measures
### MAC Address Filtering
- Allow only trusted MAC addresses on network devices
- Restrict unauthorized device connections

---
### ARP Inspection
- Implement **Dynamic ARP Inspection (DAI)**
- Validate ARP packets before updating ARP tables
- Prevent forged ARP responses

---
### Port Security
- Limit the number of MAC addresses allowed per switch port
- Disable ports when suspicious activity is detected
- Prevent MAC flooding attacks

---
### Encryption and Data Protection
- Use strong encryption mechanisms
- Protect sensitive data even if interception occurs
- Secure endpoints to reduce compromise impact

---
## Security Perspective Summary

> The Data Link Layer is a major target inside local networks because trust is often assumed between connected devices.  
> Proper switch configuration and monitoring are essential to prevent internal network attacks.
