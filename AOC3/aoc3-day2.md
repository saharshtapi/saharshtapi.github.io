---
title: Day 2
layout: page
permalink: /adventofcyber3/day2
tags: TryHackMe
---

# Day-2:Elf HR Problems
# ![front](/images/aoc3/d2/front.png)
[https://tryhackme.com/room/adventofcyber3](https://tryhackme.com/room/adventofcyber3)


## Gaining Access
- Create an account<br>
![signup](/images/aoc3/d2/signup.png)
- Look into the cookie values<br>
		- Looks like hexadecimal encoded<br>
		- Decode the value<br>
		- The cookie is in json format<br>
- Change the userame to admin and encode it in hexadecimal
![encode](/images/aoc3/d2/encode.png)
- Paste the encoded value in the cookie section
- Now open the page link again you will now be prompted with the **Monitoring Dashboard**
![db](/images/aoc3/d2/db.png)

