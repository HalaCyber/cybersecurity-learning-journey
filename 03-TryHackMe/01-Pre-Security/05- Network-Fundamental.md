# Module 5 - Network Fundamentals

## What is a Network?

A network is a group of devices or systems connected together to communicate and share resources.

The Internet is a global network made up of many interconnected networks.

**Private networks** are typically internal networks used by organizations, homes, and other environments, while **public networks** are accessible beyond a private network.

---

## IP and MAC Addresses

Devices use different types of identifiers to communicate on a network, including:

- **IP Address (Internet Protocol Address)**
- **MAC Address (Media Access Control Address)**

### IP Address

An IP address is used to identify a device or network interface within a network or address scope.

- IP addresses can change depending on the network.
- An IP address must be unique within the same network or address scope to avoid address conflicts.

### Public vs Private IP Address

- A **Public IP Address** is routable on the Internet.
- A **Private IP Address** is used within a private/local network.

Private IPv4 address ranges include:

- `10.0.0.0/8`
- `172.16.0.0/12`
- `192.168.0.0/16`

Public IP addresses are commonly assigned by an Internet Service Provider (ISP).

### IPv4 vs IPv6

| Protocol | Address Size | Address Capacity |
|---|---:|---:|
| IPv4 | 32-bit | Up to 2³² addresses |
| IPv6 | 128-bit | Up to 2¹²⁸ addresses |

### MAC Address

A MAC address is a hardware/network interface identifier typically represented as 12 hexadecimal characters (48 bits).

The first 24 bits are commonly associated with the vendor through the **OUI (Organizationally Unique Identifier)**.

> **Note:** MAC addresses can be modified through a process known as **MAC Spoofing**.

### Ping (ICMP)

Ping is a network utility used to test connectivity between devices.

It commonly works by sending **ICMP (Internet Control Message Protocol)** messages and waiting for a response.

---

## LAN Topologies

A network topology describes how devices are connected within a network.

### Star Topology

In a Star Topology, devices connect to a central device such as a switch.

**Advantages:**
- Easy to add new devices.
- Easy to manage and troubleshoot.

**Disadvantages:**
- Failure of the central device can affect connected devices.

### Bus Topology

A Bus Topology uses a single backbone cable to connect multiple devices.

### Ring Topology

In a Ring Topology, devices are connected in a loop.

**Advantages:**
- Can provide predictable traffic flow.

**Disadvantages:**
- A failure in the ring can disrupt communication, depending on the implementation.

---

## Networking Devices

### Switch

A switch connects multiple devices within the same local network and forwards Ethernet frames based on MAC addresses.

**Examples:**
- Computers
- Printers
- Servers
- Other network-enabled devices

### Router

A router connects different networks and forwards packets between them using IP addressing and routing information.

---

## Subnetting

Subnetting is the process of dividing a larger network into smaller networks (subnets).

It helps organize networks, manage IP addressing, and control network traffic.

### Subnet Mask

A subnet mask determines which portion of an IPv4 address represents the network and which portion represents the host.

### Network Address

The network address identifies the network itself and is not normally assigned to an individual host.

### Host Address

A host address identifies a specific device or interface within a network.

### Default Gateway

The default gateway is typically a router or Layer 3 device that allows a host to communicate with other networks.

---

## ARP (Address Resolution Protocol)

ARP is used in IPv4 networks to map an IP address to a MAC address on the local network.

### ARP Request

A device broadcasts a request asking:

> "Who has this IP address?"

### ARP Reply

The device that owns the IP address responds with its MAC address.

---

## DHCP (Dynamic Host Configuration Protocol)

DHCP automatically provides network configuration information to devices.

A typical DHCP process is known as **DORA**:

**Discover → Offer → Request → ACK**

### DHCP Discover

A device broadcasts a message to discover available DHCP servers.

### DHCP Offer

A DHCP server offers an IP address and other network configuration information.

### DHCP Request

The client requests the offered configuration.

### DHCP ACK

The DHCP server confirms the configuration and assigns the requested network information.

---

## OSI Model (Open Systems Interconnection)

The OSI Model is a conceptual framework that describes how network communication can be divided into seven layers.

### Layer 7 - Application

Provides network services used by applications.

**Examples:** HTTP, DNS, FTP, SSH.

### Layer 6 - Presentation

Handles data representation, translation, encoding, and formatting.

### Layer 5 - Session

Manages communication sessions between applications or systems.

### Layer 4 - Transport

Provides end-to-end transport and communication.

**Examples:** TCP and UDP.

### Layer 3 - Network

Handles logical addressing and routing using IP addresses.

### Layer 2 - Data Link

Handles local network communication, frames, and MAC addressing.

### Layer 1 - Physical

Deals with physical transmission through hardware, cables, radio signals, and electrical/optical signals.

---

## Packets and Frames

### Packet

A packet is a unit of data at the Layer 3 Network Layer and contains information such as source and destination IP addresses.

### Frame

A frame is a unit of data at the Layer 2 Data Link Layer and contains information such as source and destination MAC addresses.

### Time To Live (TTL)

TTL limits the number of Layer 3 hops a packet can make before it is discarded.

### Checksum

A checksum is used to help detect errors or corruption in transmitted data.

---

## TCP/IP Model

The TCP/IP model is a practical networking model commonly represented using four layers:

- Application
- Transport
- Internet
- Network Interface

---

## TCP (Transmission Control Protocol)

TCP is a connection-oriented protocol that provides reliable and ordered data delivery.

### Advantages

- Reliable data transfer
- Ensures correct ordering of data
- Error detection and recovery mechanisms

### Three-Way Handshake

The TCP three-way handshake establishes a connection:

1. **SYN** — The client initiates the connection.
2. **SYN-ACK** — The server acknowledges the request and sends its own SYN.
3. **ACK** — The client acknowledges the server's response.

### Connection Termination

- **FIN** — Used for graceful connection termination.
- **RST** — Used to immediately reset a connection.

---

## UDP (User Datagram Protocol)

UDP is a connectionless transport protocol.

- Low overhead
- No built-in guarantee of delivery
- No built-in ordering
- Useful for applications where low latency is important

---

## Common Network Ports and Protocols

| Protocol | Port | Common Use |
|---|---:|---|
| FTP | 21 | File Transfer |
| SSH | 22 | Secure Remote Login |
| HTTP | 80 | Web Traffic |
| HTTPS | 443 | Secure Web Traffic |
| SMB | 445 | File/Resource Sharing |
| RDP | 3389 | Remote Desktop |

---

## Firewall & Network Security

A firewall controls incoming and outgoing network traffic based on predefined rules.

### Stateful Firewall

A stateful firewall tracks the state of active connections and uses connection state when making filtering decisions.

### Stateless Firewall

A stateless firewall evaluates packets individually based on predefined rules without maintaining connection state.

---

## VPN (Virtual Private Network)

A VPN establishes an encrypted tunnel between endpoints, depending on the VPN protocol and configuration.

### Benefits

- Increased privacy
- Secure communication
- Protection of data when using untrusted networks

---

## VLAN (Virtual Local Area Network)

A VLAN divides a physical switched network into multiple logical networks.

VLANs provide logical segmentation and can help separate traffic between different groups of devices.
