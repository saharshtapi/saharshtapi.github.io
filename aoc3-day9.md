---
title: Day 9
layout: page
permalink: /adventofcyber3/day9
tags: TryHackMe
---

# Day-9:Where Is All This Data Going
# ![front](/images/aoc3/d9/front.png)
[https://tryhackme.com/room/adventofcyber3](https://tryhackme.com/room/adventofcyber3)


## WireShark Analysis
1. Finding the directory which is using the **GET** method<br>
➟ login
2. Finding the users password in **POST** method<br>
![user_passwd](/images/aoc3/d9/post_passwd.png)
3. User-Agent for this **POST** request<br>
![user_agent](/images/aoc3/d9/user_agent.png)
4. Inside TXT DNS quesry<br>
![dns](/images/aoc3/d9/dns.png)
5. FTP login password<br>
![ftp](/images/aoc3/d9/ftp.png)
6. Command used to upload `secret.txt`<br>
![secret](/images/aoc3/d9/secret.png)
7. Inside `secret.txt`<br>
![inside](/images/aoc3/d9/inside.png)