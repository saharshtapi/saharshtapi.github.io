---
title: Day 11
layout: page
permalink: /adventofcyber3/day11
tags: TryHackMe
---

# Day-11:Where Are The Reindeers?
# ![front](/images/aoc3/d11/front.png)
[https://tryhackme.com/room/adventofcyber3](https://tryhackme.com/room/adventofcyber3)

## Gaining Access
1. My sql port number
* Running nmap to find the port number<br>
![nmap](/images/aoc3/d11/nmap.png)
2. Connect using the query `sqsh -S <ip> -U sa -P t7uLKzddQzVjVFJp` to get the prompt<br>
![prompt](/images/aoc3/d11/prompt.png)
3. The name for id 9
➟ Rudolph
4. Destination of trip in Dec 7<br>
![trip](/images/aoc3/d11/trip.png)
5. Looking at table **presents** <br>
![presents](/images/aoc3/d11/presents.png)
6. Flag inside grinch's home directory<br>
![flag](/images/aoc3/d11/flag.png)