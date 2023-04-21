---
title: Day 10
layout: page
permalink: /adventofcyber3/day10
tags: TryHackMe
---

# Day-10:Offensive Is The Best Defence
# ![front](/images/aoc3/d10/front.png)
[https://tryhackme.com/room/adventofcyber3](https://tryhackme.com/room/adventofcyber3)


## Port Scanning
1. running `nmap -sT <ip>` to find open ports 1-100<br>
➟ 2
2. Smallest port open<br>
➟ 22
3. Service on the highest port<br>
➟ http
4. running `nmap -sS 10.10.47.51`<br>
➟ Y
5. web server version<br>
➟ Apache httpd 2.4.49
6. CVE for fixed Vulnerability<br>
➟ CVE-2021-42013
7. Backdoor port<br>
➟ 20212
8. Service running on backdoor<br>
➟ telnetd