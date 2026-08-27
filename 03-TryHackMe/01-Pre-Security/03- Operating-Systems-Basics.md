Module 3 : Operating Systems Basics

*Operating Systems: Introduction:
 operating system:the invisible layer that ties it all together.
  is the core software that coordinates everything happening on a computer
  *OS Responsibility:
  -> Process Management
  Opening multiple apps, like your browser, music player, and social media, without your computer freezing
  -> Memory Management
  Opening multiple app at once, the OS allocates RAM to each one and keeps them isolated so they don’t interfere or crash each other
  -> file system management 
  Creating a new folder, saving a photo, or setting a file to "read only"
  -> User Management
  Logging in with your password and keeping your files inaccessible to other user accounts
  -> Device Management
  Plugging in a new mouse, printer, or external hard drive and having it work immediately
  
  At a basic level, your operating system handles:
  *Authentication
  *Permissions
  *Isolation
  *System Protection

  *Kernel Space: Which OS space has unrestricted access to your computer's hardware?
  *User space :The area where regular applications run with limited permissions for safety and system stability.
  ------------------------------------------------------------------------------------
  OS  Interfaces:
  ----> graphical user interface (GUI)
  It provides a graphical representation of all the information you want to access on your computer
  ----> command-line interface (CU)
  . It’s direct and extremely accurate,
  where you enter specific text-based commands to retrieve or manipulate information

-----
Operating System Type:
-->Desktop: 
1-Windows :Windows 10 (end-of-life), Windows 11
2-macOS: Sonoma (14), Sequoia (15), Tahoe (26)
3-Linux:open-source operating systems called distributions
Ubuntu, Debian, Fedora
-->Server:
1-Windows:  Server 2016, 2019, 2022, 2025

2-Linux:  Ubuntu Server, Debian, CentOS, Red Hat

3-Unix: IBM AIX, Oracle Solaris

-->Mobile:
1-Android:
2-iOS: Apple's mobile OS running on iPhones, iPads, and other devices
-->Embedded and IoT Devices:
1-Embedded Linux:OpenWrt, Ubuntu Core, Yocto Project
2-Real-Time OS:FreeRTOS, VxWorks, QNX
-->Virtual/Cloud:
1-Cloud/VM:Ubuntu LTS, Amazon Linux, Rocky Linux
2-Container-optimized:Alpine Linux, Bottlerocket AWS, Flatcar Linux



----------------------------------------------------------------------------------
Windows Basics:
---------------
Windows commonly uses the account types below.

   * Guest: A restricted account intended for temporary access, with minimal permissions and no ability to change system settings
    
    *Standard: A user account for everyday tasks, such as running applications and changing personal settings, without access to system-wide changes
    
    *Administrator: A privileged account with full control over the system, including software installation, configuration changes, and user management

*When you first log in, you're presented with two main areas.

    Desktop: The main workspace where files, folders, and shortcuts live
    Taskbar: A control strip that provides access to applications, system tools, settings, and notifications

her learning.

   
    Start Menu: The primary way to access applications, settings, and power options, signified by the Windows logo
    Search: A quick access method of locating applications, settings, and files by entering search terms
    File Explorer: The built-in Windows tool to browse, manage, and organize files and folders
    Windows Update: A built-in update tool that helps keep your , native apps, and security features up to date
    Microsoft Store: The native Windows application for installing trusted applications
    Windows Settings: A centralized location for configuring system, device, personalization, and security settings
    Control Panel: The legacy management interface that provides access to system configuration options
    Task Manager: A Windows tool for monitoring what is happening on your system in real time
    Windows Security: The central dashboard for managing Windows built-in security tools
    Windows Defender : The firewall designed to help protect your system from unauthorized network traffic
------------------------------------------------------------------------------------------

Linux CLI Basics:
*  pwd : "print working directory"  ----> show me the folder I'm currently in
*  ls:   let's see what files and folders are here  _ f we need more details, we can try: ls -l
*   ls -al : to get the hidden files in the directory -Hidden files aren't really secret; they start with a dot ., and Linux hides such files by default.
*   To walk through the filesystem, we can use: cd <directory>. For example: cd Documents, and this will change our directory to Documents, as shown below
*   To go "back" one level, we will use the command cd .., as shown below:
*   find ~ -name : is used to locate files within the file system.
*   cat :  This is used to read the content of the file.
*   whoami:This prints your current username.
*   uname -a: To see details about the operating system, kernel version, and architecture, use:
*  uname: If you only want the operating system name, you can try:
*  df -h: it shows sizes like 2G
*  To practice navigating and reading files, head into /etc by running cd /etc and then list what’s inside: ls
-------------------------------------------  ---------------------------------------------------
  Windows CLI Basics|:
  ----------------
* cd : Where Am I
* dir : What's Around Me
* show everything, including hidden items, run: dir /a
* cd folder_name:  to move to the specified folder
* : dir /s name :Finding the File on the Disk
*  type name :Read the File
*  whoami:Who Am I Logged In As?
*  hostname: What Is the Name of This Computer?
*  systeminfo:What Version of Windows Is This
*  ipconfig:How Is This Machine Connected to the Network

  ---------------------------------------------------------------------------------------
  Operating System Security:
  --------------------------
  When we talk about security, we should think of protecting three things:
  Confidentiality: You want to ensure that secret and private files and information are only available to intended persons.
  integrity:: It is crucial that no one can tamper with the files stored on your system or while being transferred on the network. 
  Availability: You want your laptop or smartphone to be available to use anytime you decide to use it.

  we will discuss common attacks against these security pillars:
  ---------------------------------------------------------
 1- Authentication and Weak Passwords
 ------------------------------------
 Authentication can be achieved via three main ways:

    Something you know, such as a password or a PIN code.
    Something you are, such as a fingerprint.
    Something you have, such as a phone number via which you can receive an SMS message.

    it is vital that you choose complex passwords and use different passwords with different accounts.
    
 2- Weak File Permissions:
 -------------------------
Weak file permissions make it easy for the adversary to attack confidentiality and integrity. They can attack confidentiality as weak permissions allow them to access files they should not be able to access. Moreover, they can attack integrity as they might modify files that they should not be able to edit.
 
 3- Malicious Programs:
 ----------------------
such as Trojan horses, give the attacker access to your system. Consequently, the attacker would be able to read your files or even modify them.
Some types of malicious programs attack availability  One such example is ransomware
Ransomware is a malicious program that encrypts the user's files. Encryption makes the file(s) unreadable without knowing the encryption password
 i.e., regain access to their original files: they would give them the encryption password if the user is willing to pay the “ransom.”
  
* The National Cyber Security Centre (NCSC)
  ------------------------------------------------------------------------------------
whoami	?	Shows the current username.
ssh USERNAME@IP       	Connects/logs in to a remote computer.
ls	      	Lists files and folders in the current directory.
cat FILENAME	    : Displays the contents of a file.
history	 :	Shows commands previously typed by the user.
su - USERNAME	 :	Switches to another user accoun

---------------------------------------------------
