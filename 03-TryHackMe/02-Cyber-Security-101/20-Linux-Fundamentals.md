# Module 2: Linux Fundamentals 🐧

Linux is widely used in **servers, websites, embedded devices, cars, infrastructure**, and many other systems.

---

## 1. Basic Linux Commands

| Command  | Purpose                             |
| -------- | ----------------------------------- |
| `whoami` | Shows the current user              |
| `echo`   | Outputs specific text               |
| `ls`     | Lists files and directories         |
| `cd`     | Changes directory                   |
| `cat`    | Displays the contents of a file     |
| `pwd`    | Shows the current working directory |
| `find`   | Searches for files by name          |
| `grep`   | Searches for text inside files      |

### Examples

```bash
find -name passwords.txt
```

Searches for a file named `passwords.txt`.

```bash
grep "password123" passwords.txt
```

Searches for `password123` inside `passwords.txt`.

---

## 2. Linux Operators

### `&` — Background

Runs a command in the background without waiting for it to finish.

```bash
command &
```

Useful for commands that take a long time or need to keep running.

### `&&` — Run Commands in Order

Runs the second command only after the first command finishes.

```bash
command1 && command2
```

Think of it like a chain of dominoes: the second command waits for the first.

### `>` — Redirect Output

Sends command output to a file and **overwrites** existing content.

```bash
command > file.txt
```

### `>>` — Append Output

Sends output to a file but **adds it to the end** instead of overwriting it.

```bash
command >> file.txt
```

### Quick Reminder

```text
&   → Background
&&  → Run commands in order
>   → Overwrite file
>>  → Append to file
```

---

# 3. SSH — Secure Shell

**SSH (Secure Shell)** is a protocol used to securely connect to a remote computer over a network.

To connect using SSH, you usually need:

* **IP address** → Address of the remote machine
* **Username** → Account on the remote machine
* **Password** → Account password

### Example

```bash
ssh username@10.10.10.10
```

After connecting, commands are executed on the **remote machine**, not your own computer.

> **Remember:** SSH = Secure remote access through the command line.

---

# 4. Arguments & Flags

Arguments and flags change or control how a Linux command works.

### Basic Command

```bash
ls
```

Lists files and directories.

### Using a Flag

```bash
ls -a
```

Lists **all files**, including hidden files.

* `-a` → Option/flag
* Files starting with `.` → Hidden files

### Getting Help

```bash
ls --help
```

Shows quick help and available options.

```bash
man ls
```

Opens the detailed manual for `ls`.

### Quick Reminder

```text
--help  → Quick help
man     → Detailed documentation
-a      → Option/flag
```

---

# 5. Files & Directories

Linux provides commands to create, copy, move, rename, and delete files and directories.

| Command | Purpose                              |
| ------- | ------------------------------------ |
| `touch` | Creates an empty file                |
| `mkdir` | Creates a directory                  |
| `cp`    | Copies a file or directory           |
| `mv`    | Moves or renames a file or directory |
| `rm`    | Removes a file or directory          |

### Examples

```bash
touch file.txt
mkdir folder
cp file.txt copy.txt
mv file.txt newname.txt
rm file.txt
rm -R folder
```

### Quick Reminder

```text
touch  → Create file
mkdir  → Create folder
cp     → Copy
mv     → Move / Rename
rm     → Delete
```

---

# 6. Important Linux Directories

| Directory | Purpose                         |
| --------- | ------------------------------- |
| `/`       | Root of the filesystem          |
| `/etc`    | Configuration files             |
| `/var`    | Variable data, especially logs  |
| `/root`   | Home directory of the root user |
| `/tmp`    | Temporary files                 |

### Easy Way to Remember

```text
/      → Top of the filesystem
/etc   → Configuration
/var   → Logs / changing data
/root  → Root user's home
/tmp   → Temporary files
```

> **Important:** `/` and `/root` are not the same.
>
> `/` = Filesystem root
> `/root` = Root user's home directory

---

# 7. Linux File Permissions & Users

## File Permissions

Linux uses permissions to control what users can do with files and directories.

| Permission | Meaning        |
| ---------- | -------------- |
| `r`        | Read           |
| `w`        | Write / Modify |
| `x`        | Execute / Run  |

Use:

```bash
ls -l
```

to see detailed information, including file permissions.

---

## Users & Groups

Every file has an **owner** and can belong to a **group**.

* **Owner** → The user who owns the file.
* **Group** → A group of users with their own permissions.
* **Others** → All other users.

Different users and groups can have different permissions for the same file.

---

## Switching Users

The `su` command allows you to switch to another user.

```bash
su -l user2
```

* `su` → Switch user
* `-l` → Start a login shell
* `user2` → The user to switch to

After switching users, you may have access to files that your previous user could not access.

To display a file:

```bash
cat important
```

### Key Takeaways

```text
r → Read
w → Write
x → Execute
```

* `ls -l` → Shows file permissions.
* Files have an **owner** and can belong to a **group**.
* Different users can have different permissions.
* `su -l username` → Switches to another user.
* `cat filename` → Displays file contents.

---

# 8. Linux Text Editors

## Nano

**Nano** is a simple terminal text editor used to create and edit files.

```bash
nano filename
```

Nano allows you to:

* Search for text.
* Copy and paste.
* Jump to a specific line.
* See the current line number.
* Edit multiple lines.

Nano uses **Ctrl + key** shortcuts.

In Linux, `^` represents the **Ctrl** key.

For example:

```text
Ctrl + X → Exit Nano
```

---

## VIM

**VIM** is a more advanced terminal text editor.

Advantages include:

* Highly customisable.
* Supports syntax highlighting.
* Available on many terminals.
* Many tutorials and cheatsheets are available.

VIM is more difficult to learn than Nano, but it is very powerful and useful for developers and Linux users.

### Key Takeaways

```text
nano filename → Create or edit a file
```

* Nano → Beginner-friendly and easy to use.
* VIM → More advanced and customisable.
* Both can be used to edit files from the terminal.

---

# 9. Linux File Transfer

## Wget

`wget` is used to download files from the web using a URL.

```bash
wget https://example.com/file.txt
```

> **Wget = Download files**

---

## SCP

`scp` means **Secure Copy**.

It securely transfers files between computers using SSH.

### General Syntax

```bash
scp SOURCE DESTINATION
```

### Local → Remote

```bash
scp important.txt ubuntu@192.168.1.30:/home/ubuntu/
```

### Remote → Local

```bash
scp ubuntu@192.168.1.30:/home/ubuntu/documents.txt notes.txt
```

> **SCP = Secure file transfer between computers**

---

## Python HTTP Server

Python can create a simple web server to share files:

```bash
python3 -m http.server
```

By default, it uses **port 8000**.

Another computer can download a file using:

```bash
wget http://10.114.155.31:8000/file.txt
```

Keep the server terminal running and use another terminal for commands such as `wget`.

### Key Takeaways

```text
wget                     → Download files
scp                      → Secure file transfer
python3 -m http.server   → Share files through a web server
scp SOURCE DESTINATION   → From where → To where
```

---

# 10. Linux Processes

A **process** is a running program.

A **PID (Process ID)** is the unique ID assigned to a process.

### Viewing Processes

```bash
ps
ps aux
top
```

* `ps` → View processes.
* `ps aux` → View processes from users and the system.
* `top` → View processes in real time.

---

## Managing Processes

```bash
kill PID
```

Common signals include:

| Signal    | Purpose           |
| --------- | ----------------- |
| `SIGTERM` | Stop gracefully   |
| `SIGKILL` | Kill immediately  |
| `SIGSTOP` | Suspend a process |

---

## Services

Services can be managed using `systemctl`.

```bash
systemctl start apache2
systemctl stop apache2
systemctl status apache2
systemctl enable apache2
systemctl disable apache2
```

### Background & Foreground

```text
&        → Run in background
Ctrl + Z → Suspend a process
fg       → Bring it to the foreground
```

> **Key idea:** Linux manages running programs as processes, and each process has its own PID.

---

# 11. Linux Cron Jobs

**Cron** runs scheduled tasks automatically.

**Crontab** is used to schedule cron jobs.

A crontab uses six values:

```text
MIN HOUR DOM MON DOW CMD
```

| Value  | Meaning            |
| ------ | ------------------ |
| `MIN`  | Minute             |
| `HOUR` | Hour               |
| `DOM`  | Day of month       |
| `MON`  | Month              |
| `DOW`  | Day of week        |
| `CMD`  | Command to execute |

---

## Wildcard `*`

`*` means **any value**.

### Example

```bash
0 */12 * * * cp -R /home/cmnatic/Documents /var/backups/
```

This runs the backup command every **12 hours**.

---

## Edit Crontab

```bash
crontab -e
```

Opens the crontab for editing.

### Key Takeaways

```text
cron       → Manages scheduled tasks
crontab    → Contains scheduled jobs
*          → Any value
crontab -e → Edit the crontab
```

---

# 12. APT & Software Repositories

**APT** manages software and packages on Ubuntu.

A **Repository** is a source where software packages and updates are stored.

A **GPG key** helps verify that software comes from a trusted source.

---

## Common Commands

```bash
apt update
apt install software-name
apt remove software-name
```

* `apt update` → Updates package lists.
* `apt install` → Installs software.
* `apt remove` → Removes software.

---

## Adding Repositories

```bash
add-apt-repository
```

After adding a repository:

```bash
apt update
```

> **Key idea:** APT is used to install, update, and remove software from trusted repositories.

---

# 13. Linux Log Files

Linux stores most log files in:

```bash
/var/log
```

Logs contain information about:

* Applications.
* Services.
* The operating system.
* User activity.

Linux can automatically manage old logs through **log rotation**.

---

## Important Logs

| Service  | Purpose                                               |
| -------- | ----------------------------------------------------- |
| Apache2  | Web server logs                                       |
| Fail2ban | Logs suspicious activity such as brute-force attempts |
| UFW      | Firewall logs                                         |

---

## Web Server Logs

Two important types of web server logs are:

### Access Log

Records requests made to the web server.

It can help identify:

* Who visited the website.
* What requests were made.
* Possible suspicious activity.

### Error Log

Records errors and problems with the web server.

---

## Why Logs Are Important

Logs are useful for:

* Monitoring system health.
* Troubleshooting problems.
* Investigating suspicious activity.
* Detecting possible attacks.

> **Key takeaway:** `/var/log` is an important place to look when investigating what is happening on a Linux system.

---

# Linux Fundamentals — Quick Revision

```text
Basic Commands
├── whoami   → Current user
├── echo     → Output text
├── ls       → List files
├── cd       → Change directory
├── cat      → Read file
├── pwd      → Current directory
├── find     → Find files
└── grep     → Search inside files

Operators
├── &        → Background
├── &&       → Run in order
├── >        → Overwrite output
└── >>       → Append output

Remote Access
└── ssh      → Secure remote access

Files
├── touch    → Create
├── mkdir    → Create directory
├── cp       → Copy
├── mv       → Move / Rename
└── rm       → Delete

Permissions
├── r        → Read
├── w        → Write
└── x        → Execute

File Transfer
├── wget     → Download
├── scp      → Secure transfer
└── Python   → Share files

Processes
├── ps       → View processes
├── top      → Real-time processes
├── kill     → Manage processes
└── systemctl → Manage services

Automation
└── cron     → Scheduled tasks

Packages
└── apt      → Manage software

Logs
└── /var/log → Linux logs
```

## Final Takeaway

Linux Fundamentals provides the foundation for working with Linux systems.

The most important concepts are:

* Navigating the filesystem.
* Managing files and directories.
* Understanding users and permissions.
* Connecting to remote systems with SSH.
* Transferring files.
* Managing processes and services.
* Automating tasks with cron.
* Managing software with APT.
* Reviewing logs for troubleshooting and security investigations.

> **Practice is the key to becoming comfortable with Linux.**
