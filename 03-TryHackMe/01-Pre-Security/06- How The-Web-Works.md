# Module 6 - How the Web Works

## 1. DNS in Detail

### What is DNS?

**DNS (Domain Name System)** translates human-readable domain names into IP addresses.

Instead of remembering an IP address such as:

```text
93.184.216.34
```

we can use:

```text
example.com
```

---

## Domain Hierarchy

A domain name can be divided into different levels.

### 1. TLD (Top-Level Domain)

The **TLD** is the last part of a domain name.

Example:

```text
tryhackme.com
          └── .com = TLD
```

There are two common types:

#### gTLD (Generic Top-Level Domain)

Used historically to indicate the purpose of a domain.

| TLD    | Purpose      |
| ------ | ------------ |
| `.com` | Commercial   |
| `.org` | Organization |
| `.edu` | Education    |
| `.gov` | Government   |

#### ccTLD (Country Code Top-Level Domain)

Used to represent countries or territories.

Examples:

```text
.ca    → Canada
.uk    → United Kingdom
.tr    → Türkiye
```

---

### 2. Second-Level Domain

The **Second-Level Domain** is the main name directly before the TLD.

Example:

```text
tryhackme.com
└──────┘
  SLD
```

Rules include:

* Maximum of 63 characters
* Can contain `a-z`, `0-9`, and hyphens
* Cannot start or end with a hyphen
* Cannot contain consecutive hyphens

---

### 3. Subdomain

A **subdomain** is a name placed before the main domain.

Example:

```text
admin.tryhackme.com
└─────┘
subdomain
```

Multiple subdomains can be used:

```text
jupiter.servers.tryhackme.com
```

The complete domain name can be up to **253 characters**.

---

# DNS Record Types

DNS stores different types of records.

| Record    | Purpose                                                                 |
| --------- | ----------------------------------------------------------------------- |
| **A**     | Points a domain to an IPv4 address                                      |
| **AAAA**  | Points a domain to an IPv6 address                                      |
| **CNAME** | Points a domain to another domain name                                  |
| **MX**    | Specifies mail servers for a domain                                     |
| **TXT**   | Stores text information, often used for verification and email security |

---

# DNS Lookup

When you enter:

```text
tryhackme.com
```

your computer needs to find its IP address.

A simplified lookup process is:

```text
Computer
   ↓
Recursive DNS Server
   ↓
Root Server
   ↓
TLD Server
   ↓
Authoritative DNS Server
   ↓
IP Address
```

### Steps

1. The computer checks its **local DNS cache**.
2. If the IP is not cached, it asks the **Recursive DNS Server**.
3. The Recursive DNS Server asks a **Root Server**.
4. The Root Server directs it to the correct **TLD Server**.
5. The TLD Server identifies the **Authoritative DNS Server**.
6. The Authoritative DNS Server provides the correct DNS record/IP.
7. The result can be cached according to its **TTL (Time To Live)**.

### TTL

**TTL (Time To Live)** determines how long a DNS result can remain cached before it needs to be requested again.

---

# 2. HTTP in Detail

## HTTP

**HTTP (HyperText Transfer Protocol)** is a protocol used for communication between web clients and web servers.

It is used to transfer resources such as:

* HTML
* Images
* Videos
* JavaScript
* CSS
* Other web resources

---

## HTTPS

**HTTPS (HyperText Transfer Protocol Secure)** is the secure version of HTTP.

HTTPS provides:

* Encryption of data in transit
* Protection against someone reading the exchanged data
* Server authentication through TLS certificates

```text
HTTP  → Not encrypted by HTTP itself
HTTPS → HTTP + TLS encryption/authentication
```

---

# URL

**URL (Uniform Resource Locator)** identifies the location of a resource on the web.

Example:

```text
https://example.com:443/blog?id=10#comments
```

A URL can contain several components:

| Component        | Purpose                              |
| ---------------- | ------------------------------------ |
| **Scheme**       | Protocol used, such as HTTP or HTTPS |
| **User**         | Username information, if supported   |
| **Host**         | Domain name or IP address            |
| **Port**         | Port used for the connection         |
| **Path**         | Location of the requested resource   |
| **Query String** | Additional parameters                |
| **Fragment**     | Specific location within the page    |

Example:

```text
https://example.com:443/blog?id=10#comments
└─┬─┘   └──────┘ └┬┘ └──┬──┘ └───┬───┘
scheme    host   port   query    fragment
```

Common ports:

```text
HTTP  → 80
HTTPS → 443
```

---

# HTTP Request and Response

## Request

The client sends a request to the server.

A simplified request can contain:

```text
Method → What do I want?
Headers → Who am I? / Additional information
Path → What resource do I want?
```

Example:

```http
GET /index.html HTTP/1.1
Host: example.com
User-Agent: Browser
```

---

## Response

The server sends a response:

```text
Status → What happened?
Headers → Information about the response
Content → The requested data
```

Example:

```http
HTTP/1.1 200 OK
Content-Type: text/html

<html>...</html>
```

---

# HTTP Methods

HTTP methods describe what the client wants to do.

| Method     | Purpose             |
| ---------- | ------------------- |
| **GET**    | Read/retrieve data  |
| **POST**   | Create/send data    |
| **PUT**    | Update/replace data |
| **DELETE** | Delete data         |

---

# HTTP Status Codes

Status codes are grouped into five categories:

| Range       | Meaning       |
| ----------- | ------------- |
| **100–199** | Informational |
| **200–299** | Success       |
| **300–399** | Redirection   |
| **400–499** | Client Error  |
| **500–599** | Server Error  |

## Important Status Codes

| Code                          | Meaning                                         |
| ----------------------------- | ----------------------------------------------- |
| **200 OK**                    | Request succeeded                               |
| **201 Created**               | Resource was created                            |
| **301 Moved Permanently**     | Resource permanently moved                      |
| **302 Found**                 | Temporary redirect                              |
| **400 Bad Request**           | Invalid or malformed request                    |
| **401 Unauthorized**          | Authentication is required                      |
| **403 Forbidden**             | Access is not allowed                           |
| **404 Not Found**             | Resource does not exist                         |
| **405 Method Not Allowed**    | HTTP method is not allowed                      |
| **500 Internal Server Error** | Server encountered an unexpected error          |
| **503 Service Unavailable**   | Server unavailable/overloaded/under maintenance |

---

# HTTP Headers

Headers provide additional information about requests and responses.

## Common Request Headers

| Header              | Purpose                                           |
| ------------------- | ------------------------------------------------- |
| **Host**            | Specifies which website/server is being requested |
| **User-Agent**      | Identifies the client/browser                     |
| **Content-Length**  | Size of the request body                          |
| **Accept-Encoding** | Compression formats the client supports           |
| **Cookie**          | Sends stored cookies to the server                |

## Common Response Headers

| Header               | Purpose                                 |
| -------------------- | --------------------------------------- |
| **Set-Cookie**       | Tells the browser to store a cookie     |
| **Cache-Control**    | Controls caching                        |
| **Content-Type**     | Specifies the type of returned data     |
| **Content-Encoding** | Specifies how the content is compressed |

---

# Cookies

A **cookie** is a small piece of data stored by the browser.

Cookies can be used for things such as:

* Sessions
* Authentication
* Preferences
* Tracking

The basic flow is:

```text
Server → Browser
Set-Cookie

Browser → Server
Cookie
```

---

# 3. How Websites Work

A website generally has two main sides.

## Front End

The **front end** is the client-side part of a website.

It is what the browser renders and the user interacts with.

Examples:

* HTML
* CSS
* JavaScript

## Back End

The **back end** runs on the server.

It processes requests and performs operations such as:

* Authentication
* Business logic
* Database operations
* Generating responses

Common back-end languages/technologies include:

```text
PHP
Python
Ruby
Node.js
```

---

# HTML Injection

**HTML Injection** occurs when an application allows user-controlled input to be inserted into a webpage as HTML without proper handling.

This can allow an attacker to inject HTML elements into the page.

---

# 4. Putting Everything Together

A modern website may use several components.

## Load Balancer

A **Load Balancer** distributes incoming traffic between multiple servers.

Benefits:

* Distributes traffic
* Prevents one server from handling all requests
* Provides failover

### Health Check

A health check determines whether a server is available and working correctly.

---

## CDN

**CDN (Content Delivery Network)** stores and delivers content from servers distributed around the world.

The user can receive content from a nearby CDN server.

Benefits:

* Faster delivery
* Reduced traffic to the main server
* Better performance for static content

---

## Database

A database stores and manages application data.

Common database systems include:

```text
MySQL
MSSQL
MongoDB
PostgreSQL
```

A web application can communicate with a database to:

* Retrieve data
* Store data
* Update data
* Delete data

---

## WAF

**WAF (Web Application Firewall)** protects web applications by inspecting HTTP requests and blocking malicious or suspicious traffic according to its rules.

---

# Web Server

A **Web Server** receives HTTP requests and delivers web content.

### Virtual Host

A **Virtual Host** allows multiple websites to be hosted on the same physical server.

### Static Content

Content that does not normally change based on the request.

Examples:

```text
Images
CSS
Static HTML
```

### Dynamic Content

Content generated or changed based on the request, user, or application data.

---

# 5. Complete Website Request Flow

When you request:

```text
https://tryhackme.com
```

a simplified process is:

```text
1. Browser requests tryhackme.com
        ↓
2. Check local DNS cache
        ↓
3. Ask Recursive DNS Server
        ↓
4. DNS lookup finds the IP address
        ↓
5. Request reaches the WAF
        ↓
6. WAF inspects the request
        ↓
7. Load Balancer distributes the request
        ↓
8. Request reaches the Web Server
        ↓
9. Web Server receives the GET request
        ↓
10. Web Application processes the request
        ↓
11. Web Application may communicate with the Database
        ↓
12. Server sends the response
        ↓
13. Browser receives the response
        ↓
14. Browser renders the HTML
        ↓
15. User sees the website
```

### The Big Picture

```text
User
 ↓
Browser
 ↓
DNS
 ↓
IP Address
 ↓
WAF
 ↓
Load Balancer
 ↓
Web Server
 ↓
Web Application
 ↓
Database
 ↓
Response
 ↓
Browser
 ↓
Website
```

---

# Cybersecurity Perspective

Understanding how the web works is essential for cybersecurity.

Important concepts from this module include:

* DNS
* TLD / SLD / Subdomain
* DNS Records
* A / AAAA / CNAME / MX / TXT
* Recursive DNS
* Authoritative DNS
* TTL
* HTTP / HTTPS
* URL
* HTTP Methods
* HTTP Status Codes
* HTTP Headers
* Cookies
* Front End / Back End
* HTML Injection
* Load Balancer
* CDN
* Database
* WAF
* Web Server
* Virtual Host
* Static / Dynamic Content
* Web Application
* Complete Web Request Flow
