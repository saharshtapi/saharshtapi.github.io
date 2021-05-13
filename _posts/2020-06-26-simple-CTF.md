---
title: Simple CTF WalkThrough
permalink: /simplectf
layout: page
tags: TryHackMe
---
# Simple CTF
# ![front](/images/simplectf/front.png)
[https://tryhackme.com/room/easyctf](https://tryhackme.com/room/easyctf)

## Open Ports:
- 21: FTP
- 80: HTTP
- 2222: EtherNetIP-1
![ports](/images/simplectf/ports.png)

## Port 21:
**found name `mitch`**

## Port 80:
> Drib

1. found a page in `/simple`
	a. CMS made simple exploit found in exploitdb
		i. Found username: **mitch**
		ii. Foudn pass: **secret**
2. New using ssh to get into the machine

### User Flag:
![user flag](/images/simplectf/uflag.png)

## Priviledge Escalation 
```
sudo -l
```
![sudo](/images/simplectf/sudo.png)

### Root Flag:
![root](/images/simplectf/root.png)
