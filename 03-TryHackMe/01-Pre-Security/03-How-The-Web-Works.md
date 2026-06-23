# Module 03 - How The Web Works

## DNS (Domain Name System)

DNS provides an easy way to access websites by translating domain names into IP addresses. Instead of remembering numerical IP addresses, users can use simple and memorable domain names such as tryhackme.com.

## Top-Level Domain (TLD)

A Top-Level Domain (TLD) is the rightmost part of a domain name, such as `.com` or `.org`.

### Types of TLDs

#### Generic Top-Level Domains (gTLDs)
Used for general purposes and are not tied to a specific country.

**Examples:**
- google.com
- wikipedia.org
- harvard.edu
- usa.gov

#### Country Code Top-Level Domains (ccTLDs)
Used to represent a specific country or region.

**Examples:**
- bbc.co.uk (United Kingdom)
- canada.ca (Canada)
- example.de (Germany)

### Key Takeaway
The last part of a domain name is called the TLD. It can either represent a general purpose (`.com`, `.org`, `.edu`) or a specific country (`.uk`, `.ca`, `.de`).

---

## Second-Level Domain (SLD)

The Second-Level Domain (SLD) is the part of a domain name located directly before the Top-Level Domain (TLD).

**Examples:**
- tryhackme.com → tryhackme is the SLD
- google.com → google is the SLD
- amazon.com → amazon is the SLD

The SLD is the unique name chosen when registering a domain.

### Rules
- Maximum length: **63 characters**
- Allowed characters:
  - Letters (a-z)
  - Numbers (0-9)
  - Hyphens (-)

### Restrictions
- Cannot start with a hyphen (-)
- Cannot end with a hyphen (-)
- Cannot contain consecutive hyphens (--)

### Key Takeaway
The SLD is the main name of the website that appears before the TLD.

---

## Subdomain

A subdomain is a section of a domain that appears to the left of the Second-Level Domain (SLD). It is commonly used to organize different services or areas of a website.

**Examples:**
- admin.tryhackme.com
- blog.tryhackme.com
- mail.google.com

### Rules
- Maximum length: **63 characters**
- Allowed characters:
  - Letters (a-z)
  - Numbers (0-9)
  - Hyphens (-)

### Restrictions
- Cannot start with a hyphen (-)
- Cannot end with a hyphen (-)
- Cannot contain consecutive hyphens (--)

A domain can have multiple subdomains.

**Example:**
- jupiter.servers.tryhackme.com

In this example:
- jupiter → Subdomain
- servers → Subdomain
- tryhackme → SLD
- com → TLD

### Additional Information
- There is no limit to the number of subdomains that can be created.
- The full domain name must not exceed **253 characters**.

### Key Takeaway
Subdomains help organize and separate services within the same domain while remaining part of the main website.

## DNS Record Types

DNS uses different types of records to provide specific information about a domain and its services.

### A Record

An A (Address) Record maps a domain name to an IPv4 address.

**Example:**
- tryhackme.com → 104.26.10.229

### AAAA Record

An AAAA Record maps a domain name to an IPv6 address.

**Example:**
- tryhackme.com → 2606:4700:20::681a:be5

### CNAME Record

A CNAME (Canonical Name) Record maps one domain name to another domain name instead of directly to an IP address.

**Example:**
- store.tryhackme.com → shops.shopify.com

When a client receives a CNAME record, it must perform another DNS lookup to find the IP address of the target domain.

### MX Record

An MX (Mail Exchange) Record specifies the mail servers responsible for handling email for a domain.

**Example:**
- tryhackme.com → alt1.aspmx.l.google.com

MX records include a **priority value**, which determines the order in which mail servers should be used. If the primary mail server is unavailable, email can be delivered to a backup server.

### TXT Record

TXT Records store text-based information associated with a domain.

Common uses include:
- Email authentication (SPF, DKIM, DMARC)
- Domain ownership verification
- Security and anti-spoofing configurations

**Examples:**
- Verifying domain ownership
- Defining authorized email servers
- Configuring DMARC policies

### Key Takeaway

Different DNS record types serve different purposes:

| Record | Purpose |
|----------|----------|
| A | Domain → IPv4 Address |
| AAAA | Domain → IPv6 Address |
| CNAME | Domain → Another Domain |
| MX | Email Server |
| TXT | Text, Verification, and Security Information |

## What Happens When You Make a DNS Request?

When a user requests a domain name, the computer first checks its local cache to see if the address has been looked up recently.

If the record is not found locally, the request is sent to a **Recursive DNS Server**, which also checks its own cache for a stored result.

If no cached result exists, the Recursive Server begins a DNS lookup process:

1. **Root Server**
   - Directs the request to the correct Top-Level Domain (TLD) server.

2. **TLD Server**
   - Identifies the authoritative server responsible for the requested domain.

3. **Authoritative Server**
   - Stores the DNS records for the domain and returns the requested record (such as an IP address).

The result is then sent back to the Recursive Server, cached for future requests, and finally returned to the client.

### Time To Live (TTL)

DNS records contain a TTL (Time To Live) value, measured in seconds.

TTL determines how long a DNS response should remain cached before a new lookup is required.

Caching improves performance by reducing the number of DNS requests needed for frequently visited websites.

### DNS Lookup Flow

Client
→ Local Cache
→ Recursive DNS Server
→ Root Server
→ TLD Server
→ Authoritative Server
→ DNS Record Response
→ Client

### Key Takeaway

DNS uses a hierarchical lookup process to find the correct record for a domain. Caching and TTL help speed up future requests and reduce unnecessary traffic.
