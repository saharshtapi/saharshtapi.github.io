---
title: Day 4
layout: page
permalink: /CTF/adventofcyber3/day4
tags: TryHackMe
---

# Day-4:Christmas Blackout
# ![front](/images/aoc3/d4/front.png)
[https://tryhackme.com/room/adventofcyber3](https://tryhackme.com/room/adventofcyber3)

## Gaining Access
* Intercept the login request in burpsuite
* Now send the request to intruder<br>
![burp](/images/aoc3/d4/burp.png)
* set payload postion in and password and let the username be `santa`<br>
![ps](/images/aoc3/d4/ps.png)
* Now under payloads option paste the below possible passwords
```
christmas
elves!
santa
festive
joy123
myrrh!
yuletide
presents
candy
tidings
cookie
cookies
biscuits!
snowball
snowball123
```
* Then click on start attack
* In the new **Intruder** window you will see `cookie` payload highlighted as this is _Santa's_ password
![sp](/images/aoc3/d4/sp.png) 

### Flag
![flag](/images/aoc3/d4/flag.png)