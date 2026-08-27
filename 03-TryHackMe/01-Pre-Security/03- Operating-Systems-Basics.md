
# Module 3 - Operating Systems Basics

## 1. Operating Systems: Introduction

An **Operating System (OS)** is the core software that coordinates everything happening on a computer. It acts as the invisible layer that ties everything together.

### OS Responsibilities

#### Process Management

The OS manages running processes and allows multiple applications to run at the same time without interfering with each other.

Example:

- Browser
- Music player
- Social media application

#### Memory Management

When multiple applications are running, the OS allocates RAM to each application and keeps their memory isolated so they do not interfere with or crash each other.

#### File System Management

The OS manages files and folders.

Examples:

- Creating a new folder
- Saving a photo
- Setting a file to "read only"

#### User Management

The OS manages user accounts and access.

Example:

- Logging in with a password.
- Keeping files inaccessible to other user accounts.

#### Device Management

The OS manages hardware devices and allows them to communicate with the system.

Examples:

- Mouse
- Printer
- External hard drive

### Basic OS Security Responsibilities

At a basic level, an operating system handles:

- Authentication
- Permissions
- Isolation
- System Protection

---

## 2. Kernel Space and User Space

### Kernel Space

**Kernel Space** is the area of the operating system that has unrestricted access to the computer's hardware and system resources.

### User Space

**User Space** is the area where regular applications run with limited permissions for safety and system stability.

---

## 3. Operating System Interfaces

### Graphical User Interface (GUI)

A **Graphical User Interface (GUI)** provides a graphical representation of the information and functions that users can access on a computer.

### Command-Line Interface (CLI)

A **Command-Line Interface (CLI)** allows users to enter specific text-based commands to retrieve or manipulate information.

CLI is direct and precise.

---

## 4. Operating System Types

### Desktop Operating Systems

#### Windows

Examples:

- Windows 10 (End-of-Life)
- Windows 11

#### macOS

Examples:

- Sonoma (14)
- Sequoia (15)
- Tahoe (26)

#### Linux

Linux distributions are open-source operating systems.

Examples:

- Ubuntu
- Debian
- Fedora

### Server Operating Systems

#### Windows Server

Examples:

- Windows Server 2016
- Windows Server 2019
- Windows Server 2022
- Windows Server 2025

#### Linux

Examples:

- Ubuntu Server
- Debian
- CentOS
- Red Hat

#### Unix

Examples:

- IBM AIX
- Oracle Solaris

### Mobile Operating Systems

#### Android

Android is a mobile operating system used on smartphones, tablets, and other mobile devices.

#### iOS

iOS is Apple's mobile operating system used on iPhones and other Apple devices.

### Embedded and IoT Operating Systems

#### Embedded Linux

Examples:

- OpenWrt
- Ubuntu Core
- Yocto Project

#### Real-Time Operating Systems (RTOS)

Examples:

- FreeRTOS
- VxWorks
- QNX

### Virtual and Cloud Operating Systems

#### Cloud / VM

Examples:

- Ubuntu LTS
- Amazon Linux
- Rocky Linux

#### Container-Optimized

Examples:

- Alpine Linux
- Bottlerocket AWS
- Flatcar Linux

---

## 5. Windows Basics

Windows commonly uses the following account types.

### Guest

A **Guest** account is a restricted account intended for temporary access, with minimal permissions and no ability to make system-wide changes.

### Standard

A **Standard** user account is intended for everyday tasks, such as running applications and changing personal settings, without access to system-wide changes.

### Administrator

An **Administrator** account is a privileged account with extensive control over the system, including software installation, configuration changes, and user management.

### Windows Desktop and Taskbar

When you first log in, you are presented with two main areas:

**Desktop** → The main workspace where files, folders, and shortcuts are displayed.

**Taskbar** → A control strip that provides access to applications, system tools, settings, and notifications.

### Common Windows Tools

**Start Menu** → The primary way to access applications, settings, and power options, represented by the Windows logo.

**Search** → A quick way to locate applications, settings, and files by entering search terms.

**File Explorer** → The built-in Windows tool used to browse, manage, and organize files and folders.

**Windows Update** → A built-in update tool that helps keep Windows, native apps, and security features up to date.

**Microsoft Store** → The native Windows application for installing applications.

**Windows Settings** → A centralized location for configuring system, device, personalization, and security settings.

**Control Panel** → The legacy management interface that provides access to system configuration options.

**Task Manager** → A Windows tool for monitoring what is happening on the system in real time.

**Windows Security** → The central dashboard for managing Windows built-in security tools.

**Windows Defender Firewall** → A firewall designed to help protect the system from unauthorized network traffic.

---

## 6. Linux CLI Basics

### `pwd`

`pwd` stands for **Print Working Directory**.

It shows the folder you are currently in.

### `ls`

`ls` lists the files and folders in the current directory.

For more details, use:

```bash
ls -l
````

### `ls -al`

`ls -al` displays files and folders, including hidden files.

Hidden files are not necessarily secret. They usually start with a dot (`.`), and Linux hides them by default.

### `cd`

`cd` is used to change the current directory.

Example:

```bash
cd Documents
```

### `cd ..`

`cd ..` moves back one level in the directory structure.

### `find`

`find` is used to locate files within the file system.

Example:

```bash
find ~ -name <filename>
```

### `cat`

`cat` is used to display the contents of a file.

Example:

```bash
cat filename
```

### `whoami`

`whoami` prints the current username.

### `uname -a`

`uname -a` displays information about the operating system, kernel version, and system architecture.

### `uname`

`uname` can be used to display the operating system name.

### `df -h`

`df -h` displays disk space usage in a human-readable format, such as `2G`.

### `/etc`

To practice navigating and reading files, you can enter the `/etc` directory:

```bash
cd /etc
ls
```

---

## 7. Windows CLI Basics

### `cd`

`cd` is used to change the current directory.

### `dir`

`dir` lists files and folders in the current directory.

### `dir /a`

`dir /a` displays files and folders, including hidden items.

### `cd folder_name`

Moves to the specified folder.

Example:

```cmd
cd Documents
```

### `dir /s name`

Searches for a file on the disk.

### `type name`

Displays the contents of a file.

### `whoami`

Shows the username of the currently logged-in user.

### `hostname`

Displays the name of the computer.

### `systeminfo`

Displays detailed information about the Windows system.

### `ipconfig`

Displays network configuration information and helps show how the machine is connected to the network.

---

## 8. Operating System Security

When we talk about security, we should think about protecting three main things:

### Confidentiality

**Confidentiality** means ensuring that private and sensitive files and information are only available to authorized people.

### Integrity

**Integrity** means ensuring that files and information cannot be improperly modified or tampered with.

### Availability

**Availability** means ensuring that your laptop, smartphone, or other systems remain available when you need to use them.

These three principles are commonly known as the **CIA Triad**.

---

## 9. Common Attacks Against Security Pillars

### 1. Authentication and Weak Passwords

Authentication can be achieved through three main factors:

**Something you know** → Such as a password or PIN code.

**Something you are** → Such as a fingerprint.

**Something you have** → Such as a phone or device that can receive an SMS message.

It is important to choose strong passwords and use different passwords for different accounts.

### 2. Weak File Permissions

Weak file permissions can make it easier for an adversary to attack **confidentiality** and **integrity**.

They can attack confidentiality because weak permissions may allow unauthorized users to access files they should not be able to access.

They can attack integrity because they may be able to modify files they should not be allowed to edit.

### 3. Malicious Programs

Malicious programs, such as **Trojan horses**, can give attackers access to a system.

Consequently, an attacker may be able to read or modify files.

Some types of malicious programs attack **availability**.

One example is **ransomware**.

**Ransomware** is a malicious program that encrypts the user's files. Encryption makes the files unreadable without the required decryption key or password.

Attackers may demand a ransom in exchange for restoring access to the original files.

---

## 10. Useful Linux Commands - NCSC

The following commands are useful when working with Linux systems:

| Command           | Description                                       |
| ----------------- | ------------------------------------------------- |
| `whoami`          | Shows the current username.                       |
| `ssh USERNAME@IP` | Connects or logs in to a remote computer.         |
| `ls`              | Lists files and folders in the current directory. |
| `cat FILENAME`    | Displays the contents of a file.                  |
| `history`         | Shows commands previously typed by the user.      |
| `su - USERNAME`   | Switches to another user account.                 |

---

## Cybersecurity Perspective

Understanding operating systems is essential for cybersecurity because security professionals need to understand how systems manage users, processes, memory, files, devices, and permissions.

Important areas include:

* Authentication
* Permissions
* User management
* File systems
* Processes
* Memory
* System protection
* Linux CLI
* Windows CLI
* Confidentiality
* Integrity
* Availability
* Malicious programs
* Ransomware

```

