---
title: Anonymous WalkThrough
permalink: /CTF/anonymous
layout: page
tags: TryHackMe
---
# Anonymouos
# ![front](/images/Anonymous/front.png)
[https://tryhackme.com/room/anonymous](https://tryhackme.com/room/anonymous)

## Open Ports:
- 21: FTP
- 22: SSH
- 139: NETBIOS-SSN
- 445: MICROSOFT-DS

![ports](/images/Anonymous/ports.png)

## Gaining Access:
1. In port 21[FTP] **Anonymous login** is _allowed_<br>
	 i. Go to scripts<br> 
	 ii. Modify `clean.sh` to get revershell<br>
	 iii. Wait for a min<br>
**U will now have the reverse shell in you `netcat`**

### User Flag:
##### [90d6f992585815ff991e68748c414740]()

## Priviledge Escaltion:
```bash
find / -perm -u=s 2>/dev/null
```
* found `env` vuln found via GTFObins
* `./env/bin/bash -p`

### Root Flag:
![root](/images/Anonymous/root.png)
