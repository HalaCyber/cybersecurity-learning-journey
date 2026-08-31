module 7 : attacks and defenses :
------------------------------

* Confidentiality:
  Confidentiality ensures that sensitive data can only be accessed by authorized individuals.
  *Integrity:
  Integrity ensures that unauthorized individuals do not modify data.
  *Availability:
  Availability ensures that data and services are available to authorized users when needed


Cryptography Concepts:
-------------
















  Become a Hacker:
  ----------------
  Core Offensive Security Terms

    Red Teaming: A structured, authorized attack methodology that simulates a real adversary to test the effectiveness of defenses and find vulnerabilities within a defined scope
    Penetration Test: A structured security assessment where an authorized tester attempts to identify and exploit vulnerabilities within a defined scope to understand real-world risk
    Vulnerability: A weakness or flaw in a system, application, or configuration that an attacker could abuse
    Exploit: A technique or method used to take advantage of a vulnerability to achieve a specific outcome, such as accessing restricted functionality or data
    Scope: The boundaries of what is allowed to be tested during an engagement. Scope defines which systems, applications, and actions are permitted, and what is off-limits
### Gobuster — Short Summary

**Gobuster** is a command-line tool used to **discover hidden directories and files on a web server**.

Example command:

```bash
gobuster dir --url http://example.com -w wordlist.txt
```

### What each part means:

* **gobuster** → runs the Gobuster tool.
* **dir** → scans for hidden directories and files.
* **--url** → specifies the target website.
* **-w** → provides a wordlist containing possible directory/file names.

### Purpose:

Gobuster helps ethical hackers find hidden web pages, directories, and files that are not linked publicly.

**Remember:**

> **Gobuster = automated web content discovery tool.**
------------
Weakness chaining = combine small flaws to create bigger impact.
Dictionary attack = trying passwords from a wordlist.
Hydra = automated password testing tool.
Strong passwords prevent brute-force/dictionary attacks

What Can You Do as a Defender?
Prevention: Putting security controls in place to stop attacks before they happen, such as firewalls, antivirus software, and regular patching.
Detection: Monitoring systems and networks to identify suspicious or malicious activity through logs, alerts, and security tools.
Mitigation: Taking action during an incident to limit damage, such as blocking traffic, isolating affected systems, or disabling compromised accounts.
Analysis: Investigating what happened, how it happened, and which systems were affected by reviewing logs and other evidence.
Response and Improvement: Recovering from the incident and improving defenses to reduce the risk of similar attacks in the future.








Key Defender Principles

    Threat anticipation: Review the systems you aim to protect and ask, "What if?" Imagine realistic paths an attacker may take to achieve their goal.
    Attack awareness: Attacks typically follow recognizable stages. Studying common attack chains and frameworks is incredibly useful for defenders.
    Risk prioritization: Not every part of your system carries equal risk. Defenders should identify high-value systems and targets.
    Continuous adaptation: Defense is not a one-time set up. Threats and attackers evolve, techniques change, and vulnerabilities emerge.

