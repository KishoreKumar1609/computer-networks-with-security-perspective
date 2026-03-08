# VLAN Security and Network Segmentation

---

## What is a VLAN?

A **VLAN (Virtual Local Area Network)** is a logical method of segmenting a physical network into multiple isolated broadcast domains.

Instead of relying on separate physical switches, VLANs allow network administrators to divide a single switch into multiple logical networks.

This enables devices in the same VLAN to communicate as if they were on the same physical network, even if they are connected to different switch ports.

VLANs operate at the **Data Link Layer (Layer 2)** of the OSI model.

---

## Why VLANs are Important

VLANs are widely used in enterprise networks to improve:

- Network organization
- Traffic management
- Security segmentation
- Performance

By separating network traffic into different segments, VLANs reduce unnecessary broadcast traffic and limit potential attack surfaces.

---

## VLAN Segmentation

**VLAN segmentation** separates network devices into logical groups based on function, department, or security level.

Example VLAN structure:

VLAN 10 – Human Resources

VLAN 20 – Finance

VLAN 30 – Servers

VLAN 40 – Guest Network


Each VLAN forms its own **broadcast domain**, meaning broadcast traffic stays within that VLAN.

### Security Benefits

- Limits broadcast traffic
- Reduces network congestion
- Isolates sensitive departments
- Prevents attackers from easily reaching critical systems
- Restricts attack spread inside the network

If an attacker compromises a device in VLAN 10, they **cannot automatically access VLAN 20 or VLAN 30** without passing through routing controls.

---

## Inter-VLAN Communication

Devices in different VLANs cannot communicate directly.

To communicate between VLANs, traffic must pass through a **Layer 3 device**, such as:

- Router
- Layer 3 Switch
- Firewall

Typical architecture:

User VLAN
|
Switch
|
Router / Layer 3 Switch
|
Server VLAN
