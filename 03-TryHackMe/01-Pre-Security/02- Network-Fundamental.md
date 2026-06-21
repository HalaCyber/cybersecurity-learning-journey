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

---

## Subnetting

Subnetting is the process of splitting a large network into smaller networks (sub-networks).

It helps in organizing and managing networks more efficiently.

### Subnet Mask

A subnet mask is used to define how many hosts can exist in a network.

It is represented as a 32-bit number (similar to an IP address), usually in the range of 0–255.

### Network Address

This address identifies the start of a network and represents the network itself.

### Host Address

A host address is used to identify a specific device inside a network.

### Default Gateway

The default gateway is a device (usually a router) that allows communication between different networks.

---

## ARP (Address Resolution Protocol)

ARP is used to map IP addresses to MAC addresses within a network.

### ARP Request

A device broadcasts a request asking:
"Who has this IP address?"

### ARP Reply

The device that owns the IP address responds with its MAC address.

---

## DHCP (Dynamic Host Configuration Protocol)

DHCP automatically assigns IP addresses to devices in a network.

### DHCP Discover

A device sends a request to find a DHCP server and obtain an IP address.

### DHCP Request

The device requests the offered IP address from the server.

### DHCP ACK

The DHCP server confirms and assigns the IP address to the device.

---

## OSI Model (Open Systems Interconnection)

The OSI Model is a framework that describes how data moves across a network.

It is divided into 7 layers:

### Layer 7 - Application
Where users interact with network services (e.g., DNS, web browsing).

### Layer 6 - Presentation
Translates and formats data for the application layer.

### Layer 5 - Session
Manages communication sessions between devices.

### Layer 4 - Transport

Responsible for data delivery.

#### TCP (Transmission Control Protocol)
- Reliable
- Connection-based
- Used for web browsing, email, file transfers

#### UDP (User Datagram Protocol)
- Faster but less reliable
- No connection required
- Used for streaming and real-time data

### Layer 3 - Network
Handles routing using IP addresses.

### Layer 2 - Data Link
Handles MAC addressing and physical device communication.

### Layer 1 - Physical
Deals with hardware, cables, and electrical signals.

---

## Packets and Frames

### Packet
A packet is data sent at Layer 3 (Network Layer). It contains IP information.

### Frame
A frame is data at Layer 2 (Data Link Layer) and includes MAC address information.

### Time To Live (TTL)
Limits how long a packet can stay in the network before being discarded.

### Checksum
Used to verify data integrity during transmission.

---

## TCP/IP Model

The TCP/IP model is a simplified version of the OSI model.

It has 4 layers:
- Application
- Transport
- Internet
- Network Interface

### TCP (Transmission Control Protocol)

TCP is a connection-based protocol.

#### Advantages:
- Reliable data transfer
- Ensures correct order of data
- Error checking included

#### Disadvantages:
- Slower than UDP
- Requires stable connection

### Three-Way Handshake

Used to establish a connection:

- SYN: Initiates connection
- SYN-ACK: Response from server
- ACK: Final confirmation

### Connection Termination

- FIN: Closes connection
- RST: Abruptly terminates connection

---

## UDP (User Datagram Protocol)

UDP is a connectionless protocol.

- Faster than TCP
- No guarantee of delivery
- Used for streaming and real-time applications

---

## Common Network Ports and Protocols

- FTP: Port 21 (File Transfer)
- SSH: Port 22 (Secure remote login)
- HTTP: Port 80 (Web browsing)
- HTTPS: Port 443 (Secure web browsing)
- SMB: Port 445 (File sharing)
- RDP: Port 3389 (Remote desktop access)

---

## Firewall & Network Security

A firewall controls incoming and outgoing network traffic.

It decides whether traffic is allowed or blocked based on rules.

### Stateful Firewall
Tracks full connections and blocks based on behavior.

### Stateless Firewall
Inspects individual packets without tracking the full connection.

---

## VPN (Virtual Private Network)

A VPN creates a secure encrypted connection (tunnel) between devices over the internet.

### Benefits:
- Increased privacy
- Secure communication
- Protects data over public networks

---

## VLAN (Virtual Local Area Network)

A VLAN divides a physical network into multiple logical networks.

It helps improve security and performance by separating traffic.

