**<center>.:. sapiens dominabitur astris .:. </center>**



## :LiComputer: <font color="#00b0f0">Born2beroot</font>

<font color="#ffff00"><b>Hypervisors </b></font>
***Type - 1 (Bare Metal)***
These run directly on host's hardware, facilitating optimized resource allocation. Popular examples include ESXi, Hyper-V and Proxmox. They used in server environments. They don't need a Host OS rather works directly on hardware. Mostly used in servers.

***Type - 2 (Hosted)***
These operate as additional layer on top of your existing OS. Mostly used in PC's. 

<font color="#ffff00"><b>AppArmor</b></font>
App armor is an security system, proactively protects the operating system and applications from external or internal threats. AppArmor offers simpler, path-based approach to security. Easier to manage. Enabled by default on Ubuntu / Debian distributions. 

<font color="#ffff00"><b>SELinux</b></font>
Is a security architecture for Linux systems that allows administrators to have more control over who can access the system. SELinux offers stricter and granular label based control. Ideal for high-security environments. Preferred with CentOS  / Red Hat - Fedora distributions. Complex to manage. SELinux labels settings over all files, processes and ports. Labels are logical way of grouping things together. 

- **Discretionary access control** 
	*Files and processes have owners. Users have ability to change permissions.* 
- **Mandatory access control**
	*In DAC's root has full access over system. But on MAC's systems like SELinux, administrators set policy for access.* 


## **:LiCommand: <font color="#7030a0">Commands</font>** 

<font color="#ffff00">su </font>-> root
<font color="#31859b">lsblk</font> -> lists information about all available or the specified block devices.
<font color="#f79646">getent group users </font>-> show users 
<font color="#f79646">getent group user42</font> -> show users of the group
compgen -u -> see all users 
<font color="#f79646">groups</font> -> show groups 
<font color="#f79646">groups</font> <username> -> show user and see it's group 
sudo adduser <username> -> add user 
sudo adduser <username> <groupname> -> add user to group
sudo deluser <username> -> delete user
hostnamectl  -> check hostname 
hostnamectl set-hostname server1 -> change hostname to server1  -- vim /etc/hosts  needs 

	changing username with hostnamectl doesn't affect the hosts file, it's going to be resetted after reboot for full change we should change the hosts file

sudo ufw status -> see open ports 
sudo systemctl status <servicename> -> see status of given service
sudo chage hsari -l -> see password policy 
sudo vim /etc/login.defs -> password policy settings for aging controls
libpam-pwquality -> change password policy, upper-lowercase etc.-> `sudo vim /etc/pam.d/common-password
sudo vim /var/log/sudo/sudo.log -> see all used sudo commands 
journalctl -> see all commands used since starting of OS
sudo ufw status numbered -> see open ports as numbered list 
sudo vim /usr/local/bin/monitoring.sh -> monitoring sh directory and file 

^ = matches the starting position within the string -> ^/dev (works as XOR only true returns)
$ = Matches the ending position of the string 

:LiCodeXml: Awk
(Aho, Weinberger, and Kernighan)
Awk is a script language used for manipulating data and generating reports. Enables programmer to write tiny but effective programs. Mostly used for pattern scanning and processing. 


:LiNotebookPen: Journalctl 
journalctl is used to print the log entries stored in the journal by systemd-journald.service and systemd-journal-remote.service.


:LiGlobeLock: Obscure 

In the context of /etc/pam.d/common-password settings on Linux systems, the obscure option is associated with the pam_unix module, which handles traditional Unix authentication (e.g., managing passwords in /etc/passwd or /etc/shadow). The obscure parameter enables a set of basic password strength checks to ensure that passwords are not easily guessable or overly simplistic.

What obscure Does

When the obscure option is specified in the pam_unix module within /etc/pam.d/common-password, it enforces a series of rudimentary password quality checks. These checks are designed to reject passwords that are deemed too weak or insecure. Specifically, the obscure option typically enforces the following rules:

1. **Minimum Length**: Ensures the password meets a minimum length requirement (often 6 or 8 characters, depending on system configuration).
2. **Palindrome Check**: Rejects passwords that are palindromes (e.g., "racecar").
3. **Case-Change-Only Check**: Prevents passwords that are merely case-changed versions of the username (e.g., if the username is "john," the password "John" or "JOHN" would be rejected).
4. **Similarity Check**: Rejects passwords that are too similar to the old password (e.g., changing only one character).
5. **Simple Word Check**: May reject passwords that are too simple, such as those based on dictionary words, though this depends on the system's implementation.
6. **Rotation Check**: Rejects passwords that are simple rotations of the username or previous passwords (e.g., shifting characters).

These checks are relatively basic compared to modern password policies and are intended to provide a minimal level of security.




Chage
EXT3-EXT4 differences 
Swap area? 
Primary extended SDA5 
Apt-Aptitude difference 
Requiretty / Difference between tty -pty 
Whats the difference between getent groups and groups? 
- Getent is short for get entries. Allow users to access entriesfrom various text files or databases managed by NSS. (Name Service Switch) 
- Group is only showing the etc/group textfile one entry per line -> <groupname>:password:GID:user_list  
Shadow
RockyOS ve Debian differences
LVM

