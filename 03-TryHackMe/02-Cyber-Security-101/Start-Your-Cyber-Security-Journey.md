

# Module 1: Start Your Cyber Security Journey

## Offensive Security Intro

Introduction to offensive security and the role of penetration testing in cybersecurity.

## Defensive Security Intro

Introduction to defensive security and how security teams detect, investigate, and respond to threats.

---

# Search Skills

## Shodan

**Shodan** is a search engine for Internet-connected devices and services.

It helps security professionals discover:

- Servers and devices exposed to the Internet
- Open ports and running services
- Software versions
- Possible known vulnerabilities (CVEs)

### Useful Filters

| Filter | Purpose |
|---|---|
| `country:` | Search by country |
| `port:` | Search by port |
| `org:` | Search by organization or network owner |
| `hostname:` | Search by hostname or domain |

### Example

```text
hostname:fakebank.thm
````

Searches for devices associated with the specified hostname.

> **Key idea:** Shodan is mainly useful for discovering Internet-facing devices, services, and information about them.

---

## VirusTotal

**VirusTotal** is a platform that checks files, URLs, domains, and file hashes using many antivirus and security engines.

It helps security teams:

* Detect suspicious or malicious files and links
* Compare results from many security tools in one place
* Gather information about new threats

### Important

VirusTotal is **not 100% reliable**.

A file or URL being marked as **clean** does not always mean it is completely safe.

> **Key idea:** VirusTotal helps you investigate suspicious files, links, domains, and hashes using multiple security engines.

---

## CVE & CVSS

### CVE

**CVE (Common Vulnerabilities and Exposures)** is a system used to give known security vulnerabilities a unique identifier.

Example:

```text
CVE-2025-55182
```

The CVE identifier allows security researchers, vendors, and security tools to refer to the same vulnerability.

### CVSS

**CVSS (Common Vulnerability Scoring System)** gives a vulnerability a severity score.

It helps organizations prioritize which vulnerabilities should be addressed first.

### Important Factors

* **Impact** → How much damage can the vulnerability cause?
* **Complexity** → How difficult is it to exploit?
* **Availability** → How likely is it to be exploitable?

### PoC

**PoC (Proof of Concept)** is code or a method that demonstrates that a vulnerability can work or be exploited.

> **Key idea:**
> **CVE = identifies the vulnerability**
> **CVSS = measures its severity**
> **PoC = demonstrates the vulnerability**

---

## Official Documentation

**Official Documentation** is usually the best and most reliable source for learning how to use a security tool.

When you do not understand how a tool or command works, check its official documentation first.

### Linux MAN Pages

Linux provides **MAN (Manual) pages** containing documentation for commands and tools.

To open a manual page:

```bash
man <command>
```

### Example

```bash
man ls
```

This displays the manual page for the `ls` command.

> **Key idea:** When you don't know how a Linux command works, use `man <command>`.

---

## GitHub

**GitHub** is a useful resource for researching vulnerabilities and security threats.

Researchers often publish:

* Proof of Concept (PoC) code
* Security tools
* Vulnerability analysis
* Technical research

You can search for a **CVE ID** to find repositories related to a specific vulnerability.

### Example

```text
CVE-2026-1337
```

### Important

Not all PoCs are reliable or safe.

Some may be:

* Incomplete
* Incorrect
* Intentionally flawed
* Malicious

Always **verify and understand code before running it**.

> **Key idea:** GitHub is useful for security research, but never blindly run unknown code.

---

# Module 1 — Key Takeaways

| Resource                   | Main Purpose                                        |
| -------------------------- | --------------------------------------------------- |
| **Shodan**                 | Discover Internet-facing devices and services       |
| **VirusTotal**             | Analyze suspicious files, URLs, domains, and hashes |
| **CVE**                    | Identify known vulnerabilities                      |
| **CVSS**                   | Measure vulnerability severity                      |
| **PoC**                    | Demonstrate a vulnerability                         |
| **Official Documentation** | Learn how to properly use tools                     |
| **MAN Pages**              | Read Linux command documentation                    |
| **GitHub**                 | Research vulnerabilities, PoCs, and security tools  |

```
```
