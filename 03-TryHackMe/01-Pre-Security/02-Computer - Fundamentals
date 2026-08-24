
# Module 2 - Computer Fundamentals

## 1. Types of Computers

Computers are not limited to laptops and smartphones. They are built into many everyday devices, from kitchen appliances to security cameras and smart home devices.

### Laptop

A **laptop** is a portable computer designed to be easy to carry and use in different locations.

- Portable and compact.
- Has limited cooling space because of its small size.
- Uses smaller fans, heat pipes, and heat sinks.
- May experience thermal throttling under heavy workloads.

### Desktop

A **desktop** is a computer designed to stay in one place.

- Usually has more space for cooling components.
- Can use larger fans and heat sinks.
- Usually provides better cooling and upgradeability than laptops.

### Workstation

A **workstation** is a powerful computer designed for professional and demanding workloads.

Examples include:

- 3D modeling
- Simulations
- Engineering
- Data processing

Workstations may use powerful CPUs and GPUs and can use **ECC RAM** to improve memory reliability.

### Server

A **server** is a computer or system that provides services, data, or resources to other computers or users over a network.

Servers are designed for reliability and continuous operation.

Common server features include:

- Redundancy
- Backups
- Monitoring
- Fault tolerance

**Redundancy** helps prevent a **single point of failure** by providing additional systems or components that can continue operating if one system fails.

---

## 2. Computers in Everyday Devices

Computers are built into many everyday devices to perform specific tasks.

Examples include:

- Smartphones
- Tablets
- Smart TVs
- Smartwatches
- Smart refrigerators
- Smart speakers
- Security cameras
- Wi-Fi routers
- Thermostats
- Robot vacuums

### Smartphone

A **smartphone** is a portable computer designed for connectivity, mobility, and battery efficiency.

Its hardware and software are optimized to provide useful performance while consuming relatively little power.

### Tablet

A **tablet** is a portable computer with a larger, touch-focused screen.

### IoT Device

An **IoT (Internet of Things)** device is a physical device that can connect to a network and send or receive data.

Examples:

- Smart thermostat
- Smart doorbell
- Fitness tracker

### Embedded Computer

An **embedded computer** is a computer system built into another device to perform a specific function.

Examples:

- Automatic door controller
- Coffee maker controller
- Embedded sensor controller

### IoT vs Embedded

**IoT** focuses on network connectivity and communication.

**Embedded** focuses on a computer system being built into another device to perform a specific function.

An embedded system does not necessarily require network connectivity.

> The most important computer is not always the fastest; it is the one that best fits the job.

---

## 3. Computer Cooling and Thermal Throttling

Computers generate heat while their components are operating.

Laptops have limited cooling space because of their compact design.

Desktops usually have more space for:

- Larger fans
- Better airflow
- Larger heat sinks
- Tower coolers

### Thermal Throttling

**Thermal throttling** is a mechanism used to reduce the performance or operating speed of a component when its temperature becomes too high.

A simplified process:

```text
High Temperature
       ↓
CPU Reduces Performance
       ↓
Less Heat Generated
       ↓
Temperature Decreases
       ↓
Prevents Overheating
````

Laptops may experience thermal throttling more easily than desktops because they have less space for cooling.

---

## 4. Smart Home Hub

A **Smart Home Hub** is a central device or system that coordinates and communicates with multiple smart home devices.

Examples:

* Smart lights
* Thermostats
* Smart locks
* Sensors
* Cameras

---

## 5. Client-Server Model

The **Client-Server Model** describes how computers and applications communicate to provide and use services.

```text
Client → Request → Server
Client ← Response ← Server
```

### Client

A **client** is a device or application that requests a service or resource.

Examples:

* Web browser
* Mobile application
* Email client

### Server

A **server** is a device or application that provides a service or resource to clients.

Examples:

* Web server
* File server
* Mail server
* Database server

### Network

A **network** is a group of connected devices that communicate and share data or resources.

### Port

A **port** is a logical communication endpoint used to identify a specific service or application on a device.

Example:

```text
192.168.1.10:443
```

* `192.168.1.10` → IP address of the device
* `443` → Port number

### Protocol

A **protocol** is a set of rules that defines how devices communicate and exchange data.

Examples:

* HTTP
* HTTPS
* DNS
* TCP

### Client-Server Relationship

```text
User
 ↓
Client
 ↓
Network
 ↓
Server
 ↓
Response
 ↓
Client
```

A client requests a service, and the server processes the request and provides a response.

---

## 6. HTTP

**HTTP (Hypertext Transfer Protocol)** is an application-layer protocol used for communication between web clients and web servers.

HTTP follows a **client-server model** and is **stateless**.

### Stateless

HTTP is **stateless**, meaning each request is processed independently.

The HTTP protocol itself does not automatically remember previous requests.

### HTTP Methods

HTTP methods define what the client wants to do.

Common methods include:

* **GET** → Retrieve a resource from a server.
* **POST** → Send data to a server.
* **PUT** → Replace or update a resource.
* **PATCH** → Partially update a resource.
* **DELETE** → Delete a resource.
* **HEAD** → Request headers without the response body.

---

## 7. HTTP GET Request

When a user enters a URL in a browser, the browser may send an HTTP GET request to the web server.

```text
Browser (Client)
      ↓
   GET Request
      ↓
Web Server
      ↓
   Response
      ↓
Browser
```

Example:

```http
GET /index.html HTTP/1.1
Host: example.com
```

### Important Request Components

**Scheme** → Specifies the protocol, such as HTTP or HTTPS.

**Host** → The domain name or host being requested.

**Path** → Identifies the requested resource.

**IP Address** → The network address used to communicate with the server.

### HTTP Response

An HTTP response commonly contains:

**Status Code** → Indicates the result of the request.

**Response Headers** → Contain metadata about the response.

**Response Body** → Contains the requested content or returned data.

### Common Status Code

**200 OK** → The request was successfully processed.

---

## 8. HTTP vs HTTPS

### HTTP

**HTTP** is a protocol used for communication between web clients and servers.

### HTTPS

**HTTPS** is HTTP protected using **TLS (Transport Layer Security)**.

```text
HTTP  → Web communication
HTTPS → Web communication + TLS protection
```

HTTPS helps protect data while it is transmitted between the client and server.

---

## 9. Virtualization

**Virtualization** allows multiple virtual computers or environments to run on a single physical computer.

Before virtualization, one physical server might run one main application or workload.

This could lead to:

* Higher costs
* Low resource utilization
* Slow deployment
* Difficult scaling

Virtualization allows multiple workloads to share the resources of the same physical hardware.

```text
Physical Server
       ↓
   Hypervisor
       ↓
 ┌─────┬─────┬─────┐
 VM1   VM2   VM3
```

---

## 10. Hypervisor

A **Hypervisor** is software or firmware that creates and manages Virtual Machines (VMs).

It manages physical resources such as:

* CPU
* RAM
* Storage
* Network resources

and allocates them to virtual machines.

### Type 1 Hypervisor

A **Type 1 hypervisor** runs directly on the physical hardware.

Commonly used in:

* Servers
* Data centers
* Enterprise environments

### Type 2 Hypervisor

A **Type 2 hypervisor** runs inside an existing operating system.

Commonly used for:

* Learning
* Testing
* Development
* Home labs

---

## 11. Virtual Machine (VM)

A **Virtual Machine (VM)** is a virtual computer that behaves like an independent computer.

A VM can have its own:

* Operating System
* Virtual CPU
* RAM
* Storage
* Network interface

VMs share physical resources with other virtual machines while remaining logically isolated from each other.

---

## 12. Containers

A **Container** is a lightweight environment used to run an application and its dependencies.

Unlike a virtual machine, a container shares the host operating system kernel.

### Containers vs VMs

**Virtual Machine:**

* Includes a complete guest operating system.
* Uses more resources.
* Usually takes longer to start.
* Provides isolation through virtualization.

**Container:**

* Shares the host operating system kernel.
* Uses fewer resources.
* Starts faster.
* Mainly runs applications and their dependencies.

### Docker

**Docker** is a platform used to build, deploy, and run containers.

---

## 13. Virtualization and Containers in Cloud Computing

Virtualization and containers are important technologies that help make cloud computing efficient and scalable.

They allow organizations and cloud providers to:

* Use physical resources efficiently.
* Create environments quickly.
* Scale applications.
* Isolate workloads.
* Deploy applications consistently.

---

## 14. Cloud Computing

**Cloud Computing** provides computing resources and services over a network, commonly the Internet.

Cloud resources can include:

* Virtual machines
* Storage
* Networking
* Applications
* Databases

Instead of relying entirely on local physical hardware, organizations can use resources provided by cloud platforms.

---

## 15. Cloud Benefits

### Scalability

**Scalability** means increasing or decreasing resources according to demand.

### On-Demand Self-Service

Users can provision computing resources when they need them.

### Pay-as-you-go

Users can pay based on the resources they consume.

### High Availability

Cloud architectures can be designed to keep services available even if part of the infrastructure fails.

### Global Access

Cloud resources can be accessed from different locations around the world.

### Security

Cloud providers secure their underlying infrastructure and provide security controls.

However, customers are still responsible for securing the resources and applications they deploy.

---

## 16. Cloud Deployment Models

### Public Cloud

**Public Cloud** infrastructure and services are provided by a cloud provider and shared among multiple customers.

### Private Cloud

**Private Cloud** infrastructure is dedicated to a single organization.

It can provide greater control over the environment.

### Hybrid Cloud

**Hybrid Cloud** combines public and private cloud environments.

```text
Public Cloud + Private Cloud = Hybrid Cloud
```

---

## 17. Cloud Service Models

### IaaS - Infrastructure as a Service

**IaaS** provides basic computing infrastructure such as:

* Virtual machines
* Storage
* Networking

The customer generally manages the operating system, applications, and data.

### PaaS - Platform as a Service

**PaaS** provides a managed platform for developing and running applications.

The provider manages much of the underlying infrastructure, while the customer focuses mainly on applications and data.

### SaaS - Software as a Service

**SaaS** provides complete software applications over the Internet.

Examples:

* Gmail
* Zoom

### Simple Comparison

```text
IaaS → Infrastructure
PaaS → Platform
SaaS → Software
```

---

## 18. Major Cloud Providers

Common cloud providers include:

* AWS
* Microsoft Azure
* Google Cloud Platform (GCP)
* Alibaba Cloud
* IBM Cloud
* Oracle Cloud

---

## 19. AWS EC2

**Amazon EC2 (Elastic Compute Cloud)** provides virtual servers in the AWS cloud.

EC2 instances can be:

* Created
* Started
* Stopped
* Resized
* Terminated

EC2 is an example of **IaaS** because customers manage the operating system and applications running on the virtual machine.

---

## 20. Computer Fundamentals - Big Picture

The concepts in this module connect together to form a foundation for modern IT infrastructure.

```text
Computer Hardware
        ↓
Operating System
        ↓
Applications
        ↓
Network
        ↓
Client ↔ Server
        ↓
IP + Ports
        ↓
Protocols
        ↓
HTTP / HTTPS
        ↓
Virtualization
        ↓
VMs / Containers
        ↓
Cloud Computing
```

---

## Cybersecurity Perspective

Computer fundamentals are important for cybersecurity because security professionals need to understand how the underlying technology works before understanding how it can be attacked or protected.

A cybersecurity professional should understand:

* How computers operate.
* Where data is stored.
* How applications run.
* How computers communicate.
* How clients connect to servers.
* How IP addresses and ports are used.
* How protocols control communication.
* How HTTP and HTTPS work.
* How virtual machines provide isolated environments.
* How containers work.
* How cloud infrastructure is built.

These fundamentals provide a foundation for:

**Network Security → Web Security → Vulnerability Assessment → Malware Analysis → SOC → Cloud Security**

