---
title: Day 5
layout: page
permalink: /CTF/adventofcyber3/day5
tags: TryHackMe
---

# Day-5:Pesky Elf Forum
# ![front](/images/aoc3/d5/front.png)
[https://tryhackme.com/room/adventofcyber3](https://tryhackme.com/room/adventofcyber3)

## Gaining Access
* Login using the provided credentials
```
McSkidy
password
```
* Now click on the settings option.
* Now change the password
* Next you will notice the new password is being reflected in the URL<br>
![url](/images/aoc3/d5/url.png)
* Go to the any forum and type the payload in the comment section
```
<script>fetch('/settings?new_password=123');</script>
```
* So now when any user opens the forum his/her password will change to `123`.
* Now logout and login as grinch using the password *123*.<br>
![grinch](/images/aoc3/d5/grinch.png)
* Click on **Disable**

### Flag
![flag](/images/aoc3/d5/flag.png)