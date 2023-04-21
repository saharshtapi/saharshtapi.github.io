---
title: Day 3
layout: page
permalink: /CTF/adventofcyber3/day3
tags: TryHackMe
---

# Day-3:Christmas Blackout
# ![front](/images/aoc3/d3/front.png)
[https://tryhackme.com/room/adventofcyber3](https://tryhackme.com/room/adventofcyber3)

## Gaining Access

### Dirbuster
* Start dirbuster find files and diretocries
* `/admin` found

### Login
* Trying default credentials for **Administrator**
* Opening the network tab you will see a file `login-page.js`
* The file contatins the username and password<br>
![admin](/images/aoc3/d3/admin.png)

### Flag
![flag](/images/aoc3/d3/flag.png)