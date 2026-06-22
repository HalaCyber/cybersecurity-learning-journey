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
