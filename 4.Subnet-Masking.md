# Subnet Masking and Network Segmentation

---

## What is a Subnet Mask?

A **Subnet Mask** is a numerical value used with an IP address to determine which portion of the address represents the **network** and which portion represents the **host**.

It helps divide large networks into smaller logical networks called **subnets**.

Example:
IP Address:192.168.1.10

Subnet Mask:255.255.255.0

In this case:

- Network portion → `192.168.1`
- Host portion → `10`

This means the device belongs to the **192.168.1.0 network**.

---

## How Subnet Masks Work

Subnet masks work through **binary operations**.

An IPv4 address contains **32 bits**, divided into four octets.

Example:

IP Address(192.168.1.10)

Binary Representation(11000000.10101000.00000001.00001010)

Subnet Mask(255.255.255.0)

Binary Mask(11111111.11111111.11111111.00000000)


The **1s represent the network portion**, while the **0s represent the host portion**.

This mechanism allows routers to determine:

- which devices belong to the same network
- where packets should be routed

---

## CIDR Notation

Modern networks use **CIDR (Classless Inter-Domain Routing)** notation.

CIDR expresses the subnet mask using a prefix length.

Example: 192.168.1.10/24


Here:

- `/24` means **24 bits are used for the network**
- the remaining **8 bits are used for hosts**

Common subnet examples:

| CIDR | Subnet Mask | Number of Hosts |
|-----|-------------|----------------|
| /8 | 255.0.0.0 | 16,777,214 |
| /16 | 255.255.0.0 | 65,534 |
| /24 | 255.255.255.0 | 254 |
| /30 | 255.255.255.252 | 2 |

CIDR allows more **efficient allocation of IP addresses**.

---

## Why Subnetting is Important

Subnetting provides several advantages in network design.

### Efficient IP Address Management

Large networks can be divided into smaller segments, preventing IP address waste.

---

### Improved Network Performance

Smaller networks reduce broadcast traffic and improve overall network efficiency.

---

### Network Organization

Subnetting helps administrators organize networks logically based on departments, locations, or services.

Example:

192.168.10.0 for HR Department

192.168.20.0 for Finance Department

192.168.30.0 for IT Department


---

### Enhanced Security

Subnetting enables **network segmentation**, which is a major security strategy.

Different types of systems can be isolated from each other.

---

## Subnetting and Security

Subnetting plays a critical role in modern **network security architecture**.

By dividing networks into segments, organizations reduce the risk of attackers moving freely within the network.

This is known as **network segmentation**.

---

## Preventing Lateral Movement

**Lateral movement** occurs when attackers gain access to one system and then move through the internal network to compromise additional systems.

Subnetting limits this movement.

Example:

Without segmentation:
All devices in one network
192.168.1.0/24

If one device is compromised, attackers may access all systems.

With segmentation:

192.168.10.0 is for user devices

192.168.20.0 is for servers

192.168.30.0 is for databases


Security controls between these networks can block unauthorized communication.

---

## Demilitarized Zone (DMZ)

A **DMZ (Demilitarized Zone)** is a network segment designed to host public-facing services while protecting the internal network.

Examples of systems placed in a DMZ include:

- Web servers
- Mail servers
- DNS servers
- Application gateways

Typical architecture:
Internet
|
Firewall
|
DMZ Network
|
Internal Firewall
|
Internal Network


Benefits:

- Public services are isolated from internal systems
- Internal networks remain protected even if a DMZ server is compromised

---

## Public vs Private Network Segmentation

Organizations often separate **public networks** from **private internal networks**.

Example architecture:

Public Network:Web servers
API gateways
Load balancers


Internal Network:Database servers
Employee systems
Internal applications


This separation protects critical internal systems from direct Internet exposure.

---

## Defense-in-Depth Architecture

Subnetting is an important part of the **Defense-in-Depth** security strategy.

Defense-in-Depth means implementing multiple layers of security controls.

Example layers:
Internet
|
Perimeter Firewall
|
DMZ Network
|
Internal Firewall
|
Internal Subnets
|
Critical Systems


Even if attackers bypass one security control, additional layers still protect sensitive resources.

---

## Zero Trust and Network Segmentation

Modern security architectures follow the **Zero Trust model**.

Zero Trust assumes that **no device or user should be automatically trusted**, even inside the network.

Subnetting supports Zero Trust by:

- isolating systems
- enforcing strict access policies
- controlling communication between network segments

---

## Security Perspective Summary

Subnet masking and subnetting are essential tools for designing scalable and secure networks.

They enable:

- efficient IP address management
- logical network organization
- segmentation of critical systems
- protection against lateral movement attacks
- implementation of layered security architectures

When combined with firewalls, access controls, and monitoring systems, subnetting becomes a powerful mechanism for improving overall network security.
