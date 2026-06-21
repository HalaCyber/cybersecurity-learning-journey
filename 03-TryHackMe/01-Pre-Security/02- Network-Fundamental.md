# Module 2 - Network Fundamentals

## What is a Network?

Networks are simply things connected together.

The Internet is one giant network that consists of many smaller networks. These smaller networks are called **private networks**, while the networks that connect them together are known as **public networks**.

---

## IP and MAC Addresses

Devices have two main methods of identification:

- **IP Address (Internet Protocol Address)**
- **MAC Address (Media Access Control Address)**

### IP Address

An IP address is used to identify a device on a network.

- IP addresses can change depending on the network.
- The same IP address cannot be used by two active devices on the same network simultaneously.

#### Public vs Private IP Address

- A **Public IP Address** identifies a device on the Internet.
- A **Private IP Address** identifies a device within a local network.

Public IP addresses are usually assigned by an Internet Service Provider (ISP).

### IPv4 vs IPv6

| Protocol | Size | Address Capacity |
|-----------|------|------------------|
| IPv4 | 32-bit | Up to 2³² addresses |
| IPv6 | 128-bit | Up to 2¹²⁸ addresses |

### MAC Address

A MAC address is a unique 12-character identifier assigned to a network interface.

- The first six characters identify the manufacturer.
- The last six characters uniquely identify the device.

> Note: MAC addresses can be modified through a process known as **MAC Spoofing**.

### Ping (ICMP)

Ping is a network utility used to test connectivity between devices.

It works by sending **ICMP (Internet Control Message Protocol)** packets and waiting for a response.

---

## LAN Topologies

A network topology describes how devices are connected within a network.

### Star Topology

In a Star Topology, devices connect to a central device such as a switch or hub.

**Advantages:**
- Easy to add new devices.
- Easy to manage and troubleshoot.

**Disadvantages:**
- More expensive due to the central device.

### Bus Topology

A Bus Topology uses a single backbone cable to connect all devices.

### Ring Topology

In a Ring Topology, devices connect directly to each other to form a loop.

**Advantages:**
- Less prone to bottlenecks compared to a Bus Topology.

**Disadvantages:**
- A single cable failure can disrupt the entire network.

---

## Networking Devices

### Switch

A Switch connects multiple devices within the same network using Ethernet connections.

Examples include:

- Computers
- Printers
- Servers
- Other network-enabled devices

### Router

A Router connects different networks together and forwards data between them.
