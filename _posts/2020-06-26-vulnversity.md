---
title: Vulnversity WalkThrough
permalink: /CTF/vulnversity
layout: page
tags: TryHackMe
---
# Vulnversity
# ![front](/images/vulnversity/front.png)
[https://tryhackme.com/room/vulnversity](https://tryhackme.com/room/vulnversity)

## Open Ports:
* 21- FTP
* 22- SSH
* 139- NETBIOS-SSN
* 445- MICROSOFT-DS
* 3128- SQUID-HTTP
* 3333- DEC-NOTES

![ports](/images/vulnversity/ports.png)

## Gaining Access:
### Port 80-
1. Running dir bruteforce and found:
![internal](/images/vulnversity/internal.png)
2. `.phtml` file allowed to upload
3. Upload revershell
	1. Ip/internal/uploads/rev.phtml `this will exec the rev-shell file`

### User Flag:
![flag](/images/vulnversity/flag.png)

## Privelege Escalation:
* tty the shell
> Find / -perm -u=s type f 2> /dev/null

* found bin/systemctl
![ctl](/images/vulnversity/ctl.png)
> change id to cat root/root.png

### Root Flag:
![root](/images/vulnversity/root.png)
