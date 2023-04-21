---
title: Day 13
layout: page
permalink: /CTF/adventofcyber3/day13
tags: TryHackMe
---

# Day-13:They Lost the Plan!
# ![front](/images/aoc3/d13/front.png)
[https://tryhackme.com/room/adventofcyber3](https://tryhackme.com/room/adventofcyber3)

## Privilege Escalatation
1. username<br>
➟ pepper
2. type `sysinfo` to get the OS version<br>
➟  10.0.17763 N/A Build 17763
3. Backup service<br>
➟ IperiusSvc
4. Path to the executable<br>
➟  C:\Program Files (x86)\Iperius Backup\IperiusService.exe
5. Whomai<br>
➟ the-grinch-hack\thegrinch
6. flag<br>
➟ THM-736635221
7. Where can we find Grinch<br>
➟ jazzercize