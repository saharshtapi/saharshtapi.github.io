---
title: Day 12
layout: page
permalink: /CTF/adventofcyber3/day12
tags: TryHackMe
---

# Day-12:Sharing Without Caring
# ![front](/images/aoc3/d12/front.png)
[https://tryhackme.com/room/adventofcyber3](https://tryhackme.com/room/adventofcyber3)

## Gaining Access:
1. find the number open port<br>
![rustscan](/images/aoc3/d12/rustscan.png)
2. Looking at the mountable dir's <br>
![dirs](/images/aoc3/d12/dirs.png)
3. shars show `everyone`<br>
➟ 3
4. Mount the /share dir and cat `2680=0.txt`<br>
![2680](/images/aoc3/d12/2680.png)
5. Mount the dir /confidential <br>
![conf](/images/aoc3/d12/conf.png)
6. md5sum of `id_rsa`<br>
![md5](/images/aoc3/d12/md5.png)