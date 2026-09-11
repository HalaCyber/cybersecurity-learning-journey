Module 3 : Windows and AD Fundamentals
### Windows OS — Quick Summary

* **Windows** started in 1985 and became widely used in homes and companies.
* **Windows XP** was very popular, but it eventually reached **end-of-life**.
* **Windows Vista** had many problems and was quickly replaced.
* **Windows 7** became the next major version, followed by **Windows 8.x**.
* **Windows 10** came after Windows 8, then **Windows 11**.
* Windows 11 has two editions: **Home** and **Pro**.
* For servers, the lesson mentions **Windows Server 2025**.
* Microsoft has improved **security and usability** with newer Windows versions.
* The TryHackMe VM uses **Windows Server 2019 Standard**.
* Windows 10 support was scheduled to end on **October 14, 2025**.

**Main idea:** Windows has evolved through many versions, with newer versions generally improving security and usability.


Windows XP
   ↓
Windows Vista
   ↓
Windows 7
   ↓
Windows 8.x
   ↓
Windows 10
   ↓
Windows 11
BitLocker.:encryption can you enable on Pro that you can't enable in Home
### Windows File Systems — Quick Summary

* **NTFS** = **New Technology File System**
  The main file system used by modern Windows.

* **FAT** = **File Allocation Table**
  Older file system commonly used in USB drives and MicroSD cards.

* **HPFS** = **High Performance File System**
  Another older file system.

* **NTFS** is a **journaling file system**, meaning it can help repair files and folders after a failure using a log.

### NTFS Features

* Supports files larger than **4GB**
* Allows specific **permissions**
* Supports file and folder **compression**
* Supports **EFS** = **Encrypting File System**

### NTFS Permissions

* **Full control**
* **Modify**
* **Read & Execute**
* **List folder contents**
* **Read**
* **Write**

### ADS

* **ADS** = **Alternate Data Streams**
* ADS is a feature specific to **NTFS**.
* Every file has at least one data stream: **$DATA**.
* ADS allows a file to contain additional data streams.
* **Windows Explorer** normally does not show ADS.
* **PowerShell** can be used to view ADS.
* Malware can use ADS to hide data, but ADS can also store legitimate information, such as identifying files downloaded from the Internet.

### How to Check Permissions

**Right-click file/folder → Properties → Security → Select user or group**

### Main Idea

**NTFS** is more advanced than older file systems because it supports **large files, permissions, compression, encryption, and ADS**.
### Windows Folder — Quick Summary

* **Windows Folder** = contains the Windows operating system.
* **`C:\Windows`** = the traditional location of the Windows folder.
* Windows does **not have to be installed on the C: drive**.
* **`%windir%`** = the **System Environment Variable** for the Windows directory.
* **Environment Variables** = store information about the operating system environment.
* **System32** = contains important files critical to Windows.
* ⚠️ Deleting files from **System32** can make Windows **inoperational**.
* Many tools used in **Windows Fundamentals** are located in **System32**.
