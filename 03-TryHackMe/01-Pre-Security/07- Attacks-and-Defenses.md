# Module 7: Attacks and Defenses

## 1. The CIA Triad

The **CIA Triad** is a fundamental model in cybersecurity that describes three key security objectives.

### Confidentiality

Ensures that sensitive information can only be accessed by **authorized individuals**.

### Integrity

Ensures that data is not **modified or tampered with by unauthorized individuals**.

### Availability

Ensures that systems, data, and services are **available to authorized users when needed**.

---

## 2. Cryptography Concepts

**Cryptography** is used to protect information by transforming readable data into an unreadable form.

### Key Terms

| Term           | Description                                                       |
| -------------- | ----------------------------------------------------------------- |
| **Plaintext**  | The original, readable message or data                            |
| **Ciphertext** | The encrypted, unreadable version of the data                     |
| **Algorithm**  | The method or rules used to encrypt and decrypt data              |
| **Key**        | A secret value used with the algorithm to encrypt or decrypt data |

### Basic Encryption Process

```text
Plaintext + Algorithm + Key
              ↓
         Ciphertext
              ↓
      Decryption + Key
              ↓
          Plaintext
```

### Important Principle

The security of modern encryption should **not depend on keeping the algorithm secret**.

Instead:

> **The algorithm can be public, but the key must remain secret.**

### Lockbox Analogy

Think of encryption as a locked box:

* **Letter inside** → Plaintext
* **Locking mechanism** → Algorithm
* **Key** → Secret Key
* **Locked box** → Ciphertext

---

## 3. Caesar Cipher

The **Caesar Cipher** is a simple encryption algorithm that shifts each letter by a fixed number of positions.

For example, with a key of **3**:

```text
A → D
B → E
C → F
...
X → A
Y → B
Z → C
```

Example:

```text
HELLO
  ↓
KHOOR
```

To decrypt it, shift each letter back by 3:

```text
KHOOR
  ↓
HELLO
```

### Security

The Caesar Cipher is useful for understanding basic encryption concepts, but it is **not secure for real-world systems** because an attacker can easily try all possible shifts.

---

# 4. Symmetric Encryption

**Symmetric encryption** uses the **same secret key** for both encryption and decryption.

```text
Alice
  ↓
Encrypt with Key 🔑
  ↓
Ciphertext
  ↓
Decrypt with the same Key 🔑
  ↓
Bob
```

### Advantages

* Very fast
* Efficient for large amounts of data
* Commonly used for files, disks, and network traffic

### Key Distribution Problem

The main challenge is:

> How can Alice and Bob securely share the secret key?

If an attacker obtains the key, they may be able to decrypt the protected data.

This leads to the need for **asymmetric encryption**, which uses two different keys.

### Important Formula

```text
Plaintext + Algorithm + Key
            ↓
        Ciphertext
```

---

# 5. Asymmetric Encryption

**Asymmetric encryption** uses two mathematically related keys:

* **Public Key** → Can be shared with anyone
* **Private Key** → Must remain secret

### Example

For confidentiality:

```text
Bob generates:
    Public Key
    Private Key

Bob shares the Public Key
        ↓
Alice encrypts using Bob's Public Key
        ↓
Ciphertext
        ↓
Bob decrypts using his Private Key
```

This helps solve the key distribution problem found in symmetric encryption.

---

## 6. Symmetric vs Asymmetric Encryption

| Symmetric Encryption               | Asymmetric Encryption                           |
| ---------------------------------- | ----------------------------------------------- |
| Uses one shared secret key         | Uses a public/private key pair                  |
| Very fast                          | Slower                                          |
| Good for large amounts of data     | Useful for authentication and key establishment |
| Main challenge is key distribution | Public key can be shared openly                 |

### Easy Memory Trick

```text
Symmetric
→ One secret key
→ Fast
→ Key distribution problem

Asymmetric
→ Public + Private key
→ Public key can be shared
→ Helps solve key distribution
→ Slower
```

---

# 7. Digital Signatures

Asymmetric cryptography can also be used for **digital signatures**.

* The sender uses their **private key** to create a signature.
* Others use the sender's **public key** to verify the signature.
* Digital signatures provide **authenticity and integrity**.

> Digital signatures are not simply "encrypting with the private key." That is an oversimplification.

---

# 8. HTTPS, TLS, and Certificates

## HTTPS

**HTTPS = HyperText Transfer Protocol Secure**

HTTPS uses **TLS (Transport Layer Security)** to protect communication between a browser and a website.

### TLS Handshake — Simplified

During the TLS handshake:

1. The website provides a **digital certificate**.
2. The certificate is associated with the website's identity and public key.
3. The browser verifies the certificate using trusted **Certificate Authorities (CAs)**.
4. Asymmetric cryptography is used for authentication and secure key agreement.
5. A shared **session key** is established.
6. Symmetric encryption is then used to protect the actual data.

### Modern HTTPS Uses Both Types of Cryptography

```text
Asymmetric Cryptography
        ↓
Authentication + Key Establishment
        ↓
Session Key
        ↓
Symmetric Cryptography
        ↓
Actual Data Encryption
```

This is called a **hybrid approach**.

---

# 9. Digital Certificates

A **digital certificate** is a document that binds a public key to an identity, such as a website domain.

The browser can check:

* Whether the certificate is trusted
* Whether it was signed by a trusted **CA (Certificate Authority)**
* Whether it is valid and has not expired
* Whether the hostname matches the certificate
* Whether there are relevant certificate revocation or status issues

If there is a problem, the browser may display a security warning.

---

# 10. Offensive Security

## Red Teaming

**Red Teaming** is a structured and authorized attack methodology that simulates a real adversary to test the effectiveness of security defenses and identify vulnerabilities within a defined scope.

## Penetration Testing

A **Penetration Test** is a structured security assessment in which an authorized tester attempts to identify and exploit vulnerabilities within a defined scope to understand real-world risk.

## Vulnerability

A **Vulnerability** is a weakness or flaw in a system, application, or configuration that an attacker could potentially abuse.

## Exploit

An **Exploit** is a technique or method used to take advantage of a vulnerability to achieve a specific outcome, such as accessing restricted functionality or data.

## Scope

**Scope** defines the boundaries of what is allowed during a security assessment.

It specifies:

* Which systems can be tested
* Which applications can be tested
* Which actions are permitted
* What is off-limits

> **Always stay within the defined scope of an authorized security assessment.**

---

# 11. Gobuster

**Gobuster** is a command-line tool used to discover hidden directories and files on a web server.

Example:

```bash
gobuster dir --url http://example.com -w wordlist.txt
```

### Command Breakdown

| Part       | Purpose                           |
| ---------- | --------------------------------- |
| `gobuster` | Runs Gobuster                     |
| `dir`      | Performs directory/file discovery |
| `--url`    | Specifies the target website      |
| `-w`       | Specifies the wordlist            |

### Purpose

Gobuster can help ethical hackers discover:

* Hidden directories
* Web pages
* Files
* Other web content that is not publicly linked

> **Gobuster = automated web content discovery tool.**

---

# 12. Common Attack Concepts

## Weakness Chaining

**Weakness chaining** means combining multiple small weaknesses to create a larger security impact.

```text
Weakness A
    +
Weakness B
    +
Weakness C
    ↓
Greater Impact
```

A weakness that appears low-risk by itself may become much more serious when combined with other weaknesses.

---

## Dictionary Attack

A **Dictionary Attack** attempts passwords from a predefined wordlist.

Instead of trying every possible combination, an attacker tries commonly used passwords and words.

Strong passwords can help reduce the risk of dictionary attacks.

---

## Hydra

**Hydra** is an automated password-testing tool commonly used in authorized security testing.

It can automate attempts against authentication services using username/password combinations.

> The important concept is not memorizing the tool itself, but understanding how weak authentication and passwords can be tested.

---

# 13. What Can You Do as a Defender?

Defensive security can be viewed as a continuous process.

```text
Prevention
    ↓
Detection
    ↓
Mitigation
    ↓
Analysis
    ↓
Response & Improvement
```

## Prevention

Putting security controls in place to prevent attacks before they happen.

Examples:

* Firewalls
* Antivirus software
* Regular patching

## Detection

Monitoring systems and networks to identify suspicious or malicious activity.

Examples:

* Logs
* Alerts
* Security monitoring tools

## Mitigation

Taking action during an incident to limit damage.

Examples:

* Blocking malicious traffic
* Isolating affected systems
* Disabling compromised accounts

## Analysis

Investigating:

* What happened
* How it happened
* Which systems were affected

This can involve reviewing logs and other evidence.

## Response and Improvement

Recovering from an incident and improving defenses to reduce the likelihood and impact of similar incidents in the future.

---

# 14. Key Defender Principles

## Threat Anticipation

Ask:

> **"What if?"**

Defenders should review the systems they protect and imagine realistic attack paths an attacker might use.

---

## Attack Awareness

Attacks often follow recognizable stages.

Understanding common attack chains and security frameworks helps defenders recognize and respond to attacks.

---

## Risk Prioritization

Not every system has the same level of importance or risk.

Defenders should identify:

* High-value systems
* Sensitive data
* Critical services
* Important attack targets

---

## Continuous Adaptation

Security is **not a one-time setup**.

Threats evolve, attackers change their techniques, and new vulnerabilities appear.

Therefore:

> **Defenses must continuously evolve as well.**

---

# Module 7 — Key Takeaways

```text
CIA Triad
    ↓
Confidentiality
Integrity
Availability

Cryptography
    ↓
Plaintext → Encryption → Ciphertext
    ↓
Symmetric + Asymmetric

HTTPS / TLS
    ↓
Certificates
    ↓
Authentication + Key Establishment
    ↓
Symmetric Encryption
    ↓
Secure Data Transfer

Offensive Security
    ↓
Vulnerabilities
    ↓
Exploits
    ↓
Authorized Testing

Defensive Security
    ↓
Prevention
    ↓
Detection
    ↓
Mitigation
    ↓
Analysis
    ↓
Response & Improvement
```

## Core Principle

> **Understand how systems work, understand how they can fail or be attacked, and then understand how to defend them.**
